
### Public Pages (Routes)

| Page           | Path                        | Description                     |
| -------------- | --------------------------- | ------------------------------- |
| Home           | `/`                         | Intro, featured topics, search  |
| Topics List    | `/topics`                   | Shows all main topics           |
| Sub-topic List | `/topics/[slug]`            | Lists subtopics within category |
| Notes Viewer   | `/a/b/c`                    | Loads `.doc` from API           |
| Search Results | `/search?q=query`           | Search by title/keyword         |
| About          | `/about`                    | Site information                |
| Privacy, T\&C  | `/privacy-policy`, `/terms` | For compliance                  |

---

## File Structure (App Router + `src/app/`)

```
src/
├── app/
│   ├── layout.tsx                  # Root layout (head, theme)
│   ├── page.tsx                    # Home page
│   ├── topics/
│   │   ├── page.tsx                # Topics list
│   │   └── [slug]/
│   │       └── page.tsx            # Subtopic list
│   ├── a/
│   │   └── [b]/
│   │       └── [c]/
│   │           └── page.tsx        # Notes viewer from API
│   ├── search/
│   │   └── page.tsx                # Search results
│   ├── about/
│   │   └── page.tsx
│   ├── privacy-policy/
│   │   └── page.tsx
│   ├── terms/
│   │   └── page.tsx
├── components/
│   ├── Header.tsx
│   ├── Sidebar.tsx
│   ├── Footer.tsx
│   ├── AdBlock.tsx
│   ├── SEO.tsx                     # SEO meta helper
├── lib/
│   ├── api.ts                      # Data fetching from the API
├── public/
│   └── robots.txt
│   └── sitemap.xml
```

---

## 🧱 Reusable Layout Components

* **Header**: Logo, navigation links
* **Sidebar**: Shows related subtopics
* **Footer**: Links to About, Privacy, etc.
* **AdBlock**: Responsive AdSense placeholder
* **SEO Component**: `<SEO title="" description="" />` for meta tags

---

## 💰 AdSense Strategy (Smart Placement)

| Page           | Placement (Desktop + Mobile)              |
| -------------- | ----------------------------------------- |
| Notes/Markdown | Top, Mid block, End block                 |
| Homepage       | Right sidebar of featured list            |
| Search         | Sticky ad block, Between 3rd & 5th result |

---

## 🌐 SEO Considerations

* `robots.txt` → place in `public/`
* `sitemap.xml` → auto-generated (can use `next-sitemap`)
* Custom meta tags per page via `<SEO />` component
* Server-side rendering (`getStaticProps`) or `generateMetadata()` for SEO on subtopic/detail pages

---

## 🔡 URL Structure

| Type          | Example URL                                                        |
| ------------- | ------------------------------------------------------------------ |
| Home          | `/`                                                                |
| Topics        | `/topics`                                                          |
| Sub-topic     | `/topics/basic-computer-organisation-and-design`                   |
| Markdown View | `/basic-computer-organisation-and-design/von-neumann-architecture` |
| Search        | `/search?q=von+neumann`                                            |
| Info Pages    | `/about`, `/privacy-policy`                                        |

