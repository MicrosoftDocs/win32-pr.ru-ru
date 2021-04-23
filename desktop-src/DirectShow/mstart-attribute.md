---
description: Атрибут мстарт указывает время начала клипа относительно исходного файла мультимедиа.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Атрибут мстарт
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb637dd0c5f924a593370ceb0fb205adf5d589ea
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494322"
---
# <a name="mstart-attribute"></a><span data-ttu-id="c067a-103">Атрибут мстарт</span><span class="sxs-lookup"><span data-stu-id="c067a-103">mstart Attribute</span></span>

> [!Note]  
> <span data-ttu-id="c067a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="c067a-104">\[Deprecated.</span></span> <span data-ttu-id="c067a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c067a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c067a-106">`mstart`Атрибут задает время начала клипа относительно исходного файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c067a-106">The `mstart` attribute specifies the start time of a clip, relative to the original media file.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c067a-107">Применение</span><span class="sxs-lookup"><span data-stu-id="c067a-107">Applies To</span></span>

[<span data-ttu-id="c067a-108">**clip**</span><span class="sxs-lookup"><span data-stu-id="c067a-108">**clip**</span></span>](clip-element.md)

## <a name="possible-values"></a><span data-ttu-id="c067a-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c067a-109">Possible Values</span></span>

<span data-ttu-id="c067a-110">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="c067a-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="c067a-111">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="c067a-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="c067a-112">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="c067a-112">Leading units can be omitted.</span></span> <span data-ttu-id="c067a-113">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="c067a-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="see-also"></a><span data-ttu-id="c067a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c067a-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c067a-115">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="c067a-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="c067a-116">**Иамтимелинесрк:: Сетмедиатимес**</span><span class="sxs-lookup"><span data-stu-id="c067a-116">**IAMTimelineSrc::SetMediaTimes**</span></span>](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



