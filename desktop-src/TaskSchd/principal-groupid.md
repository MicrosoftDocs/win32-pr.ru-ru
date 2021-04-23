---
title: Свойство Principal. GroupId
description: Для создания скриптов Возвращает или задает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.
ms.assetid: be0b7cd1-0e17-4aa5-af8e-880c95b3e7dc
keywords:
- Свойство GroupId планировщик задач
- Свойство GroupId планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство GroupId
topic_type:
- apiref
api_name:
- Principal.GroupId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7b5acd17d32b0123723fe53f91e390c37f42d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681991"
---
# <a name="principalgroupid-property"></a><span data-ttu-id="33cc9-106">Свойство Principal. GroupId</span><span class="sxs-lookup"><span data-stu-id="33cc9-106">Principal.GroupId property</span></span>

<span data-ttu-id="33cc9-107">Для создания скриптов Возвращает или задает идентификатор группы пользователей, необходимой для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="33cc9-107">For scripting, gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.</span></span>

## <a name="syntax"></a><span data-ttu-id="33cc9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="33cc9-108">Syntax</span></span>


```VB
Principal.GroupId As String
```



## <a name="property-value"></a><span data-ttu-id="33cc9-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="33cc9-109">Property value</span></span>

<span data-ttu-id="33cc9-110">Идентификатор группы пользователей, связанной с этим участником.</span><span class="sxs-lookup"><span data-stu-id="33cc9-110">The identifier of the user group that is associated with this principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="33cc9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33cc9-111">Remarks</span></span>

<span data-ttu-id="33cc9-112">Не устанавливайте это свойство, если в свойстве [**UserID**](principal-userid.md) указан идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="33cc9-112">Do not set this property if a user identifier is specified in the [**UserId**](principal-userid.md) property.</span></span>

<span data-ttu-id="33cc9-113">При чтении или записи XML-кода для задачи идентификатор группы участника указывается в элементе [**groupId**](taskschedulerschema-groupid-principaltype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="33cc9-113">When reading or writing XML for a task, the group identifier for a principal is specified in the [**GroupId**](taskschedulerschema-groupid-principaltype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="33cc9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="33cc9-114">Requirements</span></span>



| <span data-ttu-id="33cc9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="33cc9-115">Requirement</span></span> | <span data-ttu-id="33cc9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="33cc9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33cc9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33cc9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="33cc9-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="33cc9-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="33cc9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33cc9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="33cc9-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="33cc9-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="33cc9-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="33cc9-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="33cc9-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="33cc9-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="33cc9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="33cc9-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33cc9-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33cc9-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33cc9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="33cc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33cc9-126">**UserId**</span><span class="sxs-lookup"><span data-stu-id="33cc9-126">**UserId**</span></span>](principal-userid.md)
</dt> <dt>

[<span data-ttu-id="33cc9-127">**Основного**</span><span class="sxs-lookup"><span data-stu-id="33cc9-127">**Principal**</span></span>](principal.md)
</dt> <dt>

[<span data-ttu-id="33cc9-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="33cc9-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





