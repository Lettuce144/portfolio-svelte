<script>
    import { locale, getLocaleFromNavigator } from 'svelte-i18n';
    import { onMount } from 'svelte';

    // Define the available languages and their codes
    const languages = [
        { code: 'en', label: 'English' },
        { code: 'nl', label: 'Nederlands' },
        // Add more languages here if needed
    ];

    let currentLocale = getLocaleFromNavigator();

    // Function to change the locale
    const changeLanguage = (langCode) => {
        locale.set(langCode);
        currentLocale = langCode;
    };

    onMount(() => {
        locale.subscribe(value => {
            currentLocale = value;
        });
    });
</script>

<details class="dropdown dropdown-bottom dropdown-end absolute right-0">
    <summary class="btn btn-secondary m-2">
        <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="size-6"
        >
            <path
                stroke-linecap="round"
                stroke-linejoin="round"
                d="m10.5 21 5.25-11.25L21 21m-9-3h7.5M3 5.621a48.474 48.474 0 0 1 6-.371m0 0c1.12 0 2.233.038 3.334.114M9 5.25V3m3.334 2.364C11.176 10.658 7.69 15.08 3 17.502m9.334-12.138c.896.061 1.785.147 2.666.257m-4.589 8.495a18.023 18.023 0 0 1-3.827-5.802"
            />
        </svg>
    </summary>
    <ul class="menu dropdown-content bg-base-100 rounded-box z-[1] w-52 p-2 shadow">
        {#each languages as { code, label }}
            <li>
                <button
                    type="button"
                    class="{currentLocale === code ? 'bg-secondary text-secondary-content' : ''}"
                    on:click={() => changeLanguage(code)}
                    aria-label={`Change language to ${label}`}
                >
                    {label}
                </button>
            </li>
        {/each}
    </ul>
</details>