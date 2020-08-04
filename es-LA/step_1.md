- Sustituir caracteres individuales con regex es bastante sencillo, al usar el módulo `re` en Python.

    ```python
    import re
    text = 'cat'
    text = re.sub(r'c', 'b', text)
    ```

- Esto convertirá `cat` en `bat`.

- Sin embargo, es posible que a veces quieras sustituir más de un tipo de carácter. Por ejemplo, tal vez quieras cambiar todas las palabras `grey` mencionadas por `black`, pero se sabe que los norteamericanos escriben esta palabra como `gray`. Por lo tanto, tienes que hacer coincidir ambas formas de escritura. Para hacer esto, puedes buscar `[ae]`, esto hará que coincida con las letras `a` y `e`.

    ```python
    import re
    text = 'The walls were grey. The walls were gray'
    text = re.sub(r'gr[ae]y', 'white', text)
    ```

- Esto convertirá `text` en lo siguiente:

  ```python
  The walls were white. The walls were white
  ```
