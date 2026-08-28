# HoneyRouter Cookies

Browser extension that syncs cookies and localStorage into [HoneyRouter / OmniRoute](https://github.com/apis-os/ApisOsHoneyRouter).

**MIT** rebrand of [jackluson/sync-your-cookie](https://github.com/jackluson/sync-your-cookie).

> Full source lives in the HoneyRouter monorepo: `extensions/honeyrouter-cookies` on branch `cursor/full-parity-api-ae71` (CI bot cannot push large trees to this empty repo yet).

## DeepSeek Web auto-push

1. Build: `pnpm install && pnpm build`
2. Chrome → Load unpacked → `dist/`
3. Options → HoneyRouter URL `https://omniroute.apisos.dev` + manage-scope admin token
4. Sign in at https://chat.deepseek.com — extension pushes `userToken` to `POST /api/providers/bulk-web-session`

## Limitations

- You must log in in your real browser (Kitesurf/WAF cannot steal sessions).
- Gateway may still stub `deepseek-web` chat until the executor is unstubbed — credential import still works.
