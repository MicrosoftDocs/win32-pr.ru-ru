---
title: Метод Регистередтаск. WebMethod
description: Для сценариев возвращает все текущие выполняющиеся экземпляры зарегистрированной задачи.
ms.assetid: 01fea94e-fdec-4edf-886a-f6d9b566f201
keywords:
- Метод планировщик задач метода
- Метод WebMethod планировщик задач, объект Регистередтаск
- Планировщик задач объекта Регистередтаск, метод GetObject
topic_type:
- apiref
api_name:
- RegisteredTask.GetInstances
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78b1579df1124fcd6d26ea658730190b5eb0f5de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136942"
---
# <a name="registeredtaskgetinstances-method"></a><span data-ttu-id="a01b9-106">Метод Регистередтаск. WebMethod</span><span class="sxs-lookup"><span data-stu-id="a01b9-106">RegisteredTask.GetInstances method</span></span>

<span data-ttu-id="a01b9-107">Для сценариев возвращает все текущие выполняющиеся экземпляры зарегистрированной задачи.</span><span class="sxs-lookup"><span data-stu-id="a01b9-107">For scripting, returns all currently running instances of the registered task.</span></span>

> [!Note]  
> <span data-ttu-id="a01b9-108">**Регистередтаск.** -экземпляры будут возвращать только экземпляры текущей зарегистрированной задачи, которые выполняются в контексте безопасности пользователя или ниже.</span><span class="sxs-lookup"><span data-stu-id="a01b9-108">**RegisteredTask.GetInstances** will only return instances of the currently running registered task that are running at or below a user's security context.</span></span> <span data-ttu-id="a01b9-109">Например, для членов группы "Администраторы" будут возвращены все экземпляры текущей зарегистрированной задачи, но члены группы "Пользователи **" будут** возвращать только экземпляры текущей зарегистрированной **задачи, которые** выполняются в контексте безопасности группы "Пользователи".</span><span class="sxs-lookup"><span data-stu-id="a01b9-109">For example, for members of the Administrators group, **GetInstances** will return all instances of the currently running registered task, but for members of the Users group, **GetInstances** will only return instances of the currently running registered task that are running under the Users group security context.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a01b9-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a01b9-110">Syntax</span></span>


```VB
RegisteredTask.GetInstances( _
  ByVal flags, _
  ByRef runningTasks _
)
```



## <a name="parameters"></a><span data-ttu-id="a01b9-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="a01b9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a01b9-112">*flags*</span><span class="sxs-lookup"><span data-stu-id="a01b9-112">*flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a01b9-113">Этот параметр зарезервирован для будущего использования и должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="a01b9-113">This parameter is reserved for future use and must be set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a01b9-114">*руннингтаскс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a01b9-114">*runningTasks* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a01b9-115">Объект [**руннингтаскколлектион**](runningtaskcollection.md) , который содержит все текущие выполняющиеся экземпляры задачи.</span><span class="sxs-lookup"><span data-stu-id="a01b9-115">A [**RunningTaskCollection**](runningtaskcollection.md) object that contains all currently running instances of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a01b9-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a01b9-116">Return value</span></span>

<span data-ttu-id="a01b9-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a01b9-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a01b9-118">Требования</span><span class="sxs-lookup"><span data-stu-id="a01b9-118">Requirements</span></span>



| <span data-ttu-id="a01b9-119">Требование</span><span class="sxs-lookup"><span data-stu-id="a01b9-119">Requirement</span></span> | <span data-ttu-id="a01b9-120">Значение</span><span class="sxs-lookup"><span data-stu-id="a01b9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a01b9-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a01b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a01b9-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a01b9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a01b9-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a01b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a01b9-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a01b9-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a01b9-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="a01b9-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="a01b9-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="a01b9-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="a01b9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="a01b9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a01b9-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a01b9-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01b9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a01b9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01b9-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a01b9-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="a01b9-131">**регистередтаск**</span><span class="sxs-lookup"><span data-stu-id="a01b9-131">**RegisteredTask**</span></span>](registeredtask.md)
</dt> </dl>

 

 





