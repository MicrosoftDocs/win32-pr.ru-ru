---
title: Комхандлер (actionGroup), элемент
description: Указывает действие, которое вызывает обработчик.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- планировщик задач элемента Комхандлер
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989110"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="af877-104">Комхандлер (actionGroup), элемент</span><span class="sxs-lookup"><span data-stu-id="af877-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="af877-105">Указывает действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="af877-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="af877-106">Элемент **комхандлер** определяется параметром [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="af877-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="af877-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="af877-107">Parent element</span></span>



| <span data-ttu-id="af877-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="af877-108">Element</span></span>                                                         | <span data-ttu-id="af877-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="af877-109">Derived from</span></span>                                                       | <span data-ttu-id="af877-110">Описание</span><span class="sxs-lookup"><span data-stu-id="af877-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="af877-111">**Действия**</span><span class="sxs-lookup"><span data-stu-id="af877-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="af877-112">**актионстипе**</span><span class="sxs-lookup"><span data-stu-id="af877-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="af877-113">Содержит действия, выполняемые задачей.</span><span class="sxs-lookup"><span data-stu-id="af877-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="af877-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="af877-114">Child elements</span></span>



| <span data-ttu-id="af877-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="af877-115">Element</span></span>                                                               | <span data-ttu-id="af877-116">Тип</span><span class="sxs-lookup"><span data-stu-id="af877-116">Type</span></span>                                                         | <span data-ttu-id="af877-117">Описание</span><span class="sxs-lookup"><span data-stu-id="af877-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="af877-118">**Класса**</span><span class="sxs-lookup"><span data-stu-id="af877-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="af877-119">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="af877-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="af877-120">Задает идентификатор класса обработчика.</span><span class="sxs-lookup"><span data-stu-id="af877-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="af877-121">**Data**</span><span class="sxs-lookup"><span data-stu-id="af877-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="af877-122">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="af877-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="af877-123">Указывает дополнительные данные, связанные с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="af877-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="af877-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af877-124">Remarks</span></span>

<span data-ttu-id="af877-125">Приложения определяют действие обработчика COM с помощью интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="af877-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="af877-126">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="af877-126">Attributes</span></span>

<span data-ttu-id="af877-127">Следующий атрибут определяется сложным типом [**актионбасетипе**](taskschedulerschema-actionbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="af877-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="af877-128">Идентификатор: идентификатор действия, выполняемого задачей.</span><span class="sxs-lookup"><span data-stu-id="af877-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="af877-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="af877-129">Examples</span></span>

<span data-ttu-id="af877-130">Следующий XML-код определяет действие обработчика COM.</span><span class="sxs-lookup"><span data-stu-id="af877-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="af877-131">Требования</span><span class="sxs-lookup"><span data-stu-id="af877-131">Requirements</span></span>



| <span data-ttu-id="af877-132">Требование</span><span class="sxs-lookup"><span data-stu-id="af877-132">Requirement</span></span> | <span data-ttu-id="af877-133">Значение</span><span class="sxs-lookup"><span data-stu-id="af877-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="af877-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af877-134">Minimum supported client</span></span><br/> | <span data-ttu-id="af877-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="af877-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="af877-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af877-136">Minimum supported server</span></span><br/> | <span data-ttu-id="af877-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="af877-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="af877-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af877-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af877-139">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="af877-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





