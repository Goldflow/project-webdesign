# Full Screen video als achtergrond

Een goeie manier om je site er iets dynamischer er uit te laten zien en de aandacht te trekken van je gebruiker is een video als achtergrond plaatsen.

Uitleg met video:

<video width="600" controls>
<source src="video-background-vb.mkv">
</video>

[Download hier het voorbeeld](video-background.zip)

## Voorbeeld uitlegt

Het belangrijkste dat je moet gebruiken om dit voorbeeld te bekomen is het volgende;

In je CSS plaats je deze klasses:

```CSS
.fullscreen-bg {
            position: fixed;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            overflow: hidden;
            z-index: -100;
        }

        .fullscreen-bg__video {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
        }
```

in je HTML dit stukje code

```HTML
   <div class="fullscreen-bg">
        <video loop muted autoplay class="fullscreen-bg__video">
            <source src="bboy.mp4" type="video/mp4">
        </video>
    </div>
```

Belangrijk: 

- in `src` komt de url naar de video (die moet dus ook in je website staan - zorg dat die niet te groot is) - in dit geval `bboy.mp4`

- `type` moet overeenkomen met het video type dat je gebruikt; in dit geval `video/mp4`

