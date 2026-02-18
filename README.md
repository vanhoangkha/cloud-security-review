# 🛡️ Awesome Cloud Security - Tổng hợp & Đánh giá Chi tiết

> **Repository:** [NextSecurity/Awesome-Cloud-Security](https://github.com/NextSecurity/Awesome-Cloud-Security)  
> **License:** GPL-3.0 | **Stars:** 126 | **Forks:** 31  
> **Ngày review:** 18/02/2026

---

## 📋 Mục lục

- [Giới thiệu](#giới-thiệu)
- [Cấu trúc Repository](#cấu-trúc-repository)
- [Phân tích chi tiết các công cụ](#phân-tích-chi-tiết-các-công-cụ)
- [Tài liệu học tập](#tài-liệu-học-tập)
- [So sánh với các Awesome List khác](#so-sánh-với-các-awesome-list-khác)
- [Đánh giá và Khuyến nghị](#đánh-giá-và-khuyến-nghị)

---

## Giới thiệu

**Awesome Cloud Security** là một curated list tổng hợp các công cụ, tài nguyên và tài liệu về bảo mật đám mây. Repository này tập trung vào 3 nhà cung cấp cloud lớn nhất: **AWS**, **Microsoft Azure** và **Google Cloud Platform (GCP)**.

### Đối tượng phù hợp

| Vai trò | Mức độ phù hợp | Lý do |
|---------|----------------|-------|
| Cloud Security Engineer | ⭐⭐⭐⭐⭐ | Công cụ audit, compliance đầy đủ |
| Penetration Tester | ⭐⭐⭐⭐⭐ | Nhiều tool offensive cho cloud |
| DevSecOps Engineer | ⭐⭐⭐⭐ | IaC scanning tools, CI/CD integration |
| Security Architect | ⭐⭐⭐⭐ | Reference về native security services |
| Beginner | ⭐⭐⭐ | Cần kiến thức nền tảng trước |

---

## Cấu trúc Repository

Repository được tổ chức theo cấu trúc logic, dễ navigate:

```
Awesome-Cloud-Security/
├── Standards/
│   ├── Compliances (CSA STAR, ISO 27017/27018, MTCS)
│   └── Benchmarks (CIS Benchmark)
├── Tools/
│   ├── Infrastructure (40+ tools)
│   ├── Container (5 tools)
│   ├── SaaS (7 tools)
│   ├── Native tools (AWS/Azure/GCP)
│   └── Penetration Testing/
│       ├── Enumeration
│       ├── Information Gathering
│       ├── Lateral Movement
│       └── Exploitation
├── Reading Materials/
│   ├── AWS
│   ├── Azure
│   ├── GCP
│   └── Others
└── Resources/
    ├── Lists and Cheat Sheets
    ├── Lab Exercises
    ├── Talks & Videos
    └── Books
```

---

## Phân tích chi tiết các công cụ

### 1. Infrastructure Security Tools

#### 🔵 Công cụ Audit & Assessment

| Tool | Cloud | Mô tả | Use Case |
|------|-------|-------|----------|
| **[Prowler](https://github.com/toniblyx/prowler)** | AWS | Security Best Practices Assessment | CIS Benchmark compliance, forensics |
| **[ScoutSuite](https://github.com/nccgroup/ScoutSuite)** | Multi-cloud | Multi-cloud security auditing | Cross-cloud security posture |
| **[CloudMapper](https://github.com/duo-labs/cloudmapper)** | AWS | Visualize AWS environments | Network topology analysis |
| **[Cloudsplaining](https://github.com/salesforce/cloudsplaining)** | AWS | IAM Security Assessment | Least privilege violations |

#### 🟢 Công cụ IaC Security

| Tool | Supported IaC | Mô tả |
|------|---------------|-------|
| **[Checkov](https://github.com/bridgecrewio/checkov)** | Terraform, CloudFormation, K8s | Static code analysis cho IaC |
| **[tfsec](https://github.com/liamg/tfsec)** | Terraform | Security scanner cho Terraform |
| **[Terrascan](https://github.com/accurics/terrascan)** | Terraform, K8s, Helm | Compliance và security violations |
| **[KICS](https://github.com/Checkmarx/kics)** | Multi-IaC | Find vulnerabilities early in dev cycle |

#### 🔴 Công cụ Offensive/Red Team

| Tool | Cloud | Mô tả |
|------|-------|-------|
| **[Pacu](https://github.com/RhinoSecurityLabs/pacu)** | AWS | AWS exploitation framework |
| **[CloudGoat](https://github.com/RhinoSecurityLabs/cloudgoat)** | AWS | "Vulnerable by Design" deployment |
| **[Leonidas](https://github.com/FSecureLABS/leonidas)** | AWS | Execute attacker actions in cloud |

### 2. Container Security Tools

| Tool | Mô tả | Tính năng chính |
|------|-------|-----------------|
| **[Falco](https://github.com/falcosecurity/falco)** | Container runtime security | Real-time threat detection |
| **[mkit](https://github.com/darkbitio/mkit)** | Managed K8s inspection | EKS/AKS/GKE audit |
| **[ccat](https://github.com/RhinoSecurityLabs/ccat)** | Cloud Container Attack Tool | Container exploitation |

### 3. Penetration Testing Tools

#### Phase 1: Enumeration

```
┌─────────────────────────────────────────────────────────────┐
│                    ENUMERATION PHASE                         │
├─────────────────────────────────────────────────────────────┤
│  o365creeper     → Enumerate valid O365 email addresses     │
│  CloudBrute      → Multi-cloud infrastructure discovery     │
│  cloud_enum      → AWS/Azure/GCP public resource enum       │
│  BlobHunter      → Azure blob storage scanner               │
│  Grayhat Warfare → Open bucket/blob search engine           │
└─────────────────────────────────────────────────────────────┘
```

#### Phase 2: Information Gathering

| Tool | Target | Chức năng |
|------|--------|-----------|
| **ROADtools** | Azure AD | Framework tương tác với Azure AD |
| **PowerZure** | Azure | PowerShell framework for Azure security |
| **Azurite** | Azure | Enumeration và reconnaissance |
| **Hawk** | O365 | Gather info về O365 intrusions |

#### Phase 3: Lateral Movement

| Tool | Mô tả |
|------|-------|
| **Stormspotter** | Graph Azure và Azure AD objects |
| **AzureADLateralMovement** | Lateral movement graph cho Azure AD |
| **SkyArk** | Discover privileged entities trong Azure/AWS |

#### Phase 4: Exploitation

| Tool | Attack Type | Mô tả |
|------|-------------|-------|
| **MicroBurst** | Multi-purpose | Collection of Azure security scripts |
| **MSOLSpray** | Password Spray | Microsoft Online accounts attack |
| **MFASweep** | MFA Bypass | Check MFA status on Microsoft services |
| **adconnectdump** | Credential Dump | Dump Azure AD Connect credentials |

### 4. Native Security Services Reference

#### AWS Security Services

```
┌────────────────────────────────────────────────────────────────┐
│                    AWS SECURITY STACK                           │
├────────────────────────────────────────────────────────────────┤
│  IDENTITY & ACCESS                                              │
│  └── IAM, Certificate Manager, KMS, CloudHSM, Secret Manager   │
│                                                                 │
│  DETECTION & MONITORING                                         │
│  └── GuardDuty, Inspector, Detective, CloudTrail, Config       │
│                                                                 │
│  NETWORK SECURITY                                               │
│  └── WAF, Shield, Network Firewall, Firewall Manager           │
│                                                                 │
│  DATA PROTECTION                                                │
│  └── Macie, VPC Flowlog                                        │
│                                                                 │
│  INTEGRATION                                                    │
│  └── Security Hub                                              │
└────────────────────────────────────────────────────────────────┘
```

#### Azure Security Services

| Category | Services |
|----------|----------|
| Network | Application Gateway (WAF), DDoS Protection |
| Identity | Key Vault, Dedicated HSM |
| Monitoring | Monitor, Security Center |
| SIEM | Sentinel |

#### GCP Security Services

| Category | Services |
|----------|----------|
| Visibility | Access Transparency, Asset Inventory, Audit Logs |
| Protection | Armor (DDoS/WAF), VPC Service Controls |
| Identity | Cloud HSM, KMS, EKM, Identity-Aware Proxy |
| Detection | Security Command Center, Event Threat Detection |

---

## Tài liệu học tập

### AWS Resources

| Resource | Type | Link |
|----------|------|------|
| AWS Security Overview | Official | [aws.amazon.com/security](https://aws.amazon.com/security/) |
| AWS IAM Privilege Escalation | Research | [RhinoSecurityLabs](https://github.com/RhinoSecurityLabs/AWS-IAM-Privilege-Escalation) |
| MITRE ATT&CK for AWS | Framework | [attack.mitre.org](https://attack.mitre.org/matrices/enterprise/cloud/aws/) |
| AWS Security Workshops | Hands-on | [aws-samples](https://github.com/aws-samples/aws-security-workshops) |

### Azure Resources

| Resource | Mô tả |
|----------|-------|
| Azure AD SSO Abuse | Kỹ thuật abuse Primary Refresh Token |
| Dynamic Groups Privilege Escalation | Escalation qua dynamic groups |
| PowerZure Introduction | Attacking Azure với PowerZure |
| Azure AD Connect for Red Teamers | Exploit AD Connect |

### GCP Resources

| Resource | Link |
|----------|------|
| GCP Security Overview | [cloud.google.com/security](https://cloud.google.com/security) |
| GKE Security Scenarios | [GoogleCloudPlatform](https://github.com/GoogleCloudPlatform/gke-security-scenarios-demo) |
| MITRE ATT&CK for GCP | [attack.mitre.org](https://attack.mitre.org/matrices/enterprise/cloud/gcp/) |

### Lab Environments

| Lab | Platform | Mô tả |
|-----|----------|-------|
| CloudGoat | AWS | Vulnerable by design AWS |
| TerraGoat | Multi-cloud | Vulnerable Terraform repo |
| azure-security-lab | Azure | Hands-on security lab |
| Serverless Goat | AWS Lambda | Serverless security flaws |

---

## So sánh với các Awesome List khác

| Feature | Awesome-Cloud-Security | HackTricks Cloud | Cloudberry Engineering |
|---------|------------------------|------------------|------------------------|
| AWS Coverage | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| Azure Coverage | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| GCP Coverage | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐ |
| Tool Links | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ |
| Tutorials | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐⭐ |
| Update Frequency | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |

---

## Đánh giá và Khuyến nghị

### Điểm mạnh ✅

1. **Tổ chức tốt**: Phân loại rõ ràng theo cloud provider và use case
2. **Đa dạng công cụ**: Cover cả defensive và offensive security
3. **Native services reference**: Hữu ích cho security architecture
4. **Penetration testing workflow**: Theo đúng methodology (Enum → Info Gathering → Lateral Movement → Exploitation)
5. **Lab resources**: Có môi trường thực hành

### Điểm cần cải thiện ⚠️

1. **Update frequency**: Repo có ít commits, một số tool có thể outdated
2. **Kubernetes security**: Thiếu coverage cho EKS/AKS/GKE security
3. **Serverless security**: Chưa có section riêng cho Lambda/Functions security
4. **Multi-cloud scenarios**: Thiếu guidance cho hybrid/multi-cloud
5. **Automation/CI-CD**: Thiếu integration examples

### Khuyến nghị sử dụng

#### Cho Blue Team / Defensive Security:

```bash
# Priority tools to learn:
1. Prowler (AWS audit)
2. ScoutSuite (Multi-cloud audit)
3. Checkov (IaC scanning)
4. Falco (Container runtime)
```

#### Cho Red Team / Offensive Security:

```bash
# Priority tools to learn:
1. Pacu (AWS exploitation)
2. MicroBurst (Azure attacks)
3. ROADtools (Azure AD)
4. CloudGoat (Practice lab)
```

#### Learning Path đề xuất:

```
Week 1-2: Fundamentals
├── Read AWS/Azure/GCP security overviews
├── Setup CloudGoat lab
└── Learn CIS Benchmarks

Week 3-4: Defensive Tools
├── Master Prowler/ScoutSuite
├── Implement Checkov in CI/CD
└── Deploy Falco for containers

Week 5-6: Offensive Tools
├── Practice with Pacu
├── Learn MicroBurst for Azure
└── Study MITRE ATT&CK Cloud matrices

Week 7-8: Advanced
├── Azure AD attacks (ROADtools, PowerZure)
├── Lateral movement techniques
└── Build custom detection rules
```

---

## Tổng kết

### Rating: ⭐⭐⭐⭐ (4/5)

**Awesome Cloud Security** là một starting point tốt cho bất kỳ ai muốn tìm hiểu về Cloud Security. Repository cung cấp một cái nhìn tổng quan về các công cụ và tài nguyên có sẵn, đặc biệt mạnh về Azure security tools.

### Khi nào nên dùng repo này:

- ✅ Tìm kiếm công cụ audit cloud infrastructure
- ✅ Cần reference về native security services
- ✅ Học penetration testing cho cloud
- ✅ Tìm lab environments để practice

### Khi nào nên tìm nguồn khác:

- ❌ Cần tutorials chi tiết step-by-step
- ❌ Tìm hiểu về cloud security mới nhất (2024-2026)
- ❌ Multi-cloud/hybrid security architecture

---

## Tài liệu tham khảo bổ sung

- [HackTricks Cloud](https://cloud.hacktricks.xyz/)
- [MITRE ATT&CK Cloud Matrix](https://attack.mitre.org/matrices/enterprise/cloud/)
- [AWS Security Documentation](https://docs.aws.amazon.com/security/)
- [Azure Security Best Practices](https://docs.microsoft.com/en-us/azure/security/fundamentals/)
- [GCP Security Best Practices](https://cloud.google.com/security/best-practices)

---

*Bài viết được tạo bởi [vanhoangkha](https://github.com/vanhoangkha) | Cập nhật: 18/02/2026*
