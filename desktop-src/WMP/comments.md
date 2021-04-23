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
# <a name="comments-msfeedsh"></a><span data-ttu-id="4a305-105">Комментарии (Мсфидс. h)</span><span class="sxs-lookup"><span data-stu-id="4a305-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="4a305-106">Добавьте комментарии в метафайлы, следуя синтаксису язык XML (XML).</span><span class="sxs-lookup"><span data-stu-id="4a305-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="4a305-107">Комментарии начинаются с " &lt; !--" и заканчиваются на "-- &gt; ".</span><span class="sxs-lookup"><span data-stu-id="4a305-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="4a305-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4a305-108">Remarks</span></span>

<span data-ttu-id="4a305-109">Комментарии могут находиться в любом месте за исключением содержимого элемента (между тегами Open и Close элемента,  < >).</span><span class="sxs-lookup"><span data-stu-id="4a305-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="4a305-110">Они не являются частью символьных данных документа и игнорируются при синтаксическом анализе метафайла.</span><span class="sxs-lookup"><span data-stu-id="4a305-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="4a305-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="4a305-111">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="4a305-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4a305-112">Requirements</span></span>



| <span data-ttu-id="4a305-113">Требование</span><span class="sxs-lookup"><span data-stu-id="4a305-113">Requirement</span></span> | <span data-ttu-id="4a305-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4a305-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4a305-115">Header</span><span class="sxs-lookup"><span data-stu-id="4a305-115">Header</span></span><br/> | <dl> <span data-ttu-id="4a305-116"><dt>Мсфидс. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a305-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a305-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4a305-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a305-118">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4a305-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





