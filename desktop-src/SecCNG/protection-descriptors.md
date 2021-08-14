---
description: Строка правила дескриптора защиты содержит последовательный список одного или нескольких предохранителей.
ms.assetid: FBFE2143-DC40-40F3-83CE-E6D8841F9C11
title: Дескрипторы защиты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e99d4ec8de08ad2f657d2b3ac1992ce6e399ede277f8fde3e12f0732571b01a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907256"
---
# <a name="protection-descriptors"></a>Дескрипторы защиты

Строка правила дескриптора защиты содержит последовательный список одного или нескольких предохранителей. Должен быть хотя бы один предохранитель. Если имеется более одного, то предохранители должны быть разделены в строке с помощью **и** или **или**. Эти значения должны быть прописными. Следующий синтаксис показывает формат строки дескриптора защиты.


```C++
Descriptor = [ Protector-or
              *( OR-separator Protector-or ) ]

    Protector-or = Protector-and
              *( AND-separator Protector-and )

    OR-separator = "OR"
    AND-separator = "AND"

    Protector-and = providerName EQUALS providerAttributes

    providerName = descr

    providerAttribute = string | hexstring

      ; The following characters are to be escaped when they appear
      ; in the value to be encoded: ESC, one of <escaped>, leading
      ; SHARP or SPACE, trailing SPACE, and NULL.
      string =   [ ( leadchar / pair ) [ *( stringchar / pair )
         ( trailchar / pair ) ] ]

      leadchar = LUTF1 / UTFMB
      LUTF1 = %x01-1F / %x21 / %x24-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      trailchar  = TUTF1 / UTFMB
      TUTF1 = %x01-1F / %x21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      stringchar = SUTF1 / UTFMB
      SUTF1 = %x01-21 / %x23-2A / %x2D-3A / %x3D / %x3F-5B / %x5D-7F

      pair = ESC ( ESC / special / hexpair )
      special = escaped / SPACE / SHARP / EQUALS
      escaped = DQUOTE / PLUS / COMMA / SEMI / LANGLE / RANGLE
      hexstring = SHARP 1*hexpair
      hexpair = HEX HEX

      descr   = leadkeychar *keychar
      leadkeychar = ALPHA
      keychar = ALPHA / DIGIT / HYPHEN
      number  = DIGIT / ( LDIGIT 1*DIGIT )

      ALPHA   = %x41-5A / %x61-7A   ; "A"-"Z" / "a"-"z"
      DIGIT   = %x30 / LDIGIT       ; "0"-"9"
      LDIGIT  = %x31-39             ; "1"-"9"
      HEX     = DIGIT / %x41-46 / %x61-66 ; "0"-"9" / "A"-"F" / "a"-"f"

      NULL    = %x00 ; null (0)
      SPACE   = %x20 ; space (" ")
      DQUOTE  = %x22 ; quote (""")
      SHARP   = %x23 ; octothorpe (or sharp sign) ("#")
      DOLLAR  = %x24 ; dollar sign ("$")
      SQUOTE  = %x27 ; single quote ("'")
      LPAREN  = %x28 ; left paren ("(")
      RPAREN  = %x29 ; right paren (")")
      PLUS    = %x2B ; plus sign ("+")
      COMMA   = %x2C ; comma (",")
      HYPHEN  = %x2D ; hyphen ("-")
      DOT     = %x2E ; period (".")
      SEMI    = %x3B ; semicolon (";")
      LANGLE  = %x3C ; left angle bracket ("<")
      EQUALS  = %x3D ; equals sign ("=")
      RANGLE  = %x3E ; right angle bracket (">")
      ESC     = %x5C ; backslash ("\")
      USCORE  = %x5F ; underscore ("_")
      LCURLY  = %x7B ; left curly brace "{"
      RCURLY  = %x7D ; right curly brace "}"

      ; Any UTF-8 [RFC3629] encoded Unicode [Unicode] character
      UTF8    = UTF1 / UTFMB
      UTFMB   = UTF2 / UTF3 / UTF4
      UTF0    = %x80-BF
      UTF1    = %x00-7F
      UTF2    = %xC2-DF UTF0
      UTF3    = %xE0 %xA0-BF UTF0 / %xE1-EC 2(UTF0) /
                %xED %x80-9F UTF0 / %xEE-EF 2(UTF0)
      UTF4    = %xF0 %x90-BF 2(UTF0) / %xF1-F3 3(UTF0) /
                %xF4 %x80-8F 2(UTF0)

      OCTET   = %x00-FF ; Any octet (8-bit data unit)
```



Дескрипторы защиты в настоящее время можно определить для следующих типов авторизации:

-   Группа в лесу Active Directory.
-   Набор учетных данных веб-сайта.
-   Сертификат в хранилище сертификатов пользователя.

Примеры строк правил дескриптора защиты для группы Active Directory включают следующее.

-   "SID = S-1-5-21-4392301 И SID = S-1-5-21-3101812"
-   "SDDL = O:S-1-5-5-0-290724G: SYD: (A;; ККДК;;; S-1-5-5-0-290724) (A;;D C;;; WD) "
-   "Локальный = пользователь"
-   "Локальный = компьютер"

Примеры строк правил дескриптора защиты для набора веб-учетных данных включают следующее.

-   "CREDENTIALs = Мипассворднаме"
-   "CREDENTIALs = Мипассворднаме, мивеб. com"

Примеры строк правила дескриптора защиты для сертификата включают следующее.

-   "CERTIFICATE = Хашид: \_ хэш SHA1 \_ для \_ сертификата"
-   "CERTIFICATE = Цертблоб: base64String"

Указанный вами дескриптор защиты автоматически определяет, какой поставщик защиты ключей используется. Дополнительные сведения см. в разделе [поставщики защиты](protection-providers.md).

Обратите внимание, что левая часть знака равенства (=) должна быть равна **SID**, **SDDL**, **Local**, **Credential** или **Certificate**. В значениях регистр не учитывается.

При вызове функции [**нкрипткреатепротектиондескриптор**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) необходимо указать строку правила (или отображаемое имя, связанное со строкой правила). Кроме того, так как строки правил дескриптора защиты достаточно громоздки для использования и запоминаются, можно связать отображаемое имя со строкой правила и зарегистрировать оба метода с помощью функции [**нкриптрегистерпротектиондескрипторнаме**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname) . Затем можно использовать отображаемое имя в **нкрипткреатепротектиондескриптор**.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[Поставщики защиты](protection-providers.md)
</dt> </dl>

 

 



