[<img src="https://mholt.github.io/json-to-go/resources/images/json-to-go.png" alt="JSON-to-Go converts JSON to a Go struct"></a>](https://mholt.github.io/json-to-go)

Translates JSON into a Go type definition. [Check it out!](http://mholt.github.io/json-to-go)

This is a sister tool to [curl-to-Go](https://mholt.github.io/curl-to-go), which converts curl commands to Go code.

Things to note:

- The script sometimes has to make some assumptions, so give the output a once-over.
- In an array of objects, it is assumed that the first object is representative of the rest of them.
- The output is indented, but not formatted. Use `go fmt`!

Contributions are welcome! Open a pull request to fix a bug, or open an issue to discuss a new feature or change.


- add cli command

```
./json2go -i './user.json' -n user
```

- output go struct

```
type User struct {
	Login string `json:"login" form:"login" bson:"login"`
	ID int `json:"id" form:"id" bson:"id"`
	AvatarURL string `json:"avatar_url" form:"avatar_url" bson:"avatar_url"`
	GravatarID string `json:"gravatar_id" form:"gravatar_id" bson:"gravatar_id"`
	URL string `json:"url" form:"url" bson:"url"`
	HTMLURL string `json:"html_url" form:"html_url" bson:"html_url"`
	FollowersURL string `json:"followers_url" form:"followers_url" bson:"followers_url"`
	FollowingURL string `json:"following_url" form:"following_url" bson:"following_url"`
	GistsURL string `json:"gists_url" form:"gists_url" bson:"gists_url"`
	StarredURL string `json:"starred_url" form:"starred_url" bson:"starred_url"`
	SubscriptionsURL string `json:"subscriptions_url" form:"subscriptions_url" bson:"subscriptions_url"`
	OrganizationsURL string `json:"organizations_url" form:"organizations_url" bson:"organizations_url"`
	ReposURL string `json:"repos_url" form:"repos_url" bson:"repos_url"`
	EventsURL string `json:"events_url" form:"events_url" bson:"events_url"`
	ReceivedEventsURL string `json:"received_events_url" form:"received_events_url" bson:"received_events_url"`
	Type string `json:"type" form:"type" bson:"type"`
	SiteAdmin bool `json:"site_admin" form:"site_admin" bson:"site_admin"`
}
```


### Credits

JSON-to-Go is brought to you by Matt Holt ([mholt6](https://twitter.com/mholt6)).

The Go Gopher is originally by Renee French. This artwork is an adaptation.
