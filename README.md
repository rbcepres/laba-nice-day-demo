# Laba Nice Day — Public Demo

Browser-only public demo of the Laba Nice Day laundry operations system.

## Important demo limitations

- Data is stored only in each tester's browser/device using local browser storage.
- There is no centralized or synchronized database.
- The GCash flow is simulated. The displayed demo QR is **not for payment**.
- Demo passcode: `1234`.
- Do not enter real customer or payment information into the public demo.

## Publish with GitHub Pages

1. Put these files in the root of the repository's `main` branch.
2. Open **Settings > Pages** in GitHub.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch **main** and folder **/(root)**, then Save.
5. GitHub will display the public HTTPS Pages URL after deployment completes.

## iPhone / Android app-like installation

Once the Pages URL is live:

- iPhone/iPad: open the URL in Safari, tap **Share > Add to Home Screen**.
- Android: open the URL in Chrome and choose **Install app** or **Add to Home screen** when available.

The included service worker caches the app shell after the first successful load so the demo can reopen offline. Browser data remains device-local.

## Updating the demo

Replace the files in the repository and push/commit the changes. Testers can refresh the same Pages URL. Preserve the `lndPublicDemo` storage key and migrate its schema when future releases change stored data.
