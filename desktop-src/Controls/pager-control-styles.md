---
title: Стили элементов управления страничного навигатора (Коммктрл. h)
description: В этом разделе перечислены стили окон, используемые при создании элементов управления страничного навигатора.
ms.assetid: 619fd8cc-e231-41af-8744-a29d14f2c6f8
topic_type:
- apiref
api_name:
- PGS_AUTOSCROLL
- PGS_DRAGNDROP
- PGS_HORZ
- PGS_VERT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496737f714ecb58c0d5a349207114cbf338e2c54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648709"
---
# <a name="pager-control-styles"></a><span data-ttu-id="1fbb7-103">Стили элементов управления страничного навигатора</span><span class="sxs-lookup"><span data-stu-id="1fbb7-103">Pager Control Styles</span></span>

<span data-ttu-id="1fbb7-104">В этом разделе перечислены стили окон, используемые при создании элементов управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-104">This section lists the window styles used when creating pager controls.</span></span>



| <span data-ttu-id="1fbb7-105">Константа</span><span class="sxs-lookup"><span data-stu-id="1fbb7-105">Constant</span></span>                                                                                                                                                         | <span data-ttu-id="1fbb7-106">Описание</span><span class="sxs-lookup"><span data-stu-id="1fbb7-106">Description</span></span>                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGS_AUTOSCROLL"></span><span id="pgs_autoscroll"></span><dl> <span data-ttu-id="1fbb7-107"><dt>**\_Автоматическая ПРОкрутка ПГС**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbb7-107"><dt>**PGS\_AUTOSCROLL**</dt></span></span> </dl> | <span data-ttu-id="1fbb7-108">Элемент управления страничный навигатор будет прокручиваться, когда пользователь наводит указатель мыши на одну из кнопок прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-108">The pager control will scroll when the user hovers the mouse over one of the scroll buttons.</span></span><br/>                                                                                                                     |
| <span id="PGS_DRAGNDROP"></span><span id="pgs_dragndrop"></span><dl> <span data-ttu-id="1fbb7-109"><dt>**ПГС \_ драгндроп**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbb7-109"><dt>**PGS\_DRAGNDROP**</dt></span></span> </dl>    | <span data-ttu-id="1fbb7-110">Вложенное окно может быть целью перетаскивания.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-110">The contained window can be a drag-and-drop target.</span></span> <span data-ttu-id="1fbb7-111">Элемент управления страничного навигатора будет автоматически прокручиваться при перетаскивании элемента за пределы пейджера по одной из кнопок прокрутки.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-111">The pager control will automatically scroll if an item is dragged from outside the pager over one of the scroll buttons.</span></span><br/>                                     |
| <span id="PGS_HORZ"></span><span id="pgs_horz"></span><dl> <span data-ttu-id="1fbb7-112"><dt>**ПГС \_ горизонтали**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbb7-112"><dt>**PGS\_HORZ**</dt></span></span> </dl>                   | <span data-ttu-id="1fbb7-113">Создает элемент управления страничного навигатора, который можно прокручивать по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-113">Creates a pager control that can be scrolled horizontally.</span></span> <span data-ttu-id="1fbb7-114">Этот стиль и стиль **ПГС по \_ вертикали** являются взаимоисключающими и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-114">This style and the **PGS\_VERT** style are mutually exclusive and cannot be combined.</span></span><br/>                                                                 |
| <span id="PGS_VERT"></span><span id="pgs_vert"></span><dl> <span data-ttu-id="1fbb7-115"><dt>**ПГС по \_ вертикали**</dt></span><span class="sxs-lookup"><span data-stu-id="1fbb7-115"><dt>**PGS\_VERT**</dt></span></span> </dl>                   | <span data-ttu-id="1fbb7-116">Создает элемент управления страничного навигатора, который может быть вертикально прокручиваться.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-116">Creates a pager control that can be scrolled vertically.</span></span> <span data-ttu-id="1fbb7-117">Это направление по умолчанию, если не указан стиль направления.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-117">This is the default direction if no direction style is specified.</span></span> <span data-ttu-id="1fbb7-118">Этот стиль и стиль **ПГС \_ горизонтали** являются взаимоисключающими и не могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="1fbb7-118">This style and the **PGS\_HORZ** style are mutually exclusive and cannot be combined.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1fbb7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1fbb7-119">Requirements</span></span>



| <span data-ttu-id="1fbb7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1fbb7-120">Requirement</span></span> | <span data-ttu-id="1fbb7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1fbb7-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1fbb7-122">Header</span><span class="sxs-lookup"><span data-stu-id="1fbb7-122">Header</span></span><br/> | <dl> <span data-ttu-id="1fbb7-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fbb7-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





