# 이중슬릿 무늬간격 계산기

원거리 작은 각도 이중슬릿 간섭무늬 간격 계산

- Plan ID: E089
- App: https://nanalab.kr/eng-double-slit-spacing/
- Repository: https://github.com/NaNaCompany/eng-double-slit-spacing
- Formula: `Δy ≈ λL/d`
- Output: 인접 밝은 무늬 간격 Δy

## Model

λ,L,d>0. 단색·결맞음 빛과 d≫λ, L≫d의 작은 각도 원거리 모델이다. 슬릿 폭 포락선·회절 세기·근접장 패턴은 제외한다.

Inputs are normalized to SI. Only one scalar is returned. Model conditions, finite numbers, physical boundaries, overflow and underflow are checked. External solver APIs and property databases are not used.

## Verification

Run `node --test tests/*.test.mjs` with Node.js 22 or later. Independent 70-digit Decimal example result: `0.005`. Source and license notices are in [SOURCES.md](SOURCES.md) and [LICENSE](LICENSE).

## Hosting

GitHub Pages uses `main` and `/`, with the NaNaCompany domain inherited. Google GTM, GA4, AdSense, Cloudflare analytics and the gray More Apps link are included. All code, descriptions and graphics are original.

## Static languages

Korean (existing root), English (`en/`), Spanish (`es/`), Simplified Chinese (`zh/`), Japanese (`ja/`) and German (`de/`). Each page has its own canonical URL, reciprocal hreflang, localized metadata, interface, validation messages and preview image. The language links work without JavaScript. Calculation code is shared and no runtime translation API is used.

Edit `localization/*.json` for text, `src/template.html` for the shared page, and run `python scripts/build-locales.py`. Run `python scripts/build-locales.py --check` and `npm test` before publishing. Decimal commas are accepted in Spanish and German; thousands separators are not supported.
