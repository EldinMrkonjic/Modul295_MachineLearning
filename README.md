# MrkonjicEldin-259


## Link zum Datensatz:
https://www.kaggle.com/datasets/camnugent/sandp500

## Datensatzbeschreibung:
Dieser Datensatz umfasst historische Börsendaten der S&P 500-Unternehmen der letzten fünf Jahre. Enthalten sind Datenfelder wie Datum (yy-mm-dd), Eröffnungskurs, Tageshoch, Tagestief, Schlusskurs, Handelsvolumen und Ticker-Name. Die Daten wurden in zwei Formaten angeboten: als zusammengeführte CSV-Datei (all_stocks_5yr.csv) sowie in Einzelfiles pro Aktie, um vielfältigen Analyse- und Modellierungsbedürfnissen gerecht zu werden. Mit diesem strukturierten Format lassen sich visuelle Darstellungen, statistische Auswertungen und Prognosemodelle entwickeln.

## Datenschutz und Massnahmen:
Da es sich ausschliesslich um öffentliche Finanzmarktdaten handelt, tangiert dieser Datensatz keine personenbezogenen Daten. Somit sind keine besonderen Datenschutzrichtlinien erforderlich. Dennoch wurden Massnahmen getroffen, um sicherzustellen, dass ausschliesslich aggregierte und anonyme Marktdaten verarbeitet werden. Als Ersteller wurde auf die Veröffentlichung sensibler Informationen verzichtet. Nutzer werden zudem darauf hingewiesen, bei weiterführenden Analysen die gängigen Datenschutzstandards einzuhalten und ausschliesslich vertrauenswürdige Datenquellen zu nutzen.


## Worum es in meinem Projekt geht

Ich wollte herausfinden, wie gut sich Bewegungen am Aktienmarkt vorhersagen lassen, wenn ich mich auf harte Fakten stütze: historische Kurse und Handelsvolumen. Dafür habe ich mir einen öffentlichen S&P-500-Datensatz genommen, der fünf Jahre Kursgeschichte für hunderte Unternehmen enthält – mit Datum, Eröffnungs- und Schlusskurs, Tageshoch, Tagestief, Volumen und dem jeweiligen Ticker. Mein Ziel: den Schlusskurs zu prognostizieren und zu verstehen, welche Merkmale dabei am meisten zählen.

Zuerst habe ich die Daten aufbereitet und beschrieben: zentrale Kennzahlen, Plausibilitätschecks und Visualisierungen, um ein Gefühl für Verteilungen und Ausreißer zu bekommen. Dabei habe ich mir auch überlegt, wann Skalierung Sinn ergibt – insbesondere beim stark schwankenden Volumen. Anschließend habe ich den Datensatz in Trainings- und Testanteile geteilt und mich bewusst für einen RandomForestRegressor entschieden. Der Grund: Baumbasierte Modelle kommen gut mit nichtlinearen Zusammenhängen klar, sind relativ robust gegenüber Ausreißern und liefern mir gleichzeitig Feature Importances, mit denen ich die Ergebnisse erklären kann.

Nach dem Training habe ich die Güte meines Modells über MAE und R² bewertet. Um die reine Regressionssicht zu ergänzen, habe ich zusätzlich eine kleine Klassifikationsaufgabe gebaut: Ist der Schlusskurs höher als der Eröffnungskurs – ja oder nein? Das habe ich mit einer Konfusionsmatrix überprüft. Besonders spannend war für mich zu sehen, wie stark open und volume als Einflussgrößen wirken – und wie sich ihr Beitrag je nach Titel unterscheiden kann.

Natürlich endet mein Projekt nicht bei den ersten Ergebnissen. Für echte Handelsstrategien müsste ich auf zeitgerechte Validierung achten (Walk-Forward-Splits statt Zufall), Ticker-Spezifika berücksichtigen und technische Indikatoren wie gleitende Durchschnitte oder Momentum-Maße ergänzen. Aber der Kern steht: Ich habe einen reproduzierbaren Weg gebaut, historische Kursdaten aufzubereiten, ein erklärbares Modell zu trainieren und die Leistung nüchtern zu messen. Damit kann ich weiter iterieren – datengetrieben, transparent und mit klarem Blick darauf, was am Markt wirklich Signale sendet.
