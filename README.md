# Pion demo-conference

This is a fork. The original is here: `https://github.com/pions/demo-conference`

TODO: set a real turn server creds before any real deploy.

demo-conference is an example of fully featured Pion deploy. A working signaler, TURN server and web app.

This is a good template for building your application, fork and start adding features to the frontend or implement
the callbacks in TURN/Signaler to get auth working with your existing application.

### Prerequisites
A working Docker and Docker Compose setup.

### Running
For developing a docker-compose.yml is available with features like hot-reloads so you can quickly start developing.

* Trust all localhost HTTPS certificates --  open [chrome://flags](chrome://flags/#allow-insecure-localhost) in a new tab and enable `#allow-insecure-localhost`
* Generate your SSL certificates, WebRTC only works over HTTPS so we have to serve `www` and `signaler` via HTTPS
```
./create-ssl-cert.sh
```
* Start demo-conference
```
docker-compose up --build
```
* Open up [demo-conference](https://localhost:5000/) After you share your webcam you have joined the conference! Open multiple tabs, chat with yourself...

Now start hacking! Everything is hot-reload, so you can start making changes in the signaler, turn or www folder and your changes will be reflected right away.

## Contributing
See [CONTRIBUTING.md](CONTRIBUTING.md)

## License
MIT License - see [LICENSE.md](LICENSE.md) for full text
