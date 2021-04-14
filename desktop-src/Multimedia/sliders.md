---
title: Ползунки (мультимедиа Windows)
description: Ползунки
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- аудио миксерс, элементы управления
- звуковые миксерс, ползунки
- миксерс, элементы управления
- миксерс, ползунки
- элементы управления "Ползунок"
- Структура MIXERCONTROLDETAILS_SIGNED
- элемент управления Pan
- Элемент управления Ксаунд Pan
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414505"
---
# <a name="sliders-windows-multimedia"></a><span data-ttu-id="37917-111">Ползунки (мультимедиа Windows)</span><span class="sxs-lookup"><span data-stu-id="37917-111">Sliders (Windows Multimedia)</span></span>

<span data-ttu-id="37917-112">Элементы управления "ползунок" обычно являются горизонтальными элементами управления, которые могут быть скорректированы влево или вправо.</span><span class="sxs-lookup"><span data-stu-id="37917-112">The slider controls are typically horizontal controls that can be adjusted to the left or right.</span></span> <span data-ttu-id="37917-113">Эти элементы управления используют [**\_ подписанную структуру миксерконтролдетаилс**](/previous-versions//dd757297(v=vs.85)) для извлечения и установки свойств элементов управления.</span><span class="sxs-lookup"><span data-stu-id="37917-113">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) structure to retrieve and set control properties.</span></span> <span data-ttu-id="37917-114">В следующей таблице описаны типы ползунков.</span><span class="sxs-lookup"><span data-stu-id="37917-114">The following table describes the types of sliders.</span></span>



| <span data-ttu-id="37917-115">Control</span><span class="sxs-lookup"><span data-stu-id="37917-115">Control</span></span>    | <span data-ttu-id="37917-116">Описание</span><span class="sxs-lookup"><span data-stu-id="37917-116">Description</span></span>                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37917-117">Ползунок</span><span class="sxs-lookup"><span data-stu-id="37917-117">Slider</span></span>     | <span data-ttu-id="37917-118">Имеет диапазон от – 32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="37917-118">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="37917-119">Драйвер микшера определяет ограничения этого элемента управления.</span><span class="sxs-lookup"><span data-stu-id="37917-119">The mixer driver defines the limits of this control.</span></span>                               |
| <span data-ttu-id="37917-120">Сдвиг</span><span class="sxs-lookup"><span data-stu-id="37917-120">Pan</span></span>        | <span data-ttu-id="37917-121">Имеет диапазон от – 32 768 до 32 767.</span><span class="sxs-lookup"><span data-stu-id="37917-121">Has a range of –32,768 through 32,767.</span></span> <span data-ttu-id="37917-122">Драйвер микшера определяет ограничения для этого элемента управления, значение 0 в качестве значения среднего.</span><span class="sxs-lookup"><span data-stu-id="37917-122">The mixer driver defines the limits of this control, with 0 as the midrange value.</span></span> |
| <span data-ttu-id="37917-123">Ксаунд Pan</span><span class="sxs-lookup"><span data-stu-id="37917-123">QSound Pan</span></span> | <span data-ttu-id="37917-124">Обеспечивает расширенное управление звуком с помощью Ксаунд.</span><span class="sxs-lookup"><span data-stu-id="37917-124">Provides expanded sound control through QSound.</span></span> <span data-ttu-id="37917-125">Этот элемент управления имеет диапазон от – 15 до 15.</span><span class="sxs-lookup"><span data-stu-id="37917-125">This control has a range of –15 through 15.</span></span>                               |



 

 

 
