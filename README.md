# Golang_standard_api_test

Golang_standard_api_test

install the external dependencies

 negroni and gorilla
 
running the build command the compilation process will install the dependencies:

[run]

go build

show in screen :

go: finding module for package github.com/gorilla/context

go: finding module for package github.com/codegangsta/negroni

go: finding module for package github.com/gorilla/mux

go: downloading github.com/codegangsta/negroni v1.0.0

go: downloading github.com/gorilla/context v1.1.1

go: downloading github.com/gorilla/mux v1.8.0

go: found github.com/codegangsta/negroni in github.com/codegangsta/negroni v1.0.0

go: found github.com/gorilla/context in github.com/gorilla/context v1.1.1

go: found github.com/gorilla/mux in github.com/gorilla/mux v1.8.0

[run]

go run main.go

  localhost:8081
  
  
-> main.go

func main() {}

func bookmarkIndex() http.Handler {}

func bookmarkFind() http.Handler {}

-> main_test.go

func Test_bookmarkIndex(t *testing.T) {}

func Test_bookmarkFind(t *testing.T) {}


> main_test.go
Running the tests, we see that everything is passing successfully:


[run]

go test -v
  
show in screen :

=== RUN   Test_bookmarkIndex

--- PASS: Test_bookmarkIndex (0.01s)

=== RUN   Test_bookmarkFind

=== RUN   Test_bookmarkFind/not_found

=== RUN   Test_bookmarkFind/found

--- PASS: Test_bookmarkFind (0.00s)

  --- PASS: Test_bookmarkFind/not_found (0.00s)

  --- PASS: Test_bookmarkFind/found (0.00s)

PASS

ok      github.com/eminetto/post-apitest        0.693s
  
  
[browser]

http://localhost:8081/v1/bookmark/1

http://localhost:8081/v1/bookmark/2

http://localhost:8081/v1/bookmark
  
  
CONLUSION :

 test our API using only the standard library
 
 But the tests code aren’t so readable, 
 
 especially when we are testing a large API, with several endpoints.


=> Only ID:2
      
      data := []*Bookmark{
         
         {
            
            ID:   2,
         
            Link: "https://apitest.dev",
      
         },
      
      }
      
