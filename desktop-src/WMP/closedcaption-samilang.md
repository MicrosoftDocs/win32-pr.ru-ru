---
title: Клоседкаптион. Самиланг
description: Свойство Самиланг указывает или получает язык, отображаемый для скрытых субтитров.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Проигрыватель Windows Media Клоседкаптион. Самиланг
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694873"
---
# <a name="closedcaptionsamilang"></a>Клоседкаптион. Самиланг

Свойство **самиланг** указывает или получает язык, отображаемый для скрытых субтитров.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Комментарии

Файл SAMI может содержать текст для одного или нескольких языков. Языки, доступные для скрытых титров, определяются между тегами <STYLE> и </STYLE> в файле Sami. Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.). Имя, указанное для языка, может быть любой строкой. Например, для определения английского языка (США) можно использовать следующую команду:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.

Значение, передаваемое с помощью *клоседкаптион*. **Самиланг** должен соответствовать атрибуту **Name** в описателе языка.

**Проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *клоседкаптион*. **Самиланг** в HTML-элементе SELECT для указания языка закрытого заголовка. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Добавление субтитров к цифровым носителям**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Объект Клоседкаптион**](closedcaption-object.md)
</dt> </dl>

 

 





