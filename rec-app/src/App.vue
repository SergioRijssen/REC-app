<template>
    <div class="container">
    <!-- Header -->
        <header class="header">
            <div class="logo">
                <img class="logo-img" src="@/assets/logoREC.png" alt="Real Estate Care Logo" />
            </div>
        </header>

        <!-- Main Content Grid -->
        <main class="main-content">
            <div class="grid-item">Scheduled</div>
            <div class="grid-item">Completed</div>
            <div class="grid-item">Knowledge base</div>
            <div class="grid-item">Settings</div>
        </main>

        <!-- Footer -->
        <footer class="footer">
            <div class="footer-item">Active Task</div>
            <div class="footer-item">Search</div>
            <div class="footer-item">Information</div>
        </footer>
    </div>
</template>

<style scoped>
    .container {
        display: flex;
        flex-direction: column;
        height: 100vh;
    }

    .header {
        display: flex;
        flex-direction: column;
        background: linear-gradient(180deg, rgba(71, 94, 108, 1) 50%, rgba(20, 27, 31, 1) 100%);
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .logo {
        display: flex;
        justify-content: center;
        padding: 1rem;
    }

    .logo-img {
        width: 100%;
        max-width: 420px; /* Optioneel: maximale breedte om te voorkomen dat het te groot wordt */
        object-fit: contain; /* Zorgt ervoor dat de afbeelding zijn aspect ratio behoudt */
    }

    .main-content {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 10px;
        padding: 20px;
        flex-grow: 1;
    }

    .grid-item {
        display: flex;
        justify-content: center;
        align-items: center;
        border: 1px solid #ddd;
        padding: 20px;
        font-size: 1.2em;
    }

    .footer {
        display: flex;
        justify-content: space-around;
        align-items: center;
        background-color: #008080; /* Hoofdkleur */
        color: white;
        padding: 15px;
        font-size: 1em; /* Zorg voor consistente tekstgrootte */
    }

    /* Media query voor schermen kleiner dan 600px */
    @media (max-width: 600px) {
        .main-content {
            grid-template-columns: 1fr; /* Zet de grid-layout naar één kolom */
            padding: 10px;
        }

        .grid-item {
            font-size: 1em; /* Pas de font-size aan voor kleinere schermen */
            padding: 15px; /* Maak de padding iets kleiner */
        }

        .logo-img {
            height: 60px; /* Verminder de hoogte van het logo op kleinere schermen */
        }

        .footer {
            font-size: 0.9em; /* Maak de tekst iets kleiner in de footer */
            padding: 10px;
        }
    }
</style>
