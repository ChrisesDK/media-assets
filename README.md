# Media Assets

Dette repository indeholder offentlige billeder og GIF'er, der hostes via GitHub Pages. Det er en enkel, statisk løsning uden buildproces. Forsiden er et mediebibliotek med forhåndsvisninger og knapper til at kopiere direkte links.

Forsiden: `https://ChrisesDK.github.io/media-assets/`

## Tilføj en ny GIF

1. Vælg en varig kategori og sti, før filen uploades. Brug `assets/gifs/` til generelle GIF'er eller `assets/projects/<projekt>/<emne>/` til projektmedier.
2. Brug et kort, ASCII-sikkert filnavn med små bogstaver og bindestreger, f.eks. `min-animation.gif`.
3. Tilføj et element i `assets/manifest.json` med den faste `id`, `category`, `path`, `title`, `description` og `alt`.
4. Commit ændringerne og push til GitHub.
5. Brug den offentlige GitHub Pages-URL fra forsiden eller manifestet.

Eksempel med Git:

```sh
git add assets/gifs/min-animation.gif
git commit -m "Add min animation"
git push
```

## Eksempler på links

Erstat filnavnene med dine egne:

- Direkte GIF-link: `https://ChrisesDK.github.io/media-assets/assets/gifs/min-animation.gif`
- Direkte PNG-link: `https://ChrisesDK.github.io/media-assets/assets/images/eksempel.png`
- Markdown-billede: `![Beskrivelse](https://ChrisesDK.github.io/media-assets/assets/images/eksempel.png)`
- HTML: `<img src="https://ChrisesDK.github.io/media-assets/assets/gifs/min-animation.gif" alt="Beskrivelse">`

## Organisering

Brug `assets/gifs/` til generelle animationer og `assets/images/` til almindelige billeder. Projekt-specifikke filer kan organiseres sådan:

```text
assets/projects/
├── project-a/
│   ├── demo.gif
│   └── screenshot.png
└── project-b/
    └── animation.gif
```

`assets/manifest.json` er bibliotekets kilde til kategori, titel og beskrivelse. Den viste titel kan altid forbedres senere, men `path` skal betragtes som permanent, når et link er delt. Brug en meningsfuld, specifik mappe fra starten, f.eks.:

```text
assets/projects/makecode-arcade/transportbaand/
└── lokal-sprite-reference-i-kollisionstjek.gif
```

Et delt medie må ikke omdøbes, flyttes eller slettes. Hvis en forbedret version er nødvendig, så behold den gamle fil og upload en ny version med et nyt navn. Så bevares alle tidligere lektioners links.

## Upload og adgang

Forsidens **Tilføj medie via GitHub**-knap åbner GitHubs officielle uploadside for dette repository. GitHub kræver login og skriveadgang til repositoryet; besøgende uden den adgang kan ikke uploade eller ændre filer.

GitHub Pages er kun statisk hosting. Den har ingen serverkode og kan derfor ikke selv tilbyde en sikker, privat uploadformular. En rigtig uploadformular på domænet ville kræve en separat backend med login, autorisation, sikker filvalidering og hemmeligheder, og er ikke nødvendig for denne løsning. Brug GitHub CLI, VS Code eller GitHubs uploadside som den sikre, standardiserede administrationsvej.

## Vigtige principper

- Alle filer i dette repository er offentligt tilgængelige. Del aldrig private oplysninger eller hemmeligheder.
- Bevar eksisterende URL'er. Omdøbning eller flytning af filer kan ødelægge eksterne links.
- Optimer store GIF'er, så de indlæses hurtigt og bruger mindre båndbredde.
- GitHub Pages har brugs- og størrelsesbegrænsninger.
- GitHub Pages er velegnet til almindelige offentlige projektaktiver, men ikke som ubegrænset CDN eller massiv filhosting.

## Fremtidig upload

Placér filen i den relevante mappe, commit og push. Når GitHub Pages har publiceret ændringen, er filen tilgængelig på dens faste Pages-URL.
