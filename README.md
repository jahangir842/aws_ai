# aws_ai
GitHub repo that helps you learn AWS AI services (like Rekognition, Comprehend, Translate, Polly, Textract, Bedrock, SageMaker) with Terraform.

Here’s a recommended repo layout:

```
aws-ai-terraform-lab/
├── README.md                 # Overview of repo, how to use
├── .gitignore                # Ignore terraform local state files etc.
├── modules/                  # Reusable Terraform modules
│   ├── rekognition/          # Custom module for Rekognition
│   │   └── main.tf
│   ├── comprehend/           # Custom module for Comprehend
│   │   └── main.tf
│   ├── polly/                # Custom module for Polly
│   │   └── main.tf
│   ├── translate/
│   │   └── main.tf
│   ├── textract/
│   │   └── main.tf
│   ├── sagemaker/
│   │   └── main.tf
│   └── bedrock/
│       └── main.tf
│
├── examples/                 # Hands-on labs / tutorials
│   ├── rekognition-demo/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   ├── outputs.tf
│   │   └── README.md
│   ├── comprehend-demo/
│   │   ├── main.tf
│   │   └── README.md
│   ├── polly-demo/
│   │   └── main.tf
│   ├── translate-demo/
│   │   └── main.tf
│   ├── textract-demo/
│   │   └── main.tf
│   ├── sagemaker-demo/
│   │   └── main.tf
│   └── bedrock-demo/
│       └── main.tf
│
├── environments/             # If you want dev/test/prod separation
│   ├── dev/
│   │   ├── main.tf
│   │   ├── variables.tf
│   │   └── terraform.tfvars
│   └── prod/
│       ├── main.tf
│       ├── variables.tf
│       └── terraform.tfvars
│
└── scripts/                  # Helper scripts (optional)
    ├── init.sh               # Terraform init + backend setup
    └── destroy.sh            # Clean up resources
```

---

✅ **How you’ll work inside this repo**

* **modules/** → reusable blueprints of AWS AI services.
* **examples/** → small labs (e.g., detect faces with Rekognition, sentiment analysis with Comprehend).
* **environments/** → manage dev/prod configs with `terraform.tfvars`.
* **scripts/** → quick setup/cleanup helpers.

---

👉 Example: If you want to try **Rekognition face detection**, you’d:

1. Go to `examples/rekognition-demo/`
2. Run:

   ```bash
   terraform init
   terraform apply
   ```
3. Test the output in AWS Console or via AWS CLI.

---
