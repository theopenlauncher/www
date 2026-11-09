# open-launcher

open-launcher is an open-source project building tools that give people more control over the software they use. Our goal is to make practical alternatives to the services offered by large technology platforms: free to use, straightforward to self-host, and developed in the open.

This repository contains the public landing page, pricing page, product overview, and custom 404 page. The site files are in `public/` and use plain HTML and CSS.

## Preview locally

Serve the public directory with any static file server. For example, with Python installed:

```sh
python3 -m http.server 8000 --directory public
```

Then visit <http://localhost:8000>.

## Self-host

Publish the contents of `public/` to any static web host or web server. No build step or application runtime is required. Keep the HTML pages, `styles.css`, and `assets/` directory together. Configure `index.html` as the entry page and `404.html` as the custom not-found page.

The site links to the [open-launcher GitHub organization](https://github.com/theopenlauncher). Hosted plans are planned, but pricing details are coming soon. Applications are presented as upcoming until they have public releases.

## Contributing

Issues and pull requests are welcome. Before proposing a change, check existing issues so related work can be coordinated. For visual changes, include the viewport sizes you checked and screenshots when useful. Please keep the page accessible, responsive, and usable without a build step.

## Design

See [DESIGN.md](DESIGN.md) for the visual direction, layout rules, and interaction guidance.

See [DOCUMENTATION.md](DOCUMENTATION.md) for the site map, architecture, current product and pricing status, and deployment guidance.

## License

This project is licensed under the [MIT License](LICENSE).
