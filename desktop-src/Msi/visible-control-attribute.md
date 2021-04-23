---
description: Если видимый контрольный бит установлен, элемент управления отображается в диалоговом окне. Если этот бит не установлен, элемент управления скрыт в диалоговом окне. Видимое или скрытое состояние видимого атрибута элемента управления может быть позже изменено событием элемента управления.
ms.assetid: 77d3164c-ea8a-4dcf-afd5-02bb2c2568c6
title: Атрибут видимого элемента управления
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550513f6bd0e40e58694c2c15a9986b5b02f289c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673257"
---
# <a name="visible-control-attribute"></a><span data-ttu-id="c3ab1-105">Атрибут видимого элемента управления</span><span class="sxs-lookup"><span data-stu-id="c3ab1-105">Visible Control Attribute</span></span>

<span data-ttu-id="c3ab1-106">Если видимый контрольный бит установлен, элемент управления отображается в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-106">If the Visible Control bit is set, the control is visible on the dialog box.</span></span> <span data-ttu-id="c3ab1-107">Если этот бит не установлен, элемент управления скрыт в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-107">If this bit is not set, the control is hidden on the dialog box.</span></span> <span data-ttu-id="c3ab1-108">Видимое или скрытое состояние видимого атрибута элемента управления может быть позже изменено [событием элемента управления](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-108">The visible or hidden state of the Visible control attribute can be later changed by a [Control Event](control-events.md).</span></span>

## <a name="valid-controls"></a><span data-ttu-id="c3ab1-109">Допустимые элементы управления</span><span class="sxs-lookup"><span data-stu-id="c3ab1-109">Valid Controls</span></span>

<span data-ttu-id="c3ab1-110">Все элементы управления.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-110">All controls.</span></span>

## <a name="value"></a><span data-ttu-id="c3ab1-111">Значение</span><span class="sxs-lookup"><span data-stu-id="c3ab1-111">Value</span></span>



| <span data-ttu-id="c3ab1-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="c3ab1-112">Decimal</span></span> | <span data-ttu-id="c3ab1-113">Шестнадцатеричный</span><span class="sxs-lookup"><span data-stu-id="c3ab1-113">Hexadecimal</span></span> | <span data-ttu-id="c3ab1-114">Константа</span><span class="sxs-lookup"><span data-stu-id="c3ab1-114">Constant</span></span>                          |
|---------|-------------|-----------------------------------|
| <span data-ttu-id="c3ab1-115">1</span><span class="sxs-lookup"><span data-stu-id="c3ab1-115">1</span></span>       | <span data-ttu-id="c3ab1-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3ab1-116">0x00000001</span></span>  | <span data-ttu-id="c3ab1-117">**мсидбконтролаттрибутесвисибле**</span><span class="sxs-lookup"><span data-stu-id="c3ab1-117">**msidbControlAttributesVisible**</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="c3ab1-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3ab1-118">Remarks</span></span>

<span data-ttu-id="c3ab1-119">[Таблицу таблица controlcondition](controlcondition-table.md) можно использовать для отображения или скрытия элемента управления в соответствии со значением свойства или условного оператора.</span><span class="sxs-lookup"><span data-stu-id="c3ab1-119">You can use the [ControlCondition table](controlcondition-table.md) to show or hide a control according to the value of a property or conditional statement.</span></span> <span data-ttu-id="c3ab1-120">Можно также показать или скрыть элемент управления, подписавший элемент управления на [таблице ControlEvent событие](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-120">You can also show or hide a control by subscribing the control to a [ControlEvent](control-events.md).</span></span> <span data-ttu-id="c3ab1-121">Введите идентификатор атрибута в столбце атрибут и идентификатор события в столбце событие [таблицы таблица eventmapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-121">Enter the attribute's identifier in the Attribute column and the event's identifier in the Event column of the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="c3ab1-122">См. раздел [Управление атрибутами](control-attributes.md) и [элементами управления](controls.md).</span><span class="sxs-lookup"><span data-stu-id="c3ab1-122">See [Control Attributes](control-attributes.md) and [Controls](controls.md).</span></span>

 

 



