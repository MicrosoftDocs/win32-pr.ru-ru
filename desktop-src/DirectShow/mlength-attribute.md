---
description: Атрибут мленгс задает длительность исходного файла. Это значение должно быть фактической длительностью, или могут возникать ошибки отрисовки.
ms.assetid: f33ce85c-df61-4248-8dea-677162fa1a07
title: Атрибут мленгс
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35eadc288e29d99df0e6af7f06e1404d86f6a938
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103989883"
---
# <a name="mlength-attribute"></a><span data-ttu-id="77658-104">Атрибут мленгс</span><span class="sxs-lookup"><span data-stu-id="77658-104">mlength Attribute</span></span>

> [!Note]  
> <span data-ttu-id="77658-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="77658-105">\[Deprecated.</span></span> <span data-ttu-id="77658-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="77658-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="77658-107">`mlength`Атрибут задает длительность исходного файла.</span><span class="sxs-lookup"><span data-stu-id="77658-107">The `mlength` attribute specifies the duration of a source file.</span></span> <span data-ttu-id="77658-108">Это значение должно быть фактической длительностью, или могут возникать ошибки отрисовки.</span><span class="sxs-lookup"><span data-stu-id="77658-108">This value must be the actual duration, or rendering errors may occur.</span></span>

## <a name="applies-to"></a><span data-ttu-id="77658-109">Применение</span><span class="sxs-lookup"><span data-stu-id="77658-109">Applies To</span></span>

[<span data-ttu-id="77658-110">**clip**</span><span class="sxs-lookup"><span data-stu-id="77658-110">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="77658-111">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="77658-111">Possible Values</span></span>

<span data-ttu-id="77658-112">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="77658-112">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="77658-113">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="77658-113">Example: 1:04:30.512.</span></span> <span data-ttu-id="77658-114">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="77658-114">Leading units can be omitted.</span></span> <span data-ttu-id="77658-115">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="77658-115">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="77658-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="77658-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77658-117">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="77658-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="77658-118">**Иамтимелинесрк:: Сетмедиаленгс**</span><span class="sxs-lookup"><span data-stu-id="77658-118">**IAMTimelineSrc::SetMediaLength**</span></span>](iamtimelinesrc-setmedialength.md)
</dt> </dl>

 

 



