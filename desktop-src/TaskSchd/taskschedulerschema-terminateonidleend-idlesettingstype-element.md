---
title: Стопонидлинд (Идлесеттингстипе), элемент
description: Указывает, что планировщик задач будет прекращать выполнение задачи, если условие простоя заканчивается до завершения задачи.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- планировщик задач элемента Стопонидлинд
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989256"
---
# <a name="stoponidleend-idlesettingstype-element"></a><span data-ttu-id="0515c-104">Стопонидлинд (Идлесеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="0515c-104">StopOnIdleEnd (idleSettingsType) Element</span></span>

<span data-ttu-id="0515c-105">Указывает, что планировщик задач будет прекращать выполнение задачи, если условие простоя заканчивается до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="0515c-105">Specifies that the Task Scheduler will stop the task if the idle condition ends before the task is completed.</span></span>

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

<span data-ttu-id="0515c-106">Элемент **стопонидлинд** определяется сложным типом [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0515c-106">The **StopOnIdleEnd** element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0515c-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0515c-107">Parent element</span></span>



| <span data-ttu-id="0515c-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="0515c-108">Element</span></span>                                                                       | <span data-ttu-id="0515c-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="0515c-109">Derived from</span></span>                                                                 | <span data-ttu-id="0515c-110">Описание</span><span class="sxs-lookup"><span data-stu-id="0515c-110">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0515c-111">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="0515c-111">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="0515c-112">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="0515c-112">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="0515c-113">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="0515c-113">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0515c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0515c-114">Remarks</span></span>

<span data-ttu-id="0515c-115">Сведения о разработке на языке C++ см. в разделе [**свойство стопонидлинд объекта иидлесеттингс**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span><span class="sxs-lookup"><span data-stu-id="0515c-115">For C++ development, see [**StopOnIdleEnd Property of IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).</span></span>

<span data-ttu-id="0515c-116">Сведения о разработке сценариев см. в разделе [**идлесеттингс. стопонидлинд**](idlesettings-stoponidleend.md).</span><span class="sxs-lookup"><span data-stu-id="0515c-116">For script development, see [**IdleSettings.StopOnIdleEnd**](idlesettings-stoponidleend.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0515c-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="0515c-117">Examples</span></span>

<span data-ttu-id="0515c-118">Следующий XML-код определяет параметр простоя, указывающий, что задачу не следует выполнять при завершении условия простоя.</span><span class="sxs-lookup"><span data-stu-id="0515c-118">The following XML defines an idle setting that indicates the task should not be performed when the idle condition ends.</span></span>


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="0515c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0515c-119">Requirements</span></span>



| <span data-ttu-id="0515c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0515c-120">Requirement</span></span> | <span data-ttu-id="0515c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0515c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0515c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0515c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0515c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0515c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0515c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0515c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0515c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0515c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0515c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0515c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0515c-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="0515c-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





