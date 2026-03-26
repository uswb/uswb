# System obsługi zamówień z dostawą

## Brudnopis
https://docs.google.com/document/d/1_yS38bcsTMefnQcKZWZIMeikfWNOddROzf7ziSlS2r8/edit?usp=sharing

## Opis wymagań
System umożliwia składanie zamówień przez klientów na produkty oferowane przez restauracje i sklepy, a następnie obsługę procesu ich realizacji i dostawy przez kurierów. Każde zamówienie jest przypisywane do konkretnego klienta oraz restauracji/sklepu. Zawiera listę wybranych produktów wraz z ich ilością, ceną oraz ewentualnymi uwagami klienta.

Zamówienie rejestrowane jest w systemie z uwzględnieniem daty i czasu złożenia zamówienia, przewidywanego czasu realizacji, statusu zamówienia, form płatności oraz adresu dostawy. System umożliwia śledzenie statusu zamówienia na każdym etapie jego realizacji.

Każda restauracja/sklep posiada w systemie swoją kartotekę, w której przechowywane są informacje (nazwa, adres, godziny otwarcia, dane kontaktowe, lista oferowanych produktów). Produkty posiadają swoją nazwę, opis, kategorię, cenę oraz dostępność. W przypadku restauracji możliwe jest określenie wariantów produktu.

Klient systemu posiada swoją kartotekę zawierającą dane osobowe oraz kontaktowe (imię, nazwisko, numer telefonu, adres e-mail, adresy dostawy). Klient może posiadać wiele adresów dostawy oraz historię zamówień przechowywaną w systemie.

W procesie realizacji zamówienia udział bierze kurier, który jest odpowiedzialny za odbiór zamówienia z restauracji/sklepu oraz dostarczenie go do klienta. Każdy kurier posiada swoją kartotekę zawierającą dane identyfikacyjne, kontaktowe oraz informacje o statusie dostępności. Kurierowi przypisywane są zamówienia wraz z informacją o czasie odbioru oraz dostawy.

System umożliwia przypisanie zamówień do kurierów na podsta![Uploading Diagram_klas.svg…]()
wie ich dostępności oraz lokalizacji. Rejestrowane są czasy odbioru zamówienia z restauracji/sklepu oraz dostarczenia do klienta, co pozwala na analizę efektywności dostaw.

W przypadku pierwszego zamówienia klienta wymagane jest utworzenie konta w systemie poprzez wprowadzenie danych osobowych oraz adresowych. Natomiast w przypadku dodania nowej restauracji/sklepu, administrator systemu wprowadza jego dane oraz ofertę produktową.

System umożliwia również obsługę płatności za zamówienia, zarówno online, jak i przy odbiorze. Rejestrowane są informacje o płatności, takie jak kwota, metoda płatności oraz status transakcji.

## Diagram klas
![Diagram_klas](https://github.com/user-attachments/assets/9a7f50ac-feb2-4c2a-bd89-8f694e7889fa)


