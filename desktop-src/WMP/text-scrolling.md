---
title: TEXT. Scroll
description: Атрибут прокрутки указывает или получает значение, указывающее, прокручивается ли текст.
ms.assetid: 1cd5cb4e-673f-4273-91ff-50165c2b08fa
keywords:
- TEXT. прокрутка проигрывателя Windows Media
topic_type:
- apiref
api_name:
- TEXT.scrolling
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fdbb80b2033d542da4894172d58451ed5da224f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717929"
---
# <a name="textscrolling"></a><span data-ttu-id="eb0f3-104">TEXT. Scroll</span><span class="sxs-lookup"><span data-stu-id="eb0f3-104">TEXT.scrolling</span></span>

<span data-ttu-id="eb0f3-105">Атрибут **прокрутки** указывает или получает значение, указывающее, прокручивается ли текст.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-105">The **scrolling** attribute specifies or retrieves a value indicating whether the text scrolls.</span></span>

``` syntax
        elementID.scrolling
```

## <a name="possible-values"></a><span data-ttu-id="eb0f3-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="eb0f3-106">Possible Values</span></span>

<span data-ttu-id="eb0f3-107">Этот атрибут является **логическим значением** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="eb0f3-108">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0f3-108">Value</span></span> | <span data-ttu-id="eb0f3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="eb0f3-109">Description</span></span>                     |
|-------|---------------------------------|
| <span data-ttu-id="eb0f3-110">true</span><span class="sxs-lookup"><span data-stu-id="eb0f3-110">true</span></span>  | <span data-ttu-id="eb0f3-111">Прокрутка включена.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-111">Scrolling is enabled.</span></span>           |
| <span data-ttu-id="eb0f3-112">false</span><span class="sxs-lookup"><span data-stu-id="eb0f3-112">false</span></span> | <span data-ttu-id="eb0f3-113">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-113">Default.</span></span> <span data-ttu-id="eb0f3-114">Прокрутка отключена.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-114">Scrolling is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="eb0f3-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="eb0f3-115">Remarks</span></span>

<span data-ttu-id="eb0f3-116">Функция прокрутки предоставляет буфер с двумя пробелами между концом текста и началом повторяющейся строки.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-116">The scrolling feature provides a two-space buffer between the end of the text and the beginning of the repeated line.</span></span>

<span data-ttu-id="eb0f3-117">Атрибут « **обоснование** » определяет место первого отображения текста перед началом прокрутки.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-117">The **justification** attribute specifies where the text first appears before the scrolling begins.</span></span>

<span data-ttu-id="eb0f3-118">См. атрибут [value](text-value.md) для примера, иллюстрирующий использование атрибутов **текстового** элемента.</span><span class="sxs-lookup"><span data-stu-id="eb0f3-118">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0f3-119">Требования</span><span class="sxs-lookup"><span data-stu-id="eb0f3-119">Requirements</span></span>



| <span data-ttu-id="eb0f3-120">Требование</span><span class="sxs-lookup"><span data-stu-id="eb0f3-120">Requirement</span></span> | <span data-ttu-id="eb0f3-121">Значение</span><span class="sxs-lookup"><span data-stu-id="eb0f3-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="eb0f3-122">Версия</span><span class="sxs-lookup"><span data-stu-id="eb0f3-122">Version</span></span><br/> | <span data-ttu-id="eb0f3-123">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="eb0f3-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eb0f3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eb0f3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0f3-125">**TEXT, элемент**</span><span class="sxs-lookup"><span data-stu-id="eb0f3-125">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="eb0f3-126">**TEXT. обоснование**</span><span class="sxs-lookup"><span data-stu-id="eb0f3-126">**TEXT.justification**</span></span>](text-justification.md)
</dt> <dt>

[<span data-ttu-id="eb0f3-127">**TEXT. Скроллингамаунт**</span><span class="sxs-lookup"><span data-stu-id="eb0f3-127">**TEXT.scrollingAmount**</span></span>](text-scrollingamount.md)
</dt> <dt>

[<span data-ttu-id="eb0f3-128">**TEXT. Скроллингделай**</span><span class="sxs-lookup"><span data-stu-id="eb0f3-128">**TEXT.scrollingDelay**</span></span>](text-scrollingdelay.md)
</dt> <dt>

[<span data-ttu-id="eb0f3-129">**TEXT. Скроллингдиректион**</span><span class="sxs-lookup"><span data-stu-id="eb0f3-129">**TEXT.scrollingDirection**</span></span>](text-scrollingdirection.md)
</dt> </dl>

 

 





