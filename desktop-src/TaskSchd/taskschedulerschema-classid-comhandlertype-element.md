---
title: Элемент ClassId (Комхандлертипе)
description: Задает идентификатор класса обработчика.
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- планировщик задач элемента ClassId
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493131"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="4cac4-104">Элемент ClassId (Комхандлертипе)</span><span class="sxs-lookup"><span data-stu-id="4cac4-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="4cac4-105">Задает идентификатор класса обработчика.</span><span class="sxs-lookup"><span data-stu-id="4cac4-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="4cac4-106">Элемент **ClassID** определяется сложным типом [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4cac4-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4cac4-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4cac4-107">Parent element</span></span>



| <span data-ttu-id="4cac4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4cac4-108">Element</span></span>                                                                  | <span data-ttu-id="4cac4-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4cac4-109">Derived from</span></span>                                                             | <span data-ttu-id="4cac4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4cac4-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="4cac4-111">**комхандлер**</span><span class="sxs-lookup"><span data-stu-id="4cac4-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="4cac4-112">**комхандлертипе**</span><span class="sxs-lookup"><span data-stu-id="4cac4-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="4cac4-113">Указывает действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="4cac4-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4cac4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cac4-114">Remarks</span></span>

<span data-ttu-id="4cac4-115">Приложения определяют идентификатор класса с помощью свойства [**ClassID**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="4cac4-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cac4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4cac4-116">Requirements</span></span>



| <span data-ttu-id="4cac4-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4cac4-117">Requirement</span></span> | <span data-ttu-id="4cac4-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4cac4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4cac4-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4cac4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4cac4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4cac4-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4cac4-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4cac4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4cac4-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4cac4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cac4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4cac4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cac4-124">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4cac4-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





