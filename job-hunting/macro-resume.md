# Using ChatGPT to Compile Your Macro-Resume
By [Kristen Steffen](https://github.com/haxys)

## Introduction

This guide will show you how to use ChatGPT to help you produce a "Macro-Resume," containing an exhaustive, well-formatted record of your education and employment history, including both technical and "soft" skills.

This macro-resume can then be used (with ChatGPT's help) to produce new, specialized resumes, custom-tailored for specific job opportunities.

## Compiling the Raw Data

Gather all your job-hunting data from everywhere you can. It doesn't matter if it's super-organized; just try to get it into one simple text document. Sort your job history chronologically, and try to describe (using regular words) each of your roles, including the tech you used and the kinds of tasks you did, as well as any projects you worked on, and any special achievements you were proud of. Just write this in stream-of-consciousness form; don't worry about making it pretty. Save this as your "raw data" file.

## Constructing the Meta-Objective

Now that you've got your raw data file, open ChatGPT. It's best to use the latest model available; GPT-4 at the time of this writing. GPT-3.5 may suffice, but I haven't tested its efficacy. Use the following prompt to start the conversation:

<pre>
I am producing a "macro-resume" which contains the sum total of my work experience. This resume will serve as the foundation for future, bespoke resumes created for specific applications. As such, this resume will need to include as much detail as possible, even if it may seem irrelevant to my current career field. Here are the loose notes I've taken regarding my work history:

```
[paste your raw data here]
```

Please produce a new objective statement for my macro-resume, suitable for a broad variety of positions.
</pre>

Once you send the prompt, ChatGPT should produce a decent Objective statement. Open a new document (I use Markdown to format mine, but you can create your resume in Word or whatever suits your fancy). My document starts like this (with the relevant details filled in):

<pre>
# [Firstname Lastname]
[Street Address]
[City, State, ZIP]  
[email]  
[phone]
[linkedin]
GitHub: [accounts]

## Objective
A seasoned professional in cybersecurity and software development, with a diverse background encompassing malware analysis, reverse engineering, and technical leadership. Bringing over two decades of experience in information security, coupled with a strong foundation in programming and system analysis. Adept at leading complex security projects, conducting in-depth technical research, and developing innovative solutions. Seeking to leverage my extensive skill set and experience in a challenging and dynamic role that allows for significant contributions to organizational security and technological advancement, while offering opportunities for professional growth and learning.
</pre>

## Adding the Education and Certification Section

This part's pretty simple; just write out long-form your education and certification information (including dates, certification IDs, etc.), then ask ChatGPT to format it as it would appear in a resume. Example:

<pre>
I'm working on my resume, and need to format my education and certification information. Here's the data:

```
[insert your notes here]
```

Please present this information in a simple, standardized format that would be suitable for a resume.
</pre>

Add the output to your macro-resume.

## Formatting Job Experience

With the Objective complete, you can start formatting your job experience. Due to the constraints of the ChatGPT context window, you don't want to make it tackle your full work history all at once; instead go job-by-job, having it construct summaries piecemeal until complete. Start with the following prompt:

<pre>
I'd like to take my previous job history and present it using the following format:

```
### [Company Name], [City, State]
#### [Job Title] (Month Year - Month Year)
- **Summary**: [Concise work summary.]
- **Key Responsibilities**:
  - Responsibility 1
  - Responsibility 2
- **Achievements**:
  - Achievement 1
  - Achievement 2
- **Skills**:
  - Skill 1: [related items]
  - Skill 2: [related items]
#### [Job Title 2] (Month Year - Month Year)
- [...]
### [Company Name 2], [City, State]
[...]
```

Here is an example of properly-formatted data:

```
### Tech Innovations Inc., San Francisco, CA
#### Senior Software Engineer (January 2019 - Present)
- **Summary**: Lead software engineer in a team focused on developing cutting-edge web and mobile applications. Specialized in full-stack development with a focus on scalable, efficient solutions.
- **Key Responsibilities**:
  - Lead the design and implementation of software projects.
  - Mentor junior engineers and conduct code reviews.
- **Achievements**:
  - Successfully led the development of a high-traffic e-commerce platform, resulting in a 40% increase in user engagement.
  - Implemented a new agile workflow process that increased team productivity by 25%.
- **Skills**:
  - Programming Languages: JavaScript, Python, Java
  - Frameworks: React, Node.js, Spring Boot
  - Tools: Docker, Kubernetes, AWS, Git
  - Methodologies: Agile, Scrum, TDD

#### Software Engineer (June 2015 - December 2018)
- **Summary**: Developed and maintained various software applications, focusing on backend development and database management.
- **Key Responsibilities**:
  - Developed backend APIs for web applications.
  - Managed SQL and NoSQL databases.
- **Achievements**:
  - Developed a critical feature that enhanced data processing speed by 30%.
  - Contributed to a team project that won the 'Innovative Tech Award' in 2017.
- **Skills**:
  - Programming Languages: Python, Ruby, SQL
  - Frameworks: Django, Rails
  - Tools: MySQL, PostgreSQL, MongoDB, Git
  - Methodologies: Kanban, Waterfall
```

Please provide the properly-formatted version of the following employment history:

```
[paste two or three positions here]
```
</pre>

ChatGPT should spit out a nicely-formatted version of the two or three positions you list. Copy and paste those into your macro-resume, then continue with the next few positions, using the following prompt (as a continuation of the same chat):

<pre>
Please continue with the following employment history, using the same format as before:

```
[paste two or three positions here]
```
</pre>

Keep repeating this particular prompt template (with subsequent positions) until your entire work history has been covered.

## Compiling Skills

Next, you'll want to assemble a list of all marketable technical and "soft" skills related to the work you did. Start a brand new chat (so there's no accidental data contamination), then use the following prompt:

<pre>
Here is my "macro-resume," which contains the exhaustive record of my employment history:

```
[paste your entire macro-resume thus far, including the objective and employment record, here]
```

Please parse through the entire document, then provide an exhaustive list of all the technical skills and "soft skills" that I possess, as implied by my work history. Be specific, and leave nothing out.
</pre>

GPT will provide you with a nice big list of skills. You may need to add or remove elements from this list, but you might find that it comes up with things you hadn't considered! Add all these skills to your macro-resume.

## Adding Projects

If you wish to include a list of projects and achievements, you can use the following prompt (continuing from the skills prompt, as your entire macro-resume is in the context of that chat already):

<pre>
I need a list of projects on which I've worked, presented in the following format:

```
### [Project Title]
- **Description**: [a concise, yet complete, summary of the project]
- **Technologies Used**: [a list of all related technologies used in the project]
- **Role**: [a description of the role I played in the project's life cycle]
```

Here is an example of properly-formatted data:

```
### Pentesting Dropbox Development
- **Description**: Developed a pentesting dropbox using a Raspberry Pi, incorporating the Nebula networking framework and Kali Linux. This dropbox facilitated secure, outbound connections for pentesters through internal company networks and also hosted its own local WiFi Access Point for nearby pentesters to connect.
- **Technologies Used**: Raspberry Pi, Nebula networking framework, Kali Linux, WiFi technology.
- **Role**: Developer and Presenter. Responsible for the entire project lifecycle, including development, documentation, and presentation at the Dallas Hacker's Association in 2019.
```

Please review the information I've provided thus far regarding my employment history and skillset; from this data, produce an exhaustive list of projects I performed at my various positions, following the aforementioned project format.
</pre>

ChatGPT should spit out a nicely-formatted set of data. Much of this data may be irrelevant, but some might be useful, and you should be able to easily supplement it with additional, similarly-formatted projects.

## Finishing Touches

Finally, I added a bit of additional information:

<pre>
## Additional Information
- **Languages**: English (Fluent)
- **Interests**: [a list of your interests]
</pre>

If you need to genereate a list of interests, try the following prompt:

<pre>
Based on our conversation so far, please produce an exhaustive list of my interests, to the best of your knowledge.
</pre>

That should suffice. You are now the proud owner of your very own Macro-Resume!

**Important Note**: Be sure to review every part of your macro-resume to ensure that the data is accurate. Feel free to revise as you see fit, to ensure optimal data accuracy.

# Custom-Tailoring Your Resume

Now that you've got a Macro-Resume, you can use it as a foundation for building bespoke resumes per-position. For example, you might start with the objective statement, using the following prompt (in a new chat window) and the copy-pasted text of a specific job listing:

<pre>
I've produced the following macro-resume that includes an exhaustive work and education history:

```
[paste your full resume here]
```

Here is a job listing to which I'd like to apply:

```
[paste the full text of the job listing here]
```

Please produce a fresh new Objective statement, based strictly on the information from my resume, designed specifically for the provided job listing.
</pre>

You can probably narrow down the specific work history you'd like to include, but you could also just ask GPT:

<pre>
From the macro-resume I provided, please list the specific positions that I should include in my targeted resume.
</pre>

You can similarly ask GPT to highlight the specific skills you should include:

<pre>
From the macro-resume I provided, please list the specific skills that I should include in my targeted resume.
</pre>

This should get you a solid start on building a bespoke resume for the application. **Caution**: As mentioned before, be sure to review everything in your bespoke resume to ensure that all the data is accurate and relevant. GPT may add skills to your resume that are useful for the job you're seeking, even if you don't actually possess the skills. As with all AI output, it's best to perform a thorough human-review prior to putting the data to use.