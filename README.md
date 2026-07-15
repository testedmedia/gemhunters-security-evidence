# GemHunters.co Security Evidence

This repository preserves the public-safe evidence submitted in support of the false-positive correction request for PhishDestroy report `5E9D7443` and issue `phishdestroy/destroylist#332`.

The evidence challenges the active malicious-domain verdict because the report does not disclose a reproducible phishing URL or payload, while broad independent and browser-backed rescans did not reproduce phishing. It does not claim that every possible URL can be proven clean.

## Files

| File | SHA-256 |
| --- | --- |
| `gemhunters-evidence-manifest-20260714.txt` | `78a005d396f14b70cc4956314c801bdf007ebbaedff73371901add9a99a0f138` |
| `gemhunters-clean-browser-cdp-20260714.png` | `97e6d028efdb6953d05f819866d7b5b3fd513c70eb56123c3c186928adcd616f` |
| `gemhunters-public-evidence-20260714.zip` | `c3aef84a1356d7ac76e3afda0bc74e08ab29d118d31eaf64e9685dc9f8896ced` |
| `gemhunters-browser-trace-public-20260714.zip` | `8c35026758d55963c0e3f185517ae8433eb49a228e348cac7927465c2ae13a78` |
| `gemhunters-phishdestroy-api-20260714.json` | `a7b5c8f0ade92f8111de0f1d89cecf0737e6cf1ddb574fcc4ce8d250ad5e4755` |
| `gemhunters-norton-url-blacklist-20260714.png` | `ff23b8fe133598e81cb7f66ed4b566ac528d480c40e1771b9088d0a2a08c6bcc` |
| `gemhunters-gridinsoft-report-20260714.png` | `ebabcae4ebab58878f3d4d897aaeee00d3a07678cddc711e6e2533fb99eede49` |
| `gemhunters-gridinsoft-http-matrix-20260714.txt` | `d8d83500875b6ab1edcd00fd2ea5b58239cea0062b0d5acfb1cc211914aba106` |
| `gemhunters-domain-ownership-proof-20260714.txt` | `c4575b55c5f46676b7ebcd300e983cbe2d4dc800044250a280549dd61805df82` |
| `gemhunters-google-safe-browsing-20260714.png` | `6379652b512d98322dc4471848a4f8698038aec0bb2b6e183c6884eceb3d213e` |
| `gemhunters-virustotal-domain-20260714.png` | `05f169fa45a80cc21f878bb071e6b769e55419190ea05a0a87f627a0a3ef5915` |
| `gemhunters-http-forensic-matrix-20260714.txt` | `bc064731b8c040e7ab0c3499539b6c65a4df647e6122639ac84db137211cf9627` |
| `gemhunters-globalping-ipv6-evidence-20260714.json` | `30c40dc7aef3076236f677bb5065bda02907369ad4d135405d05031387e6f487` |
| `gemhunters-globalping-four-entry-ipv6-20260714.json` | `2b51901ae41f9c08e6a3b04ba521af7cda69033d3f7a52ba6d9ebafde28bf35b` |
| `gemhunters-globalping-four-entry-ipv4-20260714.json` | `cd4aadd8a99c1242308453e12f0c0cff61af222a84eda12dfa0ad246d11ac3ed` |

The manifest maps each claim to its supporting artifact, method, tool version, and limitation. The browser trace archive has sanitized authentication, cookie, and API-key header values.

The Norton screenshot documents the current user-facing impact: Norton Safe Web blocks `https://www.gemhunters.co/` as `URL:Blacklist`.

The Gridinsoft screenshot preserves its July 14, 2026 `Suspicious Website` report, including the 31/100 score and single provider warning. The adjacent HTTP matrix gives Gridinsoft a compact, reproducible four-entry-URL rescan result.

The DNS proof file records the live TXT value published at `_reputation-verification.gemhunters.co` for domain-control verification during the reputation appeals.

The Google Safe Browsing and VirusTotal screenshots preserve the July 14 clean reputation observations used in the vendor appeals. The VirusTotal view displayed zero detections across 91 vendors and a last-analysis age of three days. The Google view displayed `No unsafe content found` and a July 14, 2026 update date.

The full IPv4 forensic matrix and raw Globalping IPv6 results are also exposed as direct files so reputation reviewers can inspect them without downloading the evidence archives.

The four-entry IPv6 report adds protocol and host parity across `http` and `https` for both the apex and `www` hosts. Five probes each in the United States, United Kingdom, Germany, Australia, and Brazil reproduced the expected redirect chain and final HTTP 200 apex response without a challenge marker.

The matching four-entry IPv4 report repeats the same protocol, host, and five-country matrix over IPv4. All 20 probes reproduced the expected redirect chains and final HTTP 200 apex response without a challenge marker.

## Independent references

- Globalping IPv6 measurement: https://globalping.io/?measurement=2C1z1cHuorY4Wf2db00020lJL
- Internet.nl apex test: https://internet.nl/site/gemhunters.co/4184325/
- Internet.nl www test: https://internet.nl/site/www.gemhunters.co/4184367/
- PhishDestroy dispute: https://github.com/phishdestroy/destroylist/issues/332

Security questions and private evidence requests can be sent to `support@gemhunters.co`.
