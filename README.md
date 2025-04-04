
 <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HODOR - Eco-Friendly Hoodies</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            background: #0f0f10;
            color: #e0e0e0;
            line-height: 1.6;
        }
        header {
            background: linear-gradient(90deg, #1a1a2e, #16213e);
            padding: 20px;
            text-align: center;
        }
        header h1 {
            font-size: 3rem;
            color: #00ffab;
        }
        .container {
            padding: 20px;
        }
        .article {
            margin-bottom: 40px;
            text-align: justify;
        }
        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
        }
        .gallery div {
            background: #1a1a2e;
            padding: 10px;
            text-align: center;
            border-radius: 8px;
        }
        .gallery div img {
            width: 100%;
            border-radius: 8px;
        }
        button {
            background: #00ffab;
            color: #0f0f10;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 1rem;
        }
        button:hover {
            background: #00b56a;
        }
        #survey-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
        }
        #survey-modal .modal-content {
            background: #1a1a2e;
            padding: 20px;
            border-radius: 8px;
            width: 90%;
            max-width: 400px;
        }
        #survey-modal label {
            display: block;
            margin: 10px 0 5px;
        }
        #survey-modal input, #survey-modal select {
            width: 100%;
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        #close-modal {
            background: #e63946;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>HODOR</h1>
        <p>Eco-Friendly Hoodies for a Sustainable Future</p>
    </header>

    <div class="container">
        <section class="article">
            <h2>Why Choose Eco-Friendly Hoodies?</h2>
            <p>Eco-friendly hoodies are made from sustainable materials such as organic cotton, recycled fibers, and low-impact dyes. By choosing these hoodies, you contribute to reducing waste and promoting a healthier environment. HODOR is committed to providing stylish and comfortable clothing that aligns with your values and protects the planet.</p>
        </section>

        <section class="gallery">
            <div>
                <p>Anime Art Hoodie</p>
                <div style="height: 200px; background-color: #333;">[Anime Art Placeholder]</div>
            </div>
            <div>
                <p>Artistic Hoodie</p>
                <div style="height: 200px; background-color: #333;">[Artistic Placeholder]</div>
            </div>
            <div>
                <p>Plain Hoodie</p>
                <div style="height: 200px; background-color: #333;">[Plain Placeholder]</div>
            </div>
        </section>

        <button id="open-survey">Take Our Survey</button>

        <div id="survey-modal">
            <div class="modal-content">
                <h2>Hoodie Preferences Survey</h2>
                <form id="survey-form">
                    <label for="color">Favorite Hoodie Color:</label>
                    <input type="text" id="color" name="color" required>

                    <label for="style">Preferred Style:</label>
                    <select id="style" name="style" required>
                        <option value="anime">Anime Art</option>
                        <option value="artistic">Artistic</option>
                        <option value="plain">Plain (No Image)</option>
                    </select>

                    <label for="comments">Additional Comments:</label>
                    <textarea id="comments" name="comments" rows="3"></textarea>

                    <button type="submit">Submit</button>
                    <button type="button" id="close-modal">Close</button>
                </form>
            </div>
        </div>
    </div>

    <script>
        const openSurvey = document.getElementById('open-survey');
        const surveyModal = document.getElementById('survey-modal');
        const closeModal = document.getElementById('close-modal');

        openSurvey.addEventListener('click', () => {
            surveyModal.style.display = 'flex';
        });

        closeModal.addEventListener('click', () => {
            surveyModal.style.display = 'none';
        });

        document.getElementById('survey-form').addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your feedback!');
            surveyModal.style.display = 'none';
        });
    </script>
</body>
</html>
