---
description: Этот атрибут указывает, включен или отключен данный элемент управления. Большинство элементов управления отображаются серым цветом при отключении.
ms.assetid: d84b1b55-34e1-4173-b945-39a809014d55
title: Включенный атрибут элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb7c5cbbbc12353fc07cf50404a1feae1d98f1b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650645"
---
# <a name="enabled-control-attribute"></a><span data-ttu-id="1eb0c-104">Включенный атрибут элемента управления</span><span class="sxs-lookup"><span data-stu-id="1eb0c-104">Enabled Control Attribute</span></span>

<span data-ttu-id="1eb0c-105">Этот атрибут указывает, включен или отключен данный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-105">This attribute specifies if the given control is enabled or disabled.</span></span> <span data-ttu-id="1eb0c-106">Большинство элементов управления отображаются серым цветом при отключении.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-106">Most controls appear gray when disabled.</span></span>

<span data-ttu-id="1eb0c-107">Если этот бит задан, элемент управления создается как включенный.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-107">If this bit is set, the control is created as enabled.</span></span>

<span data-ttu-id="1eb0c-108">Если этот бит не задан, элемент управления создается как отключенный.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-108">If this bit is not set, the control is created as disabled.</span></span>

## <a name="valid-controls"></a><span data-ttu-id="1eb0c-109">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="1eb0c-109">Valid Controls</span></span>

<span data-ttu-id="1eb0c-110">Все элементы управления.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-110">All controls.</span></span> <span data-ttu-id="1eb0c-111">Установка этого атрибута не влияет на внешний вид некоторых элементов управления, которые не связаны со свойством, например точечными рисунками и значками.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-111">The appearance of some controls that are not associated with a property, such as Bitmaps and Icons, are unaffected by setting this attribute.</span></span>

## <a name="value"></a><span data-ttu-id="1eb0c-112">Значение</span><span class="sxs-lookup"><span data-stu-id="1eb0c-112">Value</span></span>



| <span data-ttu-id="1eb0c-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="1eb0c-113">Decimal</span></span> | <span data-ttu-id="1eb0c-114">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="1eb0c-114">Hexadecimal</span></span> | <span data-ttu-id="1eb0c-115">Константа</span><span class="sxs-lookup"><span data-stu-id="1eb0c-115">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="1eb0c-116">2</span><span class="sxs-lookup"><span data-stu-id="1eb0c-116">2</span></span>       | <span data-ttu-id="1eb0c-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="1eb0c-117">0x00000002</span></span>  | <span data-ttu-id="1eb0c-118">**мсидбконтролаттрибутесенаблед**</span><span class="sxs-lookup"><span data-stu-id="1eb0c-118">**msidbControlAttributesEnabled**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="1eb0c-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eb0c-119">Remarks</span></span>

<span data-ttu-id="1eb0c-120">Можно также использовать [таблицу таблица controlcondition](controlcondition-table.md) для отключения или включения элемента управления в соответствии со значением свойства или условного оператора.</span><span class="sxs-lookup"><span data-stu-id="1eb0c-120">You can also use the [ControlCondition table](controlcondition-table.md) to disable or enable a control according to the value of a property or conditional statement.</span></span>

<span data-ttu-id="1eb0c-121">Можно также включить или отключить элемент управления, подписавший элемент управления на [таблице ControlEvent событие](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="1eb0c-121">You can also enable or disable a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="1eb0c-122">Введите идентификатор атрибута в столбце атрибут и идентификатор события в столбце событие [таблицы таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="1eb0c-122">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="1eb0c-123">См. раздел [атрибуты элементов управления](control-attributes.md) и элемент управления, которые необходимо создать в элементах [управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="1eb0c-123">See [Control Attributes](control-attributes.md) and the control you need to create under [Controls](controls.md).</span></span>

 

 



