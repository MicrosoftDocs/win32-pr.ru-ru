---
title: Свойство Principal. RunLevel
description: Для создания скриптов Возвращает или задает идентификатор, который используется для указания уровня привилегий, необходимого для выполнения задач, связанных с участником.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- планировщик задач свойства RunLevel
- Планировщик задач свойства RunLevel, объект Principal
- Объект Principal планировщик задач, свойство RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534292"
---
# <a name="principalrunlevel-property"></a><span data-ttu-id="6a183-106">Свойство Principal. RunLevel</span><span class="sxs-lookup"><span data-stu-id="6a183-106">Principal.RunLevel property</span></span>

<span data-ttu-id="6a183-107">Для создания скриптов Возвращает или задает идентификатор, который используется для указания уровня привилегий, необходимого для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="6a183-107">For scripting, gets or sets the identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>

<span data-ttu-id="6a183-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6a183-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a183-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6a183-109">Syntax</span></span>


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="6a183-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6a183-110">Property value</span></span>

<span data-ttu-id="6a183-111">Идентификатор, который используется для указания уровня привилегий, необходимого для выполнения задач, связанных с участником.</span><span class="sxs-lookup"><span data-stu-id="6a183-111">The identifier that is used to specify the privilege level that is required to run the tasks that are associated with the principal.</span></span>



| <span data-ttu-id="6a183-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6a183-112">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="6a183-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6a183-113">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <span data-ttu-id="6a183-114"><dt>**Задача \_ RUNLEVEL \_ Lua**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="6a183-114"><dt>**TASK\_RUNLEVEL\_LUA**</dt> <dt>0</dt></span></span> </dl>             | <span data-ttu-id="6a183-115">Задачи будут выполняться с наименьшими привилегиями (LUA).</span><span class="sxs-lookup"><span data-stu-id="6a183-115">Tasks will be run with the least privileges (LUA).</span></span><br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <span data-ttu-id="6a183-116"><dt>**Задача \_ RUNLEVEL, \_ самый высокий**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="6a183-116"><dt>**TASK\_RUNLEVEL\_HIGHEST**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="6a183-117">Задачи будут выполняться с самыми высокими привилегиями.</span><span class="sxs-lookup"><span data-stu-id="6a183-117">Tasks will be run with the highest privileges.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="6a183-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a183-118">Remarks</span></span>

<span data-ttu-id="6a183-119">Если задача зарегистрирована с помощью встроенной \\ учетной записи администратора или учетных записей локальной системы или локальной службы, свойство **runlevel** будет пропущено.</span><span class="sxs-lookup"><span data-stu-id="6a183-119">If a task is registered using the Builtin\\Administrator account or the Local System or Local Service accounts, then the **RunLevel** property will be ignored.</span></span> <span data-ttu-id="6a183-120">Значение свойства также будет пропущено, если контроль учетных записей (UAC) отключен.</span><span class="sxs-lookup"><span data-stu-id="6a183-120">The property value will also be ignored if User Account Control (UAC) is turned off.</span></span>

<span data-ttu-id="6a183-121">Если задача зарегистрирована с помощью группы администраторов для контекста безопасности задачи, необходимо также задать для свойства [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) значение **Task \_ runlevel \_ высшего** , если требуется выполнить задачу.</span><span class="sxs-lookup"><span data-stu-id="6a183-121">If a task is registered using the Administrators group for the security context of the task, then you must also set the [**RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) property to **TASK\_RUNLEVEL\_HIGHEST** if you want to run the task.</span></span> <span data-ttu-id="6a183-122">Дополнительные сведения см. в разделе [контексты безопасности для задач](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="6a183-122">For more information, see [Security Contexts for Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a183-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6a183-123">Requirements</span></span>



| <span data-ttu-id="6a183-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6a183-124">Requirement</span></span> | <span data-ttu-id="6a183-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6a183-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a183-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6a183-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6a183-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a183-127">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="6a183-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6a183-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6a183-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6a183-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a183-130">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6a183-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="6a183-131"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6a183-131"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6a183-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6a183-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a183-133"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a183-133"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a183-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a183-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a183-135">**Основного**</span><span class="sxs-lookup"><span data-stu-id="6a183-135">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





