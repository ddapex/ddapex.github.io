# site — страницы для кабинета TikTok for Developers

Поля `Terms of Service URL`, `Privacy Policy URL` и `Web/Desktop URL` требуют
подтверждённого домена. Бесплатный вариант — GitHub Pages на личном корне
`https://<username>.github.io/`.

## Что сделать

1. Создай репозиторий с именем **`<твой-username>.github.io`** — именно так, тогда
   корень сайта будет `https://<username>.github.io/`, а не `/repo/`.
2. Скопируй `index.html`, `terms.html`, `privacy.html` в корень репозитория.
3. Замени `REPLACE_WITH_YOUR_EMAIL` на свою почту во всех трёх файлах.
4. В кабинете TikTok открой **URL properties → Verify** (или ссылку
   `Verify URL properties` под полем) и скопируй мета-тег вида
   `<meta name="tiktok-developers-site-verification" content="...">`.
5. Вставь его в `index.html` вместо строки с `PASTE_TIKTOK_CODE_HERE`, закоммить.
6. Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, папка `/ (root)` → Save.
7. Через минуту открой `https://<username>.github.io/` — страница должна открыться.
   Вернись в TikTok и нажми **Verify**.

## Что вписать в форму

| Поле | Значение |
|---|---|
| Web/Desktop URL | `https://<username>.github.io/` |
| Terms of Service URL | `https://<username>.github.io/terms.html` |
| Privacy Policy URL | `https://<username>.github.io/privacy.html` |

Redirect URI остаётся локальным и в эти поля не попадает:
вкладка **Desktop** → `http://127.0.0.1:8765/callback/`.

## Если подтверждение требует файл, а не мета-тег

TikTok иногда даёт `tiktok<ID>.txt`. Положи этот файл в корень репозитория рядом
с `index.html` — он станет доступен по адресу
`https://<username>.github.io/tiktok<ID>.txt`.
