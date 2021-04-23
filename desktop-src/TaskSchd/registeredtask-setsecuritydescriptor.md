---
title: Регистередтаск. Сетсекуритидескриптор, метод
description: Для сценариев задает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- планировщик задач метода Сетсекуритидескриптор
- Планировщик задач метода Сетсекуритидескриптор, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод Сетсекуритидескриптор
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137235"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a><span data-ttu-id="280cd-106">Регистередтаск. Сетсекуритидескриптор, метод</span><span class="sxs-lookup"><span data-stu-id="280cd-106">RegisteredTask.SetSecurityDescriptor method</span></span>

<span data-ttu-id="280cd-107">Для сценариев задает дескриптор безопасности, который используется в качестве учетных данных для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="280cd-107">For scripting, sets the security descriptor that is used as credentials for the registered task.</span></span>

## <a name="syntax"></a><span data-ttu-id="280cd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="280cd-108">Syntax</span></span>


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="280cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="280cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="280cd-110">*SDDL* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="280cd-110">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="280cd-111">Дескриптор безопасности, используемый в качестве учетных данных для зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="280cd-111">The security descriptor that is used as credentials for the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="280cd-112">Если локальной системной учетной записи запрещен доступ к задаче, то служба планировщик задач может получить непредвиденные результаты.</span><span class="sxs-lookup"><span data-stu-id="280cd-112">If the Local System account is denied access to a task, then the Task Scheduler service can produce unexpected results.</span></span>

 

</dd> <dt>

<span data-ttu-id="280cd-113">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="280cd-113">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="280cd-114">Флаги, указывающие, как задать дескриптор безопасности.</span><span class="sxs-lookup"><span data-stu-id="280cd-114">Flags that specify how to set the security descriptor.</span></span> <span data-ttu-id="280cd-115">Для задачи \_ не \_ Добавить \_ основной \_ элемент ACE (0x10) из перечисления [**\_ создания задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) можно указать.</span><span class="sxs-lookup"><span data-stu-id="280cd-115">The TASK\_DONT\_ADD\_PRINCIPAL\_ACE flag (0x10) from the [**TASK\_CREATION**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) enumeration can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="280cd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="280cd-116">Return value</span></span>

<span data-ttu-id="280cd-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="280cd-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="280cd-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="280cd-118">Remarks</span></span>

<span data-ttu-id="280cd-119">Вы можете указать список управления доступом (ACL) в дескрипторе безопасности задачи, чтобы разрешить или запретить определенным пользователям и группам доступ к задаче.</span><span class="sxs-lookup"><span data-stu-id="280cd-119">You can specify the access control list (ACL) in the security descriptor for a task in order to allow or deny certain users and groups access to a task.</span></span>

## <a name="requirements"></a><span data-ttu-id="280cd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="280cd-120">Requirements</span></span>



| <span data-ttu-id="280cd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="280cd-121">Requirement</span></span> | <span data-ttu-id="280cd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="280cd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="280cd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="280cd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="280cd-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="280cd-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="280cd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="280cd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="280cd-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="280cd-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="280cd-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="280cd-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="280cd-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="280cd-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="280cd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="280cd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="280cd-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="280cd-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="280cd-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="280cd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="280cd-132">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="280cd-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> <dt>

[<span data-ttu-id="280cd-133">**Таскфолдер. Жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="280cd-133">**TaskFolder.GetSecurityDescriptor**</span></span>](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[<span data-ttu-id="280cd-134">**Регистередтаск. Сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="280cd-134">**RegisteredTask.SetSecurityDescriptor**</span></span>](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





