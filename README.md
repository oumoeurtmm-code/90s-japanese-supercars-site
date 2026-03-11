# 90s Japanese Supercars Site

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![AWS S3](https://img.shields.io/badge/AWS_S3-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)
![CloudFront](https://img.shields.io/badge/CloudFront-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)

A **responsive static website** showcasing the **Top 5 '90s Japanese Supercars** — built as the content layer for **AWS Lab 01** of a hands-on cloud engineering study series.

---

## 🏎 The Cars

| # | Car | Nickname |
|---|---|---|
| 1 | Nissan Skyline GT-R R34 | Godzilla |
| 2 | Toyota Supra MkIV | 2JZ Legend |
| 3 | Mazda RX-7 FD | Rotary King |
| 4 | Honda NSX-R | Ferrari Killer |
| 5 | Mitsubishi 3000GT | Tech Showcase |

---

## ☁️ AWS Deployment — Lab 01

This site is deployed on AWS as part of a hands-on cloud engineering lab series. The infrastructure uses:

| Service | Role |
|---|---|
| **Amazon S3** | Object storage — private bucket, versioning enabled, public access blocked |
| **Amazon CloudFront** | CDN — HTTPS enforced, HTTP/2, 400+ global edge locations |
| **Origin Access Control (OAC)** | SigV4-signed requests — S3 never directly accessible |
| **IAM Bucket Policy** | Least-privilege — scoped to this specific CloudFront distribution ARN |
| **Amazon CloudWatch** | 4xx error rate alarm — alerts if error rate exceeds 5% |

### 🔗 Related Links

- **[Lab 01 Project Page](https://oumoeurtmm-code.github.io/projects/aws-lab-01-static-website/)** — Architecture diagrams, deployment process, key concepts, and cost breakdown
- **[Deploy + Cleanup Scripts](https://github.com/oumoeurtmm-code/ai-terminal-workflow/tree/master/aws-projects/01-static-website-aws-fundamentals)** — Full IaC automation in `ai-terminal-workflow`
- **[AWS Lab Series Tracker](https://oumoeurtmm-code.github.io/projects/project-tracker/)** — Track progress across all 5 labs

---

## 🗂 File Structure

```
90s-japanese-supercars-site/
├── index.html      # Main site — 5 car showcase
├── style.css       # Responsive styling
└── images/
    ├── r34.jpg     # Nissan Skyline GT-R R34
    ├── supra.jpg   # Toyota Supra MkIV
    ├── rx7.jpg     # Mazda RX-7 FD
    ├── nsx.jpg     # Honda NSX-R
    └── 3000gt.jpg  # Mitsubishi 3000GT
```

---

## 💻 Run Locally

```bash
git clone https://github.com/oumoeurtmm-code/90s-japanese-supercars-site.git
cd 90s-japanese-supercars-site
open index.html    # macOS
start index.html   # Windows
```

---

## 🚀 Deploy to AWS (Lab 01)

```bash
# Clone the lab repo
git clone https://github.com/oumoeurtmm-code/ai-terminal-workflow.git

# Run the deploy script
bash ai-terminal-workflow/aws-projects/01-static-website-aws-fundamentals/scripts/deploy.sh

# Clean up all resources when done
bash ai-terminal-workflow/aws-projects/01-static-website-aws-fundamentals/scripts/cleanup.sh
```

---

<div align="center">
  <sub>Part of the <a href="https://oumoeurtmm-code.github.io">oumoeurtmm-code</a> AWS Lab Series · Built with HTML/CSS · Deployed on AWS</sub>
</div>
