---
title: Регистередтаск. останавливаться, метод
description: Для создания скриптов немедленно останавливает зарегистрированную задачу.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- планировщик задач метода завершения
- Метод завершения планировщик задач, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод завершения
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416061"
---
# <a name="registeredtaskstop-method"></a><span data-ttu-id="54925-106">Регистередтаск. останавливаться, метод</span><span class="sxs-lookup"><span data-stu-id="54925-106">RegisteredTask.Stop method</span></span>

<span data-ttu-id="54925-107">Для создания скриптов немедленно останавливает зарегистрированную задачу.</span><span class="sxs-lookup"><span data-stu-id="54925-107">For scripting, stops the registered task immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="54925-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54925-108">Syntax</span></span>


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="54925-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="54925-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54925-110">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="54925-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54925-111">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="54925-111">Reserved.</span></span> <span data-ttu-id="54925-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="54925-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54925-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54925-113">Return value</span></span>

<span data-ttu-id="54925-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="54925-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54925-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54925-115">Remarks</span></span>

<span data-ttu-id="54925-116">Функция **регистередтаск. Stop** останавливает все экземпляры задачи.</span><span class="sxs-lookup"><span data-stu-id="54925-116">The **RegisteredTask.Stop** function stops all instances of the task.</span></span>

<span data-ttu-id="54925-117">Системная учетная запись. пользователи с правами группы администраторов могут прерывать задачу, а если пользователь имеет права на выполнение и чтение задачи, он может прерывать задачу.</span><span class="sxs-lookup"><span data-stu-id="54925-117">System account users can stop a task, users with Administrator group privileges can stop a task, and if a user has rights to execute and read a task, then the user can stop the task.</span></span> <span data-ttu-id="54925-118">Пользователь может прерывать экземпляры задач, работающие под теми же учетными данными, что и учетная запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="54925-118">A user can stop the task instances that are running under the same credentials as the user account.</span></span> <span data-ttu-id="54925-119">Во всех остальных случаях пользователю отказано в доступе для завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="54925-119">In all other cases, the user is denied access to stop the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="54925-120">Требования</span><span class="sxs-lookup"><span data-stu-id="54925-120">Requirements</span></span>



| <span data-ttu-id="54925-121">Требование</span><span class="sxs-lookup"><span data-stu-id="54925-121">Requirement</span></span> | <span data-ttu-id="54925-122">Значение</span><span class="sxs-lookup"><span data-stu-id="54925-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54925-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54925-123">Minimum supported client</span></span><br/> | <span data-ttu-id="54925-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54925-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="54925-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54925-125">Minimum supported server</span></span><br/> | <span data-ttu-id="54925-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54925-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54925-127">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="54925-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="54925-128"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="54925-128"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="54925-129">DLL</span><span class="sxs-lookup"><span data-stu-id="54925-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54925-130"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54925-130"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54925-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54925-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54925-132">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="54925-132">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





