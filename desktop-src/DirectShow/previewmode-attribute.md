---
description: Атрибут PreviewMode указывает режим предварительного просмотра для группы. Если значение равно TRUE, фреймы могут быть удалены во время предварительной версии. В противном случае во время предварительной версии никакие кадры не удаляются. Значение по умолчанию — TRUE.
ms.assetid: 5e4f4407-b43e-4b31-8676-1e12b6b70034
title: Атрибут PreviewMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d3b589b279a11b8ec329641ea2522a6a46dfa0e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416684"
---
# <a name="previewmode-attribute"></a><span data-ttu-id="e7c09-106">Атрибут PreviewMode</span><span class="sxs-lookup"><span data-stu-id="e7c09-106">previewmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="e7c09-107">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="e7c09-107">\[Deprecated.</span></span> <span data-ttu-id="e7c09-108">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7c09-108">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7c09-109">`previewmode`Атрибут задает режим предварительного просмотра для группы.</span><span class="sxs-lookup"><span data-stu-id="e7c09-109">The `previewmode` attribute specifies the preview mode for the group.</span></span> <span data-ttu-id="e7c09-110">Если значение равно **true**, фреймы могут быть удалены во время предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="e7c09-110">If the value is **TRUE**, frames might be dropped during preview.</span></span> <span data-ttu-id="e7c09-111">В противном случае во время предварительной версии никакие кадры не удаляются.</span><span class="sxs-lookup"><span data-stu-id="e7c09-111">Otherwise, no frames are dropped during preview.</span></span> <span data-ttu-id="e7c09-112">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="e7c09-112">The default value is **TRUE**.</span></span>

## <a name="possible-values"></a><span data-ttu-id="e7c09-113">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e7c09-113">Possible Values</span></span>

<span data-ttu-id="e7c09-114">Следующие значения определены как TRUE: y, Y, t, T, 1.</span><span class="sxs-lookup"><span data-stu-id="e7c09-114">The following values are defined as TRUE: y, Y, t, T, 1.</span></span> <span data-ttu-id="e7c09-115">Следующие значения определены как FALSE: n, N, f, F, 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="e7c09-115">The following values are defined as FALSE: n, N, f, F, 0 (zero).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e7c09-116">Применение</span><span class="sxs-lookup"><span data-stu-id="e7c09-116">Applies To</span></span>

[<span data-ttu-id="e7c09-117">**сгруппировать**</span><span class="sxs-lookup"><span data-stu-id="e7c09-117">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="e7c09-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7c09-118">Remarks</span></span>

<span data-ttu-id="e7c09-119">В параметре по умолчанию фреймы удаляются при предварительном просмотре нестандартных эффектов или переходов для синхронизации видео с аудио.</span><span class="sxs-lookup"><span data-stu-id="e7c09-119">Under the default setting, frames are dropped while previewing slow effects or transitions, to keep the video synchronized with the audio.</span></span> <span data-ttu-id="e7c09-120">В результате видео может выглядеть прерывисто.</span><span class="sxs-lookup"><span data-stu-id="e7c09-120">The video might look choppy as a result.</span></span> <span data-ttu-id="e7c09-121">Если задать для этого атрибута **значение false** , каждый кадр будет отображаться во время предварительного просмотра, что может привести к тому, что видео не будет синхронизировано с аудио.</span><span class="sxs-lookup"><span data-stu-id="e7c09-121">Setting this attribute to **FALSE** forces every frame to render during preview, possibly resulting in the video becoming out of sync with the audio.</span></span> <span data-ttu-id="e7c09-122">Фреймы никогда не удаляются при записи в файл.</span><span class="sxs-lookup"><span data-stu-id="e7c09-122">Frames are never dropped when writing to a file.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7c09-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7c09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7c09-124">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="e7c09-124">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="e7c09-125">**Иамтимелинеграуп:: Сетпревиевмоде**</span><span class="sxs-lookup"><span data-stu-id="e7c09-125">**IAMTimelineGroup::SetPreviewMode**</span></span>](iamtimelinegroup-setpreviewmode.md)
</dt> </dl>

 

 



