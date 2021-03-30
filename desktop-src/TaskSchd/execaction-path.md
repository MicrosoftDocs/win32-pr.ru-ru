---
title: Ексекактион. Path, свойство
description: Для создания скриптов Возвращает или задает путь к исполняемому файлу.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Свойство пути планировщик задач
- Свойство Path планировщик задач, объект Ексекактион
- Планировщик задач объекта Ексекактион, свойство Path
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801793"
---
# <a name="execactionpath-property"></a><span data-ttu-id="9487d-106">Ексекактион. Path, свойство</span><span class="sxs-lookup"><span data-stu-id="9487d-106">ExecAction.Path property</span></span>

<span data-ttu-id="9487d-107">Для создания скриптов Возвращает или задает путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="9487d-107">For scripting, gets or sets the path to an executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9487d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9487d-108">Syntax</span></span>


```VB
ExecAction.Path As String
```



## <a name="property-value"></a><span data-ttu-id="9487d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9487d-109">Property value</span></span>

<span data-ttu-id="9487d-110">Путь к исполняемому файлу, запускаемому действием.</span><span class="sxs-lookup"><span data-stu-id="9487d-110">The path to the executable file to be run by the action.</span></span>

## <a name="remarks"></a><span data-ttu-id="9487d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9487d-111">Remarks</span></span>

<span data-ttu-id="9487d-112">Это действие выполняет операцию командной строки.</span><span class="sxs-lookup"><span data-stu-id="9487d-112">This action performs a command-line operation.</span></span> <span data-ttu-id="9487d-113">Например, действие может выполнить сценарий или запустить исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="9487d-113">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="9487d-114">При чтении или записи XML путь операции командной строки указывается в элементе [**Command**](taskschedulerschema-command-exectype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="9487d-114">When reading or writing XML, the command-line operation path is specified in the [**Command**](taskschedulerschema-command-exectype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="9487d-115">Путь проверяется, чтобы убедиться, что он действителен при регистрации задачи, а не когда это свойство задано.</span><span class="sxs-lookup"><span data-stu-id="9487d-115">The path is checked to make sure it is valid when the task is registered, not when this property is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9487d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9487d-116">Requirements</span></span>



| <span data-ttu-id="9487d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9487d-117">Requirement</span></span> | <span data-ttu-id="9487d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9487d-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9487d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9487d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9487d-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9487d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9487d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9487d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9487d-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9487d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9487d-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9487d-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9487d-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9487d-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9487d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9487d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9487d-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9487d-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9487d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9487d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9487d-128">**ексекактион**</span><span class="sxs-lookup"><span data-stu-id="9487d-128">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="9487d-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="9487d-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





