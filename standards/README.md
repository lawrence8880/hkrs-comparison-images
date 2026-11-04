# Standard PDF uploads

This folder hosts original PDF assets for the HKRS Comparison website. Application source and the independent clause-to-standard inventory remain in the separate private application repository.

## Upload directly in GitHub

1. Open this `standards/` folder on the `main` branch.
2. Select **Add file → Upload files**.
3. Upload the original PDF using its **exact mapped filename** from the application's standard-PDF inventory.
4. Commit the upload to `main`. Wait for the repository's **pages build and deployment** workflow to finish before testing the document.
5. Click the standard name in the comparison matrix or its source-quote heading. Chinese standards open directly in your browser's native PDF reader in a new tab. Use that reader's search, zoom, print and download controls.

Example published URLs:

- https://lawrence8880.github.io/hkrs-comparison-images/standards/GB-50307-2012.pdf
- https://lawrence8880.github.io/hkrs-comparison-images/standards/GB-T-50123-2019.pdf

`Project_Administration_Handbook.pdf` remains the mapped filename for the supplied HK handbook. Official HK documents use their exact source-site URLs; CS1:2010 keeps separate Volume 1 and Volume 2 links.

Do not upload a standard under a different filename unless you also update its mapping in the private app's `client/src/data/standardPdfCatalog.json`. Filenames and case must match. Use actual PDF bytes, not Git LFS pointer files. Do not store PDFs in the application's `client/public` or `src/assets` folders.

## Native PDF delivery

GitHub Pages publishes this media repository from `main` → `/(root)`. `.nojekyll` disables content transformation so original PDF bytes and paths are preserved. The private application is not published by this repository.

The Chinese PDF links use the published `github.io` URLs, not raw GitHub URLs or a custom viewer that must download the entire PDF first. Already-mapped new uploads need no application rebuild, but require the Pages deployment to finish. New names or filenames require an app mapping update. Missing documents return a file-not-found response; no alternative edition is substituted.

Native viewing depends on your browser and PDF settings. If your browser is configured to download PDFs, it may download rather than display them. Large scanned files and slow connections can still delay viewing. Pages/browser caches can delay replacements; use a new mapped filename when an immediate revision must be distinguished.

The HK documents whose official URLs were supplied are linked directly to their source sites, not duplicated in this library. Uploading a GitHub filename does not override an explicitly configured official URL unless its mapping is changed.

## Edition, privacy and rights

This repository and its Pages site are **public**. Every uploaded PDF is publicly accessible and downloadable. Upload only documents you are authorized to redistribute. Do not upload confidential or restricted material. Adding this folder grants no license to source standards.

Upload the edition actually used by the quotes. Different years, amendment editions, `GB` versus `GB/T` prefixes and explicitly numbered Geoguide editions are not automatically interchangeable. Generic field names do not establish an edition. Forty unique supplied PDFs were added on 4 November 2026; a repeated GB-50007-2011 attachment was stored once. All uploaded PDFs retain their original bytes.
