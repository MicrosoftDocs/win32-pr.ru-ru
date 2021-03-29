---
description: Элемент управления "линия" является горизонтальной линией.
ms.assetid: 8b180b71-1e80-47c0-bb44-d5fcecabaed2
title: Line, элемент управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba3b7374574e2a0087e7dae8d0ffa9f097be9f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812863"
---
# <a name="line-control"></a><span data-ttu-id="22699-103">Line, элемент управления</span><span class="sxs-lookup"><span data-stu-id="22699-103">Line Control</span></span>

<span data-ttu-id="22699-104">Элемент управления "линия" является горизонтальной линией.</span><span class="sxs-lookup"><span data-stu-id="22699-104">The Line control is a horizontal line.</span></span>

## <a name="control-attributes"></a><span data-ttu-id="22699-105">Атрибуты элемента управления</span><span class="sxs-lookup"><span data-stu-id="22699-105">Control Attributes</span></span>

<span data-ttu-id="22699-106">С этим элементом управления можно использовать следующие атрибуты.</span><span class="sxs-lookup"><span data-stu-id="22699-106">You can use the following attributes with this control.</span></span> <span data-ttu-id="22699-107">Чтобы изменить значение атрибута с помощью события, подпишите элемент управления на таблице ControlEvent событие в [таблице таблица eventmapping](eventmapping-table.md) и перечислите идентификатор атрибута в столбце Attribute.</span><span class="sxs-lookup"><span data-stu-id="22699-107">To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column.</span></span> <span data-ttu-id="22699-108">Введите идентификатор таблице ControlEvent событие в столбце событий.</span><span class="sxs-lookup"><span data-stu-id="22699-108">Enter the identifier of the ControlEvent in the Event column.</span></span>



| <span data-ttu-id="22699-109">Идентификатор атрибута</span><span class="sxs-lookup"><span data-stu-id="22699-109">Attribute identifier</span></span>                       | <span data-ttu-id="22699-110">Шестнадцатеричный бит</span><span class="sxs-lookup"><span data-stu-id="22699-110">Hexadecimal bit</span></span>                  | <span data-ttu-id="22699-111">Описание</span><span class="sxs-lookup"><span data-stu-id="22699-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22699-112">Позиция</span><span class="sxs-lookup"><span data-stu-id="22699-112">Position</span></span>](position-control-attribute.md) |                                  | <span data-ttu-id="22699-113">Расположение элемента управления в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="22699-113">Position of the control in the dialog box.</span></span> <span data-ttu-id="22699-114">Введите ширину элемента управления, высоту и координаты левого угла элемента управления в столбцах ширина, высота, X и Y [таблицы управления](control-table.md) или [таблицы ббконтрол](bbcontrol-table.md).</span><span class="sxs-lookup"><span data-stu-id="22699-114">Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md).</span></span> <span data-ttu-id="22699-115">Используйте [единицы установщика](installer-units.md) для длины и расстояния.</span><span class="sxs-lookup"><span data-stu-id="22699-115">Use [installer units](installer-units.md) for length and distance.</span></span><br/>                                         |
| [<span data-ttu-id="22699-116">Visible</span><span class="sxs-lookup"><span data-stu-id="22699-116">Visible</span></span>](visible-control-attribute.md)   | <span data-ttu-id="22699-117">0x00000000 0x00000001</span><span class="sxs-lookup"><span data-stu-id="22699-117">0x00000000 0x00000001</span></span><br/> | <span data-ttu-id="22699-118">Скрытый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="22699-118">Hidden control.</span></span> <span data-ttu-id="22699-119">Видимый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="22699-119">Visible control.</span></span><br/> <span data-ttu-id="22699-120">Включите этот бит в битовое слово столбца Attributes [таблицы Control](control-table.md) или [ббконтрол](bbcontrol-table.md) , чтобы сделать элемент управления видимым или скрытым при его создании.</span><span class="sxs-lookup"><span data-stu-id="22699-120">Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) to make the control visible or hidden upon its creation.</span></span><br/> <span data-ttu-id="22699-121">Можно также скрыть или показать элемент управления с помощью [таблицы таблица controlcondition](controlcondition-table.md).</span><span class="sxs-lookup"><span data-stu-id="22699-121">You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).</span></span><br/> |
| [<span data-ttu-id="22699-122">Sunken</span><span class="sxs-lookup"><span data-stu-id="22699-122">Sunken</span></span>](sunken-control-attribute.md)     | <span data-ttu-id="22699-123">0x00000000 0x00000004</span><span class="sxs-lookup"><span data-stu-id="22699-123">0x00000000 0x00000004</span></span><br/> | <span data-ttu-id="22699-124">Отображает стиль оформления по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="22699-124">Displays the default visual style.</span></span> <span data-ttu-id="22699-125">Отображает элемент управления с утопленным, трехмерным представлением.</span><span class="sxs-lookup"><span data-stu-id="22699-125">Displays the control with a sunken, 3-D look.</span></span><br/> <span data-ttu-id="22699-126">Включите эти биты в битовое слово в столбец Attributes [таблицы Control](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="22699-126">Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="22699-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22699-127">Remarks</span></span>

<span data-ttu-id="22699-128">Этот элемент управления можно создать из статического класса с помощью функции [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .</span><span class="sxs-lookup"><span data-stu-id="22699-128">This control can be created from the STATIC class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="22699-129">У него есть стили **SS \_ Етчедхорз** и **СС \_** .</span><span class="sxs-lookup"><span data-stu-id="22699-129">It has the **SS\_ETCHEDHORZ** and **SS\_SUNKEN** styles.</span></span>

 

 
