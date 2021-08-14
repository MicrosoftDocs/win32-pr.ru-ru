---
title: Клоседкаптион. Самиланг
description: Свойство Самиланг указывает или получает язык, отображаемый для скрытых субтитров.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- клоседкаптион. самиланг проигрыватель Windows Media
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
ms.openlocfilehash: 4c423b041601a38e81b1c4e83c34c010edb3365a4eb7e05596038fa887818ba1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342289"
---
# <a name="closedcaptionsamilang"></a>Клоседкаптион. Самиланг

Свойство **самиланг** указывает или получает язык, отображаемый для скрытых субтитров.

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** для чтения и записи.

## <a name="remarks"></a>Remarks

Файл SAMI может содержать текст для одного или нескольких языков. Языки, доступные для скрытых титров, определяются между тегами <STYLE> и </STYLE> в файле Sami. Идентификатор языка указывается с уникальной буквенно-цифровой строкой, которой предшествует точка (.). Имя, указанное для языка, может быть любой строкой. Например, для определения английского языка (США) можно использовать следующую команду:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



Если язык SAMI не указан, по умолчанию используется первый язык, определенный в файле SAMI.

Значение, передаваемое с помощью *клоседкаптион*. **Самиланг** должен соответствовать атрибуту **Name** в описателе языка.

**проигрыватель Windows Media 10 Mobile:** Это свойство доступно только для чтения и всегда возвращает пустую строку.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *клоседкаптион*. **Самиланг** в HTML-элементе SELECT для указания языка закрытого заголовка. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



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

 

 





