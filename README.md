# Basic Question
[View](./basic_solution.md)

---

# Database Question
[View](./database_solution.md)

---

# JavaScript Question
[View](./javascript_solution.md)

---

# Website Security Best Practises
1. Least Privilege
    - Grant only the minimum permissions users, apps, and services need.
    - Use role-based access control (RBAC) and fine-grained permissions.

2. Strong Authentication
    - Enforce strong, unique passwords (12+ characters, mix of types).
    - Require Multi-Factor Authentication (MFA/2FA) everywhere possible.

3. Secure Software & Dependency Management
    - Keep all OS, libraries, and frameworks up to date.
    - Pin versions and use dependency scanning tools (Snyk, Dependabot).
    - Remove unused software and dependencies.

4. Encryption Everywhere
    - Encrypt data in transit (TLS/HTTPS).
    - Encrypt data at rest (disk/database encryption).
    - Never store passwords in plaintext — use strong hashing (bcrypt, Argon2).

5. Regular Patching
    - Automate updates for critical systems.
    - Patch third-party libraries and dependencies quickly.
    - Maintain an asset inventory so you know what to patch.

6. Firewall & Network Segmentation
    - Use default-deny firewall rules.
    - Isolate sensitive systems (e.g., production DBs) from the internet.
    - Use VPNs or bastion hosts for access.

---

# Website Performance Best Practises
1. Optimize Page Load Time
    - Minimize initial HTML, CSS, and JS payload.
    - Inline critical CSS and defer non-critical CSS.
    - Minify and compress assets (HTML, CSS, JS).

2. Reduce JavaScript Bloat
    - Remove unused libraries and polyfills.
    - Split code (tree-shaking, code-splitting, lazy loading).
    - Defer or async non-essential scripts.
    - Avoid blocking the main thread with heavy JS.

3. Image Optimization
    - Use modern formats (WebP, AVIF) instead of JPG/PNG when possible.
    - Serve responsive images (srcset, sizes).
    - Use lazy loading (loading="lazy").
    - Compress without noticeable quality loss (e.g., ImageOptim, Squoosh).

4. Caching & CDN
    - Use a CDN to deliver static assets from edge locations.
    - Set far-future cache headers (Cache-Control, ETag).
    - Implement Service Workers for offline caching (PWA).

5. Database Performance
    - Use connection pooling.
    - Cache heavy queries.
    - Use pagination and limit queries.
    - Regularly analyze slow queries.
    - Use indexes on frequently queried columns.
    - Normalize database schema to reduce redundancy.

---

# Golang
package main
```
import (
	"fmt"
	"regexp"
	"strings"
)

func wordFrequency(text string) map[string]int {
	text = strings.ToLower(text)

	re := regexp.MustCompile(`[^a-z0-9\s]+`)
	text = re.ReplaceAllString(text, "")

	words := strings.Fields(text)

	freq := make(map[string]int)
	for _, word := range words {
		freq[word]++
	}
	return freq
}

func main() {
	str := "Four, One two two three Three three four  four   four"
	result := wordFrequency(str)

	for word, count := range result {
		fmt.Printf("%s: %d\n", word, count)
	}
}
```

---

# Tools
- Git (5)
- Redis (3)
- VSCode (5)
- Linux (4)
- AWS
    - EC2 (3)
    - Lambda
    - RDS
    - Cloudwatch
    - S3
- Kanban boards (5) = Jira, Trello
