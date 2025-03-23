<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Conteneurs Solutions</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <script src="https://unpkg.com/@tailwindcss/browser@4"></script>
    <style>
        /* Styles personnalisés pour les animations et les couleurs */
        .slide-in {
            animation: slideIn 0.5s ease-out;
        }
        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        .fade-in {
            animation: fadeIn 0.5s ease-out;
        }
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .custom-shadow {
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15); /* Légère ombre portée */
        }
        .bold-title {
            font-weight: 600; /* Medium font weight */
        }

    </style>
</head>
<body class="bg-gray-100 font-inter">
    <header class="bg-blue-900 text-white py-4 flex justify-between items-center shadow-md sticky top-0 z-10 rounded-md">
        <div class="logo text-xl font-bold ml-6">
            <a href="#" class="hover:text-blue-300 transition duration-300">Conteneurs Solutions</a>
        </div>
        <nav class="mr-6">
            <ul class="flex space-x-6">
                <li><a href="#accueil" class="hover:text-blue-300 transition duration-300">Accueil</a></li>
                <li><a href="#conteneurs" class="hover:text-blue-300 transition duration-300">Conteneurs</a></li>
                <li><a href="#pourquoi-nous" class="hover:text-blue-300 transition duration-300">Pourquoi nous choisir ?</a></li>
                <li><a href="#devis" class="hover:text-blue-300 transition duration-300">Devis</a></li>
            </ul>
        </nav>
    </header>

    <section id="accueil" class="bg-gradient-to-br from-blue-900 to-blue-700 text-white text-center py-20 px-4 rounded-md">
        <div class="container mx-auto flex flex-col items-center">
            <h1 class="text-4xl font-bold mb-4 slide-in">Votre solution conteneur, simplifiée.</h1>
            <p class="text-lg mb-8 max-w-2xl fade-in">Achetez ou louez des conteneurs de qualité supérieure.  Large sélection, prix compétitifs, et service client exceptionnel.</p>
            <a href="#conteneurs" class="bg-yellow-500 text-blue-900 py-3 px-6 rounded-full hover:bg-yellow-600 transition duration-300 text-lg font-semibold shadow-md">
                Découvrez nos conteneurs
            </a>
        </div>
    </section>

    <section id="conteneurs" class="container mx-auto py-16 px-4">
        <h2 class="text-3xl font-bold text-blue-900 text-center mb-8">Nos Conteneurs Disponibles</h2>

        <div class="bg-white rounded-lg shadow-md p-6 mb-8 flex flex-wrap justify-center gap-4">
            <div class="flex flex-col sm:flex-row gap-2 sm:items-center">
                <label for="taille" class="text-gray-700 font-semibold">Taille:</label>
                <select id="taille" class="border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <option value="">Toutes</option>
                    <option value="20">20 pieds</option>
                    <option value="40">40 pieds</option>
                </select>
            </div>
            <div class="flex flex-col sm:flex-row gap-2 sm:items-center">
                <label for="etat" class="text-gray-700 font-semibold">État:</label>
                <select id="etat" class="border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <option value="">Tous</option>
                    <option value="neuf">Neuf</option>
                    <option value="occasion">Occasion</option>
                </select>
             </div>
            <div class="flex flex-col sm:flex-row gap-2 sm:items-center">
                <label for="type" class="text-gray-700 font-semibold">Type:</label>
                <select id="type" class="border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <option value="">Tous</option>
                    <option value="standard">Standard</option>
                    <option value="refrigerere">Réfrigéré</option>
                    <option value="amenage">Aménagé</option>
                </select>
            </div>
            <div class="flex flex-col sm:flex-row gap-2 sm:items-center">
                <label for="location" class="text-gray-700 font-semibold">Ville:</label>
                 <select id="location" class="border border-gray-300 rounded-md py-2 px-3 focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <option value="">Toutes</option>
                    <option value="tunis">Tunis</option>
                    <option value="sfax">Sfax</option>
                    <option value="sousse">Sousse</option>
                </select>
            </div>
            <button id="filter-button" class="bg-green-500 text-white py-2 px-4 rounded-md hover:bg-green-600 transition duration-300 font-semibold">Filtrer</button>
        </div>

        <div id="container-grid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
            </div>
    </section>

    <section id="pourquoi-nous" class="bg-blue-100 py-16 px-4 rounded-md">
        <div class="container mx-auto text-center">
            <h2 class="text-3xl font-bold text-blue-900 mb-8">Pourquoi nous choisir ?</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="flex flex-col items-center">
                    <img src="https://placehold.co/50x50/EEE/31343C?text=%F0%9F%92%A6&font=Noto+Emoji" alt="Étanche" class="mb-4">
                    <h3 class="text-xl font-semibold text-blue-800 mb-2">Étanche</h3>
                    <p class="text-gray-700">Nos conteneurs sont garantis étanches pour protéger vos biens.</p>
                </div>
                <div class="flex flex-col items-center">
                    <img src="https://placehold.co/50x50/EEE/31343C?text=%F0%9F%9A%9A&font=Noto+Emoji" alt="Livraison Rapide" class="mb-4">
                    <h3 class="text-xl font-semibold text-blue-800 mb-2">Livraison Rapide</h3>
                    <p class="text-gray-700">Livraison efficace et rapide de votre conteneur.</p>
                </div>
                <div class="flex flex-col items-center">
                    <img src="https://placehold.co/50x50/EEE/31343C?text=%E2%82%B5&font=Noto+Emoji" alt="Qualité/Prix" class="mb-4">
                    <h3 class="text-xl font-semibold text-blue-800 mb-2">Meilleure Qualité/Prix</h3>
                    <p class="text-gray-700">Conteneurs de qualité premium à des prix compétitifs.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="devis" class="bg-blue-900 text-white py-16 px-4 rounded-md">
        <div class="container mx-auto text-center">
            <h2 class="text-3xl font-bold mb-8">Demandez un devis personnalisé</h2>
            <p class="text-lg mb-8 max-w-2xl mx-auto">Intéressé par un de nos conteneurs ? Remplissez le formulaire ci-dessous pour recevoir une offre sur mesure.</p>
             <a href="#quote-form-section" class="bg-yellow-500 text-blue-900 py-3 px-6 rounded-full hover:bg-yellow-600 transition duration-300 text-lg font-semibold shadow-md inline-block">
                Obtenir un devis
            </a>
        </div>
    </section>

    <section id="quote-form-section" class="container mx-auto py-16 px-4">
        <div class="bg-white rounded-lg shadow-md p-8 max-w-2xl mx-auto">
            <h2 class="text-2xl font-bold text-blue-900 mb-6 text-center">Formulaire de demande de devis</h2>
            <form id="quote-form" class="space-y-4">
                <div>
                    <label for="client-type" class="block text-gray-700 text-sm font-bold mb-2">Type de client:</label>
                    <select id="client-type" name="client-type" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                        <option value="">Sélectionner...</option>
                        <option value="particulier">Particulier</option>
                        <option value="societe">Société</option>
                    </select>
                    <div id="client-type-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div>
                    <label for="name" class="block text-gray-700 text-sm font-bold mb-2">Prénom et Nom:</label>
                    <input type="text" id="name" name="name" placeholder="Votre prénom et nom" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                     <div id="name-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div>
                    <label for="phone" class="block text-gray-700 text-sm font-bold mb-2">Téléphone:</label>
                    <input type="tel" id="phone" name="phone" placeholder="Votre numéro de téléphone" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <div id="phone-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div>
                    <label for="email" class="block text-gray-700 text-sm font-bold mb-2">Email:</label>
                    <input type="email" id="email" name="email" placeholder="Votre adresse email" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <div id="email-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div>
                    <label for="governorate" class="block text-gray-700 text-sm font-bold mb-2">Gouvernorat:</label>
                    <input type="text" id="governorate" name="governorate" placeholder="Votre gouvernorat" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                    <div id="governorate-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <div>
                    <label for="container-model" class="block text-gray-700 text-sm font-bold mb-2">Modèle du conteneur souhaité:</label>
                     <select id="container-model" name="container-model" required class="border border-gray-300 rounded-md py-2 px-3 w-full focus:outline-none focus:ring-2 focus:ring-blue-500">
                        <option value="">Sélectionner...</option>
                        <option value="20-standard">20 pieds Standard</option>
                        <option value="40-standard">40 pieds Standard</option>
                        <option value="20-refrigerere">20 pieds Réfrigéré</option>
                        <option value="40-refrigerere">40 pieds Réfrigéré</option>
                        <option value="20-amenage">20 pieds Aménagé</option>
                        <option value="40-amenage">40 pieds Aménagé</option>
                    </select>
                    <div id="container-model-error" class="text-red-500 text-xs italic" style="display: none;"></div>
                </div>
                <button type="submit" class="bg-blue-500 text-white py-3 px-6 rounded-md hover:bg-blue-600 transition duration-300 w-full font-semibold">
                    Envoyer la demande de devis
                </button>
            </form>
            <div id="quote-form-message" class="mt-6 text-center font-semibold" style="display: none;"></div>
        </div>
    </section>

    <footer class="bg-gray-800 text-gray-300 py-6 text-center rounded-md">
        <p>© 2024 Conteneurs Solutions. Tous droits réservés.</p>
    </footer>

    <script>
        // Sample container data (in real scenario, this would come from a database or API)
        const containers = [
            { id: 1, taille: '20', etat: 'neuf', type: 'standard', prix: 2500, ville: 'Tunis', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+20\'&font=Roboto' },
            { id: 2, taille: '40', etat: 'occasion', type: 'standard', prix: 3200, ville: 'Sfax', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+40\'&font=Roboto' },
            { id: 3, taille: '20', etat: 'neuf', type: 'refrigerere', prix: 6000, ville: 'Tunis', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+20\'R&font=Roboto' },
            { id: 4, taille: '40', etat: 'occasion', type: 'amenage', prix: 8000, ville: 'Sousse', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+40\'A&font=Roboto' },
            { id: 5, taille: '20', etat: 'occasion', type: 'standard', prix: 2000, ville: 'Sousse', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+20\'&font=Roboto' },
            { id: 6, taille: '40', etat: 'neuf', type: 'standard', prix: 4000, ville: 'Sfax', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+40\'&font=Roboto' },
            { id: 7, taille: '20', etat: 'neuf', type: 'amenage', prix: 7500, ville: 'Tunis', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+20\'A&font=Roboto' },
            { id: 8, taille: '40', etat: 'occasion', type: 'refrigerere', prix: 5500, ville: 'Sfax', image: 'https://placehold.co/400x300/EEE/31343C?text=Conteneur+40\'R&font=Roboto' },
        ];

        const containerGrid = document.getElementById('container-grid');
        const filterButton = document.getElementById('filter-button');

        function displayContainers(filteredContainers) {
            containerGrid.innerHTML = ''; // Clear previous results
            filteredContainers.forEach(container => {
                const containerCard = document.createElement('div');
                containerCard.classList.add('bg-white', 'rounded-lg', 'shadow-md', 'p-4', 'flex', 'flex-col', 'transition-transform', 'hover:scale-105');
                containerCard.innerHTML = `
                    <img src="${container.image}" alt="Conteneur ${container.taille} pieds" class="rounded-md mb-4">
                    <h3 class="text-xl font-semibold text-blue-900 mb-2">${container.taille} pieds ${container.type}</h3>
                    <p class="text-gray-700 mb-2">État: ${container.etat}</p>
                    <p class="text-gray-700 mb-2">Ville: ${container.ville}</p>
                    <p class="text-lg font-bold text-green-600 mb-4">${container.prix} TND</p>
                    <a href="#devis" class="bg-yellow-500 text-blue-900 py-2 px-4 rounded-full hover:bg-yellow-600 transition duration-300 text-center font-semibold">Demander un devis</a>
                `;
                containerGrid.appendChild(containerCard);
            });
        }

        function applyFilters() {
            const tailleFilter = document.getElementById('taille').value;
            const etatFilter = document.getElementById('etat').value;
            const typeFilter = document.getElementById('type').value;
            const villeFilter = document.getElementById('location').value;

            const filteredContainers = containers.filter(container => {
                return (
                    (!tailleFilter || container.taille === tailleFilter) &&
                    (!etatFilter || container.etat === etatFilter) &&
                    (!typeFilter || container.type === typeFilter) &&
                    (!villeFilter || container.ville === villeFilter)
                );
            });
            displayContainers(filteredContainers);
        }

        // Initial display of all containers
        displayContainers(containers);

        // Event listener for the filter button
        filterButton.addEventListener('click', applyFilters);



        // --- Quote Form Validation ---
        const quoteForm = document.getElementById('quote-form');
        const quoteFormMessage = document.getElementById('quote-form-message');

        function validateForm() {
            let isValid = true;

            // Client Type Validation
            const clientType = document.getElementById('client-type').value;
            const clientTypeError = document.getElementById('client-type-error');
            if (!clientType) {
                clientTypeError.textContent = "Veuillez sélectionner un type de client.";
                clientTypeError.style.display = "block";
                isValid = false;
            } else {
                clientTypeError.style.display = "none";
            }

            // Name Validation
            const name = document.getElementById('name').value.trim();
            const nameError = document.getElementById('name-error');
            if (!name) {
                nameError.textContent = "Veuillez entrer votre nom.";
                nameError.style.display = "block";
                isValid = false;
            } else if (!/^[a-zA-Z\s]+$/.test(name)) {
                nameError.textContent = "Le nom ne doit contenir que des lettres et des espaces.";
                nameError.style.display = "block";
                isValid = false;
            }else {
                nameError.style.display = "none";
            }

            // Phone Validation
            const phone = document.getElementById('phone').value.trim();
            const phoneError = document.getElementById('phone-error');
            if (!phone) {
                phoneError.textContent = "Veuillez entrer votre numéro de téléphone.";
                phoneError.style.display = "block";
                isValid = false;
            } else if (!/^[0-9]{8}$/.test(phone)) {
                phoneError.textContent = "Le numéro de téléphone doit contenir 8 chiffres.";
                phoneError.style.display = "block";
                isValid = false;
            } else {
                phoneError.style.display = "none";
            }

            // Email Validation
            const email = document.getElementById('email').value.trim();
            const emailError = document.getElementById('email-error');
            if (!email) {
                emailError.textContent = "Veuillez entrer votre adresse email.";
                emailError.style.display = "block";
                isValid = false;
            } else if (!/^[\w-\.]+@([\w-]+\.)+[\w-]{2,4}$/.test(email)) {
                emailError.textContent = "Veuillez entrer une adresse email valide.";
                emailError.style.display = "block";
                isValid = false;
            } else {
                emailError.style.display = "none";
            }

            // Governorat Validation
            const governorate = document.getElementById('governorate').value.trim();
            const governorateError = document.getElementById('governorate-error');
            if (!governorate) {
                governorateError.textContent = "Veuillez entrer votre gouvernorat.";
                governorateError.style.display = "block";
                isValid = false;
            } else if (!/^[a-zA-Z\s]+$/.test(governorate)) {
                governorateError.textContent = "Le gouvernorat ne doit contenir que des lettres et des espaces.";
                governorateError.style.display = "block";
                isValid = false;
            }else {
                governorateError.style.display = "none";
            }

             // Container Model Validation
            const containerModel = document.getElementById('container-model').value;
            const containerModelError = document.getElementById('container-model-error');
            if (!containerModel) {
                containerModelError.textContent = "Veuillez sélectionner un modèle de conteneur.";
                containerModelError.style.display = "block";
                isValid = false;
            } else {
                containerModelError.style.display = "none";
            }

            return isValid;
        }

        quoteForm.addEventListener('submit', (event) => {
            event.preventDefault(); // Prevent default form submission

            if (validateForm()) {
                // Simulate form submission (replace with actual backend submission)
                console.log('Form submitted successfully!');
                quoteFormMessage.textContent = "Votre demande de devis a été envoyée avec succès !";
                quoteFormMessage.style.display = "block";
                quoteForm.reset(); // Clear the form
                 setTimeout(() => {
                    quoteFormMessage.style.display = "none";
                }, 5000);

            } else {
                console.log('Form submission failed due to validation errors.');
            }
        });
    </script>
</body>
</html>
