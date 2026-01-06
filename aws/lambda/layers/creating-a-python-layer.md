# Create a python layer in aws lambda and attach it to the lambda function.

**Create an AWS Layer

1. Install the libraries in local dir `python`.
    `pip install requests -t python/`
            or
    `pip install -r requirements.txt -t python/`

2. Create the zip file.
    `zip -r layer.zip python/`

3. Upload the layer to Lambda Layer.

    3.1 Go to Lambda -> Layers -> Create Layer.
    3.2 Give the name and description.
    3.3 Upload the zip `layer.zip`.
    3.4 Choose the architecture and runtime.
    3.5 Click Create.

**Attach it to the Lambda.**

1. Go to the Lambda function's Code section and scroll to the bottom.

2. In the layer section, choose add a layer.

3. Choose Custom layers, and select the layer in the drop down and choose the version.
