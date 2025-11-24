## Missing/Unwanted Asset References (Node log lines 83–99)

The local dev server reported repeated 404s for the following asset paths. These references currently point to non-existent locations and should be corrected or removed.

| Requested Path | Likely Issue | Suggested Fix |
| --- | --- | --- |
| `/assets/img/all-images/Products/property-img19.png` | Folder name uses `Products` (capital P); actual files live in `public/assets/img/all-images/properties`. | Update every import to `/assets/img/all-images/properties/property-img19.png`. |
| `/assets/img/all-images/Products/property-img20.png` | Same as above. | Update path to lowercase `properties`. |
| `/assets/img/all-images/Products/property-img21.png` | Same as above. | Update path to lowercase `properties`. |
| `/assets/img/all-images/Products/property-img22.png` | Same as above. | Update path to lowercase `properties`. |
| `/assets/img/all-images/Products/property-img23.png` | Same as above. | Update path to lowercase `properties`. |
| `/assets/img/all-images/Products/property-img24.png` | Same as above. | Update path to lowercase `properties`. |
| `/property/Rotomech_horizontal_non_clog_pump_2.webp` | File name does not exist; closest asset is `public/property/Rotomech_non_clog_pumps_2.webp`. | Point the component to the existing filename or add the missing asset. |

Double-checked against the filesystem (`public/assets/img/all-images/properties` and `public/property`). Update the consuming components (e.g., `components/sections/Properties4.tsx` and `data/property.json`) so the server stops requesting these unwanted paths.

