
# Lab 1: Customising the API Connect Developer Portal

The developer portal section of this lab is split into 3 parts, which must be followed in order since each part builds upon the previous part. From a high level, the 3 parts are:
  1.	Set up API Connect (lab 0 in the PoT)
  2.	Perform the basic developer portal customisation lab (lab 7.1 in PoT) 
  3.	Perform the advanced developer portal customisation lab (new lab and the steps are described in this document) 

## Part 1: Set up API Connect

This section can be skipped if you already have a Bluemix account and an API Connect service provisioned. If not, please follow the link below and complete ‘Lab 0 - Setup IBM API Connect’. Once complete, return to this document and move onto part 2. 

[Setup IBM API Connect Instructions](https://ibm-apiconnect.github.io/pot/lab0.html) 


## Part 2: Basic Developer Portal Customisation

This section can be skipped if you have already completed lab 7.1 of the PoT. Otherwise, please follow the link below and complete section 7.1 (Customise the Developer Portal) of the PoT. Do not move into section 7.2, return to this page and move onto part 3 below once lab 7.1 is complete. 

[Customise the Developer Portal] (https://ibm-apiconnect.github.io/pot/lab7.html#customize-the-developer-portal)


## Part 3: Advanced Developer Portal Customisation

### Adding the slogan
1.	Click Configuration > System > Site Information 
2.	In the 'Slogan' field enter: 'Welcome to the API Portal'

      <img src="/images/1.png" width="450">

3.	Save the configuration 

      <img src="/images/2.png" width="450">
 
4.	Close the current window

      <img src="/images/3.png" width="700">
 
5.	Click Appearance > Settings 
6.	Navigate to the thinkibm_connect theme settings
 
      <img src="/images/4.png" width="700">
 
7.	Expand the Toggle display section and check the box for 'Site Slogan' 

      <img src="/images/5.png" width="450">
 
8.	Save the configuration 
9.	You will notice that you will not be able to see any changes. This is because the color scheme of the slogan is set to white text on the white background. 




### Colour schemes and custom CSS
Here we are going to add custom CSS to our theme. For this we are going to use the ‘Custom CSS’ extension in the developer portal. Note the ‘Custom CSS’ extension is designed to make small CSS changes in the case of emergencies in production. However, the ‘Custom CSS’ extension is also useful to quickly make CSS changes at development time when you are building the look and feel of a developer portal. It saves the need to re-upload the theme every time a new CSS change is made throughout development. Once you are happy with the CSS and it is stable, it should be moved from the ‘Custom CSS’ extension and placed inside the overrides.css file inside the theme itself. 

1.	To activate the ‘Custom CSS’ extension go to Appearance > Setting > thinkibm_connect > Extensions > Check box ‘Custom CSS’.

      <img src="/images/6.png" width="700">
      
2.	Save the changes by clicking ‘Save Configuration’ at the bottom of the page. 
3.	Now if you go to Appearance > Setting > thinkibm_connect then scroll down to the menu at the bottom (extensions), there will be a new menu tab called ‘Custom CSS’. In here, any custom CSS declarations can be set. 
4.	Inside the custom CSS editor area, copy the flowing 2 CSS declarations:
             
             /*  CSS for changing the site slogan: */
                h2#site-slogan {
                  padding-top: 1.9em;
                  font-size: 2em !important;
                  color: #444849;

                }
                /* CSS for changing the logo padding: */
                img.site-logo {
                  height: 95px;
                  padding-top: 14px;
                }

      <img src="/images/7.png" width="700">

5.	Now scroll to the bottom of the page and hit ‘Save Configuration’. 
6.	Scroll to the top and hit the X to close the Appearance menu and view the changes you have made. 

      <img src="/images/8.png" width="700">
      

## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/garyk295/madridapiclab1/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/garyk295/madridapiclab1/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
