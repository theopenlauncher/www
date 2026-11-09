# Open Launcher

Open Launcher is an open-source project building tools that give people more control over the software they use. Our goal is to make practical alternatives to the services offered by large technology platforms: free to use, straightforward to self-host, and developed in the open.

This repository contains the public landing page. It is a small, framework-free static site.

## Preview locally

You can open `index.html` directly in a browser, or serve the repository with any static file server. For example, with Python installed:

```sh
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Self-host

Copy the repository files to any static web host or web server. No build step or application runtime is required. Keep `index.html`, `styles.css`, and the `assets/` directory together. Configure your host to serve `index.html` as the site’s entry page.

The page currently links to the [Open Launcher GitHub organization](https://github.com/theopenlauncher). Update the page when project links or product information become available.

## Contributing

Issues and pull requests are welcome. Before proposing a change, check existing issues so related work can be coordinated. For visual changes, include the viewport sizes you checked and screenshots when useful. Please keep the page accessible, responsive, and usable without a build step.

## Design

See [DESIGN.md](DESIGN.md) for the visual direction, layout rules, and interaction guidance.

## License

This project is licensed under the [MIT License](LICENSE).
