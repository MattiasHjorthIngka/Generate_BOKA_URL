# BOKA URL Builder

Enable **Generate store URLs** to list a URL for each store in the selected
market. The list uses the Calendar URL when a service is selected, or the
Service List URL otherwise, with each store's postcode. Stores without a
postcode are listed with a warning instead of a URL.

The app uses Skapa Web Components from IKEA's private npm registry. Configure
the `@ingka` scope and authenticate with the registry before installing:

```sh
npm config set @ingka:registry https://npm.m2.blue.cdtapps.com/
npm login --registry=https://npm.m2.blue.cdtapps.com/ --scope=@ingka
npm ci
npm run dev
```

Run `npm run build` to generate the deployable site in `dist`. GitHub Pages
builds this output in Actions; configure the repository or `github-pages`
environment secret `SKAPA_NPM_TOKEN` with a read token for the private registry.
The Actions runner must also be able to reach that registry.
