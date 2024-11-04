
## Ex 05: Server Side Processing


## Date:
26th October 2024

## AIM:
To design a website that calculates the power of a lamp filament using the formula 
𝑃
=
𝐼
2
×
𝑅
P=I 
2
 ×R, with server-side processing.

## FORMULA:
𝑃
=
𝐼
2
×
𝑅
P=I 
2
 ×R
Where:

𝑃
P = Power (in watts)
𝐼
I = Intensity (in amps)
𝑅
R = Resistance (in ohms)
## DESIGN STEPS:
## Step 1:
Create the front-end using HTML to collect the intensity (I) and resistance (R) values from the user.

## Step 2:
Set up a Flask server to handle the form submission and calculate the power using the formula.

## Step 3:
Create a route in Flask to handle the POST request, extract user inputs, and compute the power using the formula 
𝑃
=
𝐼
2
×
𝑅
P=I 
2
 ×R.

## Step 4:
Use Flask to send the computed result back to the client-side and display the result on the webpage.

## Step 5:
Style the website using CSS for a user-friendly interface.

## Step 6:
Test the website by running the Flask server and interacting with the form.

## PROGRAM :
```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lamp Filament Power Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        h1 {
            color: #4CAF50;
            text-align: center;
        }

        form {
            background-color: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);
            max-width: 300px;
            width: 100%;
            text-align: left;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        input[type="number"] {
            width: calc(100% - 20px);
            padding: 10px;
            margin-bottom: 20px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 16px;
        }

        button {
            width: 100%;
            padding: 10px;
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

        h2 {
            text-align: center;
            color: #333;
        }

        p#result {
            font-size: 18px;
            text-align: center;
            color: #555;
            margin-top: 10px;
        }
    </style>

    <script>
        function calculatePower(event) {
            event.preventDefault(); 
            let intensity = parseFloat(document.getElementById('intensity').value);
            let resistance = parseFloat(document.getElementById('resistance').value);
            let power = Math.pow(intensity, 2) * resistance;
            document.getElementById('result').textContent = `Power: ${power.toFixed(2)} watts`;
        }
    </script>
</head>
<body>
    <div>
        <h1>Lamp Filament Power Calculator</h1>
        <form id="powerForm" onsubmit="calculatePower(event)">
            <label for="intensity">Intensity (I in Amps):</label>
            <input type="number" id="intensity" name="intensity" step="any" required>

            <label for="resistance">Resistance (R in Ohms):</label>
            <input type="number" id="resistance" name="resistance" step="any" required>

            <button type="submit">Calculate Power</button>
        </form>

        <h2>Result:</h2>
        <p id="result">Please enter values and calculate power.</p>
    </div>
</body>
</html>
```
## Output:

![Screenshot 2024-10-26 092133](https://github.com/user-attachments/assets/efa00670-b50a-4112-b2a5-d189489b41a9)

## Result":

The program for performing server side processing is completed successfully.

