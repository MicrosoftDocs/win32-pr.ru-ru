---
title: Состояния элементов List-View (Коммктрл. h)
description: Значение состояния элемента состоит из состояния элемента, необязательного индекса маски оверлея и необязательного индекса маски изображения состояния.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648710"
---
# <a name="list-view-item-states"></a><span data-ttu-id="0ea5f-103">Состояния элементов List-View</span><span class="sxs-lookup"><span data-stu-id="0ea5f-103">List-View Item States</span></span>

<span data-ttu-id="0ea5f-104">Значение состояния элемента состоит из состояния элемента, необязательного индекса маски оверлея и необязательного индекса маски изображения состояния.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="0ea5f-105">Состояние элемента определяет его внешний вид и функциональность.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="0ea5f-106">Состояние может быть равно нулю или иметь одно или несколько из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0ea5f-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="0ea5f-107">Константа</span><span class="sxs-lookup"><span data-stu-id="0ea5f-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="0ea5f-108">Описание</span><span class="sxs-lookup"><span data-stu-id="0ea5f-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="0ea5f-109"><dt>**\_Активация лвис**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="0ea5f-110">В настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="0ea5f-111"><dt>**ЛВИС \_ Вырезать**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="0ea5f-112">Элемент помечен для операции вырезания и вставки.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="0ea5f-113"><dt>**ЛВИС \_ дрофилитед**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="0ea5f-114">Элемент выделяется как цель перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="0ea5f-115"><dt>**ЛВИС \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="0ea5f-116">Элемент имеет фокус, поэтому он окружается стандартным прямоугольником фокуса.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="0ea5f-117">Хотя можно выбрать несколько элементов, фокус может быть только одного элемента.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="0ea5f-118"><dt>**ЛВИС \_ оверлаймаск**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="0ea5f-119">Индекс изображения оверлея элемента извлекается маской.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="0ea5f-120"><dt>**ЛВИС \_ выбрано**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="0ea5f-121">Элемент выбран.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-121">The item is selected.</span></span> <span data-ttu-id="0ea5f-122">Внешний вид выбранного элемента зависит от того, имеет ли он фокус, а также от системных цветов, используемых для выбора.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="0ea5f-123"><dt>**ЛВИС \_ статеимажемаск**</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="0ea5f-124">Индекс изображения состояния элемента извлекается маской.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="0ea5f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ea5f-125">Remarks</span></span>

<span data-ttu-id="0ea5f-126">С помощью маски **\_ оверлаймаск лвис** можно изолировать Отсчитываемый от единицы индекс изображения оверлея.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="0ea5f-127">С помощью маски **\_ статеимажемаск лвис** можно изолировать Отсчитываемый от единицы индекс изображения состояния.</span><span class="sxs-lookup"><span data-stu-id="0ea5f-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ea5f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0ea5f-128">Requirements</span></span>



| <span data-ttu-id="0ea5f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0ea5f-129">Requirement</span></span> | <span data-ttu-id="0ea5f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0ea5f-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea5f-131">Header</span><span class="sxs-lookup"><span data-stu-id="0ea5f-131">Header</span></span><br/> | <dl> <span data-ttu-id="0ea5f-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea5f-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





