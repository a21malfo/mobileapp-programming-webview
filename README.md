
# Rapport

**Jag började med att forka ett projekt från GitHub. Därefter gick jag in i Android Studio och 
** New-file-project from version control-mitt github och hämtade projektet. 
Sen Rename your App, i mappen values och filen strings.xml. Döpte till Malins.
Create a WebView element in the layout file `content_main.xml` by replacing the existing `TextView`.
Detta gjorde jag i layout- filen activity_main.xml. Ändrade <WebText till <WebView
Give the WebView an ID. Hint: `android:id="@+id/my_webview"` Detta gjorde jag i layout under webViem 

Därefter skapade jag en ny variabel av klassen WebView och döpte den till myWebView, i MainActivity.java filen. 
Jag satte private innan för att göra variabelm privat. 

Därefter skapade jag i metoden on create som startar upp appen att den ska läsa in till min my_webview i activity_main.xml
hämta data från loadUrl("https://his.se"). Jag deklarade en ny variabel WebViewClient också i detta skede. 

Därefter fixade jag så att javascript kan läsas in i webview client





_Du kan ta bort all text som finns sedan tidigare_.

## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            // Geolocation API stöds inte, gör något
            break;
        case error.POSITION_UNAVAILABLE:
            // Misslyckat positionsanrop, gör något
            break;
        case error.UNKNOWN_ERROR:
            // Okänt fel, gör något
            break;
    }
}
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
