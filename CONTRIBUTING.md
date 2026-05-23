# 🤝 Contributing to T-Work FCM Notify

Thank you for helping improve **T-Work FCM Notify**! 🎉  
This guide explains how to set up the project locally, follow our commit conventions, and submit high-quality pull requests.

---

## 🛠 Development Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/tworksystem/twork-fcm-notify.git
cd twork-fcm-notify
```

### 2️⃣ Configure Firebase Credentials

```bash
cp serviceAccountKey.json.example serviceAccountKey.json
chmod 600 serviceAccountKey.json
# Edit serviceAccountKey.json with your Firebase service account JSON
```

### 3️⃣ Configure Project ID

In `twork-fcm-notify.php`:

```php
define('TWORK_FCM_PROJECT_ID', 'your-firebase-project-id');
```

### 4️⃣ Activate in WordPress

Place the plugin in `wp-content/plugins/`, then activate **T-Work FCM Notify** from the WordPress admin dashboard.

---

## 📝 Commit Message Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/) with a date stamp:

```
<type>: 24052026 - <clear, imperative description>
```

| Type | Use When |
|------|----------|
| `feat` | ✨ New feature or user-facing enhancement |
| `fix` | 🐛 Bug fix |
| `docs` | 📚 Documentation only |
| `style` | 💄 Formatting, whitespace, no logic change |
| `refactor` | ♻️ Code restructure without behavior change |
| `perf` | ⚡ Performance improvement |
| `test` | ✅ Tests added or updated |
| `chore` | 🔧 Tooling, deps, maintenance |
| `ci` | 👷 CI/CD pipeline changes |

### ✅ Good Examples

```
feat: 24052026 - add FCM token registration REST endpoint
fix: 24052026 - preserve camelCase keys in FCM data payload
docs: 24052026 - expand mobile integration section in README
chore: 24052026 - add gitattributes for consistent line endings
```

### ❌ Avoid

```
updated stuff
fix bug
WIP
```

---

## 🔀 Pull Request Process

1. 🍴 Fork [tworksystem/twork-fcm-notify](https://github.com/tworksystem/twork-fcm-notify)
2. 🌿 Create a feature branch: `git checkout -b feat/your-feature-name`
3. ✅ Commit using the convention above
4. 🧪 Test on WordPress 5.0+ and WooCommerce 3.0+
5. 📤 Push and open a Pull Request with:
   - What changed and why
   - Steps to verify
   - Screenshots or log snippets if relevant

---

## 📏 Code Standards

- Follow [WordPress PHP Coding Standards](https://developer.wordpress.org/coding-standards/wordpress-coding-standards/php/)
- Sanitize and validate all REST input
- Never commit `serviceAccountKey.json` or other secrets
- Add `[T-Work FCM]` prefixed `error_log()` messages for operational failures
- Update `README.md` when adding or changing public API behavior
- Preserve camelCase keys in FCM `data` payloads for mobile clients

---

## 🐛 Reporting Issues

Open an issue with:

- WordPress, WooCommerce, and PHP versions
- Steps to reproduce
- Expected vs actual behavior
- Relevant excerpts from `wp-content/debug.log` (redact tokens and secrets)

---

## 📄 License

By contributing, you agree that your contributions will be licensed under the [MIT License](LICENSE).
