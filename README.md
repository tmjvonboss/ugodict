# ugodict
The most complete wrapper in GO with Keep-Alive support for UrbanDictionary

Functions:
- Get random
- List by word
- Get by defid


## Example
```
//Initialize client
client:= ugodict.GetClient()

//Get definitions
result, err := client.DefineByTerm("Eugene")

//Check null
if err == nil {
    
    //Print data
    definition := result[0]
    fmt.Println("ID: " + strconv.Itoa(definition.DefId))
    fmt.Println("Author: " + definition.Author)
    fmt.Println("Word: " + definition.Word)
    fmt.Println("Definition: " + definition.Definition)
    fmt.Println("Example: " + definition.Example)
    fmt.Println("Thumbs up: " + strconv.Itoa(definition.ThumbsUp))
    fmt.Println("Thumbs down: " + strconv.Itoa(definition.ThumbsDown))
    fmt.Println("Permalink: " + definition.PermaLink)
    fmt.Println("Written on: " + definition.WrittenOn)
} else {
    fmt.Println(err)
}
```
