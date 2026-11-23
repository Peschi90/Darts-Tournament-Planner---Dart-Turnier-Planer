## v0.1.29
- Der Light Mode nutzt ruhige blau-graue Flächen, dezente Dialog- und Buttonverläufe sowie klarere Tabellen-, Auswahl- und Statusfarben.

---

## v0.1.28
- Der Dark Mode verwendet abgestimmte Flächen, besser lesbare Texte und einheitliche Farben für Auswahl, Fokus und Status. Auch Turnierübersicht, PowerScoring, Import-, Lizenz- und Einstellungsdialoge ziehen beim Themewechsel mit.

---

## v0.1.27
- Ein manuell erfasster PowerScoring-Spieler kann wieder für Hub-Ergebnisse freigegeben werden. Ein vorhandener Hub-Stand wird wiederhergestellt. Ohne Hub-Stand wartet der Spieler erneut auf sein Ergebnis.

---

## v0.1.26
- Im laufenden PowerScoring lassen sich Ergebnisse pro Spieler manuell eingeben und korrigieren. Der Gesamtscore bestimmt den 3-Dart-Average und wird in der lokalen Rangliste verwendet. Spätere Hub-Ergebnisse überschreiben eine gespeicherte Korrektur nicht.

---

## v0.1.25
- Der Druckdialog und die Vorlagenauswahl verwenden die Farben und Bedienelemente der Anwendung. Die Aktionen passen sich der Fensterbreite an.
- PowerScoring druckt persönliche A4-Startkarten mit Namen, Regel und scanbarem QR-Link der aktiven Hub-Sitzung. Die Karten lassen sich vor dem Drucken in der Vorschau prüfen und einzeln verteilen.

---

## v0.1.24
### Turnierdruck
- Die Turniermappe ersetzt die zehn mitgelieferten Einzelvorlagen und wird für Vorschau und Standarddruck im Turnierdialog verwendet.
- Sie übernimmt Klassen, Gruppen, Titel, Untertitel und Spielphasen aus dem Druckdialog. Enthalten sind Deckblatt, Spielerliste, Paarungsübersicht, Gruppentabellen, Gruppenspielpläne und die ausgewählten Final- und KO-Inhalte.
- Match-QR-Spalten erscheinen in Gruppen-, KO- und Round-Robin-Spielplänen bei aktiver Hub-Registrierung. Jede Seite erhält die zu ihrem Layout passende Papierausrichtung.

---

## v0.1.23
### Neue Funktionen
- Druckdialog: „Alle Klassen“ fasst die ausgewählten Inhalte in einem Druckdokument zusammen. Gruppen werden mit ihrer Klasse angezeigt und getrennt ausgewählt, auch bei gleichen Gruppen-IDs in verschiedenen Klassen.
- Druckvorlagen: Seiten können einmal oder für jede ausgewählte Gruppe ausgegeben werden. Tabellen, Klassen-/Gruppenbezeichnungen und Textvariablen verwenden je Wiederholung den passenden Kontext; Seitenzahlen laufen über das gesamte Dokument weiter.
- Textfelder: Variablen über eine Auswahl an der Cursorposition einfügen, einschließlich Turnier, Klasse, Gruppe, Klasse und Gruppe, Phase, Gruppengröße, Matchanzahl und Druckdatum. Vorhandene statische Texte bleiben unverändert, bis die Variablenauflösung aktiviert wird.
- Matchtabellen: Direkte Aktion zum Einfügen einer QR-Spalte; die Wahl des Online-QR-Felds aktiviert automatisch eine QR-Größe. Die bestehende Hub-Registrierung bleibt Voraussetzung für Online-Match-QR-Codes.

---

## v0.1.22
### Verbesserungen
- **Druckvorlagen-Designer überarbeitet**: Anpassbare Bereiche für Elemente, Seiten, Ebenen und Eigenschaften, übersichtliche Werkzeugleiste und Ausrichtungshilfen. Light/Dark und DE/EN folgen dem vorhandenen App-Design.
- **Tabellenspalten visuell bearbeiten**: Überschriften, Datenfelder, Breiten und QR-Größen direkt bearbeiten, Spalten hinzufügen, entfernen und umsortieren. Vorhandene Spaltenformatierungen bleiben erhalten.
- **Druckvorschau erneuert**: Native WPF-Seitenansicht mit Miniaturen, Seitenwechsel, Zoom und verzögerter Live-Aktualisierung; Vorschau und Druck nutzen denselben Renderer.

### Fehlerbehebungen
- Zoom skaliert den gesamten Seiteninhalt. Verschieben und Größenänderung berücksichtigen Raster, gesperrte Elemente und feste gegenüberliegende Kanten; Escape bricht die laufende Änderung ab.
- Rückgängig/Wiederholen erhält Seitenauswahl und Elemente. Unveränderte Eingaben erzeugen keine Bearbeitungsschritte; Speichern erhält die Genauigkeit vorhandener Maße. Abgebrochene Speicherdialoge verwerfen keine Änderungen.
- Bibliotheksvorlagen lassen sich als rückgängig machbare Seitenänderung anwenden, ohne den Speicherpfad des Dokuments zu übernehmen.
- Seiteneinstellungen werden pro Seite konsistent verarbeitet. Ältere Vorlagendateien bleiben lesbar; ungültige Maße werden vor Speichern und Designervorschau gemeldet.
- Tabellenkopf, Seitenumbrüche, Rotation und Druckstile korrigiert. Teilnehmerlisten verwenden laufende Nummern; klassenübergreifende Listen erfassen alle Klassen. Match-QR-Codes beachten die bestehende Hub-Registrierungsbedingung.

---

## v0.1.21
### Neue Funktionen
- **Visueller Drucklayout-Designer**: Neuer Editor zum Erstellen eigener Druckvorlagen per Drag & Drop (Elemente, Tabellen, Bindings, Seiteneinstellungen, Undo/Redo, Zoom, Snap-to-Grid). Vorlagen werden als neutrales JSON gespeichert (kein WPF-XAML), unter `%AppData%\DartTournamentPlaner\PrintTemplates`.
- **Vorlagen-Vorschau & Direktdruck**: Aus dem bestehenden Druckdialog lassen sich eigene Vorlagen auswählen und mit dem gleichen Renderer wie beim Ausdruck als Vorschau anzeigen oder direkt drucken („Vorschau = Ausdruck").
- **10 mitgelieferte Standard-Vorlagen**

### Verbesserungen
- Lizenzprüfung: Layout-Designer und Vorlagen-Aktionen sind an das bestehende Feature `ENHANCED_PRINTING` gekoppelt.
- Neue Übersetzungen (DE/EN) für Designer- und Vorlagen-Buttons sowie zugehörige Meldungen.
- Bestehender Standard-Druckpfad bleibt unverändert; die neuen Funktionen sind additiv.

---

## v0.1.20
### Neue Funktionen
- **Board-Verwaltung im Setup-Wizard**: Im Turnier-Einrichtungsassistenten kann pro Klasse optional festgelegt werden, welche Boards verwendet werden sollen. Der Schritt ist Ã¼berspringbar.
- **PowerScoring direkt aus dem Wizard starten**: Wird der Wizard mit aktiviertem PowerScoring abgeschlossen, Ã¶ffnet sich das PowerScoring automatisch â€“ inklusive aller bereits erfassten Spieler.

### Verbesserungen
- Der Abschluss-Dialog des Setup-Wizards passt jetzt optisch zu allen anderen App-Dialogen.
- Im Abschlussschritt wird bei aktiviertem PowerScoring ein Hinweistext angezeigt, der erklÃ¤rt, was als nÃ¤chstes passiert.

### Fehlerbehebungen
- Fehler beim Starten von PowerScoring bei fehlerhafter oder leerer Session-Datei behoben (kein Absturz mehr).
- â€žNeues Turnier" setzt jetzt alle Turnierdaten korrekt zurÃ¼ck.

### Optik & Dark Mode
- **Spieler hinzufÃ¼gen-Dialog**: GrÃ¶ÃŸer, anpassbar und vollstÃ¤ndig im Dark Mode.
- **Gruppe hinzufÃ¼gen-Dialog**: Etwas vergrÃ¶ÃŸert, Inhalt wird nicht mehr abgeschnitten.
- **Hub-Registrierungsdialog** und **Registrierungserfolgsdialog**: VollstÃ¤ndiger Dark-Mode-Support, GrÃ¶ÃŸe angepasst, scrollbar.
- **Hub-Spielerzuordnungs-Dialog**: VergrÃ¶ÃŸert und scrollbar â€“ Inhalt wird nicht mehr abgeschnitten.
- **Spielregeln-Dialog**: Modernisiert, vergrÃ¶ÃŸert, vollstÃ¤ndiger Dark-Mode-Support.
- **PowerScoring-Dialoge** (Spielerdetails, Turnier anlegen, Spieler hinzufÃ¼gen): VollstÃ¤ndiger Dark-Mode-Support.

---

## v0.1.19
### Neue Funktionen
- **Sync-Ã„nderungsprotokoll**: Vor jedem Abgleich mit dem Tournament Hub wird angezeigt, welche Teilnehmer neu hinzugekommen sind, entfernt oder geÃ¤ndert wurden â€“ inklusive einer kompakten Zusammenfassung im Debug-Fenster.

### Verbesserungen
- **Teilnehmerdaten werden jetzt vollstÃ¤ndig synchronisiert**: Kontaktdaten wie Telefon, Adresse, Verein und weitere Felder wurden bisher beim Hub-Abgleich nicht Ã¼bermittelt. Das ist jetzt behoben.
- **Verbesserte Hub-Verbindung**: Die Nachrichtenverarbeitung vom Hub lÃ¤uft flÃ¼ssiger und blockiert die Anwendung nicht mehr unnÃ¶tig.
- **Effizienterer Daten-Sync**: Identische Datenpakete werden beim automatischen 5-Minuten-Sync nicht erneut Ã¼bertragen â€“ spart Netzwerkverkehr.
- **Stabilere WebSocket-Verbindung**: Bei VerbindungsabbrÃ¼chen wartet die App jetzt lÃ¤nger zwischen den Wiederverbindungsversuchen (bis zu 5 Minuten) und gibt nach 20 Fehlversuchen auf, anstatt den Server dauerhaft zu Ã¼berlasten.
- **GroÃŸe Hub-Nachrichten**: Das Limit fÃ¼r fragmentierte Nachrichten wurde stark erhÃ¶ht. Bei Ãœberschreitung erfolgt automatisch ein vollstÃ¤ndiger Sync.
- **Live-Match-Ereignisse zuverlÃ¤ssiger**: Spielergebnisse werden jetzt mit einer eindeutigen ID Ã¼bermittelt und bei ausbleibender BestÃ¤tigung automatisch erneut gesendet.
- **UnnÃ¶tiger Hintergrundverkehr entfernt**: Ein interner Polling-Timer, der regelmÃ¤ÃŸig unnÃ¶tige Anfragen an die lokale API schickte, wurde entfernt.

### Fehlerbehebungen
- Teilnehmer-Ã„nderungen (Name, Telefon, Verein, Adresse) landen jetzt zuverlÃ¤ssig im Hub und im Dashboard.

### Optik
- **Teilnehmerverwaltungs-Dialog**: Buttons und Farben passen jetzt zum App-Design und unterstÃ¼tzen vollstÃ¤ndig den Dark Mode.

### Sicherheit (Hub-Server)
- Das fest hinterlegte Standard-Passwort im Hub-Server wurde entfernt. Ein eigenes Passwort in der `.env`-Datei ist jetzt Pflicht.

### Betrieb (Hub-Server)
- Neue Metriken fÃ¼r den Hub-Server (Prometheus-kompatibel, optional aktivierbar).
- Spielergebnis-BestÃ¤tigungen kÃ¶nnen optional in der Datenbank protokolliert werden.
- Hinweise zur korrekten `.env`-Datei-Kodierung (UTF-8 ohne BOM) und zum PM2-Neustart nach ENV-Ã„nderungen ergÃ¤nzt.

---

## v0.1.18
### bugfix
- fixed tournament synchronisation bug


## v0.1.17
### bugfix
- fixed tournament synchronisation bug
- fixed user id handling and possibility to add a club  for each user
- user account is now nessecary to sync/register tournaments with dashboard.darts-tournament-planner.de


## v0.1.16
### bugfix
- fixed tournmanet registragion bug
- fixed user id handling and possibility to add a club  for each user
- add player dialog doesnt duplicate the users anymore
- player information can now change anytime in add player dialog

## v0.1.15.2
### New Features
- License Request Email Copy**: Users now receive a copy of the license request email at their provided email address
- License Request Improvements**: Enhanced email sending reliability and user feedback
- User Account handling and registration at dashboard.darts-tournament-planner.de
- Possibility to Plan Tournaments over User Dashboard and sync them any time to Darts-Tournament Planner
- Fetch all opened Tournaments from User Dashboard for your license
- share license keys with different user Accounts to let other user acces Dashboard functionality and manage tournaments
- Implement Live Ticker features for tournamnets.
- Implement Online Tournament participants registration. 

### Backend Improvements
- change domain to Darts-Tournament-Planner.de
- build new sync routines to get tournaments from user dashboard

## v0.1.14

### ðŸŽ¯ New Features
- **ðŸ“§ Automatic License Request Email**: License requests are now sent automatically via email without opening a mail client
  - Smart fallback to mail client if automatic sending fails
  - User receives a copy at their email address
- **âš¡ Skip Group Phase**: Start tournaments directly with knockout phase without group stage

### ðŸŽ¨ UI/UX Improvements
- **Modern Email Dialogs**: New success and error dialogs with professional design
- **Feature Update**: "PowerScoring" replaces deprecated "API Access" in license requests
- **Generate Knockout Dialog**: Modern confirmation dialog replacing standard MessageBox

### ðŸ› Bug Fixes
- **Bye Match Loser Propagation**: Bye match losers now correctly moved to loser bracket
- **DataGrid Context Menus**: Added right-click menus to Winner/Loser Bracket DataGrids (edit, give bye, undo bye)
- **DataGrid Button Handlers**: Fixed Give Bye and Undo Bye buttons in DataGrids
- **TournamentOverview Filter**: Classes with "Skip Group Phase" now correctly displayed
- **Email Button Fix**: License request button no longer hangs during email sending

### ðŸŒ Localization
- Complete German/English translations for email system dialogs
- **Skip Group Phase Translations**: Game rules and confirmation dialogs fully translated
- **Generate Knockout Dialog**: All UI elements translated

### ðŸ”§ Technical
- **MailKit Integration**: Added MailKit library for reliable SMTP email delivery (Port 465)
- **EmailService**: New service class for automated email handling
- **ByeMatchManager**: Improved bye match loser handling and propagation logic
- **GenerateKnockoutDialog**: New reusable dialog component with localization support

## v0.1.13

### ðŸŽ¯ New Features
- **ðŸ†” Custom Tournament-ID**: Users can set custom Tournament-IDs or generate them automatically
  - Optional ID input field in Hub registration dialog
  - ðŸ”„ Generate button for quick ID creation
  - ID validation and sanitization (alphanumeric characters, `_`, `-` only)
  - Automatic `TOURNAMENT_` prefix if not present
  - Persistent storage of Tournament-ID in `TournamentData`
  - Reuse of saved IDs on reconnect for persistent QR codes

- **âš¡ PowerScoring System**: Intelligent player seeding based on performance data
  - **Scoring Sessions**: Create scoring sessions with customizable rules (1x3, 8x3, 10x3, 15x3 throws)
  - **Remote Scoring**: QR code integration for remote score entry via Tournament Hub
  - **Player Ranking**: Automatic ranking based on total and average scores
  - **Group Distribution**: Intelligent player distribution across tournament classes
	- Support for 5 classes (Platinum, Gold, Silver, Bronze, Iron)
	- Configurable groups per class (1-4 groups)
	- Configurable players per group (2-6 players)
  - **Distribution Modes**: 
	- âš–ï¸ Balanced: Even distribution by ranking
	- ðŸ Snake Draft: 1-2-3-4-4-3-2-1 zigzag pattern for balanced groups
	- ðŸ” Top-Heavy: Strongest players grouped first
	- ðŸŽ² Random: Random distribution
  - **Advanced Settings**: 
	- Class-specific group and player counts
	- Skip classes functionality
	- Individual player limits per class
	- Distribution preview before confirmation
  - **Tournament Creation**: 
	- Create new tournament directly from PowerScoring distribution
	- Automatic tournament data migration
	- Existing tournament backup before creation
	- Seamless UI transition to tournament view
  - **Session Management**: 
	- Session persistence (auto-save/auto-load)
	- Tournament-ID integration for Hub synchronization
	- QR code generation for all players
	- Live scoring updates via WebSocket
  - **Comprehensive Help**: Detailed PowerScoring documentation in Help Window (DE/EN)

- **ðŸŽ¨ Dark Mode Enhancements**: Complete dark mode support for all PowerScoring components
  - **Theme Persistence**: Dark/Light mode preference saved and restored on app restart
  - **PowerScoring Dialogs**: All dialogs fully theme-aware
	- Main PowerScoring window with dark mode support
	- Advanced distribution settings dialog
	- Group distribution dialog
	- Tournament creation confirmation dialog
	- Session management dialogs
  - **UI Components**: 
	- ComboBox dropdowns with dark mode support (custom templates)
	- DataGrid with theme-aware cells, rows, and headers
	- Context menus with proper dark mode colors
	- All text elements with dynamic foreground colors
  - **Automatic Config Save**: Theme selection automatically persisted to config.json

### ðŸŒ Hub Integration Improvements
- **Tournament-ID Persistence**: Tournament-ID managed via `TournamentManagementService`
  - Correct Tournament-ID propagation in all dialog paths (Print, Overview, Match entry)
  - Auto-load of saved Tournament-ID during Hub registration
  - QR codes remain valid after connection interruptions
- **âœ¨ NEW: Live-Match-Updates**: Real-time match progress tracking from Tournament Hub
  - Match-Start Events: Automatic detection when a match begins
  - Leg-Completed Events: Updates after each finished leg with detailed statistics
  - Match-Progress Events: Optional live updates during ongoing legs
  - Live-Status indicators (ðŸ”´ LIVE) in UI
  - Leg-Counter display (e.g. "Leg 2/5")
  - Detailed leg statistics (winner, darts, duration, average, checkout)
  - Automatic UI synchronization without data persistence
  - Full internationalization (DE/EN)
- **ðŸ”„ Automatic WebSocket Reconnect**: Robust connection recovery after server outages
  - Continuous reconnect attempts every 5-10 seconds until server is back online
  - Automatic tournament re-registration with preserved Tournament-ID
  - Full tournament data synchronization after reconnect (matches, game rules, players)
  - Duplicate reconnect prevention with smart scheduling
  - No manual intervention required - seamless reconnection
- **ðŸ“Š Enhanced Connection Status Display**: Detailed WebSocket and tournament status indicators
  - Separate states for WebSocket connection and tournament registration
  - Status bar shows: Disconnected / WebSocket Ready / Tournament Registered
  - Visual indicators (ðŸ”´ Red / ðŸŸ¢ Green / ðŸŸ¡ Yellow) for connection state
  - Preserved Tournament-ID display during disconnection for reconnect info
  - Real-time status updates in both status bar and debug console
  - Clear distinction between connection loss and registration status

### ðŸ”§ Bug Fixes
- **Tournament-ID in QR Codes**: Complete integration of Tournament-ID in all QR code generations
  - âœ… Print Dialog (all 4 methods)
  - âœ… Tournament Overview Window
  - âœ… Match Result Windows (Group phase, Finals, K.O.)
  - âœ… Tournament Tree (Winner & Loser Bracket)
  - âœ… EditMatchResult (TournamentTab)
- **Hub Registration Dialog**: 
  - Dialog height increased from 350px to 420px (all content fully visible)
  - Complete translation of all info texts (German & English)
  - TextBlocks dynamically translated instead of static texts
- **WebSocket Connection Management**:
  - Fixed NullReferenceException in CloseAsync method
  - Robust exception handling for ObjectDisposedException
  - Safe disposal of CancellationTokenSource
  - Prevented crash on disconnect
- **Status Bar Display**:
  - Fixed status bar remaining green after server disconnect
  - Eliminated duplicate event handlers causing incorrect status display
  - Status now correctly shows "Disconnected" when connection is lost
  - Tournament-ID preserved and displayed during reconnection attempts
- **Dark Mode Issues**:
  - âœ… Fixed ComboBox dropdown readability (white text on white background)
  - âœ… Fixed DataGrid visibility in dark mode (proper cell/row/header colors)
  - âœ… Fixed PowerScoring session dialogs dark mode support
  - âœ… Fixed PowerScoringAdvancedConfigDialog dark mode (footer, content cards)
  - âœ… Fixed PowerScoringConfirmDialog dark mode (background, text, footer)
  - âœ… Fixed theme persistence (dark mode now restored on app restart)

### ðŸŒ Localization
- **Hub Registration Dialog Translations**: 13 new translation keys added
  - German translations in `GermanHubLanguageProvider`
  - English translations in `EnglishHubLanguageProvider`
  - Dynamic UI translation for all dialog elements
  - Tooltips and buttons fully translated
- **PowerScoring Translations**: Comprehensive translation coverage
  - **German**: 100+ translation keys in `GermanPowerScoringLanguageProvider`
  - **English**: 100+ translation keys in `EnglishPowerScoringLanguageProvider`
  - **Categories**:
	- Main window UI elements (buttons, labels, tooltips)
	- Scoring rules and session management
	- Group distribution and configuration
	- Advanced settings dialog
	- Error messages and confirmations
	- Success notifications
	- Distribution modes and descriptions
	- Tournament creation workflow
  - **Help System**: PowerScoring section added to Help Window
	- Detailed getting started guide
	- Scoring rules explanation
	- Distribution modes documentation
	- Advanced settings guide
	- QR code integration instructions
	- Fully translated in German and English

### ðŸŽ¨ UI/UX Improvements
- **Hub Registration Dialog**:
  - Optimal dialog size (500x420px)
  - Modern animations and hover effects
  - Info box with helpful tips and notes
  - Generate button with icon (ðŸ”„)
  - Theme support (Light/Dark Mode)
  - No more cut-off content
- **Status Bar Enhancements**:
  - Color-coded connection indicators (Red/Green/Yellow)
  - Three-tier status display: Connection / Registration / Sync status
  - Tournament-ID preserved during disconnection for user awareness
  - Real-time status updates without page refresh
  - Clickable status area for debug console access
- **Debug Console Improvements**:
  - Detailed logging of all reconnect attempts
  - Step-by-step reconnection process visualization
  - WebSocket state tracking with timestamps
  - Tournament data sync progress indicators
  - Color-coded log messages for easy debugging
- **PowerScoring UI**:
  - **Modern Design**: Card-based layout with shadows and gradients
  - **Loading Overlay**: Animated loading screen during Hub registration
  - **Responsive Layout**: Adaptive UI for different content states (setup/scoring/results)
  - **Visual Feedback**: Success/error notifications for all actions
  - **Player Management**: Inline player add/remove with visual feedback
  - **Score Entry**: Clean score input interface with validation
  - **Results Display**: DataGrid with sorting and context menus
  - **Preview System**: Visual distribution preview before tournament creation
  - **Dark Mode Compatible**: All UI elements properly themed
- **PowerScoring Workflow**:
  - **Step 1**: Tournament-ID and scoring rule selection
  - **Step 2**: Player management with add/remove functionality
  - **Step 3**: Scoring phase with QR codes or manual entry
  - **Step 4**: Results ranking and distribution preview
  - **Step 5**: Tournament creation with confirmation
  - Seamless transitions between all phases
  - Context-aware button visibility

### ðŸš€ Performance & Stability
- **Reconnect Reliability**: Continuous retry mechanism until connection is restored
- **Memory Management**: Proper disposal of WebSocket and cancellation tokens
- **Exception Handling**: Comprehensive try-catch blocks preventing crashes
- **Resource Cleanup**: Safe cleanup of timers, connections, and event handlers
- **Thread Safety**: Dispatcher-based UI updates for thread-safe operations
- **State Management**: Robust tracking of connection and registration states
- **PowerScoring Performance**:
  - Efficient player ranking algorithms (O(n log n))
  - Optimized distribution calculations
  - Async/await for non-blocking UI operations
  - Session persistence for quick resume
  - Minimal memory footprint for large player lists

### ðŸ“š Documentation
- **Code Comments**: Extensive documentation of reconnect logic and state management
- **Debug Logging**: Detailed trace output for all connection operations
- **State Transitions**: Clear documentation of connection state changes
- **Error Handling**: Comprehensive error logging and recovery documentation

## v0.1.12
- moved
	- Tournament Hub out of the repository.

- bugfixes
	- Fixed some bugs in the license system.
	- **Reset Buttons Functionality**: Fixed reset buttons behavior to preserve match structure
		- Reset KO Phase button now only resets KO phase data (preserves group phase results)
		- Reset Finals button now only resets finals phase data (preserves group phase results)
		- Reset Matches button now context-aware (works in Group, KO, and Finals phases)

- improvements
	- **Landscape Format Support**: Automatic landscape format (1122.5 x 793.7px) when QR codes are available
	- **Larger Font Sizes**: Doubled font sizes (22pt headers, 20pt cells) for better readability
	- **Multi-Page Support**: Automatic creation of continuation pages for many matches
		- Intelligent calculation of matches per page based on available space
		- Page numbering for overflow pages ("Page 2", "Page 3", etc.)
		- Support for group phase, finals and knockout brackets
	- **QR Code Optimization**: 90x90px QR codes in 110px wide columns
	- **Optimized Table Layouts**: 
		- Widened match number column (60px instead of 40px)
		- Adjusted row height (95px) for optimal space utilization
		- 5 matches with QR codes fit on one page
	- Better code organization and reusability
	- **Context-Aware Match Reset**: 
		- Reset Matches button now intelligently resets only match results based on current phase
		- Preserves match generation and tournament structure
		- Works across Group Phase, KO Phase, and Finals Phase
		- Button activation logic improved for all tournament phases
	- **Tournament Overview Auto-Scroll**: 
		- Auto-scroll feature now synchronized with auto-cycle timing
		- âœ… **Intelligent Scroll Strategies**:
			- **Small Content (<10px)**: Delayed single-scroll at 50% of cycle time for optimal visibility
			- **Large Content (â‰¥10px)**: Smooth animated scrolling over entire cycle duration with easing

## v0.1.11
- adds
	- Progress bar for update to new version implemented. 
- bugfixes
	- Fixed some translation bugs.

## v0.1.10
- bugfixes
	- Fixed bug for license request email.

## v0.1.9
- bugfixes
	- Improved sharpness and overall clarity.

## v0.1.8

### ðŸŽ¯ New Features
- **ðŸ”‘ Complete License System**: Comprehensive feature management with Core/Premium features, offline validation and license management
- **ðŸŽ¨ Dark/Light Theme System**: Full theme switching with persistent settings and one-click toggle
- **ðŸ“Š Extended Player Statistics**: New statistics columns "Fastest Match" and "Fewest Darts" with detailed performance analysis
- **ðŸŒ Tournament Hub Integration**: Enhanced real-time synchronization with WebSocket connections and QR code support
- **ðŸ“± Professional Startup**: Animated splash screen with progress indicators and modern animations
- **ðŸŽ­ Statistics Tab**: New dedicated tab for detailed player statistics in each tournament class

### ðŸ”‘ License System Features
- **Premium Feature Management**: Granular control over advanced features
- **Offline License Validation**: Functionality even without internet connection
- **License Dialogs**: User-friendly activation, status display and management
- **Feature-driven UI**: Dynamic display based on license status
- **Security Features**: Hardware ID-based licensing with activation limits

### ðŸŽ¨ Theme System
- **Light/Dark Mode Toggle**: Complete theme switching via menu button
- **Consistent Theme Application**: Uniform display across all UI elements
- **Theme Persistence**: Storage of theme selection between app starts
- **Modern Color Palettes**: Professional color schemes for both modes
- **Real-time Theme Switching**: Theme change without application restart

### ðŸŒ Hub Integration Improvements
- **WebSocket Statistics Integration**: Complete extraction and processing of dart statistics from WebSocket messages
- **QR Code Support**: QRCoder integration for easy tournament access
- **Extended Match Data**: Processing of `dartScoringResult` for detailed game analysis
- **Automatic Synchronization**: Real-time updates of player statistics on match completion
- **Debug Console**: Global debug console for hub connection diagnostics
- **Fallback Mechanisms**: Robust processing for different data formats

### ðŸ“Š Statistics Features
- **Match Efficiency**: Display of fastest match duration (MM:SS format)
- **Throw Efficiency**: Tracking of fewest darts per match
- **Detailed Data**: High Finish details with darts breakdown
- **Leg Averages**: Tracking of individual leg performance
- **Checkout Statistics**: Count and details of all successful checkouts
- **180 Tracking**: Complete tracking of all maximum scores
- **Score Analysis**: Tracking of 26+ scores and performance trends

### ðŸ”§ Improvements
- **UI Button Activation**: Reset buttons are no longer incorrectly grayed out
- **Match Statistics Processing**: Extended extraction of 180s, 26+ scores, high finishes and checkouts
- **Localization**: New German and English translations for all new features
- **Performance**: Optimized statistics calculation and UI updates
- **Debug Output**: Extended logging functionality for better error diagnosis
- **Splash Screen**: Professional startup experience with loading animations and status updates

### ðŸ—ï¸ Technical Improvements
- **Manager Classes**: Split UI logic into specialized managers (TournamentTabUIManager, PlayerStatisticsManager, TranslationManager)
- **ThemeService**: Dedicated service class for theme management
- **LicenseFeatureService**: Comprehensive license feature management
- **Event Handling**: Improved event delegation for better maintainability
- **Code Organization**: Clearer separation of responsibilities
- **Type Safety**: Enhanced null-safety and error handling
- **.NET 9.0 Upgrade**: Update to the latest .NET version with C# 13.0

### ðŸ“± User Experience
- **Animated Startup**: Professional splash screen with progress bar and status updates
- **Theme Toggle**: One-click switch between Light and Dark mode
- **Formatting**: Time displays in user-friendly MM:SS format
- **Tooltips**: Extended help texts for new statistics fields and features
- **Sorting**: Improved sorting options for statistics tables
- **License Management**: Intuitive license activation and management

### ðŸ”„ API & Integration
- **QRCoder Package**: New dependency for QR code generation (v1.6.0)
- **System.Management**: New dependency for hardware ID generation (v9.0.0)
- **WebSocket Protocol**: Extended support for Tournament Hub WebSocket messages
- **JSON Parsing**: Robust processing of complex match data structures and license validation
- **Backward Compatibility**: Support for existing and new data formats
- **Error Recovery**: Improved recovery from connection errors

### ðŸ› Bug Fixes
- **Reset Button Problem**: Tournament reset buttons work correctly again
- **Statistics Storage**: Correct persistence in tournament-data.json
- **UI Synchronization**: Improved user interface updates
- **Null Reference Handling**: More robust error handling for missing data
- **Theme Consistency**: Correct theme application across all UI components
- **License Validation**: Robust offline/online license verification

### ðŸ“š Documentation
- **Code Comments**: Extended documentation of new features
- **Debug Logging**: Detailed trace output for development and maintenance
- **Localization Keys**: Complete translation keys for all UI elements
- **License Integration**: Comprehensive documentation of the license system
- **Theme System**: Documentation of the theme switching mechanism

### ðŸŽ Premium Features (License required)
- **ðŸ“ˆ Extended Statistics**: Detailed player performance analysis with hub integration
- **ðŸŒ Tournament Hub Premium**: Extended hub connection features
- **ðŸ–¨ï¸ Enhanced Printing**: Professional print layouts and extended options
- **ðŸ“Š Tournament Overview Premium**: Extended presentation modes and features

### ðŸš€ Performance & Stability
- **Async/Await Pattern**: Consistent use of asynchronous programming
- **Memory Management**: Improved resource management and garbage collection
- **Exception Handling**: Robust error handling with user feedback
- **UI Responsiveness**: Improved UI responsiveness through background threading
- **Startup Performance**: Optimized application startup time with splash screen


## v0.0.0
- **PowerScoring Documentation**:
  - Inline code documentation for all public methods
  - Phase-based implementation documentation (Phase 1-3)
  - Service layer responsibility documentation
  - Translation key documentation
  - Help Window integration with comprehensive user guide
  - Distribution mode explanations and use cases

