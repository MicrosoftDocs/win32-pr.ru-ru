---
title: Principal (taskType), элемент
description: Указывает контексты безопасности, которые могут использоваться для выполнения задачи.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- планировщик задач элементов Principal
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988293"
---
# <a name="principals-tasktype-element"></a><span data-ttu-id="9cb59-104">Principal (taskType), элемент</span><span class="sxs-lookup"><span data-stu-id="9cb59-104">Principals (taskType) Element</span></span>

<span data-ttu-id="9cb59-105">Указывает контексты безопасности, которые могут использоваться для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="9cb59-105">Specifies the security contexts that can be used to run the task.</span></span>

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

<span data-ttu-id="9cb59-106">Элемент **Principals** определяется сложным типом [**TaskType**](taskschedulerschema-tasktype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb59-106">The **Principals** element is defined by the [**taskType**](taskschedulerschema-tasktype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="9cb59-107">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="9cb59-107">Parent element</span></span>



| <span data-ttu-id="9cb59-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="9cb59-108">Element</span></span>                                          | <span data-ttu-id="9cb59-109">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="9cb59-109">Derived from</span></span>                                                 | <span data-ttu-id="9cb59-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9cb59-110">Description</span></span>                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="9cb59-111">**Задача**</span><span class="sxs-lookup"><span data-stu-id="9cb59-111">**Task**</span></span>](taskschedulerschema-task-element.md) | [<span data-ttu-id="9cb59-112">**taskType**</span><span class="sxs-lookup"><span data-stu-id="9cb59-112">**taskType**</span></span>](taskschedulerschema-tasktype-complextype.md) | <span data-ttu-id="9cb59-113">Определяет задачу, выполняемую службой планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9cb59-113">Defines the task that is performed by the Task Scheduler service.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="9cb59-114">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="9cb59-114">Child elements</span></span>



| <span data-ttu-id="9cb59-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="9cb59-115">Element</span></span>                                                                  | <span data-ttu-id="9cb59-116">Тип</span><span class="sxs-lookup"><span data-stu-id="9cb59-116">Type</span></span>                                                                   | <span data-ttu-id="9cb59-117">Описание</span><span class="sxs-lookup"><span data-stu-id="9cb59-117">Description</span></span>                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="9cb59-118">**Основного**</span><span class="sxs-lookup"><span data-stu-id="9cb59-118">**Principal**</span></span>](taskschedulerschema-principal-principaltype-element.md) | [<span data-ttu-id="9cb59-119">**principalType**</span><span class="sxs-lookup"><span data-stu-id="9cb59-119">**principalType**</span></span>](taskschedulerschema-principaltype-complextype.md) | <span data-ttu-id="9cb59-120">Указывает учетные данные безопасности для участника.</span><span class="sxs-lookup"><span data-stu-id="9cb59-120">Specifies the security credentials for a principal.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9cb59-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9cb59-121">Remarks</span></span>

<span data-ttu-id="9cb59-122">Для задачи можно указать до 32 участников.</span><span class="sxs-lookup"><span data-stu-id="9cb59-122">You can specify up to 32 principals for a task.</span></span>

<span data-ttu-id="9cb59-123">Для разработки сценариев участники задачи указываются с помощью свойства [**таскдефинитион. Principal**](taskdefinition-principal.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb59-123">For scripting development, the principals of a task are specified using the [**TaskDefinition.Principal**](taskdefinition-principal.md) property.</span></span>

<span data-ttu-id="9cb59-124">Для разработки на C++ субъекты задачи указываются с помощью [**Свойства Principal объекта итаскдефинитион**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span><span class="sxs-lookup"><span data-stu-id="9cb59-124">For C++ development, the principals of a task are specified using the [**Principal property of ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).</span></span>

## <a name="examples"></a><span data-ttu-id="9cb59-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="9cb59-125">Examples</span></span>

<span data-ttu-id="9cb59-126">Следующий XML-код определяет двух участников: идентификатор пользователя и участника идентификатора группы для задачи.</span><span class="sxs-lookup"><span data-stu-id="9cb59-126">The following XML defines two principals: a user identifier and group identifier principal for the task.</span></span>


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a><span data-ttu-id="9cb59-127">Требования</span><span class="sxs-lookup"><span data-stu-id="9cb59-127">Requirements</span></span>



| <span data-ttu-id="9cb59-128">Требование</span><span class="sxs-lookup"><span data-stu-id="9cb59-128">Requirement</span></span> | <span data-ttu-id="9cb59-129">Значение</span><span class="sxs-lookup"><span data-stu-id="9cb59-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9cb59-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9cb59-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9cb59-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9cb59-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9cb59-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9cb59-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9cb59-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9cb59-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9cb59-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9cb59-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cb59-135">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="9cb59-135">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9cb59-136">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="9cb59-136">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





