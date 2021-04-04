---
title: Элемент Data (Комхандлертипе)
description: Указывает дополнительные данные, связанные с обработчиком.
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- Элемент данных планировщик задач
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989109"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="89b16-104">Элемент Data (Комхандлертипе)</span><span class="sxs-lookup"><span data-stu-id="89b16-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="89b16-105">Указывает дополнительные данные, связанные с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="89b16-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="89b16-106">Элемент **Data** определяется сложным типом [**комхандлертипе**](taskschedulerschema-comhandlertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="89b16-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="89b16-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="89b16-107">Parent element</span></span>



| <span data-ttu-id="89b16-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="89b16-108">Element</span></span>                                                                  | <span data-ttu-id="89b16-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="89b16-109">Derived from</span></span>                                                             | <span data-ttu-id="89b16-110">Описание</span><span class="sxs-lookup"><span data-stu-id="89b16-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="89b16-111">**комхандлер**</span><span class="sxs-lookup"><span data-stu-id="89b16-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="89b16-112">**комхандлертипе**</span><span class="sxs-lookup"><span data-stu-id="89b16-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="89b16-113">Указывает действие, которое вызывает обработчик.</span><span class="sxs-lookup"><span data-stu-id="89b16-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="89b16-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="89b16-114">Remarks</span></span>

<span data-ttu-id="89b16-115">Приложения определяют данные обработчика с помощью свойства [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) интерфейса [**икомхандлерактион**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .</span><span class="sxs-lookup"><span data-stu-id="89b16-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="89b16-116">Требования</span><span class="sxs-lookup"><span data-stu-id="89b16-116">Requirements</span></span>



| <span data-ttu-id="89b16-117">Требование</span><span class="sxs-lookup"><span data-stu-id="89b16-117">Requirement</span></span> | <span data-ttu-id="89b16-118">Значение</span><span class="sxs-lookup"><span data-stu-id="89b16-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89b16-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="89b16-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89b16-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="89b16-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="89b16-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="89b16-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89b16-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="89b16-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89b16-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="89b16-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89b16-124">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="89b16-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





