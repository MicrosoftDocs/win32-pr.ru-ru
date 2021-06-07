---
title: Таскфолдер. Креатефолдер, метод
description: Для создания сценариев создает папку для связанных задач.
ms.assetid: 4fdc96bc-8c85-4b36-b3ea-bad7a46c3d35
keywords:
- планировщик задач метода Креатефолдер
- Планировщик задач метода Креатефолдер, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Креатефолдер
topic_type:
- apiref
api_name:
- TaskFolder.CreateFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93a873ef59ea9d099a7a739e5238c722f4b908fd
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387082"
---
# <a name="taskfoldercreatefolder-method"></a><span data-ttu-id="3c2ae-106">Таскфолдер. Креатефолдер, метод</span><span class="sxs-lookup"><span data-stu-id="3c2ae-106">TaskFolder.CreateFolder method</span></span>

<span data-ttu-id="3c2ae-107">Для создания сценариев создает папку для связанных задач.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-107">For scripting, creates a folder for related tasks.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3c2ae-108">Syntax</span></span>


```VB
ppFolder = .CreateFolder( _
  ByVal folderName, _
  ByVal sddl _
)
```



## <a name="parameters"></a><span data-ttu-id="3c2ae-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c2ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2ae-110">*имя_папки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ae-111">Имя, используемое для задания папки.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-111">The name that is used to identify the folder.</span></span> <span data-ttu-id="3c2ae-112">Если указан параметр "имя_папки \\ SubFolder1 \\ SubFolder2", будет создано полное дерево папок, если папки не существуют.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-112">If "FolderName\\SubFolder1\\SubFolder2" is specified, the entire folder tree will be created if the folders do not exist.</span></span> <span data-ttu-id="3c2ae-113">Этот параметр может быть относительным путем к текущему экземпляру [**таскфолдер**](taskfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="3c2ae-113">This parameter can be a relative path to the current [**TaskFolder**](taskfolder.md) instance.</span></span> <span data-ttu-id="3c2ae-114">Корневая папка задач указывается с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="3c2ae-114">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="3c2ae-115">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-115">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="3c2ae-116">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="3c2ae-116">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="3c2ae-117">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-117">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="3c2ae-118">*SDDL* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-118">*sddl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2ae-119">Дескриптор безопасности, связанный с папкой.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-119">The security descriptor that is associated with the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2ae-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c2ae-120">Return value</span></span>

<span data-ttu-id="3c2ae-121">Объект [**таскфолдер**](taskfolder.md) , представляющий новую вложенную папку.</span><span class="sxs-lookup"><span data-stu-id="3c2ae-121">A [**TaskFolder**](taskfolder.md) object that represents the new subfolder.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2ae-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3c2ae-122">Requirements</span></span>



| <span data-ttu-id="3c2ae-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3c2ae-123">Requirement</span></span> | <span data-ttu-id="3c2ae-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3c2ae-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2ae-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c2ae-125">Minimum supported client</span></span><br/> | <span data-ttu-id="3c2ae-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3c2ae-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c2ae-127">Minimum supported server</span></span><br/> | <span data-ttu-id="3c2ae-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c2ae-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c2ae-129">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3c2ae-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="3c2ae-130"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ae-130"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3c2ae-131">DLL</span><span class="sxs-lookup"><span data-stu-id="3c2ae-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c2ae-132"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c2ae-132"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c2ae-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c2ae-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2ae-134">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="3c2ae-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





