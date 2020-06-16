# Progressive web app - 101

This is an intro project for progressive web apps that pass 100% in Google Lighthouse checks

## Make it run

- Clone the repository
- In the terminal install the dependencies with `npm install`
- Run `npm run server-debug`

If you need to generate the certs you can use:

```sh
openssl req -x509 -out localhost.crt -keyout localhost.key \
  -newkey rsa:2048 -nodes -sha256 \
  -subj '/CN=localhost' -extensions EXT -config <( \
   printf "[dn]\nCN=localhost\n[req]\ndistinguished_name = dn\n[EXT]\nsubjectAltName=DNS:localhost\nkeyUsage=digitalSignature\nextendedKeyUsage=serverAuth")
```

To test using Chrome with invalid certs use the following to open the browser:

```
/Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --user-data-dir=/tmp/foo --ignore-certificate-errors --unsafely-treat-insecure-origin-as-secure=https://localhost
```

## Contributing

This is a reference repository for this [article](https://blog.logrocket.com/how-to-build-a-progressive-web-app-pwa-with-node-js/) so I will only look into accept any bug fix or improvement that doesn't vastly change the current content.

On the other hand, you're encouraged to fork and improve it in your own repository, let me know what you come up with ^^.
