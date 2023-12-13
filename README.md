# book_management_system

commands to send or add book!
Invoke-WebRequest -Uri "http://localhost:8080/books" -Method Post -Headers @{"Content-Type"="application/json"} -Body '{"title": "The Great Gatsby", "author": "F. Scott Fitzgerald"}'  

command to show books present!
Invoke-RestMethod -Uri "http://localhost:8080/books" -Method Get

command to delete books with specific id no!
Invoke-RestMethod -Uri "http://localhost:8080/books/10" -Method Delete                                        


command to update the book title or author information!
$headers = @{"Content-Type"="application/json"}; $body = @{ "title" = "New Title"; "author" = "New Author" } | ConvertTo-Json; Invoke-WebRequest -Uri "http://localhost:8080/books/9" -Method Put -Headers $headers -Body $body
