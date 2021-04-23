---
title: Ексекактион. WorkingDirectory, свойство
description: Для создания скриптов Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- планировщик задач свойства WorkingDirectory
- Планировщик задач свойства WorkingDirectory, объект Ексекактион
- Планировщик задач объекта Ексекактион, свойство WorkingDirectory
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672591"
---
# <a name="execactionworkingdirectory-property"></a><span data-ttu-id="348e7-106">Ексекактион. WorkingDirectory, свойство</span><span class="sxs-lookup"><span data-stu-id="348e7-106">ExecAction.WorkingDirectory property</span></span>

<span data-ttu-id="348e7-107">Для создания скриптов Возвращает или задает каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="348e7-107">For scripting, gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="348e7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="348e7-108">Syntax</span></span>


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a><span data-ttu-id="348e7-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="348e7-109">Property value</span></span>

<span data-ttu-id="348e7-110">Каталог, содержащий исполняемый файл или файлы, используемые исполняемым файлом.</span><span class="sxs-lookup"><span data-stu-id="348e7-110">The directory that contains either the executable file or the files that are used by the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="348e7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="348e7-111">Remarks</span></span>

<span data-ttu-id="348e7-112">При чтении или записи XML рабочий каталог приложения указывается в элементе [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="348e7-112">When reading or writing XML, the working directory of the application is specified in the [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="348e7-113">Путь проверяется, чтобы убедиться, что он действителен при регистрации задачи, а не когда это свойство задано.</span><span class="sxs-lookup"><span data-stu-id="348e7-113">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="348e7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="348e7-114">Requirements</span></span>



| <span data-ttu-id="348e7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="348e7-115">Requirement</span></span> | <span data-ttu-id="348e7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="348e7-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="348e7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="348e7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="348e7-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="348e7-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="348e7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="348e7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="348e7-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="348e7-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="348e7-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="348e7-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="348e7-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="348e7-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="348e7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="348e7-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="348e7-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="348e7-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348e7-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="348e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348e7-126">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="348e7-126">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="348e7-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="348e7-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





