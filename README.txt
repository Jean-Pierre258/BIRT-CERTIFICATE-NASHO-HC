NASHO BIRTH CERTIFICATE SYSTEM

FILES
1. index.html - nurse portal and large A4 certificate
2. admin.html - administrator dashboard
3. Code.gs - Google Apps Script API

SETUP
A. Create a Google Sheet.
B. Open Extensions > Apps Script and paste Code.gs.
C. In Apps Script Project Settings > Script Properties add:
   TOKEN_SECRET = a long random secret
D. Run setup() once from the Apps Script editor.
E. In Nurses sheet add accounts:
   Username | Password | Name | Active
   etienne | CHANGE_PASSWORD | HABIMANA Etienne | TRUE
   japhet | CHANGE_PASSWORD | TUYISHIME Japhet | TRUE
   jamila | CHANGE_PASSWORD | NIRERE Lita Jamila | TRUE
   rebecca | CHANGE_PASSWORD | MUKANDAYAMBAJE Rebecca | TRUE
   patrick | CHANGE_PASSWORD | NJENYERI Patrick | TRUE
   marie | CHANGE_PASSWORD | MUKASINE Marie | TRUE
   assumpta | CHANGE_PASSWORD | UWIRINGIYE Assumpta | TRUE
F. In Admins sheet add:
   Username | Password | Name | Active
   admin | CHANGE_ADMIN_PASSWORD | NASHO Administrator | TRUE
G. Deploy > New deployment > Web app.
   Execute as: Me
   Who has access: Anyone with the link
H. Copy the /exec URL.
I. Put that URL in BOTH index.html and admin.html:
   const API_URL="YOUR_EXEC_URL";
J. Deploy index.html and admin.html to Vercel.

IMPORTANT
- Replace all example passwords before use.
- Do not put real passwords in public GitHub repositories.
- For a real production health-data system, add stronger authentication, access logging, HTTPS-only hosting, backups, and appropriate Rwanda health-data/privacy controls.
- The certificate is deliberately kept unavailable as VERIFIED until the admin supplies Application Number and NIN.
