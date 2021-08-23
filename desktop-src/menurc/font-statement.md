---
title: FONT, инструкция
description: Определяет шрифт, с помощью которого система будет рисовать текст в диалоговом окне. Шрифт должен быть ранее загружен; Например, путем вызова функции Лоадресаурце.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Меню инструкций шрифтов и другие ресурсы
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad289923503866ba2bcd9338bb59a556d0e37cd0a839d4eede0f95a0bec5fd76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972073"
---
# <a name="font-statement"></a>FONT, инструкция

Определяет шрифт, с помощью которого система будет рисовать текст в диалоговом окне. Шрифт должен быть ранее загружен; Например, путем вызова функции [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span id="pointsize"></span><span id="POINTSIZE"></span>*PointSize*
</dt> <dd>

Размер шрифта в пунктах.

</dd> <dt>

<span id="typeface"></span><span id="TYPEFACE"></span>*начертан*
</dt> <dd>

Имя гарнитуры. Этот параметр должен быть заключен в кавычки (").

</dd> <dt>

<span id="weight"></span><span id="WEIGHT"></span>*оценку*
</dt> <dd>

Вес шрифта в диапазоне от 0 до 1000. Например, 400 является нормальным, а 700 — полужирным. Если это значение равно 0, используется вес по умолчанию. Список предварительно определенных значений см. в разделе **значения \_ \* FW** , определенные в вингди. h.

</dd> <dt>

<span id="italic"></span><span id="ITALIC"></span>*деле*
</dt> <dd>

Обозначает курсив, если задано значение TRUE.

</dd> <dt>

<span id="charset"></span><span id="CHARSET"></span>*charset*
</dt> <dd>

Набор символов. Список значений см. в описании элемента **лфчарсет** структуры [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере показано использование оператора **Font** :

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a>См. также

<dl> <dt>

[**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 