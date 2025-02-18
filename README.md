# Root Certificate Authority (CA) - Template

This is a repository template for Root Certificate Authority (CA) that deploys
to Github Pages.

## Usage

The intent of this repository is that it will be used as the deployment target
for [`doubleu-labs/ca-bootstrap`](https://github.com/doubleu-labs/ca-bootstrap).

## Customization

[.github/workflows/pages.yaml](./.github/workflows/pages.yaml) generates a
simple `index.html` from this `README.md`, so be sure to edit this file to
reflect what you want to be displayed for your CA.

If you're using a custom domain and not the default `<USER>.github.io` domain,
be sure to create a `CNAME` file in the root of this repository and uncomment
the `CNAME` copy line in [.github/workflows/pages.yaml](./.github/workflows/pages.yaml).

Uncomment and modify the copy line for DER-encoded certificates (`crt`) and
DER-encoded Certificate Revocation Lists (CRL) (`crl`) to reflect the location
of these files. The existing copy line assumes that these files are in the root
of the repository. If you want these files in a subdirectory, modify the line to
reflect the location if your `crt` and `crl` files.

If you want any other assets to be included in your pages deployment, then add
new copy lines for those files.

## License

This template is licensed under the [MIT No Attribution License](./LICENSE).

Since this is intended to host your the root of trust for your Public Key
Infrastructure, you are free to license your repository in any way you want.
