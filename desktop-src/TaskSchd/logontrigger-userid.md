---
title: Логонтригжер. UserId, свойство
description: Для создания скриптов Возвращает или задает идентификатор пользователя.
ms.assetid: d28eea9b-8238-49e7-afec-5a96281b3063
keywords:
- UserId, свойство планировщик задач
- UserId, свойство планировщик задач, объект Логонтригжер
- Планировщик задач объекта Логонтригжер, свойство UserId
topic_type:
- apiref
api_name:
- LogonTrigger.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dde08f82742325303e62e405cd13d2b9e7c1191
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414981"
---
# <a name="logontriggeruserid-property"></a><span data-ttu-id="8b937-106">Логонтригжер. UserId, свойство</span><span class="sxs-lookup"><span data-stu-id="8b937-106">LogonTrigger.UserId property</span></span>

<span data-ttu-id="8b937-107">Для создания скриптов Возвращает или задает идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b937-107">For scripting, gets or sets the identifier of the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b937-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8b937-108">Syntax</span></span>


```VB
LogonTrigger.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="8b937-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8b937-109">Property value</span></span>

<span data-ttu-id="8b937-110">Идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="8b937-110">The identifier of the user.</span></span> <span data-ttu-id="8b937-111">Например, "MyDomain \\ myname" или для локальной учетной записи "Administrator".</span><span class="sxs-lookup"><span data-stu-id="8b937-111">For example, "MyDomain\\MyName" or for a local account, "Administrator".</span></span>

<span data-ttu-id="8b937-112">Это свойство может иметь один из следующих форматов:</span><span class="sxs-lookup"><span data-stu-id="8b937-112">This property can be in one of the following formats:</span></span>

-   <span data-ttu-id="8b937-113">Имя пользователя или идентификатор безопасности: задача запускается при входе пользователя в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8b937-113">User name or SID: The task is started when the user logs on to the computer.</span></span>
-   <span data-ttu-id="8b937-114">NULL: задача запускается, когда любой пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8b937-114">NULL: The task is started when any user logs on to the computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b937-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8b937-115">Remarks</span></span>

<span data-ttu-id="8b937-116">Если требуется активировать задачу при входе любого члена группы на компьютер, а не при входе определенного пользователя в систему, не присваивайте свойству **логонтригжер. UserID** значение.</span><span class="sxs-lookup"><span data-stu-id="8b937-116">If you want a task to be triggered when any member of a group logs on to the computer rather than when a specific user logs on, then do not assign a value to the **LogonTrigger.UserId** property.</span></span> <span data-ttu-id="8b937-117">Вместо этого создайте триггер LOGON с пустым свойством **логонтригжер. UserID** и назначьте участнику значение для задачи с помощью свойства [**Principal. groupId**](principal-groupid.md) .</span><span class="sxs-lookup"><span data-stu-id="8b937-117">Instead, create a logon trigger with an empty **LogonTrigger.UserId** property and assign a value to the principal for the task using the [**Principal.GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="8b937-118">При чтении или записи XML-кода для задачи идентификатор входа пользователя указывается с помощью элемента [**UserID**](taskschedulerschema-userid-logontriggertype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="8b937-118">When reading or writing XML for a task, the logon user identifier is specified using the [**UserId**](taskschedulerschema-userid-logontriggertype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b937-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8b937-119">Requirements</span></span>



| <span data-ttu-id="8b937-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8b937-120">Requirement</span></span> | <span data-ttu-id="8b937-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8b937-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b937-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8b937-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8b937-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8b937-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8b937-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8b937-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8b937-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8b937-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8b937-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8b937-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b937-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b937-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b937-128">DLL</span><span class="sxs-lookup"><span data-stu-id="8b937-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b937-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b937-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b937-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8b937-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b937-131">**логонтригжер**</span><span class="sxs-lookup"><span data-stu-id="8b937-131">**LogonTrigger**</span></span>](logontrigger.md)
</dt> <dt>

[<span data-ttu-id="8b937-132">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="8b937-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





