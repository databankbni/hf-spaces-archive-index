# HF Spaces Archive — catalogue

A catalogue of Hugging Face Spaces captured by a private backup, published so
the record survives even when the Spaces themselves do not.

**[Open the catalogue](https://databankbni.github.io/hf-spaces-archive-index/)**
— password required.

Hugging Face Spaces disappear. Owners delete them, accounts go quiet, and the
URL starts returning 404 with nothing left behind. This page is the readable
half of a private backup: what existed, who made it, what it was for, how to
use it, the recorded input and output of the test that proved it worked, and
whether it is still up.

## It is locked

The repository is public because GitHub Pages requires it. The contents are
not. The page carries no readable data at all — the catalogue is gzipped and
sealed with AES-256-GCM under a key derived by PBKDF2-HMAC-SHA256 at 600,000
iterations over a random salt. Your browser derives the key and decrypts
locally through Web Crypto; the password is never sent anywhere and is held
only for the tab you opened.

Without the password this page is an inert block of ciphertext. With it, you
get the full catalogue: search, six filters, nine sort orders, per-record
detail, and a full Indonesian/English toggle.

Curation scoring and its reasoning are stripped out before encryption, so they
are not merely hidden here — they are not present.

Needs a browser with Web Crypto and `DecompressionStream`: Chrome 80+,
Firefox 113+, Safari 16.4+. The page says so if yours is too old.

## What is not here

The Space files themselves — source, weights, assets — stay in the private
backup repository and are never served from this page.

## Housekeeping

Rebuilt automatically after every backup run, and on demand. One
self-contained file, no tracking, no analytics, no network requests once it
loads. `robots.txt` and a `noindex` meta tag ask crawlers to stay out; the
encryption is what actually keeps them out.
