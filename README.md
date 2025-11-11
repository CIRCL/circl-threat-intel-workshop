# CIRCL Threat Intelligence Open Source Tools Workshop

This repository contains hands-on Jupyter notebooks for learning threat intelligence analysis using CIRCL's open source tools and services. The workshop covers essential platforms and APIs for cybersecurity professionals and researchers.

## Workshop Contents

### Notebooks Overview

| Notebook | Service | Description |
|----------|---------|-------------|
| `01_misp.ipynb` | MISP | Threat intelligence platform for sharing and correlating IOCs |
| `02_passive_dns.ipynb` | PassiveDNS | Historical DNS resolution data for infrastructure analysis |
| `03_passive_ssl.ipynb` | PassiveSSL | SSL/TLS certificate intelligence and historical tracking |
| `04_passive_ssh.ipynb` | PassiveSSH | SSH fingerprint analysis and infrastructure mapping |
| `05_ransomlook_onionlookup.ipynb` | RansomLook & OnionLookup | Ransomware tracking and Tor hidden service analysis |
| `06_hashlookup.ipynb` | Hashlookup | File hash intelligence and malware identification |
| `07_vulnerability_lookup.ipynb` | Vulnerability-Lookup | Search known vulnerabilities (CVEs), affected products, trends |
| `08_lookyloo.ipynb` | Lookyloo | Website capture and content analysis |

### Learning Objectives

By completing this workshop, you will learn to:

- **Query and analyze threat intelligence** from multiple CIRCL services
- **Correlate indicators across platforms** for comprehensive threat analysis
- **Perform infrastructure analysis** using DNS, SSL, and SSH intelligence
- **Track ransomware activities** and analyze dark web infrastructure
- **Validate file reputation** and identify malicious samples
- **Build automated threat intelligence workflows** using APIs
- **Generate actionable security intelligence** for operational use

### Prerequisites

- Basic Python programming knowledge
- Understanding of cybersecurity fundamentals
- Familiarity with threat intelligence concepts
- Network protocol basics (DNS, SSL/TLS, SSH)

## Getting Started

### Option 1: GitHub Codespaces (Recommended)

GitHub Codespaces provides a cloud-based development environment with all dependencies pre-configured.

#### Using Codespaces

1. **Launch Codespace**
   - Navigate to this repository on GitHub and fork it.
   - While browsing your fork of this repository, click the green **"Code"** button
   - Select the **"Codespaces"** tab
   - Click **"Create codespace on main"**
   - Wait for the environment to initialize (2-3 minutes)

2. **Access Jupyter Notebooks**
   - Once the Codespace loads, the VS Code interface will appear
   - In the terminal, check the open ports and open the URL associated with port 8888. 
   - Copy the Jupyter token from the Codespace terminal and use it to load the Jupyter Notebooks.

3. **Run Notebooks**
   - Select the Python kernel when prompted
   - Execute cells using `Shift + Enter` or the play button
   - Follow the instructions in each notebook

4. **Codespace Features**
   - **Pre-configured Environment**: All required packages are pre-installed
   - **Persistent Storage**: Your work is automatically saved
   - **Port Forwarding**: Access to web services and APIs
   - **Resource Limits**: 2-core, 4GB RAM, 32GB storage (GitHub Free tier)

#### Codespace Management

- **Pause/Resume**: Codespaces automatically pause after 30 minutes of inactivity
- **Multiple Codespaces**: You can run multiple Codespaces simultaneously
- **Sharing**: Share your Codespace with collaborators for pair programming
- **Customization**: Modify the environment using `.devcontainer/` configuration

### Option 2: Local Installation

For local development or when Codespaces quotas are exceeded.

#### Installation Steps

1. **Clone Repository**
   ```bash
   git clone https://github.com/your-org/circl-threat-intel-workshop.git
   cd circl-threat-intel-workshop
   ```

2. **Create Virtual Environment**
   ```bash
   # Ubuntu/Debian
   apt install python3.12-venv
   python3.12 -m venv .venv

   # macOS (with Homebrew)
   brew install python@3.12
   python3.12 -m venv .venv

   # Windows
   python -m venv .venv
   ```

3. **Activate Environment**
   ```bash
   # Linux/macOS
   source .venv/bin/activate

   # Windows
   .venv\Scripts\activate
   ```

4. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Launch Jupyter**
   ```bash
   jupyter lab notebooks/
   ```

## API Credentials Required

Most exercises require API access to CIRCL services. Obtain credentials from:

### Required Services

| Service | URL | API Key Required |
|---------|-------------|-----------------|
| **MISP Training** | https://training.misp-community.org | Yes |
| **PassiveDNS** | https://www.circl.lu/pdns | Yes |
| **PassiveSSL** | https://www.circl.lu/pssl | Yes |
| **PassiveSSH** | https://pssh.circl.lu | Yes |
| **RansomLook** | https://www.ransomlook.io | No |
| **OnionLookup** | https://onion.ail-project.org | No |
| **Hashlookup** | https://hashlookup.circl.lu | No |
| **Vulnerability-Lookup** | https://vulnerability.circl.lu/ | No |
| **Lookyloo** | https://lookyloo.circl.lu | No |
| **Pandora** | https://pandora.circl.lu | No |

### Credential Management

- **Never commit API keys** to version control
- Use environment variables or secure credential managers
- The notebooks use `getpass()` for secure credential input
- Follow the principle of least privilege for API access

## Workshop Structure

### Difficulty Progression

1. **Beginner**: Notebooks 01-02 (MISP, PassiveDNS)
2. **Intermediate**: Notebooks 03-04 (PassiveSSL, PassiveSSH)
3. **Advanced**: Notebooks 05-06 (RansomLook/OnionLookup, Hashlookup)

### Exercise Types

- **Guided Examples**: Step-by-step API usage with explanations
- **Hands-on Practice**: Apply concepts to real-world scenarios
- **Student Challenges**: Independent problem-solving exercises
- **Homework Assignments**: Extended practice with deliverables

### Best Practices

- **Start with MISP**: Foundation for threat intelligence concepts
- **Complete notebooks sequentially**: Each builds on previous knowledge
- **Practice correlation**: Combine data from multiple sources
- **Focus on practical applications**: Real-world security use cases
- **Document your findings**: Build a threat intelligence methodology

## Troubleshooting

### Common Issues

**Codespace won't start**
- Check GitHub Codespaces usage limits
- Try creating a new Codespace
- Verify repository permissions

**API authentication errors**
- Verify API keys are correct and active
- Check service status pages
- Ensure proper credential input format

**Notebook kernel issues**
- Restart the kernel: `Kernel > Restart`
- Clear output: `Cell > All Output > Clear`
- Reinstall packages if needed

**Network connectivity problems**
- Check internet connection
- Verify firewall/proxy settings
- Some services may have geographic restrictions

### Getting Help

- **GitHub Issues**: Report bugs or request features
- **CIRCL Documentation**: Service-specific help and examples
- **Community Forums**: Join threat intelligence communities
- **Workshop Discussions**: Use GitHub Discussions for questions

## Contributing

We welcome contributions to improve the workshop:

- **Report Issues**: Bug reports and improvement suggestions
- **Submit Pull Requests**: Code improvements and new exercises
- **Update Documentation**: Clarify instructions and add examples
- **Share Use Cases**: Real-world applications and success stories

## License

All the materials are dual-licensed under GNU Affero General Public License version 3 or later and the Creative Commons Attribution-ShareAlike 4.0 International. You can use either one of the licenses depending of your use case of the training materials.

## Acknowledgments

- **CIRCL Team**: For developing and maintaining the threat intelligence services
- **MISP Community**: For the collaborative threat intelligence platform
- **Contributors**: Community members who improve and extend the workshop

## Additional Resources

### Documentation Links
- [CIRCL Services](https://www.circl.lu/services/)
- [MISP Project](https://www.misp-project.org/)
- [PyMISP Documentation](https://pymisp.readthedocs.io/)
- [PassiveDNS](https://www.circl.lu/services/passive-dns/)
- [PassiveSSL](https://www.circl.lu/services/passive-ssl/)
- [PassiveSSH](https://d4-project.github.io/passive-ssh/)
- [RansomLook](https://www.ransomlook.io/doc/)
- [OnionLookup](https://onion.ail-project.org/apiman/swagger/)
- [VulnerabilityLookup](https://www.vulnerability-lookup.org/documentation/)
- [Lookyloo](https://www.lookyloo.eu/docs/main/index.html/)
- [Pandora](https://github.com/pandora-analysis/pandora)

### Training Materials
- [MISP Training Materials](https://github.com/MISP/misp-training)
- [Online Video Trainings](https://www.youtube.com/CIRCL)
- [CIRCL Workshops and Conferences](https://www.circl.lu/training/)

For more advanced MISP playbooks check the dedicated repository:
- https://github.com/MISP/misp-playbooks

---

**Ready to start?** Launch a GitHub Codespace or follow the local installation instructions above, then begin with `01_misp.ipynb` to start your threat intelligence journey!