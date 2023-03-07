# DeniseBarbosadeCastro.github.io
1 - The scrape was carried out to collect the HTML of the main page, as well as the one-level deep pages.
For this, a python code was used where each page was accessed using the selenium package.
Once the pages were accessed via code, the HTML of those pages was read using the page_source function of the webdriver_manager package.
After reading, the HTML of each page was saved in different files.

Obtaining the URL one-level dip:
After accessing the main page of the site, it was possible to verify that each button is associated with a specific URL.
For example the 'Free certificate button' is associated with the URL: 'https://www.classcentral.com/report/free-certificates/'
Such URLs were identified by reading all the 'href' attributes of the 'a' elements of the HTML.
When reading all the URLs identified with the CSS_SELECTOR method associated with the get_attribute method, it was possible to generate a list of URLs associated with all the dynamic buttons of the main page.

2 - The translation process took place between scraping the pages and reading the HTML of each one.
Right after collecting all those URLs one level deep, these were accessed, along with the main page via selenium, with some specifications for browser configuration.
These options allowed access to the URLs via selenium with simultaneous translation into the selected language (Hindi). Setting the options.add_argument ("--lang=hi") and prefs ("translate_whitelists": {"en":"hi"}) options to allow translating the page from English to Hindi.
Once each URL was accessed with the language settings, the subsequent collection of HTML files took place.

All the files were saved in the GitHub repository.
With the site https://raw.githack.com it was possible to obtain a copy of the URL in production for the translated main page, however, it was not possible to affect the same for all the others, making it impossible for the buttons to work dynamically for the translated site.
The repository with all the HTML was released for access by: marizendelrosario@codingallstars.com
