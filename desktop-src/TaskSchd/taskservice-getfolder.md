---
title: TaskService. @ Folder, метод
description: Для создания скриптов Возвращает папку с зарегистрированными задачами.
ms.assetid: 57e5b411-1fb6-4ee1-9802-ed2adbb4fdf8
keywords:
- Метод onfolder планировщик задач
- Метод GetObject планировщик задач, объект TaskService
- Объект TaskService планировщик задач, метод GetObject
topic_type:
- apiref
api_name:
- TaskService.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e58f2d930a0577b6f1be620891b7ba631f18d77
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387103"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="00c03-106">TaskService. @ Folder, метод</span><span class="sxs-lookup"><span data-stu-id="00c03-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="00c03-107">Для создания скриптов Возвращает папку с зарегистрированными задачами.</span><span class="sxs-lookup"><span data-stu-id="00c03-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c03-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00c03-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="00c03-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="00c03-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c03-110">*путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00c03-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c03-111">Путь к извлекаемой папке.</span><span class="sxs-lookup"><span data-stu-id="00c03-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="00c03-112">Не используйте обратную косую черту после имени последней папки в пути.</span><span class="sxs-lookup"><span data-stu-id="00c03-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="00c03-113">Корневая папка задач указывается с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="00c03-113">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="00c03-114">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="00c03-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="00c03-115">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="00c03-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="00c03-116">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="00c03-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c03-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00c03-117">Return value</span></span>

<span data-ttu-id="00c03-118">Объект [**таскфолдер**](taskfolder.md) для запрошенной папки.</span><span class="sxs-lookup"><span data-stu-id="00c03-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c03-119">Требования</span><span class="sxs-lookup"><span data-stu-id="00c03-119">Requirements</span></span>



| <span data-ttu-id="00c03-120">Требование</span><span class="sxs-lookup"><span data-stu-id="00c03-120">Requirement</span></span> | <span data-ttu-id="00c03-121">Значение</span><span class="sxs-lookup"><span data-stu-id="00c03-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00c03-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00c03-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00c03-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="00c03-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="00c03-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00c03-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00c03-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="00c03-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="00c03-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="00c03-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="00c03-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00c03-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00c03-128">DLL</span><span class="sxs-lookup"><span data-stu-id="00c03-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00c03-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c03-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00c03-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00c03-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00c03-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="00c03-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





