---
title: UserId (Логонтригжертипе), элемент
description: Идентификатор пользователя. Задача запускается, когда пользователь входит в систему на компьютере.
ms.assetid: 52568899-e351-4ee1-b613-d7c42d7b983d
keywords:
- Элемент UserId планировщик задач
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69d6534122b4b5e11a18a64ffa9bbb5e29e2a68a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535480"
---
# <a name="userid-logontriggertype-element"></a><span data-ttu-id="4c7c4-105">UserId (Логонтригжертипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4c7c4-105">UserId (logonTriggerType) Element</span></span>

<span data-ttu-id="4c7c4-106">Идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="4c7c4-106">Identifier of the user.</span></span> <span data-ttu-id="4c7c4-107">Задача запускается, когда пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4c7c4-107">The task is started when this user logs on to the computer.</span></span>

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
    maxOccurs="1"
    minOccurs="0"
 />
```

<span data-ttu-id="4c7c4-108">Элемент **UserID** определяется сложным типом [**логонтригжертипе**](taskschedulerschema-logontriggertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7c4-108">The **UserId** element is defined by the [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="4c7c4-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="4c7c4-109">Parent element</span></span>



| <span data-ttu-id="4c7c4-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="4c7c4-110">Element</span></span>                                                                       | <span data-ttu-id="4c7c4-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="4c7c4-111">Derived from</span></span>                                                                 | <span data-ttu-id="4c7c4-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4c7c4-112">Description</span></span>                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="4c7c4-113">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="4c7c4-113">**LogonTrigger**</span></span>](taskschedulerschema-logontrigger-triggergroup-element.md) | [<span data-ttu-id="4c7c4-114">**логонтригжертипе**</span><span class="sxs-lookup"><span data-stu-id="4c7c4-114">**logonTriggerType**</span></span>](taskschedulerschema-logontriggertype-complextype.md) | <span data-ttu-id="4c7c4-115">Указывает триггер, который запускает задачу при входе пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="4c7c4-115">Specifies a trigger that starts a task when a user logs on.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4c7c4-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c7c4-116">Remarks</span></span>

<span data-ttu-id="4c7c4-117">Для разработки сценариев идентификатор пользователя для триггера LOGON указывается с помощью свойства [**логонтригжер. UserID**](logontrigger-userid.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7c4-117">For scripting development, the user identifier for the logon trigger is specified using the [**LogonTrigger.UserId**](logontrigger-userid.md) property.</span></span>

<span data-ttu-id="4c7c4-118">Для разработки на C++ идентификатор пользователя для триггера LOGON указывается с помощью свойства [**илогонтригжер:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) .</span><span class="sxs-lookup"><span data-stu-id="4c7c4-118">For C++ development, the user identifier for the logon trigger is specified using the [**ILogonTrigger::UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid) property.</span></span>

## <a name="examples"></a><span data-ttu-id="4c7c4-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="4c7c4-119">Examples</span></span>

<span data-ttu-id="4c7c4-120">Полный пример XML-кода для задачи, указывающей триггер входа, см. в разделе [пример триггера LOGON (XML)](logon-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="4c7c4-120">For a complete example of the XML for a task that specifies a logon trigger, see [Logon Trigger Example (XML)](logon-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7c4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4c7c4-121">Requirements</span></span>



| <span data-ttu-id="4c7c4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4c7c4-122">Requirement</span></span> | <span data-ttu-id="4c7c4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4c7c4-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4c7c4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c7c4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7c4-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c7c4-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4c7c4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c7c4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7c4-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c7c4-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c7c4-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c7c4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c7c4-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="4c7c4-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="4c7c4-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4c7c4-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





