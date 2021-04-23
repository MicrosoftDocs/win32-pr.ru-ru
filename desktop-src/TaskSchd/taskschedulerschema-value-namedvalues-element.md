---
title: Элемент value (Намедвалуес)
description: Содержит значение, связанное с именем в паре «имя-значение».
ms.assetid: d5582b55-0b9b-4fed-a425-9d15a1a62fb7
keywords:
- планировщик задач элемента value
topic_type:
- apiref
api_name:
- Value
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afa12156a15ff399f3cbc967a5fd9c612df582b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803640"
---
# <a name="value-namedvalues-element"></a><span data-ttu-id="c1898-104">Элемент value (Намедвалуес)</span><span class="sxs-lookup"><span data-stu-id="c1898-104">Value (namedValues) Element</span></span>

<span data-ttu-id="c1898-105">Содержит значение, связанное с именем в паре «имя-значение».</span><span class="sxs-lookup"><span data-stu-id="c1898-105">Contains the value that is associated with a name in a name-value pair.</span></span>

``` syntax
<xs:element name="Value"
    type="namedValue"
    minOccurs="1"
    maxOccurs="32"
 />
```

<span data-ttu-id="c1898-106">Элемент **value** определяется сложным типом [**намедвалуес**](taskschedulerschema-namedvalues-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1898-106">The **Value** element is defined by the [**namedValues**](taskschedulerschema-namedvalues-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c1898-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c1898-107">Parent element</span></span>



| <span data-ttu-id="c1898-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="c1898-108">Element</span></span>                                                                                              | <span data-ttu-id="c1898-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c1898-109">Derived from</span></span>                                                       | <span data-ttu-id="c1898-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c1898-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1898-111">**Валуекуериес (Евенттригжертипе)**</span><span class="sxs-lookup"><span data-stu-id="c1898-111">**ValueQueries (eventTriggerType)**</span></span>](taskschedulerschema-valuequeries-eventtriggertype-element.md) | [<span data-ttu-id="c1898-112">**намедвалуес**</span><span class="sxs-lookup"><span data-stu-id="c1898-112">**namedValues**</span></span>](taskschedulerschema-namedvalues-complextype.md) | <span data-ttu-id="c1898-113">Задает коллекцию именованных запросов XPath.</span><span class="sxs-lookup"><span data-stu-id="c1898-113">Specifies a collection of named XPath queries.</span></span> <span data-ttu-id="c1898-114">Каждый запрос в коллекции применяется к последнему соответствующему XML-событию, возвращенному из запроса подписки, указанного в элементе [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c1898-114">Each query in the collection is applied to the last matching event XML that is returned from the subscription query specified in the [**Subscription**](taskschedulerschema-subscription-eventtriggertype-element.md) element.</span></span> <span data-ttu-id="c1898-115">Имя запроса можно использовать в качестве переменной в сообщении для действия ShowMessage.</span><span class="sxs-lookup"><span data-stu-id="c1898-115">The name of the query can be used as a variable in the message of a ShowMessage action.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c1898-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1898-116">Remarks</span></span>

<span data-ttu-id="c1898-117">Сведения о разработке на языке C++ см. в разделе [**свойство Value объекта итаскнамедвалуепаир**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span><span class="sxs-lookup"><span data-stu-id="c1898-117">For C++ development, see [**Value Property of ITaskNamedValuePair**](/windows/desktop/api/taskschd/nf-taskschd-itasknamedvaluepair-get_value).</span></span>

<span data-ttu-id="c1898-118">Сведения о разработке сценариев см. в разделе [**таскнамедвалуепаир. Value**](tasknamedvaluepair-value.md).</span><span class="sxs-lookup"><span data-stu-id="c1898-118">For script development, see [**TaskNamedValuePair.Value**](tasknamedvaluepair-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1898-119">Требования</span><span class="sxs-lookup"><span data-stu-id="c1898-119">Requirements</span></span>



| <span data-ttu-id="c1898-120">Требование</span><span class="sxs-lookup"><span data-stu-id="c1898-120">Requirement</span></span> | <span data-ttu-id="c1898-121">Значение</span><span class="sxs-lookup"><span data-stu-id="c1898-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c1898-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1898-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c1898-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1898-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1898-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1898-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c1898-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c1898-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





