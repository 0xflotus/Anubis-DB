# Anubis-DB

Sister project to [Anubis](https://github.com/jonluca/Anubis)

## About

This server came about due to a lack of free and open APIs for subdomain enumeration. 

## Usage

There is only one endpoing - `https://jonlu.ca/anubis/subdomains/:domain`, where `:domain` is the domain. 

| Method | Endpoint | Parameters | Return | 
| -------- | -------- | -------- | -------- |
| GET | `https://jonluca.me/anubis/subdomains/:domain` | `:domain`: Valid domain (e.g. google.com, reddit.com, etc)| JSON Array of subdomains (`["reddit.com","www.reddit.com","blog.reddit.com"...]`)|
| POST | `https://jonluca.me/anubis/subdomains/:domain` | `subdomains`: Array of submitted subdomains | Status Code (see below) |


A sample AJAX POST request looks like:

```
$.ajax({
    method: 'POST',
    url: "https://jonluca.me/anubis/subdomains/reddit.com",
    type: 'json',
    data: { 
        "subdomains": ["reddit.com","www.reddit.com","blog.reddit.com"]
    }
    success: function(data, textStatus, jqXHR) {
        //Handle data and status code here
    }
});
```
## Contributing

