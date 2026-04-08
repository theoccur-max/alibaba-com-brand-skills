# Alibaba.com Brand Assets Usage Rules (All Libraries)

## Audience routing rules

### When the user specifies an audience
- **CGS / 中国供应商 / 卖家** → read `cgs_brand_assets.md` only
- **GGS / 全球供应商 / global supplier** → read `ggs_brand_assets.md` only
- **Buyer / 全球买家 / 买家** → read `buyer_brand_assets.md` only
- **Main brand / 主品牌 / cross-market** → read `main_brand_assets.md` only
- **Accio** → read `buyer_brand_assets.md` (Accio libraries are housed under the Buyer scope)

### When the audience is ambiguous
- Read all four reference files
- Return confirmed matches per audience with clear labels (e.g. **CGS：** / **GGS：** / **Buyer：**)
- Omit audiences that have no confirmed matching asset — do not return empty or speculative results

## Asset type routing

| Asset type | Primary audience(s) | Reference file(s) |
| --- | --- | --- |
| Alibaba.com main logo | Main / CGS / GGS / Buyer | All four — check each |
| Brand guideline / brandbook | Main / CGS / GGS / Buyer | All four — check each |
| PPT template | Main / CGS / GGS / Buyer | All four — check each |
| Official social media icon | Main / CGS | main_brand_assets.md, cgs_brand_assets.md |
| Brand video | CGS / GGS / Buyer | cgs_brand_assets.md, ggs_brand_assets.md, buyer_brand_assets.md |
| Buyer story / seller story | Buyer / GGS | buyer_brand_assets.md, ggs_brand_assets.md |
| Product introduction | CGS / GGS / Buyer | cgs_brand_assets.md, ggs_brand_assets.md, buyer_brand_assets.md |
| Whitepaper / report | GGS / Buyer | ggs_brand_assets.md, buyer_brand_assets.md |
| Webinar | GGS / Buyer | ggs_brand_assets.md, buyer_brand_assets.md |
| Exhibition / event | CGS / Buyer | cgs_brand_assets.md, buyer_brand_assets.md |
| GTM / campaign | CGS | cgs_brand_assets.md |
| Accio brand (all) | Buyer | buyer_brand_assets.md |
| Product Content Hub | Buyer | buyer_brand_assets.md |

## Link handling rule

Default to the most specific confirmed browseable link in this order:
1. Folder link (directoryFile parameter)
2. Category link (categoryId parameter)
3. Root library link
4. Direct file link — only when the user explicitly asks for a direct file, or when no browseable link is confirmed

Never invent a direct asset link not present in the reference files.

## General constraints

- Current library contents are treated as latest and externally usable unless a reference notes otherwise.
- Do not recommend assets from outside the confirmed libraries.
- If the user asks for something not yet indexed, return the closest confirmed category or root link and explain how to navigate from there.
