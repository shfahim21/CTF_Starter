Here's a comprehensive guide to advanced Google search techniques, often called "Google Dorks" or "Google Fu":

1. Basic Operators:
```
" "     Exact match (e.g., "exact phrase")
OR      Search for either term (e.g., cats OR dogs)
AND     Search for both terms
-       Exclude term (e.g., security -clothing)
*       Wildcard character
( )     Group terms
```

2. Advanced Operators:
```
site:       Search specific website (site:example.com)
filetype:   Search for specific file types (filetype:pdf)
inurl:      Text appears in URL (inurl:admin)
intitle:    Text appears in title (intitle:login)
intext:     Text appears in body (intext:password)
cache:      Show Google's cached version
related:    Find similar websites
```

3. Common File Types:
```
filetype:pdf
filetype:doc
filetype:xls
filetype:ppt
filetype:txt
filetype:sql
filetype:conf
filetype:log
```

4. Security-Related Examples:
```
# Find login pages
inurl:login OR inurl:signin OR inurl:admin

# Find exposed configuration files
filetype:conf OR filetype:config OR filetype:env

# Find exposed databases
filetype:sql "INSERT INTO" -git

# Find exposed documents
site:target.com filetype:pdf OR filetype:doc OR filetype:xls

# Find subdomains
site:*.target.com -www

# Find exposed directories
intitle:"Index of /" site:target.com
```

5. Information Gathering:
```
# Find email addresses
site:target.com "@target.com"

# Find LinkedIn profiles
site:linkedin.com "at Target Company"

# Find specific error messages
intext:"sql syntax near" OR intext:"syntax error has occurred"

# Find specific technologies
intext:"powered by" site:target.com
```

6. Date-Based Searches:
```
before:2020     Find results before year
after:2020      Find results after year
2019..2021      Find results between years
```

7. Social Media:
```
@username       Find social media mentions
#hashtag        Find hashtag usage
```

8. Practical Combinations:
```
# Find potentially sensitive files
site:target.com filetype:pdf intext:confidential

# Find potential vulnerabilities
site:target.com intext:"error" OR intext:"warning" OR intext:"debug"

# Find exposed admin interfaces
site:target.com inurl:admin OR inurl:login OR inurl:dashboard

# Find specific software versions
site:target.com "running on" OR "powered by" OR "built with"
```

9. Safety Tips:
```
• Always ensure you have permission to search/test
• Don't use these techniques for malicious purposes
• Be aware that some searches might trigger security alerts
• Respect robots.txt and security policies
• Document your findings responsibly
```

10. Additional Resources:
```
• Google Advanced Search page
• Google Search Operators reference
• Exploit-DB Google Hacking Database (GHDB)
• Google Dorks cheat sheets
```

11. Search Refinements:
```
# Price searches
$50..$100       Find items between price range

# Numeric ranges
5000..10000     Find numbers in range

# Site exclusions
site:target.com -site:blog.target.com
```

To be noted:
- Combine operators for more precise results
- Use lowercase for operators (they're case-sensitive)
- Keep searches specific and targeted
