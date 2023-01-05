Global-News-Crawler

# Install
!pip install newspaper3k

# Import
import newspaper

# Show URL of popular news websites
newspaper.popular_urls()

# Import Article
from newspaper import Article

# Import fulltext
from newspaper import fulltext

# Get news links 
paper = newspaper.build('https://abcnews.go.com/', language='en')
print(' Link: ')

for i, article in enumerate(paper.articles):
    print(i+1, article.url)

# Get news fulltext
url = 'https://edition.cnn.com/2023/01/04/tech/apple-battery-replacement-cost-increase'
article = Article(url)
article.download()
print(fulltext(article.html))

# License
[MIT](https://choosealicense.com/licenses/mit/)
