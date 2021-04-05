---
description: Атрибут кутпоинт указывает, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание. Значение задается относительно начала перехода.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Атрибут кутпоинт
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd516bd67577906a0a06d8da692ffbd7563ce32f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140050"
---
# <a name="cutpoint-attribute"></a><span data-ttu-id="74a1e-104">Атрибут кутпоинт</span><span class="sxs-lookup"><span data-stu-id="74a1e-104">cutpoint Attribute</span></span>

> [!Note]  
> <span data-ttu-id="74a1e-105">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="74a1e-105">\[Deprecated.</span></span> <span data-ttu-id="74a1e-106">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74a1e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="74a1e-107">`cutpoint`Атрибут указывает, когда переход переходит от одного источника к другому, если переход визуализируется как вырезание.</span><span class="sxs-lookup"><span data-stu-id="74a1e-107">The `cutpoint` attribute specifies when a transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="74a1e-108">Значение задается относительно начала перехода.</span><span class="sxs-lookup"><span data-stu-id="74a1e-108">The value is relative to the start of the transition.</span></span>

## <a name="possible-values"></a><span data-ttu-id="74a1e-109">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="74a1e-109">Possible Values</span></span>

<span data-ttu-id="74a1e-110">Должен быть строкой формата *чч: мм: СС. FF* , где *чч* = ч, *мм* = минуты, *SS* = секунды и *FF* = доли секунды.</span><span class="sxs-lookup"><span data-stu-id="74a1e-110">Must be a string with the format *hh:mm:ss.ff* format, where *hh* = hours, *mm* = minutes, *ss* = seconds, and *ff* = fractions of seconds.</span></span> <span data-ttu-id="74a1e-111">Пример: 1:04:30.512.</span><span class="sxs-lookup"><span data-stu-id="74a1e-111">Example: 1:04:30.512.</span></span> <span data-ttu-id="74a1e-112">Начальные единицы можно опустить.</span><span class="sxs-lookup"><span data-stu-id="74a1e-112">Leading units can be omitted.</span></span> <span data-ttu-id="74a1e-113">Например, допустимыми являются 3:00 (три минуты) и 45 (45 секунд).</span><span class="sxs-lookup"><span data-stu-id="74a1e-113">For example, 3:00 (three minutes) and 45 (45 seconds) are both valid.</span></span>

## <a name="applies-to"></a><span data-ttu-id="74a1e-114">Применение</span><span class="sxs-lookup"><span data-stu-id="74a1e-114">Applies To</span></span>

[<span data-ttu-id="74a1e-115">**режима**</span><span class="sxs-lookup"><span data-stu-id="74a1e-115">**transition**</span></span>](transition-element.md)

## <a name="see-also"></a><span data-ttu-id="74a1e-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74a1e-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a1e-117">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="74a1e-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="74a1e-118">**Иамтимелинетранс:: Сеткутпоинт**</span><span class="sxs-lookup"><span data-stu-id="74a1e-118">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



