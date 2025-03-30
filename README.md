<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Les Chouchous des Managers</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
            background-color: #f9f9f9;
            color: #333;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #ffccd5;
            padding: 20px;
            text-align: center;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        header img {
            height: 50px;
            margin-right: 10px;
        }
        main {
            padding: 20px;
            padding-bottom: 60px; /* Ajout de padding pour éviter que le contenu soit caché par le bandeau */
        }
        .definition {
            background-color: #cce7ff;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 20px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .manager-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-bottom: 20px;
        }
        .manager {
            text-align: center;
            margin-bottom: 20px;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }
        .manager:hover {
            transform: translateY(-10px);
        }
        .manager img {
            border-radius: 50%;
            width: 100px;
            height: 100px;
            object-fit: cover;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .manager h3 {
            margin-top: 10px;
            color: #ff6347;
        }
        .favorite-button {
            background-color: #ffb3c1;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 10px;
            transition: background-color 0.3s;
        }
        .favorite-button:hover {
            background-color: #ff99b3;
        }
        .dropdown {
            position: relative;
            display: inline-block;
        }
        .dropdown-content {
            display: none;
            position: absolute;
            background-color: #fff;
            min-width: 200px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1;
            border-radius: 8px;
            overflow: hidden;
            padding: 10px;
        }
        .dropdown-content div {
            padding: 10px;
            cursor: pointer;
        }
        .dropdown-content div:hover {
            background-color: #f1f1f1;
        }
        .dropdown-content .add-button {
            color: red;
            font-weight: bold;
        }
        .popup {
            display: none;
            position: fixed;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
        }
        .popup.show {
            display: block;
        }
        .popup-close {
            background: none;
            border: none;
            font-size: 16px;
            cursor: pointer;
        }
        .collaborator {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        .collaborator img {
            border-radius: 50%;
            width: 50px;
            height: 50px;
            object-fit: cover;
            margin-right: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        }
        .banner {
            background-color: #ffccd5;
            padding: 10px;
            text-align: center;
            position: fixed;
            bottom: 0;
            width: 100%;
            box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
            z-index: 10;
        }
        .banner-content {
            display: flex;
            width: calc(300%);
            animation: scrolling 10s linear infinite;
        }
        .banner img {
            border-radius: 50%;
            width: 50px;
            height: 50px;
            object-fit: cover;
            margin: 0 10px;
        }
        @keyframes scrolling {
            0% {
                transform: translateX(0);
            }
            100% {
                transform: translateX(-66.66%);
            }
        }
    </style>
</head>
<body>
    <header>
        <img src="https://www.fr-dba.com/wp-content/uploads/2020/11/logo-dba-vf-1.png" alt="Logo DBA">
        <h1>Les Chouchous des Managers</h1>
    </header>
    <main>
        <div class="definition">
            <h2>Définition de Chouchou</h2>
            <p>Un chouchou est une personne ou une chose qui est particulièrement appréciée ou préférée par quelqu'un. Ce terme affectueux est souvent utilisé pour désigner les favoris dans divers contextes.</p>
        </div>
        <div class="manager-section">
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQGsE6Fv_OQmMQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1540125746107?e=1748476800&v=beta&t=oybW8-m8CFChiyNwlpdVnNWnzUaMttJo8fjK3yPCyvo" alt="Manager Benoit">
                <h3>Benoit</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/C4D03AQGjPIXw8SQjpQ/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646234300085?e=1748476800&v=beta&t=MDXOTK7PoPIwgWfQKZXRdNp1pPDJCmbSbIUOmTnthNQ" alt="Gautier">
                            <span>Gautier</span>
                        </div>
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/D4E03AQEzrxVyDeD5Tw/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1682360050580?e=1749081600&v=beta&t=l8VwBftupthcoYJF_RTaQ1D3QhFAZ_2b8F2yzCG_6D8" alt="Alban">
                            <span>Alban</span>
                        </div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C5603AQFOT57GvjYZaA/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1517053081934?e=1748476800&v=beta&t=DAx2WaBZehwcDDUGm7m6D578ksUvVwHiX0KlhBOl4NM" alt="Manager Audrey">
                <h3>Audrey</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div>En raison d'une indisponibilité, son classement est indisponible pour le moment.</div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C4D03AQEISt7mKRzUdQ/profile-displayphoto-shrink_800_800/profile-displayphoto-shrink_800_800/0/1539187124432?e=1748476800&v=beta&t=Z6mPEZe7DRpRB2T7XeP1Au1imwfzUxnduba_AE26YqM" alt="Manager Dan">
                <h3>Dan</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/D4E03AQGHw2jZmQ-WBA/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1698047557143?e=1749081600&v=beta&t=3jBusMZC9AUUbDMdjBN9l_a9SHPm9ZnlCPn3JGoDIbg" alt="Pierre">
                            <span>Pierre</span>
                        </div>
                        <div class="collaborator">
                            <img src="https://media.licdn.com/dms/image/v2/C4D03AQFNl6r2rDKdJA/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1633415863258?e=1749081600&v=beta&t=HUb2woRwaClAhRvH0OA90Y_IjW67Imx7IBbw-klWqb8" alt="Marie">
                            <span>Marie</span>
                        </div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
            <div class="manager">
                <img src="https://media.licdn.com/dms/image/v2/C5603AQG-Gryr95xBAg/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1541498116747?e=1748476800&v=beta&t=2X3ZbITi7rN6sdChkDUK_rCwwJxldmnjHurr2Xhdb68" alt="Manager Alimath">
                <h3>Alimath</h3>
                <div class="dropdown">
                    <button class="favorite-button">Voir les Chouchous</button>
                    <div class="dropdown-content">
                        <div>Pas de chouchou, elle adore tout le monde.</div>
                        <div class="add-button" onclick="showAddPopup()">Ajouter un Chouchou</div>
                    </div>
                </div>
            </div>
        </div>
        <div class="popup" id="add-popup">
            <div class="popup-content">
                <p>T'as cru t'allais pouvoir t'ajouter en chouchou comme ça ? Espèce de fou ! Au boulot.</p>
            </div>
            <button class="popup-close" onclick="hideAddPopup()">Fermer</button>
        </div>
    </main>
    <div class="banner" id="dynamic-banner">
        <span>Nos Chouchous :</span>
        <div class="banner-content">
            <img src="https://media.licdn.com/dms/image/v2/C4D03AQGjPIXw8SQjpQ/profile-displayphoto-shrink_400_400/profile-displayphoto-shrink_400_400/0/1646234300085?e=1748476800&v=beta&t=MDXOTK7PoPIwgWfQKZXRdNp1pPDJCmbSbIUOmTnthNQ" alt="Gautier">
            <img src="https://media.licdn.com/dms/image/v2/D4E03AQEzrxVyDeD5Tw/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1682360050580?e=1749081600&v=beta&t=l8VwBftupthcoYJF_RTaQ1D3QhFAZ_2b8F2yzCG_6D8" alt="Alban">
            <img src="https://media.licdn.com/dms/image/v2/D4E03AQGHw2jZmQ-WBA/profile-displayphoto-shrink_100_100/profile-displayphoto-shrink_100_100/0/1698047557143?e=1749081600&v=beta&t=3jBusMZC9AUUbDMdjBN9l_a9SHPm9ZnlCPn3JGoDIbg" alt="Pierre">
        </div>
    </div>
    <script>
        let currentDropdown = null;

        function toggleDropdown(manager) {
            const dropdownContent = document.querySelector(`.manager:has(> img[alt='Manager ${manager}']) .dropdown-content`);
            if (currentDropdown && currentDropdown !== dropdownContent) {
                currentDropdown.style.display = 'none';
            }
            dropdownContent.style.display = dropdownContent.style.display === 'block' ? 'none' : 'block';
            currentDropdown = dropdownContent;
        }

        function showAddPopup() {
            document.getElementById('add-popup').classList.add('show');
        }

        function hideAddPopup() {
            document.getElementById('add-popup').classList.remove('show');
        }

        document.querySelectorAll('.dropdown').forEach(dropdown => {
            dropdown.addEventListener('click', function(event) {
                if (event.target.tagName === 'BUTTON') {
                    toggleDropdown(event.target.closest('.manager').querySelector('h3').textContent);
                }
            });
        });

        window.onclick = function(event) {
            if (!event.target.matches('.favorite-button')) {
                const dropdowns = document.querySelectorAll('.dropdown-content');
                dropdowns.forEach(dropdown => {
                    if (dropdown.style.display === 'block') {
                        dropdown.style.display = 'none';
                    }
                });
                currentDropdown = null;
            }
        }
    </script>
</body>
</html>
