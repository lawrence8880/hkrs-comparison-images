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
- `GEO_Publication_1-2023.pdf` for GEO Publication No. 1/2023.
- `Geoguide_1_2nd_edition.pdf` for the explicitly named second edition.

Do not upload the same standard under a different filename unless you also update its mapping in the private app's `client/src/data/standardPdfCatalog.json`. Filenames and case must match. Use actual PDF files, not Git LFS pointer files. Do not store PDFs in the application's `client/public` or `src/assets` folders.

The website fetches the PDFs from GitHub at runtime, renders them locally in a popup, and lets users download the original PDF. Uploading an already mapped filename needs no app rebuild. Adding a new mapping requires syncing/publishing the app. Missing PDFs show an explicit upload-needed message rather than a substituted document. GitHub caching can delay new uploads or replacements.

## Edition, privacy and rights

This repository is **public**. Every uploaded PDF is publicly accessible and downloadable. Upload only documents you are authorized to redistribute. Do not upload confidential documents or restricted/copyrighted standards without permission. Adding this folder grants no license to source standards.

Upload the edition actually used by your quotes. Different years, amendment editions, `GB` versus `GB/T` prefixes, and explicitly numbered Geoguide editions are not automatically interchangeable. Generic field names do not establish which edition is intended. Confirm ambiguous names before uploading. No standard PDFs were supplied or uploaded when this folder was created.
