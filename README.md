## Introduction

Auto_Jobs_Applier_Automate Form Filler is a cutting-edge, automated tool designed to revolutionize the job search and application process. In today's fiercely competitive job market, where opportunities can vanish in the blink of an eye, this program offers job seekers a significant advantage. By leveraging the power of automation and artificial intelligence, Auto_Jobs_Applier_Automate Form Filler enables users to apply to a vast number of relevant positions efficiently and in a personalized manner, maximizing their chances of landing their dream job.

### The Challenge of Modern Job Hunting

In the digital age, the job search landscape has undergone a dramatic transformation. While online platforms have opened up a world of opportunities, they have also intensified competition. Job seekers often find themselves spending countless hours scrolling through listings, tailoring applications, and repetitively filling out forms. This process can be not only time-consuming but also emotionally draining, leading to job search fatigue and missed opportunities.

### Enter Auto_Jobs_Applier_Automate Form Filler: Your Personal Job Search Assistant

Auto_Jobs_Applier_Automate Form Filler steps in as a game-changing solution to these challenges. It's not just a tool; it's your tireless, 24/7 job search partner. By automating the most time-consuming aspects of the job search process, it allows you to focus on what truly matters - preparing for interviews and developing your professional skills.


## Installation

**Confirmed succesfull runs on the following:**
- Operating Systems:
  - Windows 10
  - Ubuntu 22
- Python versions:
  - 3.10
  - 3.11.9(64b)
  - 3.12.5(64b)

1. **Download and Install Python:**

   Ensure you have the last Python version  installed. If not, download and install it from Python's official website. For detailed instructions, refer to the tutorials:

   

2. **Download and Install Google Chrome:**
   - Download and install the latest version of Google Chrome in its default location from the 

## Configuration

### 1. secrets.yaml

This file contains sensitive information. Never share or commit this file to version control.

- `llm_api_key: [Your OpenAI or Ollama API key or Gemini API key]`
  - Replace with your OpenAI API key for GPT integration
  - To obtain an API key, 
  - Note: You need to add credit to your OpenAI account to use the API. You can add credit by visiting the
  - According to the  and our users' reports, right after setting up the OpenAI account and purchasing the required credits, users still have a `Free` account type. This prevents them from having unlimited access to OpenAI models and allows only 200 requests per day. This might cause runtime errors such as:  
     
    OpenAI will update your account automatically, but it might take some time, ranging from a couple of hours to a few days.  
    You can find more about your organization limits on the .
 


#### Usage

Using this folder as a guide can be particularly helpful for:

1. Understanding the correct structure of each configuration file
2. Seeing examples of valid data for each field
3. Having a reference point while filling out your personal files


## Usage
0. **Account language**
   To ensure the bot works, your account language must be set to English.
   
2. **Data Folder:**
   Ensure that your data_folder contains the following files:
   - `secrets.yaml`
   - `config.yaml`
   - `plain_text_resume.yaml`

3. **Run the Bot:**

   Auto_Jobs_Applier_Automate Form Filler offers flexibility in how it handles your pdf resume:

- **Dynamic Resume Generation:**
  If you don't use the `--resume` option, the bot will automatically generate a unique resume for each application. This feature uses the information from your `plain_text_resume.yaml` file and tailors it to each specific job application, potentially increasing your chances of success by customizing your resume for each position.
   ```bash
   python main.py
   ```
- **Using a Specific Resume:**
  If you want to use a specific PDF resume for all applications, place your resume PDF in the `data_folder` directory and run the bot with the `--resume` option:
  ```bash
  python main.py --resume /path/to/your/resume.pdf
  ```


### Troubleshooting Common Issues

#### 1. OpenAI API Rate Limit Errors

**Error Message:**

openai.RateLimitError: Error code: 429 - {'error': {'message': 'You exceeded your current quota, please check your plan and billing details. For more information on this error, 'type': 'insufficient_quota', 'param': None, 'code': 'insufficient_quota'}}

**Solution:**

- Ensure you have added a valid payment method to your OpenAI account
- Note that ChatGPT Plus subscription is different from API access
- If you've recently added funds or upgraded, wait 12-24 hours for changes to take effect
- Free tier has a 3 RPM limit; spend at least $5 on API usage to increase

#### 2. Easy Apply Button Not Found

**Error Message:**

Exception: No clickable 'Easy Apply' button found

**Solution:**
- Ensure that you're logged properly
- Check if the job listings you're targeting actually have the "Easy Apply" option
- Verify that your search parameters in the `config.yaml` file are correct and returning jobs with the "Easy Apply" button
- Try increasing the wait time for page loading in the script to ensure all elements are loaded before searching for the button

#### 3. Incorrect Information in Job Applications

**Issue:** Bot provides inaccurate data for experience, CTC, and notice period

**Solution:**
- Update prompts for professional experience specificity
- Add fields in `config.yaml` for current CTC, expected CTC, and notice period
- Modify bot logic to use these new config fields

#### 4. YAML Configuration Errors

**Error Message:**

yaml.scanner.ScannerError: while scanning a simple key

**Solution:**
- Copy example `config.yaml` and modify gradually
- Ensure proper YAML indentation and spacing
- Use a YAML validator tool
- Avoid unnecessary special characters or quotes

#### 5. Bot Logs In But Doesn't Apply to Jobs

**Issue:** Bot searches for jobs but continues scrolling without applying

**Solution:**
- Check for security checks or CAPTCHAs
- Verify `config.yaml` job search parameters
- Ensure your account profile meets job requirements
- Review console output for error messages

### General Troubleshooting Tips

- Use the latest version of the script
- Verify all dependencies are installed and updated
- Check internet connection stability
- Clear browser cache and cookies if issues persist

For further assistance, please create an issue on the  with detailed information about your problem, including error messages and your configuration (with sensitive information removed).

## Setup Documents

### Ollama & Gemini Setup

To install and configure **Ollama** and **Gemini**

Follow the instructions in these guides to ensure proper configuration of **Automate Form Filler** with **Ollama** and **Gemini**.


### Editing YAML Files
For detailed instructions on editing YAML configuration sections for **Automate Form Filler**

### Auto-start Automate Form Filler
To make **Automate Form Filler** automatically start when your system boots

Navigate to the docs/ directory and download the PDF guides you need.


### Additional Resources



If you encounter any issues, you can open an issue on 
  Please add valuable details to the subject and to the description. If you need new feature then please reflect this.  
  I'll be more than happy to assist you!

## Conclusion

Auto_Jobs_Applier_Automate Form Filler provides a significant advantage in the modern job market by automating and enhancing the job application process. With features like dynamic resume generation and AI-powered personalization, it offers unparalleled flexibility and efficiency. Whether you're a job seeker aiming to maximize your chances of landing a job, a recruiter looking to streamline application submissions, or a career advisor seeking to offer better services, Auto_Jobs_Applier_Automate Form Filler is an invaluable resource. By leveraging cutting-edge automation and artificial intelligence, this tool not only saves time but also significantly increases the effectiveness and quality of job applications in today's competitive landscape.

## Contributors



Auto_Jobs_Applier_Automate Form Filler is still in beta, and your feedback, suggestions, and contributions are highly valued. Feel free to open issues, suggest enhancements, or submit pull requests to help improve the project. Let's work together to make Auto_Jobs_Applier_Automate Form Filler an even more powerful tool for job seekers worldwide.




## Disclaimer
This tool, Auto_Jobs_Applier_Automate Form Filler, is intended for educational purposes only. The creator assumes no responsibility for any consequences arising from its use. Users are advised to comply with the terms of service of relevant platforms and adhere to all applicable laws, regulations, and ethical guidelines. The use of automated tools for job applications may carry risks, including potential impacts on user accounts. Proceed with caution and at your own discretion.
