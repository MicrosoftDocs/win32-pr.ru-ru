---
title: Интерфейс IDWriteTextLayout2
description: Представляет блок текста после полного анализа и форматирования. | Интерфейс IDWriteTextLayout2
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- Непосредственная запись интерфейса IDWriteTextLayout2
- Непосредственная запись интерфейса IDWriteTextLayout2, описание
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353282"
---
# <a name="idwritetextlayout2-interface"></a><span data-ttu-id="5d8c4-106">Интерфейс IDWriteTextLayout2</span><span class="sxs-lookup"><span data-stu-id="5d8c4-106">IDWriteTextLayout2 interface</span></span>

<span data-ttu-id="5d8c4-107">Представляет блок текста после полного анализа и форматирования.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-107">Represents a block of text after it has been fully analyzed and formatted.</span></span>

## <a name="members"></a><span data-ttu-id="5d8c4-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="5d8c4-108">Members</span></span>

<span data-ttu-id="5d8c4-109">Интерфейс **IDWriteTextLayout2** наследует от [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span><span class="sxs-lookup"><span data-stu-id="5d8c4-109">The **IDWriteTextLayout2** interface inherits from [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1).</span></span> <span data-ttu-id="5d8c4-110">**IDWriteTextLayout2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d8c4-110">**IDWriteTextLayout2** also has these types of members:</span></span>

-   [<span data-ttu-id="5d8c4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5d8c4-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d8c4-112">Методы</span><span class="sxs-lookup"><span data-stu-id="5d8c4-112">Methods</span></span>

<span data-ttu-id="5d8c4-113">Интерфейс **IDWriteTextLayout2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-113">The **IDWriteTextLayout2** interface has these methods.</span></span>



| <span data-ttu-id="5d8c4-114">Метод</span><span class="sxs-lookup"><span data-stu-id="5d8c4-114">Method</span></span>                                                                                | <span data-ttu-id="5d8c4-115">Описание</span><span class="sxs-lookup"><span data-stu-id="5d8c4-115">Description</span></span>                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d8c4-116">**жетфонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-116">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | <span data-ttu-id="5d8c4-117">Возвращает текущий объект отката шрифта.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-117">Get the current font fallback object.</span></span> <br/>                                           |
| [<span data-ttu-id="5d8c4-118">**жетластлиневраппинг**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-118">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | <span data-ttu-id="5d8c4-119">Возвращает значение, указывающее, упаковано ли Последнее слово в последней строке.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-119">Get whether or not the last word on the last line is wrapped.</span></span><br/>                    |
| [<span data-ttu-id="5d8c4-120">**Метрики**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-120">**GetMetrics**</span></span>](idwritetextlayout2-getmetrics.md)                                   | <span data-ttu-id="5d8c4-121">Получает общие метрики для форматированной строки.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-121">Retrieves overall metrics for the formatted string.</span></span> <br/>                             |
| [<span data-ttu-id="5d8c4-122">**жетоптикалалигнмент**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | <span data-ttu-id="5d8c4-123">Узнайте, как глифы выровняйте по краям поля.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-123">Get how the glyphs align to the edges the margin.</span></span> <br/>                               |
| [<span data-ttu-id="5d8c4-124">**жетвертикалглифориентатион**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | <span data-ttu-id="5d8c4-125">Получение предпочтительной ориентации глифов при использовании направления чтения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |
| [<span data-ttu-id="5d8c4-126">**сетфонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | <span data-ttu-id="5d8c4-127">Применение настраиваемого резервного шрифта на макете.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-127">Apply a custom font fallback onto layout.</span></span><br/>                                        |
| [<span data-ttu-id="5d8c4-128">**сетластлиневраппинг**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-128">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | <span data-ttu-id="5d8c4-129">Задает, упаковано ли Последнее слово в последней строке.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-129">Set whether or not the last word on the last line is wrapped.</span></span> <br/>                   |
| [<span data-ttu-id="5d8c4-130">**сетоптикалалигнмент**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-130">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | <span data-ttu-id="5d8c4-131">Укажите, как глифы выдаются по краям поля.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-131">Set how the glyphs align to the edges the margin.</span></span><br/>                                |
| [<span data-ttu-id="5d8c4-132">**сетвертикалглифориентатион**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-132">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | <span data-ttu-id="5d8c4-133">Задает предпочтительную ориентацию глифов при использовании направления чтения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="5d8c4-133">Set the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5d8c4-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5d8c4-134">Requirements</span></span>



| <span data-ttu-id="5d8c4-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5d8c4-135">Requirement</span></span> | <span data-ttu-id="5d8c4-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5d8c4-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d8c4-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d8c4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5d8c4-138">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="5d8c4-138">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5d8c4-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d8c4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5d8c4-140">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="5d8c4-140">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5d8c4-141">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="5d8c4-141">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5d8c4-142">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="5d8c4-142">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="5d8c4-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="5d8c4-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d8c4-144"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d8c4-144"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5d8c4-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5d8c4-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d8c4-146"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d8c4-146"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5d8c4-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d8c4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d8c4-148">**IDWriteTextLayout1**</span><span class="sxs-lookup"><span data-stu-id="5d8c4-148">**IDWriteTextLayout1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

