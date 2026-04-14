# System obsługi zamówień z dostawą

## Brudnopis
https://docs.google.com/document/d/1_yS38bcsTMefnQcKZWZIMeikfWNOddROzf7ziSlS2r8/edit?usp=sharing

## Opis wymagań
System umożliwia składanie zamówień przez klientów na produkty oferowane przez restauracje i sklepy, a następnie obsługę procesu ich realizacji i dostawy przez kurierów. Każde zamówienie jest przypisywane do konkretnego klienta oraz restauracji/sklepu. Zawiera listę wybranych produktów wraz z ich ilością, ceną oraz ewentualnymi uwagami klienta.

Zamówienie rejestrowane jest w systemie z uwzględnieniem daty i czasu złożenia zamówienia, przewidywanego czasu realizacji, statusu zamówienia, form płatności oraz adresu dostawy. System umożliwia śledzenie statusu zamówienia na każdym etapie jego realizacji.

Każda restauracja/sklep posiada w systemie swoją kartotekę, w której przechowywane są informacje (nazwa, adres, godziny otwarcia, dane kontaktowe, lista oferowanych produktów). Produkty posiadają swoją nazwę, opis, kategorię, cenę oraz dostępność. W przypadku restauracji możliwe jest określenie wariantów produktu.

Klient systemu posiada swoją kartotekę zawierającą dane osobowe oraz kontaktowe (imię, nazwisko, numer telefonu, adres e-mail, adresy dostawy). Klient może posiadać wiele adresów dostawy oraz historię zamówień przechowywaną w systemie.

W procesie realizacji zamówienia udział bierze kurier, który jest odpowiedzialny za odbiór zamówienia z restauracji/sklepu oraz dostarczenie go do klienta. Każdy kurier posiada swoją kartotekę zawierającą dane identyfikacyjne, kontaktowe oraz informacje o statusie dostępności. Kurierowi przypisywane są zamówienia wraz z informacją o czasie odbioru oraz dostawy.

System umożliwia przypisanie zamówień do kurierów na podstawie ich dostępności oraz lokalizacji. Rejestrowane są czasy odbioru zamówienia z restauracji/sklepu oraz dostarczenia do klienta, co pozwala na analizę efektywności dostaw.

W przypadku pierwszego zamówienia klienta wymagane jest utworzenie konta w systemie poprzez wprowadzenie danych osobowych oraz adresowych. Natomiast w przypadku dodania nowej restauracji/sklepu, administrator systemu wprowadza jego dane oraz ofertę produktową.

System umożliwia również obsługę płatności za zamówienia, zarówno online, jak i przy odbiorze. Rejestrowane są informacje o płatności, takie jak kwota, metoda płatności oraz status transakcji.

## Diagram klas
<img width="2558" height="1247" alt="image" src="https://github.com/user-attachments/assets/cfbaed1b-a8cc-4f51-89ab-ff0b21197ec8" />

### Komentarz
Centralnym pojęciem w rozpatrywanej dziedzinie jest zamówienie. Każde zamówienie jest składane przez konkretnego klienta, zatem w przypadku częstego korzystania z systemu, przypisana do klienta historia może zawierać wiele zamówień (relacja jeden-do-wielu od strony klienta do zamówienia). Zamówienie jest zawsze skierowane do konkretnej restauracji lub sklepu (dostawcy), przy czym dany dostawca realizuje w systemie wiele zamówień (relacja jeden-do-wielu od restauracji do zamówienia).

W ramach zamówienia rejestrowane są wybrane przez klienta produkty, co tworzy listę pozycji zamówienia (relacja jeden-do-wielu od zamówienia do pozycji zamówienia). Każda taka pozycja precyzuje wybrany produkt, jego zamawianą ilość, zamrożoną cenę oraz ewentualne uwagi (relacja jeden-do-wielu od produktu do pozycji). Produkty są przypisane do kartoteki konkretnej restauracji lub sklepu, która oferuje ich wiele (relacja jeden-do-wielu od restauracji do produktu). W przypadku restauracji produkt może dodatkowo posiadać zdefiniowane warianty (relacja jeden-do-wielu od produktu do wariantu).

Użytkownikiem zamawiającym jest klient, który posiada w systemie własną kartotekę z danymi osobowymi i kontaktowymi. Klient musi posiadać utworzone konto dostępowe (relacja jeden-do-jednego między kontem a klientem). W systemie klient może zdefiniować więcej niż jeden adres dostawy (relacja jeden-do-wielu od klienta do adresu), natomiast każde konkretne zamówienie jest powiązane z dokładnie jednym, wybranym adresem (relacja jeden-do-wielu od adresu do zamówienia).

Za fizyczną realizację procesu dostarczenia odpowiada kurier. Kurier posiada własną kartotekę określającą jego dostępność i dane kontaktowe. Może on mieć przypisanych wiele zamówień do doręczenia w ramach swojej historii pracy (relacja jeden-do-wielu od kuriera do zamówienia), przy czym konkretne zamówienie może być w danej chwili obsługiwane najwyżej przez jednego kuriera, który jest do niego przypisywany na podstawie lokalizacji (relacja zero-lub-jeden-do-wielu, gdyż nowo złożone zamówienie może jeszcze nie mieć przypisanego kuriera).

Dodatkowo, proces finalizuje płatność. Każde zamówienie posiada powiązaną ze sobą transakcję płatniczą, określającą kwotę, status oraz metodę – online lub przy odbiorze (relacja jeden-do-jednego pomiędzy zamówieniem a płatnością). Zarządzaniem całokształtem danych, w tym dodawaniem nowych kartotek restauracji i sklepów oraz ich asortymentu, zajmuje się przypisany administrator systemu.

## Diagram przypadków użycia
<img width="493" height="1131" alt="image" src="https://github.com/user-attachments/assets/faa830de-c21f-45af-a901-c808b99d7d25" />

