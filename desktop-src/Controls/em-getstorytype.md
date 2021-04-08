---
title: Сообщение EM_GETSTORYTYPE (RichEdit. h)
description: Возвращает тип истории.
ms.assetid: 06D87AA1-5AA3-4235-AC1D-045CE9975384
keywords:
- Элементы управления Windows для EM_GETSTORYTYPE сообщений
topic_type:
- apiref
api_name:
- EM_GETSTORYTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fed85183f292bd1c69e3bbebdadb4b38f9f3bdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891837"
---
# <a name="em_getstorytype-message"></a><span data-ttu-id="f6a26-104">\_Сообщение ЖЕТСТОРИТИПЕ EM</span><span class="sxs-lookup"><span data-stu-id="f6a26-104">EM\_GETSTORYTYPE message</span></span>

<span data-ttu-id="f6a26-105">Возвращает тип истории.</span><span class="sxs-lookup"><span data-stu-id="f6a26-105">Gets the story type.</span></span>


```C++
#define EM_GETSTORYTYPE       (WM_USER + 290)
```



## <a name="parameters"></a><span data-ttu-id="f6a26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6a26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6a26-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f6a26-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a26-108">Индекс истории.</span><span class="sxs-lookup"><span data-stu-id="f6a26-108">The story index.</span></span>

</dd> <dt>

<span data-ttu-id="f6a26-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f6a26-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f6a26-110">Процессу значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="f6a26-110">Reserved; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6a26-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6a26-111">Return value</span></span>

<span data-ttu-id="f6a26-112">Возвращает тип истории, который может быть определяемым клиентом пользовательским значением или одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="f6a26-112">Returns the story type, which can be a client-defined custom value, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="f6a26-113">**[**томкомментсстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-113">**[**tomCommentsStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-114">**[**томенднотесстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-114">**[**tomEndnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-115">**[**томевенпажесфутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-115">**[**tomEvenPagesFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-116">**[**томевенпажешеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-116">**[**tomEvenPagesHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-117">**[**томфиндстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-117">**[**tomFindStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-118">**[**томфирстпажефутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-118">**[**tomFirstPageFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-119">**[**томфирстпажехеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-119">**[**tomFirstPageHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-120">**[**томфутнотесстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-120">**[**tomFootnotesStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-121">**[**томмаинтекстстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-121">**[**tomMainTextStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-122">**[**томпримарифутерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-122">**[**tomPrimaryFooterStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-123">**[**томпримарихеадерстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-123">**[**tomPrimaryHeaderStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-124">**[**томреплацестори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-124">**[**tomReplaceStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-125">**[**томскратчстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-125">**[**tomScratchStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-126">**[**томтекстфраместори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-126">**[**tomTextFrameStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> <dt>

<span data-ttu-id="f6a26-127">**[**томункновнстори**](/windows/win32/api/tom/ne-tom-tomconstants)**</span><span class="sxs-lookup"><span data-stu-id="f6a26-127">**[**tomUnknownStory**](/windows/win32/api/tom/ne-tom-tomconstants)**</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f6a26-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f6a26-128">Requirements</span></span>



| <span data-ttu-id="f6a26-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f6a26-129">Requirement</span></span> | <span data-ttu-id="f6a26-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f6a26-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a26-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f6a26-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f6a26-132">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f6a26-132">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f6a26-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f6a26-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f6a26-134">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f6a26-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f6a26-135">Header</span><span class="sxs-lookup"><span data-stu-id="f6a26-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6a26-136"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6a26-136"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6a26-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6a26-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6a26-138">**EM \_ сетсторитипе**</span><span class="sxs-lookup"><span data-stu-id="f6a26-138">**EM\_SETSTORYTYPE**</span></span>](em-setstorytype.md)
</dt> <dt>

[<span data-ttu-id="f6a26-139">**Итекстсториранжес:: Item**</span><span class="sxs-lookup"><span data-stu-id="f6a26-139">**ITextStoryRanges::Item**</span></span>](/windows/desktop/api/Tom/nf-tom-itextstoryranges-item)
</dt> </dl>

 

 





