---
title: TaskService. TargetServer, свойство
description: Для создания скриптов возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.
ms.assetid: 8b0edf18-2a79-46f2-9b90-2c4726db881e
keywords:
- планировщик задач свойства TargetServer
- Планировщик задач свойства TargetServer, объект TaskService
- Планировщик задач объекта TaskService, свойство TargetServer
topic_type:
- apiref
api_name:
- TaskService.TargetServer
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4347915fae57585716a64a6a4ca549ccc1c299
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535471"
---
# <a name="taskservicetargetserver-property"></a><span data-ttu-id="da0c6-106">TaskService. TargetServer, свойство</span><span class="sxs-lookup"><span data-stu-id="da0c6-106">TaskService.TargetServer property</span></span>

<span data-ttu-id="da0c6-107">Для создания скриптов возвращает имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="da0c6-107">For scripting, gets the name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0c6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da0c6-108">Syntax</span></span>


```VB
TaskService.TargetServer As String
```



## <a name="property-value"></a><span data-ttu-id="da0c6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="da0c6-109">Property value</span></span>

<span data-ttu-id="da0c6-110">Имя компьютера, на котором запущена служба планировщик задач, к которой подключен пользователь.</span><span class="sxs-lookup"><span data-stu-id="da0c6-110">The name of the computer that is running the Task Scheduler service that the user is connected to.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0c6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da0c6-111">Remarks</span></span>

<span data-ttu-id="da0c6-112">Это свойство возвращает пустую строку, когда пользователь передает IP-адрес, localhost или "." в качестве параметра, и возвращает имя компьютера, на котором выполняется служба планировщик задач, когда пользователь не передает значение параметра.</span><span class="sxs-lookup"><span data-stu-id="da0c6-112">This property returns an empty string when the user passes an IP address, Localhost, or '.' as a parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.</span></span>

## <a name="requirements"></a><span data-ttu-id="da0c6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="da0c6-113">Requirements</span></span>



| <span data-ttu-id="da0c6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="da0c6-114">Requirement</span></span> | <span data-ttu-id="da0c6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="da0c6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da0c6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da0c6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="da0c6-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da0c6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="da0c6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da0c6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="da0c6-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da0c6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="da0c6-120">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="da0c6-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="da0c6-121"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="da0c6-121"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="da0c6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="da0c6-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da0c6-123"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da0c6-123"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





