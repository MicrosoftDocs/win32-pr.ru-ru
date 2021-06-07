---
title: Таскфолдер. Делетефолдер, метод
description: Для сценариев удаляет вложенную папку из родительской папки.
ms.assetid: 0d6a9a60-7909-4945-8186-3495e6fe9bc4
keywords:
- планировщик задач метода Делетефолдер
- Планировщик задач метода Делетефолдер, объект Таскфолдер
- Планировщик задач объекта Таскфолдер, метод Делетефолдер
topic_type:
- apiref
api_name:
- TaskFolder.DeleteFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31080f017329cde376b646befd4b7e12ba02926b
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387043"
---
# <a name="taskfolderdeletefolder-method"></a><span data-ttu-id="fd870-106">Таскфолдер. Делетефолдер, метод</span><span class="sxs-lookup"><span data-stu-id="fd870-106">TaskFolder.DeleteFolder method</span></span>

<span data-ttu-id="fd870-107">Для сценариев удаляет вложенную папку из родительской папки.</span><span class="sxs-lookup"><span data-stu-id="fd870-107">For scripting, deletes a subfolder from the parent folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd870-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fd870-108">Syntax</span></span>


```VB
TaskFolder.DeleteFolder( _
  ByVal folderName, _
  ByVal flags _
)
```



## <a name="parameters"></a><span data-ttu-id="fd870-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fd870-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd870-110">*имя_папки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd870-110">*folderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd870-111">Имя удаляемой вложенной папки.</span><span class="sxs-lookup"><span data-stu-id="fd870-111">The name of the subfolder to be removed.</span></span> <span data-ttu-id="fd870-112">Корневая папка задач указывается с помощью обратной косой черты ( \\ ).</span><span class="sxs-lookup"><span data-stu-id="fd870-112">The root task folder is specified with a backslash (\\).</span></span> <span data-ttu-id="fd870-113">Этот параметр может быть относительным путем к папке, которую необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="fd870-113">This parameter can be a relative path to the folder you want to delete.</span></span> <span data-ttu-id="fd870-114">Примером пути к папке задачи в корневой папке задачи является \\ митаскфолдер.</span><span class="sxs-lookup"><span data-stu-id="fd870-114">An example of a task folder path, under the root task folder, is \\MyTaskFolder.</span></span> <span data-ttu-id="fd870-115">Символ "." нельзя использовать для указания текущей папки задач и ".."</span><span class="sxs-lookup"><span data-stu-id="fd870-115">The '.' character cannot be used to specify the current task folder and the '..'</span></span> <span data-ttu-id="fd870-116">символы нельзя использовать для указания родительской папки задач в пути.</span><span class="sxs-lookup"><span data-stu-id="fd870-116">characters cannot be used to specify the parent task folder in the path.</span></span>

</dd> <dt>

<span data-ttu-id="fd870-117">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fd870-117">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd870-118">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fd870-118">Not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd870-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fd870-119">Return value</span></span>

<span data-ttu-id="fd870-120">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="fd870-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd870-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fd870-121">Requirements</span></span>



| <span data-ttu-id="fd870-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fd870-122">Requirement</span></span> | <span data-ttu-id="fd870-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fd870-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd870-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fd870-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fd870-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fd870-125">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd870-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fd870-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fd870-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fd870-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fd870-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fd870-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="fd870-129"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fd870-129"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fd870-130">DLL</span><span class="sxs-lookup"><span data-stu-id="fd870-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd870-131"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd870-131"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd870-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fd870-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd870-133">**таскфолдер**</span><span class="sxs-lookup"><span data-stu-id="fd870-133">**TaskFolder**</span></span>](taskfolder.md)
</dt> <dt>

[<span data-ttu-id="fd870-134">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fd870-134">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





