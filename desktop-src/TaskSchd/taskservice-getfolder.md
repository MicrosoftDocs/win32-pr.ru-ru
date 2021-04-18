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
ms.openlocfilehash: 74504e9cad124f8cbc9ec23e896ba4dec7d7f50c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672895"
---
# <a name="taskservicegetfolder-method"></a><span data-ttu-id="3f152-106">TaskService. @ Folder, метод</span><span class="sxs-lookup"><span data-stu-id="3f152-106">TaskService.GetFolder method</span></span>

<span data-ttu-id="3f152-107">Для создания скриптов Возвращает папку с зарегистрированными задачами.</span><span class="sxs-lookup"><span data-stu-id="3f152-107">For scripting, gets a folder of registered tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f152-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f152-108">Syntax</span></span>


```VB
TaskService.GetFolder( _
  ByVal path _
)
```



## <a name="parameters"></a><span data-ttu-id="3f152-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f152-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f152-110">*путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3f152-110">*path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f152-111">Путь к извлекаемой папке.</span><span class="sxs-lookup"><span data-stu-id="3f152-111">The path to the folder to be retrieved.</span></span> <span data-ttu-id="3f152-112">Не используйте обратную косую черту после имени последней папки в пути.</span><span class="sxs-lookup"><span data-stu-id="3f152-112">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="3f152-113">Корневая папка задач указывается с помощью обратной косой черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="3f152-113">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="3f152-114">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="3f152-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="3f152-115">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="3f152-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="3f152-116">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="3f152-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f152-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f152-117">Return value</span></span>

<span data-ttu-id="3f152-118">Объект [**таскфолдер**](taskfolder.md) для запрошенной папки.</span><span class="sxs-lookup"><span data-stu-id="3f152-118">A [**TaskFolder**](taskfolder.md) object for the requested folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f152-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3f152-119">Requirements</span></span>



| <span data-ttu-id="3f152-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3f152-120">Requirement</span></span> | <span data-ttu-id="3f152-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3f152-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f152-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f152-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3f152-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f152-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f152-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f152-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3f152-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f152-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f152-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3f152-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f152-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f152-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f152-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3f152-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f152-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f152-129"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f152-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f152-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f152-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3f152-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





