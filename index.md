
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
      

### Custom footer block
1.	Click 'Structure' > 'Blocks' 
2.	Click configure on the 'Developer portal footer' block

    <img src="/images/9.png" width="700">

3.	Open the wysiwyg (button with html on it) editor and paste in the contents below. 

        <div class="footer_wrapper_div"><div class="upper_grey_block"><div class="table_div_left" style="text-align:    center;">&nbsp;</div></div><div class="lower_grey_block"><div class="centered_link" style="text-align: center;"><a>Terms of use |</a>&nbsp;<a>Terms &amp; Conditions</a>&nbsp; |&nbsp;<a>Privacy Policy</a>&nbsp; |&nbsp;<a>Cookies</a>&nbsp;<a>Accessibility</a>&nbsp; |&nbsp;<a>Sitemap</a></div><div class="list_div_left">&nbsp;</div><div class="list_div_left" style="text-align: center;"><a></a>© IBM 2016. All Rights Reserved</div></div></div>

  <img src="/images/10.png" width="700">

4.	Click Update 
5.	Select 'Full HTML' from the 'Text Format' drop down 

  <img src="/images/11.png" width="700">
  
6.	Save the block from the foot of the page
7.	Close the window and view the changes made to the footer. 




### Adding a Custom block to the home page
1.	Click Structure > Pages
2.	Click 'edit' on the 'page-welcome' page (towards the bottom of the list)
3.	Click 'content'

    <img src="/images/12.png" width="700">
    
4.	Using the cog on 'Middle (conditional)' select 'Add content'
5.	Click Custom Blocks
6.	Click on ‘New Custom Content’ and set:
- Administrative Title: Homepage block 1
- Title: leave blank

7.	Click on the html button and add in the following html to the body                      
                                        
        <div class="light_grey_homepage_block"><div class="left_side_50_div"><div class="fixed_width_block_div"><h3 class="block_heading_2 align_text_center" style="text-align: center;"><span style="color: #444849;">Create a seamless experience with direct access to our services and intergrate them with your business</span></h3><h3 class="block_heading_2 align_text_center" style="text-align: center;"><span style="color: #444849;">Look through our API products to find the right one for your business. There's dedicated documentaion on hand for you to get started.&nbsp;</span></h3><h3 class="block_heading_2 align_text_center" style="text-align: center;"><span style="color: #444849;">If you have any questions about how to get started or need help with your existing intergration, take a look in our support section.</span></h3></div></div></div>
                      
      <img src="/images/13.png" width="700">

8.	Click update on the html source editor

      <img src="/images/14.png" width="700">
      
9.	Click finish. 
10.	Drag the Homepage block 1 that you just created to the top of the middle section (above the features_apis_title block). This will position this new section on the page underneath the welcome banner.

      <img src="/images/15.png" width="700">


11.	Click 'Update and save'
12.	Close the welcome screen admin menu to see the results on the home page of the portal
