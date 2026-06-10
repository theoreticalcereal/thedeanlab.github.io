# Kevin Dean Profile Page Design

## Goal

Add a canonical `kevin-dean` landing page to the Dean Lab Sphinx site that presents Kevin Dean as a clear public scientific entity, consolidates profile links, and gives search engines structured data that matches the public identity language.

## Approved Decisions

- Keep the page native to the existing Sphinx/Read the Docs theme.
- Use modest custom CSS only where it makes the profile page more readable.
- Copy the supplied headshot and public CV into the site source so the GitHub Pages build is reproducible.
- Use the canonical personal one-liner: "I build open-source, adaptive light-sheet microscopes and image-analysis workflows to reveal rare metastatic colonization events in intact tissues."
- Include `ProfilePage` and `Person` JSON-LD with `sameAs` profile links.

## Content Structure

- `Hero`: headshot, name, current title, 25-word bio, and quick links.
- `Profile prose`: 100-word bio immediately below the hero without an explicit bio label.
- `Professional positions`: current titles, memberships, and institutional roles.
- `Selected publications`: research thesis followed by a compact list grounded in the CV and UTSW profile.
- `Selected tools`: navigate, Altair, clearex, cyDPNI, and related GitHub organizations.
- `Talks and media`: selected talks/workshops from the public CV, with a note that the CV has the full list.
- `Contact`: compact institutional email and office mailing address from the CV.
- `Profiles`: Scholar, ORCID, GitHub, LinkedIn, Bluesky, and UTSW profile links.
- `Public CV`: downloadable PDF copied from the CV repository.

## Integration Points

- Add `source/kevin-dean.rst`.
- Add `kevin-dean` to the homepage visible section list and hidden toctree.
- Add `source/_static/profile.css` and enable it in `source/conf.py`.
- Copy the headshot to `source/_static/kevin-dean-headshot.jpg`.
- Copy the public CV to `source/_static/kevin-dean-cv.pdf`.

## Validation

- Add a focused pytest that checks the profile page source for required canonical content, links, image, CV, and JSON-LD types.
- Run the test first and confirm it fails before adding the page.
- Build Sphinx with warnings treated as errors.
- Visually inspect the rendered page in the browser at a local static server URL.
