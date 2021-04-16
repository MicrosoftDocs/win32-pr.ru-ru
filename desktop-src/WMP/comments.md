---
title: Комментарии (Мсфидс. h)
description: Добавьте комментарии в метафайлы, следуя синтаксису язык XML (XML). Комментарии начинаются с \ 0034; --\ 0034; и заканчиваются на \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Комментарии Windows Media Player
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
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699277"
---
# <a name="comments-msfeedsh"></a>Комментарии (Мсфидс. h)

Добавьте комментарии в метафайлы, следуя синтаксису язык XML (XML). Комментарии начинаются с " &lt; !--" и заканчиваются на "-- &gt; ".

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a>Комментарии

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
| Header<br/> | <dl> <dt>Мсфидс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Справочник по элементам метафайлов Windows Media**](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





