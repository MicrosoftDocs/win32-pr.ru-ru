---
title: Клоседкаптион. Самистиле
description: Свойство Самистиле указывает или получает стиль закрытых субтитров.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- клоседкаптион. самистиле проигрыватель Windows Media
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4a12671877cf0d4d8abdb77d169b0f13000bc564e6c1dc37e65bf6eccdf005
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580769"
---
# <a name="closedcaptionsamistyle"></a>Клоседкаптион. Самистиле

Свойство **самистиле** указывает или получает стиль закрытых субтитров.

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Файл SAMI может содержать несколько определений стиля формата. Стили SAMI определены между тегами <STYLE> и </STYLE> в файле Sami. Стиль определяется с помощью текстовой строки, предшествующей \# символу. Пример:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



Указывает стиль, создающий определенный шрифт.

Если параметр SAMI не указан, по умолчанию используется первый стиль, определенный в файле SAMI.

**проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

в следующем примере JScript создается HTML-элемент SELECT, использующий *клоседкаптион*. **Самистиле** для изменения внешнего вида текста закрытого заголовка. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> </dl>

 

 





