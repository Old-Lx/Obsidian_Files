whisper-env\Scripts\activate


Comando de ejecucion:

whisper "archivo.formato" --model turbo --language es --task transcribe --output_dir "ruta de salida" --output_format txt

```
whisper "archivo_a_transcribir.formato" --device cuda --language es --task transcribe --output_dir ".\ruta_donde_se_guardará_la_transcripción" --output_format txt
```

Se puede poner el archivo sin comillas si el nombre no tiene espacios ni caracteres raros