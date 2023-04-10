
# Rapport

Jag började med att forka ett projekt från GitHub. Därefter gick jag in i Android Studio och 
öppnade projektet genom att välja File-New och sedan Project from version control. 
Där hittade jag mitt github konto och hämtade projektet. 

## Rename your App

I filen strings.xml och ändrades namnet till "Malins WebWiewApp".

Kod som ändrades:
```
<resources>
    <string name="app_name">Malins WebViewApp</string>
    <string name="action_external_web">External Web Page</string>
    <string name="action_internal_web">Internal Web Page</string>
</resources>

```
## Enable Internet access for your App

I mappen manifests och filen AndroidManifest.xml lades kod till för att skapa tillgång till internet för appen.

Kod som lades till:
```
<uses-permission android:name="android.permission.INTERNET" />

```

## Create a WebView element 

I layout och i filen `activity_main.xml` skapades ett Webview element genom att ändra från `TextView` till `WebView`.

Kod som ändrades: 
```
<WebView
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:text="@string/app_name"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toBottomOf="@+id/appBarLayout" />
```

## Give the WebView an ID. 

Genom att lägga till koden `android:id="@+id/my_webview"`i layout och i filen `activity_main.xml`under funktionen WebView så fick 
WebViem funktionen ett ID. 

Kod som lades till, se första raden under WebView: 
```
<WebView
        android:id="@+id/my_webview"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/app_name"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/appBarLayout" />

```

## Create a private member variable called `myWebView` of the type `WebView` and instantiate it in `onCreate()`and Create a new WebViewClient to attach to the WebView

I `MainActivity.java` filen deklarerades en ny variabel av klassen WebView med namnet `myWebView`.
Denna variabeln deklareras direkt under Mainklassen, se ändrad kod (1). Variabeln skulle också vara en privat variabel, 
därför sattes "private" före klassen WebView. Därefter instansieras variabeln genom att tilldela nyckelordet `New` I detta fall
`new WebViewClient` som kopplas till WebView. Detta ger oss åtkomst till att surfa på webben. Koden som lades till finns i kod (2), se nedan.


Kod (1) som skapades, se andra raden:

```
public class MainActivity extends AppCompatActivity {
private WebView myWebView;

    public void showExternalWebPage(){
        myWebView.loadUrl("https://his.se");
    }

    public void showInternalWebPage(){
        myWebView.loadUrl("file:///android_asset/assets.html");

    }
```

Kod (2) som skapades, se rad 6-7:

```
protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);

        myWebView = findViewById(R.id.my_webview);
        myWebView.setWebViewClient(new WebViewClient()); // Do not open in Chrome!


        WebSettings webSettings = myWebView.getSettings();
        webSettings.setJavaScriptEnabled(true);
 ```






Därefter skapade jag i metoden on create som startar upp appen att den ska läsa in till min my_webview i activity_main.xml
hämta data från loadUrl("https://his.se"). Jag deklarade en ny variabel WebViewClient också i detta skede. 

Därefter fixade jag så att javascript kan läsas in i webview client, commit pusch

Efter detta så skapade jag en tillgänglig assets html fil. högerklicka app -new- folder- assets folder-sparade 
sen lades den som en fil i mitt projekt. Jag högerklickade på denna och döpte den till assets.html








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

![](Screenshot_20230404_123544.png)
![](Screenshot_20230404_124259.png)


Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.
