<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Market Research Survey</title>
    <style>
        /* Basic styling for layout and typography */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            margin: 0;
            padding: 0;
        }

        .container {
            max-width: 800px;
            margin: 50px auto;
            padding: 20px;
            background-color: #ffffff;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            border-radius: 8px;
        }

        h1 {
            text-align: center;
            color: #333;
        }

        h2 {
            color: #555;
        }

        label {
            font-size: 14px;
            color: #555;
            margin: 10px 0 5px;
            display: block;
        }

        select, input[type="text"], input[type="radio"], input[type="checkbox"] {
            width: 100%;
            padding: 10px;
            margin-bottom: 15px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            width: 100%;
            padding: 12px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        .section {
            margin-bottom: 20px;
        }

        .form-footer {
            text-align: center;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Market Research Survey for New Product</h1>
        
        <!-- Survey Form -->
        <form id="survey-form">
            <!-- Section 1: Demographic Information -->
            <section class="section">
                <h2>Demographic Information</h2>
                <label for="age">1. What is your age?</label>
                <select id="age" name="age" required>
                    <option value="Under 18">Under 18</option>
                    <option value="18-24">18-24</option>
                    <option value="25-34">25-34</option>
                    <option value="35-44">35-44</option>
                    <option value="45-54">45-54</option>
                    <option value="55-64">55-64</option>
                    <option value="65+">65+</option>
                </select>
                
                <label for="gender">2. What is your gender?</label>
                <select id="gender" name="gender" required>
                    <option value="Male">Male</option>
                    <option value="Female">Female</option>
                    <option value="Other">Other</option>
                </select>

                <label for="location">3. What is your location?</label>
                <input type="text" id="location" name="location" required>
            </section>

            <!-- Section 2: Product Awareness -->
            <section class="section">
                <h2>Product Awareness</h2>
                <label for="heard-about">4. Have you heard about our new product before?</label>
                <input type="radio" id="yes" name="heard-about" value="Yes" required> Yes
                <input type="radio" id="no" name="heard-about" value="No" required> No
            </section>

            <!-- Section 3: Product Preferences -->
            <section class="section">
                <h2>Product Preferences</h2>
                <label for="purchase-frequency">5. How often do you purchase products in this category?</label>
                <select id="purchase-frequency" name="purchase-frequency" required>
                    <option value="Never">Never</option>
                    <option value="Rarely">Rarely</option>
                    <option value="Occasionally">Occasionally</option>
                    <option value="Frequently">Frequently</option>
                    <option value="Always">Always</option>
                </select>

                <label for="features">6. What features are most important when purchasing a product like this? (Select up to 3)</label>
                <input type="checkbox" id="price" name="features" value="Price"> Price
                <input type="checkbox" id="quality" name="features" value="Quality"> Quality
                <input type="checkbox" id="design" name="features" value="Design"> Design
                <input type="checkbox" id="durability" name="features" value="Durability"> Durability
            </section>

            <!-- Section 4: Pricing and Purchase Intent -->
            <section class="section">
                <h2>Pricing and Purchase Intent</h2>
                <label for="price-range">7. What price range would you consider reasonable for this product?</label>
                <select id="price-range" name="price-range" required>
                    <option value="Under $20">Under $20</option>
                    <option value="$20 - $50">$20 - $50</option>
                    <option value="$51 - $100">$51 - $100</option>
                    <option value="$101 - $200">$101 - $200</option>
                    <option value="Over $200">Over $200</option>
                </select>

                <label for="purchase-likelihood">8. How likely are you to purchase this product?</label>
                <input type="radio" id="very-likely" name="purchase-likelihood" value="Very likely" required> Very Likely
                <input type="radio" id="unlikely" name="purchase-likelihood" value="Unlikely" required> Unlikely
            </section>

            <!-- Submit Button -->
            <section class="form-footer">
                <button type="submit">Submit Survey</button>
            </section>
        </form>
    </div>

    <script>
        // JavaScript for handling the form submission and showing feedback
        document.getElementById('survey-form').addEventListener('submit', function(event) {
            event.preventDefault();

            // Collect form data
            const age = document.getElementById('age').value;
            const gender = document.getElementById('gender').value;
            const location = document.getElementById('location').value;
            const heardAbout = document.querySelector('input[name="heard-about"]:checked')?.value;
            const purchaseFrequency = document.getElementById('purchase-frequency').value;
            const features = Array.from(document.querySelectorAll('input[name="features"]:checked'))
                                    .map(checkbox => checkbox.value);
            const priceRange = document.getElementById('price-range').value;
            const purchaseLikelihood = document.querySelector('input[name="purchase-likelihood"]:checked')?.value;

            // Here you can log data to console or send to a server using fetch/AJAX
            console.log({
                age, gender, location, heardAbout, purchaseFrequency, features, priceRange, purchaseLikelihood
            });

            // Show thank you message
            alert('Thank you for completing the survey!');
            document.getElementById('survey-form').reset(); // Reset the form
        });
    </script>
</body>
</html>
