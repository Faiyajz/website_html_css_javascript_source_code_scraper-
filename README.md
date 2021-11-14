# website_html_css_javascript_source_code_scraper-

Step 1:
npm install website-scraper

Step 2:
create a js file (e.g. index.js)

Step 3:
write the following codes in that js file.

  const scrape = require('website-scraper');
  const websiteUrl = 'http://your_website_name.com/';

  scrape({
      urls: [websiteUrl],
      urlFilter: function (url) {
          return url.indexOf(websiteUrl) === 0;
      },
      recursive: true,
      maxDepth: 50,
      prettifyUrls: true,
      filenameGenerator: 'bySiteStructure',
      directory: './node-website'
  }).then((data) => {
      console.log("Entire website succesfully downloaded");
  }).catch((err) => {
      console.log("An error ocurred", err);
  });
  
  Step 4:
  node index.js

P.S. This will take several times to download all the files.
