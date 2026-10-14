# Go Mobile Inc. — corporate website

A static, responsive, single-page corporate website for **Go Mobile Inc.** at **gomobilehq.com**.
No build step, paid hosting, analytics scripts, user tracking, database, or third-party resources.

## Publishing on GitHub Pages

1. Create a **public** GitHub repository, e.g. `gomobile-website`.
2. Upload the **four files** (`index.html`, `favicon.svg`, `CNAME`, `README.md`) into the **repository root**. Do not upload the containing directory as a folder.
3. Go to **Settings → Pages**. Set **Source: Deploy from a branch**, **Branch: main**, **Folder: / (root)** and click **Save**.
4. On the same **Settings → Pages** screen, check **Custom domain** is `gomobilehq.com` and save it if prompted. The checked-in `CNAME` file has this value already.
5. **After** configuring the domain in GitHub, open **Namecheap → Domain List → Manage → Advanced DNS → Host Records**.
    - Remove the *parking* CNAME for `www` (`parkingpage.namecheap.com`) and the URL redirect for `@` (`http://www.gomobilehq.com/`), if present.
    - Add four **A records**, all with host `@`:
      `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
    - Add a **CNAME** for host `www` pointing to **YOUR-GITHUB-USERNAME.github.io** (substitute the repository owner's exact username; do not append repository name).
    - Leave **MX**, **SPF**, **DKIM**, **Google verification TXT**, and all **Mail Settings / Custom MX** settings untouched. They control corporate email and are unrelated to the website.
    - Reconfirm DNS values against current GitHub documentation when making changes: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
6. Wait for DNS propagation. GitHub **Settings → Pages** should show successful DNS checks. Enable **Enforce HTTPS** once available. DNS and certificate issuance may take some time.
7. Open `https://gomobilehq.com` and `https://www.gomobilehq.com` on desktop and mobile; check that one redirects as expected. Test the email link, **and independently confirm that `arif@gomobilehq.com` can receive external messages**.

## Notes

- Site is a public information page; it does not offer online checkout, process payments, or deliver SaaS on GitHub Pages. Consult GitHub's usage policy before adding commercial functionality: https://docs.github.com/en/pages/getting-started-with-github-pages/github-pages-limits
- All copy is in `index.html`. It intentionally makes no claims about released apps, existing clients, employee headcount, or awards.
- Apple Developer enrollment requires a publicly available **functional website** associated with the organization. This template is a starting point; Apple's approval is not guaranteed: https://developer.apple.com/help/account/membership/program-enrollment/
- The legal entity name used is **Go Mobile Inc.**, matching the company paperwork supplied for this project.
