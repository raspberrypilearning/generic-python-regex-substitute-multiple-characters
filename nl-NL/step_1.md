- Het vervangen van afzonderlijke tekens met regex is vrij eenvoudig met behulp van de `re` module in Python.

    ```python
    import re
tekst = 'kat'
tekst = re.sub (r'k', 'r', tekst)
    ```

- Hiermee wordt `kat` naar `rat` omgezet.

- Soms wil je echter meer dat ene type karakter vervangen. Je wilt bijvoorbeeld alle vermeldingen van het woord `doei` veranderen in `dag`, maar je weet dat sommige Nederlanders het woord `doeg` gebruiken. Daarom moet je beide spelling aanpassen. Om dit te doen, kun je zoeken naar `[ig]`, wat overeenkomt met zowel de letters `i` als `g`.

    ```python
    import re
tekst = 'Bij het afscheid zeiden ze doei. Bij het afscheid zeiden ze doeg'
tekst = re.sub(r'doe[ig]', 'dag', tekst)
    ```

- Dit zal `tekst` in het volgende veranderen:

  ```python
  Bij het afscheid zeiden ze dag. Bij het afscheid zeiden ze dag
  ```
