# Encriptador y Desencriptador de Textos

## Descripción
Este proyecto permite encriptar y desencriptar textos utilizando un algoritmo de cifrado sencillo. Es útil para proteger información sensible en archivos de texto o comunicaciones.

## Características
- Encripta textos usando un algoritmo seguro.
- Desencripta textos previamente cifrados.
- Fácil de usar y personalizable.

## Instalación
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu_usuario/encriptador.git
   ```
2. Accede al directorio del proyecto:
   ```bash
   cd encriptador
   ```
3. Instala las dependencias necesarias (si las hay):
   ```bash
   pip install -r requirements.txt  # Para Python
   ```

## Uso
### Encriptar un texto
Ejecuta el script y proporciona el texto que deseas encriptar:
```bash
python encriptador.py --encrypt "Texto a encriptar"
```

### Desencriptar un texto
Ejecuta el script y proporciona el texto cifrado:
```bash
python encriptador.py --decrypt "Texto encriptado"
```

## Ejemplo de Código
```python
from cryptography.fernet import Fernet

# Generar clave (solo la primera vez)
clave = Fernet.generate_key()
cipher_suite = Fernet(clave)

# Encriptar
texto = "Hola Mundo"
cifrado = cipher_suite.encrypt(texto.encode())
print("Texto encriptado:", cifrado)

# Desencriptar
descifrado = cipher_suite.decrypt(cifrado).decode()
print("Texto desencriptado:", descifrado)
```

## Contribuciones
Las contribuciones son bienvenidas. Si deseas mejorar este proyecto, por favor envía un pull request o abre un issue.

## Licencia
Este proyecto está bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.


