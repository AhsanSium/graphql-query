# graphql-query

Question: Write a query to
1. Display all the books of authors who live in a specific country (e.g. all books of all authors living in Bangladesh)
2. Total number of books published by an author (e.g. total number of books sold by J. K. Rowling)
NOTE: you need to use variables instead of values in the query. Example values like Bangladesh and J. K Rowling is used as an example to help you understand.


## Answer:

 1. 
 		query GetBookOfAuthor($country : country)

		Author(country: $country){
			Book{
				book_title
			}
		}
    
 2. 
		query GetTotalNumberOfBooks($name:author_name)

		Author(author_name : $name){
				Book{
					summaries{
						count	
					}
				}
		}
