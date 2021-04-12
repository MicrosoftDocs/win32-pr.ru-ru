---
title: Свойство Principal. UserId
description: Для сценариев Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.
ms.assetid: 57a34d7b-70b2-4156-b525-befecbaf070d
keywords:
- UserId, свойство планировщик задач
- Свойство UserId планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство UserId
topic_type:
- apiref
api_name:
- Principal.UserId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae6fce7fcfdf235ba8a83f262161c2e0f2afc71c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136350"
---
# <a name="principaluserid-property"></a><span data-ttu-id="97c4f-106">Свойство Principal. UserId</span><span class="sxs-lookup"><span data-stu-id="97c4f-106">Principal.UserId property</span></span>

<span data-ttu-id="97c4f-107">Для сценариев Возвращает или задает идентификатор пользователя, необходимый для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="97c4f-107">For scripting, gets or sets the user identifier that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c4f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97c4f-108">Syntax</span></span>


```VB
Principal.UserId As String
```



## <a name="property-value"></a><span data-ttu-id="97c4f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="97c4f-109">Property value</span></span>

<span data-ttu-id="97c4f-110">Идентификатор пользователя, необходимый для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="97c4f-110">The user identifier that is required to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c4f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97c4f-111">Remarks</span></span>

<span data-ttu-id="97c4f-112">Не устанавливайте это свойство, если в свойстве [**groupId**](principal-groupid.md) указан идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="97c4f-112">Do not set this property if a group identifier is specified in the [**GroupId**](principal-groupid.md) property.</span></span>

<span data-ttu-id="97c4f-113">При чтении или записи XML для задачи идентификатор пользователя для субъекта указывается с помощью элемента [**UserID**](taskschedulerschema-userid-principaltype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="97c4f-113">When reading or writing XML for a task, the user identifier for the principal is specified using the [**UserId**](taskschedulerschema-userid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="97c4f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="97c4f-114">Requirements</span></span>



| <span data-ttu-id="97c4f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="97c4f-115">Requirement</span></span> | <span data-ttu-id="97c4f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="97c4f-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="97c4f-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97c4f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97c4f-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97c4f-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="97c4f-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97c4f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97c4f-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97c4f-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="97c4f-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="97c4f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="97c4f-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="97c4f-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="97c4f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="97c4f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97c4f-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97c4f-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97c4f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97c4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97c4f-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="97c4f-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="97c4f-127">**Основного**</span><span class="sxs-lookup"><span data-stu-id="97c4f-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="97c4f-128">**Principal. GroupId**</span><span class="sxs-lookup"><span data-stu-id="97c4f-128">**Principal.GroupId**</span></span>](principal-groupid.md)
</dt> </dl>

 

 





