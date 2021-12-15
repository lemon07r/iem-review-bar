<script lang="ts">
    const siteName: string = "IEM Review Bar";

    let activePage: number = 1;

    function changeActivePage(currentPage: number) {
        activePage = currentPage;
    }
</script>

<div class="navbar mb-2 shadow-lg bg-neutral text-neutral-content rounded-box">
    <div class="flex-none hidden lg:flex">
        <button class="btn btn-square btn-ghost">
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                class="inline-block w-6 h-6 stroke-current"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M4 6h16M4 12h16M4 18h16"
                />
            </svg>
        </button>
    </div>
    <div class="flex-none px-2 mx-2">
        <span class="text-lg font-bold"> {siteName} </span>
    </div>
    <div class="flex-1 px-2 mx-2">
        <div class="items-stretch hidden lg:flex">
            <div class="btn-group">
                <button
                    on:click={() => changeActivePage(1)}
                    class="btn {activePage === 1 ? 'btn-active' : ''}"
                    >Home</button
                >
                <button
                    on:click={() => changeActivePage(2)}
                    class="btn {activePage === 2 ? 'btn-active' : ''}"
                    >Reviews</button
                >
                <button
                    on:click={() => changeActivePage(3)}
                    class="btn {activePage === 3 ? 'btn-active' : ''}"
                    >Ranking</button
                >
                <button
                    on:click={() => changeActivePage(4)}
                    class="btn {activePage === 4 ? 'btn-active' : ''}"
                    >Graphs</button
                >
            </div>
        </div>
    </div>
    <div class="flex-1 lg:flex-none">
        <div class="form-control">
            <input type="text" placeholder="Search" class="input input-ghost" />
        </div>
    </div>
    <div class="flex-none">
        <button class="btn btn-square btn-ghost">
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                class="inline-block w-6 h-6 stroke-current"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"
                />
            </svg>
        </button>
    </div>
    <div class="flex-none">
        <button class="btn btn-square btn-ghost">
            <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                class="inline-block w-6 h-6 stroke-current"
            >
                <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M5 12h.01M12 12h.01M19 12h.01M6 12a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0zm7 0a1 1 0 11-2 0 1 1 0 012 0z"
                />
            </svg>
        </button>
    </div>
</div>
