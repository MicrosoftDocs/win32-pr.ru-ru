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
ms.openlocfilehash: 308173660ffff7d2062febd087c89cb63bcd8d99
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135419"
---
# <a name="taskfoldergetfolder-property"></a><span data-ttu-id="1565c-106">Таскфолдер. @ Folder, свойство</span><span class="sxs-lookup"><span data-stu-id="1565c-106">TaskFolder.GetFolder property</span></span>

<span data-ttu-id="1565c-107">Для создания скриптов Возвращает папку, содержащую задачи в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="1565c-107">For scripting, gets a folder that contains tasks at a specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="1565c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1565c-108">Syntax</span></span>


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a><span data-ttu-id="1565c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1565c-109">Property value</span></span>

<span data-ttu-id="1565c-110">Путь (расположение) к папке.</span><span class="sxs-lookup"><span data-stu-id="1565c-110">The path (location) to the folder.</span></span> <span data-ttu-id="1565c-111">Не используйте обратную косую черту после имени последней папки в пути.</span><span class="sxs-lookup"><span data-stu-id="1565c-111">Do not use a backslash following the last folder name in the path.</span></span> <span data-ttu-id="1565c-112">Корневая папка задач указывается с помощью обратной косой черты ( \) .</span><span class="sxs-lookup"><span data-stu-id="1565c-112">The root task folder is specified with a backslash (\).</span></span> <span data-ttu-id="1565c-113">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="1565c-113">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="1565c-114">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="1565c-114">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="1565c-115">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="1565c-115">characters cannot be used to specify the parent task folder in the path.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1565c-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="1565c-116">Error codes</span></span>

<span data-ttu-id="1565c-117">Папка в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="1565c-117">The folder at the specified location.</span></span> <span data-ttu-id="1565c-118">Папка является объектом [**таскфолдер**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="1565c-118">The folder is a [**TaskFolder**](taskfolder.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="1565c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="1565c-119">Requirements</span></span>



| <span data-ttu-id="1565c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="1565c-120">Requirement</span></span> | <span data-ttu-id="1565c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="1565c-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1565c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1565c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1565c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1565c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1565c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1565c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1565c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1565c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1565c-126">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1565c-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="1565c-127"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1565c-127"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1565c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="1565c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1565c-129"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1565c-129"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





