# 4d-macro-string-to-text
Replace deprecated variable/array declarations in legacy 4D code. 


###As a function

```
$code:=macro_replace_deprecated_types (Current method path)
```

* Example

```
C_POINTER($pointerB;$pointerA)
C_TEXT($textC)
C_BLOB($blobE)
C_TEXT($textD)
C_BLOB($blobF)
C_BOOLEAN($booleanH;$booleanG)
C_DATE($dateJ)
EXECUTE FORMULA("C_BOOLEAN($booleanW)")
C_DATE($dateI)
C_TIME($timeK)
C_TIME($timeL)
C_REAL($realM)
C_PICTURE($pictureQ)
C_LONGINT($longintO;$longintP)
C_REAL($realN)
C_PICTURE($pictureR)
_o_C_INTEGER($integerS)
C_GRAPH($graphT)
_o_C_STRING(10;$stringU)
_o_C_STRING(11;$stringV;$stringW)

$code:=macro_replace_deprecated_types (Current method path)

SET TEXT TO PASTEBOARD($code)
```

* Result

```
//%attributes = {"lang":"en"} comment added and reserved by 4D.
C_POINTER($pointerB;$pointerA)
C_TEXT($textC)
C_BLOB($blobE)
C_TEXT($textD)
C_BLOB($blobF)
C_BOOLEAN($booleanH;$booleanG)
C_DATE($dateJ)
EXECUTE FORMULA("C_BOOLEAN($booleanW)")
C_DATE($dateI)
C_TIME($timeK)
C_TIME($timeL)
C_REAL($realM)
C_PICTURE($pictureQ)
C_LONGINT($longintO;$longintP)
C_REAL($realN)
C_PICTURE($pictureR)
C_LONGINT($integerS)//_o_C_INTEGER
C_GRAPH($graphT)
C_TEXT($stringU)//_o_C_STRING(10)
C_TEXT($stringV;$stringW)//_o_C_STRING(11)

$code:=macro_replace_deprecated_types (Current method path)

SET TEXT TO PASTEBOARD($code)
```
