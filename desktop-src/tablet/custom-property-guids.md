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
# <a name="custom-property-guids"></a><span data-ttu-id="0dff4-103">Идентификаторы GUID настраиваемых свойств</span><span class="sxs-lookup"><span data-stu-id="0dff4-103">Custom Property GUIDs</span></span>

<span data-ttu-id="0dff4-104">В журнале Windows используются следующие глобальные уникальные идентификаторы (GUID) для идентификации пользовательских свойств для штрихов или атрибутов рисования.</span><span class="sxs-lookup"><span data-stu-id="0dff4-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="0dff4-105">\_Метка времени штриха GUID \_</span><span class="sxs-lookup"><span data-stu-id="0dff4-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="0dff4-106">Это структура [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) , указывающая время, когда штрих был создан или добавлен в документ.</span><span class="sxs-lookup"><span data-stu-id="0dff4-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="0dff4-107">GUID \_ Stroke \_ TIMEID</span><span class="sxs-lookup"><span data-stu-id="0dff4-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="0dff4-108">Это структура **TIMEID** .</span><span class="sxs-lookup"><span data-stu-id="0dff4-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="0dff4-109">Он позволяет поддерживать порядок штрихов в операциях вставки и удаления.</span><span class="sxs-lookup"><span data-stu-id="0dff4-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="0dff4-110">Без структуры **TIMEID** метка времени для всех объектов [**интерфейса иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , вырезанных и вставленных в [коллекцию инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , будет одинаковой.</span><span class="sxs-lookup"><span data-stu-id="0dff4-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="0dff4-111">\_маркер GUID</span><span class="sxs-lookup"><span data-stu-id="0dff4-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="0dff4-112">Это **логическое** значение, где **true**= выделение, **false**= обычный рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="0dff4-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="0dff4-113">Применяется к атрибутам рисования.</span><span class="sxs-lookup"><span data-stu-id="0dff4-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="0dff4-114">GUID \_ стиль рукописного \_ \_ шрифта</span><span class="sxs-lookup"><span data-stu-id="0dff4-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="0dff4-115">Это **логическое** значение, где **true**= полужирный рукописный ввод, **false**= обычный.</span><span class="sxs-lookup"><span data-stu-id="0dff4-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="0dff4-116">Применяется к атрибутам рисования.</span><span class="sxs-lookup"><span data-stu-id="0dff4-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="0dff4-117">\_Шрифт GUID \_ стиль \_ курсив</span><span class="sxs-lookup"><span data-stu-id="0dff4-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="0dff4-118">Это **логическое** значение, где **true**= курсивное перо, **false**= нормальный.</span><span class="sxs-lookup"><span data-stu-id="0dff4-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="0dff4-119">Применяется к атрибутам рисования.</span><span class="sxs-lookup"><span data-stu-id="0dff4-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="0dff4-120">См. также</span><span class="sxs-lookup"><span data-stu-id="0dff4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dff4-121">**Интерфейс Ижаурналреадер**</span><span class="sxs-lookup"><span data-stu-id="0dff4-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
