---
title: Таскфолдер. @ Folder, свойство
description: Для создания скриптов Возвращает папку, содержащую задачи в указанном расположении.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- планировщик задач Свойства папки
- Свойство GetObject планировщик задач, объект Таскфолдер
- Объект Таскфолдер планировщик задач, свойство GetObject
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65b3f50cc5b8ab75bb041a61b36ad66bb35891
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387033"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="354bb-106">Таскфолдер. @ Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="354bb-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="354bb-107">Для создания скриптов Возвращает папку, содержащую задачи в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="354bb-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="354bb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="354bb-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="354bb-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="354bb-109">Property value</span></span>

<span data-ttu-id="354bb-110">Путь (расположение) к папке.</span><span class="sxs-lookup"><span data-stu-id="354bb-110">The path (location) to the folder.</span></span> <span data-ttu-id="354bb-111">Не используйте обратную косую черту после имени последней папки в пути.</span><span class="sxs-lookup"><span data-stu-id="354bb-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="354bb-112">Корневая папка задач указывается с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="354bb-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="354bb-113">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="354bb-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="354bb-114">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="354bb-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="354bb-115">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="354bb-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="354bb-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="354bb-116">Error codes</span></span>

<span data-ttu-id="354bb-117">Папка в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="354bb-117">The folder at the specified location.</span></span> <span data-ttu-id="354bb-118">Папка является объектом [**таскфолдер**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="354bb-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="354bb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="354bb-119">Requirements</span></span>



| <span data-ttu-id="354bb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="354bb-120">Requirement</span></span> | <span data-ttu-id="354bb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="354bb-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="354bb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="354bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="354bb-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="354bb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="354bb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="354bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="354bb-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="354bb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="354bb-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="354bb-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="354bb-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="354bb-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="354bb-128">DLL</span><span class="sxs-lookup"><span data-stu-id="354bb-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="354bb-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="354bb-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





