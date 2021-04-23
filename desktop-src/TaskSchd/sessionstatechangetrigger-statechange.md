---
title: Сессионстатечанжетригжер. StateChange, свойство
description: Для создания скриптов Возвращает или задает тип изменения сеанса сервера терминалов, который вызывает запуск задачи.
ms.assetid: ae1460c7-2939-4fcb-b7fc-edc859596bc4
keywords:
- планировщик задач свойства StateChange
- Планировщик задач свойства StateChange, объект Сессионстатечанжетригжер
- Планировщик задач объекта Сессионстатечанжетригжер, свойство StateChange
topic_type:
- apiref
api_name:
- SessionStateChangeTrigger.StateChange
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac4be561482917788f6afb9b8eb7394cdcce7985
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801612"
---
# <a name="sessionstatechangetriggerstatechange-property"></a><span data-ttu-id="a3a04-106">Сессионстатечанжетригжер. StateChange, свойство</span><span class="sxs-lookup"><span data-stu-id="a3a04-106">SessionStateChangeTrigger.StateChange property</span></span>

<span data-ttu-id="a3a04-107">Для создания скриптов Возвращает или задает тип изменения сеанса сервера терминалов, который вызывает запуск задачи.</span><span class="sxs-lookup"><span data-stu-id="a3a04-107">For scripting, gets or sets the kind of Terminal Server session change that would trigger a task launch.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3a04-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a3a04-108">Syntax</span></span>


```VB
SessionStateChangeTrigger.StateChange As Integer
```



## <a name="property-value"></a><span data-ttu-id="a3a04-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a3a04-109">Property value</span></span>

<span data-ttu-id="a3a04-110">Тип изменения сеанса сервера терминалов, запускающего задачу для запуска.</span><span class="sxs-lookup"><span data-stu-id="a3a04-110">The kind of Terminal Server session change that triggers a task to launch.</span></span>

<span data-ttu-id="a3a04-111">Возможные значения: перечисление [**\_ \_ \_ \_ типа изменения состояния сеанса задачи**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) .</span><span class="sxs-lookup"><span data-stu-id="a3a04-111">The possible values are from the [**TASK\_SESSION\_STATE\_CHANGE\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) enumeration.</span></span>



| <span data-ttu-id="a3a04-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a04-112">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="a3a04-113">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a04-113">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_CONSOLE_CONNECT"></span><span id="task_console_connect"></span><dl> <span data-ttu-id="a3a04-114"><dt>**Задача \_ \_Подключение к консоли**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-114"><dt>**TASK\_CONSOLE\_CONNECT**</dt> <dt>1</dt></span></span> </dl>          | <span data-ttu-id="a3a04-115">Изменение состояния подключения к консоли сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-115">Terminal Server console connection state change.</span></span> <span data-ttu-id="a3a04-116">Например, при подключении к сеансу пользователя на локальном компьютере путем переключения пользователей на компьютер.</span><span class="sxs-lookup"><span data-stu-id="a3a04-116">For example, when you connect to a user session on the local computer by switching users on the computer.</span></span> <br/>                           |
| <span id="TASK_CONSOLE_DISCONNECT"></span><span id="task_console_disconnect"></span><dl> <span data-ttu-id="a3a04-117"><dt>**Задача \_ \_Отключение консоли**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-117"><dt>**TASK\_CONSOLE\_DISCONNECT**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="a3a04-118">Изменение состояния отключения консоли сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-118">Terminal Server console disconnection state change.</span></span> <span data-ttu-id="a3a04-119">Например, при отключении сеанса пользователя на локальном компьютере путем переключения пользователей на компьютер.</span><span class="sxs-lookup"><span data-stu-id="a3a04-119">For example, when you disconnect to a user session on the local computer by switching users on the computer.</span></span><br/>                      |
| <span id="TASK_REMOTE_CONNECT"></span><span id="task_remote_connect"></span><dl> <span data-ttu-id="a3a04-120"><dt>**Задача \_ УДАЛЕНное \_ Подключение**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-120"><dt>**TASK\_REMOTE\_CONNECT**</dt> <dt>3</dt></span></span> </dl>             | <span data-ttu-id="a3a04-121">Изменение состояния удаленного подключения сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-121">Terminal Server remote connection state change.</span></span> <span data-ttu-id="a3a04-122">Например, когда пользователь подключается к сеансу пользователя с помощью подключение к удаленному рабочему столу программы с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3a04-122">For example, when a user connects to a user session by using the Remote Desktop Connection program from a remote computer.</span></span><br/>            |
| <span id="TASK_REMOTE_DISCONNECT"></span><span id="task_remote_disconnect"></span><dl> <span data-ttu-id="a3a04-123"><dt>**Задача \_ УДАЛЕНное \_ Отключение**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-123"><dt>**TASK\_REMOTE\_DISCONNECT**</dt> <dt>4</dt></span></span> </dl>    | <span data-ttu-id="a3a04-124">Изменение состояния удаленного отключения сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-124">Terminal Server remote disconnection state change.</span></span> <span data-ttu-id="a3a04-125">Например, когда пользователь отключается от сеанса пользователя при использовании подключение к удаленному рабочему столу программы с удаленного компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3a04-125">For example, when a user disconnects from a user session while using the Remote Desktop Connection program from a remote computer.</span></span><br/> |
| <span id="TASK_SESSION_LOCK"></span><span id="task_session_lock"></span><dl> <span data-ttu-id="a3a04-126"><dt>**Задача \_ \_Блокировка сеанса**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-126"><dt>**TASK\_SESSION\_LOCK**</dt> <dt>7</dt></span></span> </dl>                   | <span data-ttu-id="a3a04-127">Изменение состояния блокировки сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-127">Terminal Server session locked state change.</span></span> <span data-ttu-id="a3a04-128">Например, это изменение состояния приводит к запуску задачи при блокировке компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3a04-128">For example, this state change causes the task to run when the computer is locked.</span></span> <br/>                                                      |
| <span id="TASK_SESSION_UNLOCK"></span><span id="task_session_unlock"></span><dl> <span data-ttu-id="a3a04-129"><dt>**Задача \_ \_Разблокировка сеанса**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-129"><dt>**TASK\_SESSION\_UNLOCK**</dt> <dt>8</dt></span></span> </dl>             | <span data-ttu-id="a3a04-130">Изменение состояния разблокировки сеанса сервера терминалов.</span><span class="sxs-lookup"><span data-stu-id="a3a04-130">Terminal Server session unlocked state change.</span></span> <span data-ttu-id="a3a04-131">Например, это изменение состояния приводит к выполнению задачи при разблокировании компьютера.</span><span class="sxs-lookup"><span data-stu-id="a3a04-131">For example, this state change causes the task to run when the computer is unlocked.</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="a3a04-132">Требования</span><span class="sxs-lookup"><span data-stu-id="a3a04-132">Requirements</span></span>



| <span data-ttu-id="a3a04-133">Требование</span><span class="sxs-lookup"><span data-stu-id="a3a04-133">Requirement</span></span> | <span data-ttu-id="a3a04-134">Значение</span><span class="sxs-lookup"><span data-stu-id="a3a04-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a04-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a3a04-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a04-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3a04-136">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a3a04-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a3a04-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a04-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a3a04-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3a04-139">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a3a04-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="a3a04-140"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-140"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a3a04-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a3a04-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3a04-142"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3a04-142"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





