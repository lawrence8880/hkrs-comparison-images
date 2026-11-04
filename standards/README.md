# Standard PDF uploads

This folder hosts PDF assets for the HKRS Comparison website. The application source and the private clause-to-standard inventory remain in the separate application repository.

## Upload directly in GitHub

1. Open this `standards/` folder on the `main` branch.
2. Select **Add file → Upload files**.
3. Upload your original PDF using the **exact mapped filename** shown in the website's PDF popup or in the private application's standard-PDF inventory.
4. Commit the upload to `main`. Click the standard name on the webpage and use **Retry** if a missing-file response was cached.

Examples of configured filenames:

- `GB-50307-2012.pdf` for GB 50307-2012.
- `GB-T-50123-2019.pdf` for GB/T 50123-2019.
- `Project_Administration_Handbook.pdf` for the supplied handbook.

Do not upload the same standard under a different filename unless you also update its mapping in the private app's `client/src/data/standardPdfCatalog.json`. Filenames and case must match. Use actual PDF files, not Git LFS pointer files. Do not store PDFs in the application's `client/public` or `src/assets` folders.

The website fetches GitHub-backed PDFs at runtime, renders them locally in a popup, and lets users download the original PDF. Uploading an already mapped filename needs no app rebuild. Adding a new mapping requires syncing/publishing the app. Missing PDFs show an explicit upload-needed message rather than a substituted document. GitHub caching can delay new uploads or replacements.

The HK documents whose official URLs were supplied are linked directly to their source sites, not duplicated in this library. Official sites currently prohibit in-page fetching/embedding, so the website offers a direct browser PDF-window option. CS1:2010 has separate Volume 1 and Volume 2 links beside its standard name. Uploading a GitHub filename does not override an explicitly configured official source URL unless its mapping is changed.

## Edition, privacy and rights

This repository is **public**. Every uploaded PDF is publicly accessible and downloadable. Upload only documents you are authorized to redistribute. Do not upload confidential documents or restricted/copyrighted standards without permission. Adding this folder grants no license to source standards.

Upload the edition actually used by your quotes. Different years, amendment editions, `GB` versus `GB/T` prefixes, and explicitly numbered Geoguide editions are not automatically interchangeable. Generic field names do not establish which edition is intended. Confirm ambiguous names before uploading. Forty unique supplied PDFs were added on 4 November 2026; a repeated GB-50007-2011 attachment was stored only once. All uploaded files retain their original bytes.
