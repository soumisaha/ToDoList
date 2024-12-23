1. Equivalent of npm init in Go
```-> go mod init <module_name>```
go mod init is used to initialize a new module. It creates a go.mod file in the crrent directory.
The go.mod file contains info about the module, its dependencies and the go version
You can provide the github repo link in place of teh module module_name

2. Equivalent of npm run start in Go
```-> go run <file_name.go>```
go run is used to compile and run a Go program
It compiles the program and executes it

3. Equivalent of npm install <package_name> in Go
```-> go get <package_name>```
go get is not a package manager
go get is used to download and install packages from remote repositories
It does not handle versioning
It fetches the package and its dependencies (if any)

4. Equivalent of package.json in Go
```-> go.mod file```
It contains info about the module, its dependencies and Go version

5. Equivalent of npm install in Go
```-> go get tidy```
go mod tidy is used to add missing and remove unused modules
It updates the go.mod file to use the latest version of the dependencies

6. Equivalent of JSON.stringify() in Go
```-> json.Marshal()```
json.Marshal() is used to convert a Go data structure to a JSON string

7. Equivalent of JSON.parse() in Go
```-> json.Unmarshal()```
json.Unmarshal() is used to convert a JSON string to a Go data structure

8. Equivalent of nodemon in Go
```-> go install github.com/cosmtrek/air@latest```
air is live reload tool for Go applications
It watches for file changes and automatically rebuilds and restarts the application
It is similar to nodemon in the Node.js ecosystem
There are other tools like fresh which can also be used for live reloading in Go

9. Equivalent of dotenv in Go
```-> go get github.com/joho/godotenv```
godotenv is a Go package that loads environment variables from a .env file
It is similar to dotenv in the Node.js ecosystem
It allows developers to store sensitive info like API keys, database URIs, etc in a .env file and load them into the application
We can load env variables from a .env file using godotenv.Load(".env")
We can then access the env variables using os.Getenv("MONGODB_URI")

10. Equivalent of Express.js in Go
```-> go get github.com/gofiber/fiber/v2```
Fiber is a web framework for Go that is insprired by Express.js
It is fast, lightweight and easy to use
It provides a similar API to Express.js making it easy for developers familiar with Express.js to transition to Go
Other popular web frameworks in Go include Gin and Echo

11. Equivalent of `Express.js Middleware` in Go
func main(){
    app:= fiber.New() //create an instance
    app.Use(middleware) //mount middlware to func
    app.Get("/", func(c *fiber.Ctx) error{
        return c.SendString("Hello World")
    })
    app.listen(":3000")
}
func middleware(next http.Handler) http.Handler {
    return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
        //middleware logic
        next.ServeHTTP(w, r)
    })
}
We define a middleware function taht takes the next handler as an argument
The middleware function wraps the next handler and executes some logic before calling the next handler

12. Equivalent of Express.js `Route Handling` in Go
func main(){
    app:= fiber.New() //create an instance
    app.Get("/", helloHandler)
    app.listen(":3000")
}
func helloHandler(c *fiber.Ctx) error {
    return c.SendString("Hello World")
}
We define a route handler function helloHandler that sends a response back to the client
We then register the route handler with the app.Get() method specifying the route path and the handler function

13. `Packages collectively form a module`