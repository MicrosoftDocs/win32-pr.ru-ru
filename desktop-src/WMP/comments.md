---
title: Комментарии (Мсфидс. h)
description: Добавьте комментарии в метафайлы, следуя синтаксису язык XML (XML). Комментарии начинаются с \ 0034; --\ 0034; и заканчиваются на \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- комментарии проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fe5aaf9dde3d804bb91a1e2551636c86aa54ff2bec599bf06100ee2622b592a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135787"
---
# <a name="comments-msfeedsh"></a>Комментарии (Мсфидс. h)

Добавьте комментарии в метафайлы, следуя синтаксису язык XML (XML). Комментарии начинаются с " &lt; !--" и заканчиваются на "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Remarks

Комментарии могут находиться в любом месте за исключением содержимого элемента (между тегами Open и Close элемента,  < >). Они не являются частью символьных данных документа и игнорируются при синтаксическом анализе метафайла.

## <a name="examples"></a>Примеры


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Мсфидс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Windows Справочник по элементам метафайлов мультимедиа**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





