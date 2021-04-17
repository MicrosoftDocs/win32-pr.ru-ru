---
description: В журнале Windows используются следующие глобальные уникальные идентификаторы (GUID) для идентификации пользовательских свойств для штрихов или атрибутов рисования.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: Идентификаторы GUID настраиваемых свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693478"
---
# <a name="custom-property-guids"></a>Идентификаторы GUID настраиваемых свойств

В журнале Windows используются следующие глобальные уникальные идентификаторы (GUID) для идентификации пользовательских свойств для штрихов или атрибутов рисования.

## <a name="guid_stroke_timestamp"></a>\_Метка времени штриха GUID \_


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Это структура [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , указывающая время, когда штрих был создан или добавлен в документ.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>GUID \_ Stroke \_ TIMEID


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Это структура **TIMEID** . Он позволяет поддерживать порядок штрихов в операциях вставки и удаления. Без структуры **TIMEID** метка времени для всех объектов [**интерфейса иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , вырезанных и вставленных в [коллекцию инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , будет одинаковой.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>\_маркер GUID

Это **логическое** значение, где **true**= выделение, **false**= обычный рукописный ввод. Применяется к атрибутам рисования.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>GUID \_ стиль рукописного \_ \_ шрифта

Это **логическое** значение, где **true**= полужирный рукописный ввод, **false**= обычный. Применяется к атрибутам рисования.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>\_Шрифт GUID \_ стиль \_ курсив

Это **логическое** значение, где **true**= курсивное перо, **false**= нормальный. Применяется к атрибутам рисования.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ижаурналреадер**](ijournalreader.md)
</dt> </dl>

 

 
