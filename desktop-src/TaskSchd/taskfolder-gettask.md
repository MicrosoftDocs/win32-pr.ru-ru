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
ms.openlocfilehash: b697b8fa2d0715dcf0282c5f32490bfccec79fec
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387680"
---
# <a name="taskfoldergettask-property"></a><span data-ttu-id="1a4cb-106">Таскфолдер. Задание свойства</span><span class="sxs-lookup"><span data-stu-id="1a4cb-106">TaskFolder.GetTask property</span></span>

<span data-ttu-id="1a4cb-107">Для сценариев возвращает задачу в указанном месте в папке.</span><span class="sxs-lookup"><span data-stu-id="1a4cb-107">For scripting, gets a task at a specified location in a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a4cb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a4cb-108">Syntax</span></span>


```VB
TaskFolder.GetTask( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="1a4cb-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1a4cb-109">Property value</span></span>

<span data-ttu-id="1a4cb-110">Путь к задаче в папке (Location).</span><span class="sxs-lookup"><span data-stu-id="1a4cb-110">The path (location) to the task in a folder.</span></span> <span data-ttu-id="1a4cb-111">Корневая папка задач указывается с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="1a4cb-111">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="1a4cb-112">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="1a4cb-112">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="1a4cb-113">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="1a4cb-113">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="1a4cb-114">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="1a4cb-114">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1a4cb-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1a4cb-115">Error codes</span></span>

<span data-ttu-id="1a4cb-116">Задача в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="1a4cb-116">The task at the specified location.</span></span> <span data-ttu-id="1a4cb-117">Задача является объектом [**регистередтаск**](registeredtask.md) .</span><span class="sxs-lookup"><span data-stu-id="1a4cb-117">The task is a [**RegisteredTask**](registeredtask.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a4cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="1a4cb-118">Requirements</span></span>



| <span data-ttu-id="1a4cb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1a4cb-119">Requirement</span></span> | <span data-ttu-id="1a4cb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1a4cb-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a4cb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a4cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a4cb-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1a4cb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1a4cb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a4cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a4cb-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1a4cb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1a4cb-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1a4cb-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1a4cb-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1a4cb-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1a4cb-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1a4cb-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a4cb-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a4cb-128"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





