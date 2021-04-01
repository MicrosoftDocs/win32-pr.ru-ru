---
title: Таскфолдер. Задание свойства
description: Для сценариев возвращает задачу в указанном месте в папке.
ms.assetid: c0ad4402-dd63-499f-964c-0eada5665d1b
keywords:
- планировщик задач свойства задачи
- Планировщик задач свойства задачи, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, свойство Task
topic_type:
- apiref
api_name:
- TaskFolder.GetTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e813538cfcb995949cbe1fb8ec6a3b0d7772061c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801600"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="57527-106">Таскфолдер. Задание свойства</span><span class="sxs-lookup"><span data-stu-id="57527-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="57527-107">Для сценариев возвращает задачу в указанном месте в папке.</span><span class="sxs-lookup"><span data-stu-id="57527-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="57527-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="57527-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="57527-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="57527-109">Property value</span></span>

<span data-ttu-id="57527-110">Путь к задаче в папке (Location).</span><span class="sxs-lookup"><span data-stu-id="57527-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="57527-111">Корневая папка задач указывается с помощью обратной косой черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="57527-111">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="57527-112">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="57527-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="57527-113">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="57527-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="57527-114">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="57527-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57527-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="57527-115">Error codes</span></span>

<span data-ttu-id="57527-116">Задача в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="57527-116">The task at the specified location.</span></span> <span data-ttu-id="57527-117">Задача является объектом [**регистередтаск**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="57527-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="57527-118">Требования</span><span class="sxs-lookup"><span data-stu-id="57527-118">Requirements</span></span>



| <span data-ttu-id="57527-119">Требование</span><span class="sxs-lookup"><span data-stu-id="57527-119">Requirement</span></span> | <span data-ttu-id="57527-120">Значение</span><span class="sxs-lookup"><span data-stu-id="57527-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57527-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57527-121">Minimum supported client</span></span><br/> | <span data-ttu-id="57527-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="57527-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="57527-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57527-123">Minimum supported server</span></span><br/> | <span data-ttu-id="57527-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="57527-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="57527-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="57527-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="57527-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="57527-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="57527-127">DLL</span><span class="sxs-lookup"><span data-stu-id="57527-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57527-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57527-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





