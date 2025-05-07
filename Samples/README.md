
# 📄 Kapodistrian Scientific Document Signing System

This repository provides tools and guidance for validating the authenticity of scientific documents officially signed by the **Kapodistrian Academy of Science (KAS)**.

All official `.pdf` documents bearing the `SIGNED_KAS` stamp are:
- Authored by verified researchers
- Integrity-protected using SHA-256 cryptographic fingerprints
- Signed with the Academy’s private key
- Accompanied by `.sha256` and `.sig` companion files

---

## 📝 Submit Your Paper for Signing

Use the secure submission form to request a digital signature from the Kapodistrian Academy:

[![📝 Submit Your Paper](https://img.shields.io/badge/%F0%9F%93%9D%20Submit%20Your%20Paper-KAS%20Secure%20Form-2AA198?style=for-the-badge&logo=googleforms&logoColor=white)](https://forms.gle/oLhKr2KA17NPhSvr9)

KAS will:
- Stamp your PDF with institutional footer + SHA256
- Generate and sign the official `.sha256` hash
- Return a certified bundle: `.pdf`, `.sha256`, `.sig`

---

## 🔍 Verify Official Document Authenticity

Use the included notebook to:
- Upload your `.pdf`, `.sha256`, `.sig`, and `public_key.pem`
- Recalculate PDF hash and confirm signature
- Authenticate the signature using OpenSSL or Python (Module Availability TBA)

👉 Launch in Colab:

[![Launch Verifier in Colab](https://colab.research.google.com/assets/colab-badge.svg)]((https://colab.research.google.com/github/Galactic-Code-Developers/kas-verifier-page/blob/main/KAS_Verifier_OpenSSL.ipynb) OpenSSL Version

---

## 📄 File Naming Convention

```
[AuthorLastName]_[ShortTitle]_v[Version]_SIGNED_KAS_[YYYY-MM-DD].pdf
```

Includes:
- `.sha256` — cryptographic hash
- `.sig` — digital signature
- `.meta.txt` — optional metadata
- `public_key.pem` — shared by KAS for verification

---

## 🛡 Verification Trust Policy

- Only KAS is authorized to issue `.sig` files
- All `.sig` must verify using the official `public_key.pem`
- Any mismatch in `.sha256` or `.sig` invalidates the document

---

## ⚠️ Disclaimer & Terms of Use

The Kapodistrian Academy of Science provides this system to enhance trust in academic authorship.

By using this system, you agree:
- Submissions are final and reviewed
- Metadata (author, ORCID, institution) must be truthful
- Verified documents may be publicly cited, archived, or published

🔐 Contact for audit or compliance: `security@kapodistrian.edu.gr`

---

## License

This repo is provided under the MIT License. Document verification policy is governed by the Kapodistrian Academy of Science.
