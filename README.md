# Simple Static Website Example

This repository contains a **simple static HTML website** that can be hosted on **AWS S3** using a fully automated **AWS CodePipeline** setup. The infrastructure for deploying this website is managed using **Terraform**, and the deployment pipeline is triggered automatically on changes to the GitHub repository.

## Project Structure

```bash
.
├── index.html           # The homepage of the static website
├── styles.css           # Basic styles for the website
└── README.md            # This file
```

## Features

- **Static Website**: The website is purely HTML and CSS, with no server-side code required.
- **AWS S3**: The website is deployed to an **S3 bucket**, which is configured for static website hosting.
- **Automated Pipeline**: **AWS CodePipeline** is used for CI/CD to automatically deploy the website to S3 when changes are pushed to the GitHub repository.

## How to Use

1. **Clone the repository:**

   Clone the repository to your local machine or fork it for your own use:

   ```bash
   git clone https://github.com/prathameshmhatre/html-static-website.git
   cd html-static-website
   ```

2. **Modify the HTML content:**

   Customize the `index.html` file and any other files (e.g., `styles.css`) as required for your static website. You can add images, more pages, or styles as needed.

3. **Push your changes to GitHub:**

   After making changes to your static website, push them to your GitHub repository. This will automatically trigger the **AWS CodePipeline** pipeline and deploy the changes to the S3 bucket.

   ```bash
   git add .
   git commit -m "Updated website content"
   git push origin main
   ```

4. **Check the deployed website:**

   Once the pipeline runs successfully, your static website will be available at the **S3 bucket's website endpoint**.

## Project Deployment

This repository is designed to work with the **Terraform infrastructure** from [aws-static-website-codepipeline-infra](https://github.com/prathameshmhatre/aws-static-website-codepipeline-infra). Please follow the instructions in that repository to set up the **AWS CodePipeline**, S3 bucket, and other resources.

### Deployment Process

1. The **AWS CodePipeline** automatically triggers when code is pushed to the GitHub repository.
2. The pipeline will:
   - Pull the static website code from GitHub.
   - The **S3 bucket** will serve the website content publicly as a static website.

## Demo

To see a live demo of this static website, you can deploy it using the provided infrastructure, or you can customize the code and host it on your own AWS account.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
