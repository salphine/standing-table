<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Market Research Survey</title>
</head>
<body>
    <h2>Market Research Survey for a New Product</h2>
    <form action="survey.php" method="POST">
        <h3>1. Demographic Information</h3>
        <label>What is your age?</label><br>
        <select name="age" required>
            <option>Under 18</option>
            <option>18-24</option>
            <option>25-34</option>
            <option>35-44</option>
            <option>45-54</option>
            <option>55-64</option>
            <option>65 or older</option>
        </select><br><br>

        <label>What is your gender?</label><br>
        <select name="gender" required>
            <option>Male</option>
            <option>Female</option>
            <option>Non-binary/Third gender</option>
            <option>Prefer not to say</option>
        </select><br><br>

        <label>Location:</label><br>
        <input type="text" name="location" required><br><br>

        <label>Occupation:</label><br>
        <input type="text" name="occupation" required><br><br>

        <h3>2. Product Awareness</h3>
        <label>Have you heard about our new product before?</label><br>
        <select name="heard_about" required>
            <option>Yes</option>
            <option>No</option>
        </select><br><br>

        <label>If yes, where did you hear about it?</label><br>
        <input type="checkbox" name="source[]" value="Social Media"> Social Media
        <input type="checkbox" name="source[]" value="Email"> Email
        <input type="checkbox" name="source[]" value="Word of Mouth"> Word of Mouth
        <input type="checkbox" name="source[]" value="Advertisement"> Advertisement<br><br>

        <h3>3. Product Preferences</h3>
        <label>What features are most important? (Select up to 3)</label><br>
        <input type="checkbox" name="important_features[]" value="Price"> Price
        <input type="checkbox" name="important_features[]" value="Quality"> Quality
        <input type="checkbox" name="important_features[]" value="Brand"> Brand
        <input type="checkbox" name="important_features[]" value="Durability"> Durability<br><br>

        <h3>4. Pricing and Purchase Intent</h3>
        <label>What price range would you consider reasonable?</label><br>
        <select name="price_range" required>
            <option>Under $20</option>
            <option>$20 - $50</option>
            <option>$51 - $100</option>
            <option>$101 - $200</option>
            <option>Over $200</option>
        </select><br><br>

        <h3>5. Competitor Products</h3>
        <label>Are you using a similar product from another brand?</label><br>
        <select name="competitor_product">
            <option>Yes</option>
            <option>No</option>
        </select><br><br>

        <label>What do you like most about the current product?</label><br>
        <textarea name="competitor_likes"></textarea><br><br>

        <label>Final thoughts?</label><br>
        <textarea name="product_feedback"></textarea><br><br>

        <button type="submit">Submit Survey</button>
    </form>
</body>
</html>
