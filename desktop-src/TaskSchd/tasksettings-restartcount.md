---
title: Тасксеттингс. Рестарткаунт, свойство
description: Для сценариев Возвращает или задает количество попыток перезапуска задачи планировщик задач.
ms.assetid: 7d92c2c6-e846-4664-b22a-b2a6ca46c225
keywords:
- планировщик задач свойства Рестарткаунт
- Планировщик задач свойства Рестарткаунт, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Рестарткаунт
topic_type:
- apiref
api_name:
- TaskSettings.RestartCount
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bee033eebde7b085d6df40f1e5e20d6dcf640a93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415220"
---
# <a name="tasksettingsrestartcount-property"></a><span data-ttu-id="1dece-106">Тасксеттингс. Рестарткаунт, свойство</span><span class="sxs-lookup"><span data-stu-id="1dece-106">TaskSettings.RestartCount property</span></span>

<span data-ttu-id="1dece-107">Для сценариев Возвращает или задает количество попыток перезапуска задачи планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="1dece-107">For scripting, gets or sets the number of times that the Task Scheduler will attempt to restart the task.</span></span>

<span data-ttu-id="1dece-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1dece-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dece-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dece-109">Syntax</span></span>


```VB
TaskSettings.RestartCount As Integer
```



## <a name="property-value"></a><span data-ttu-id="1dece-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1dece-110">Property value</span></span>

<span data-ttu-id="1dece-111">Количество попыток перезапуска задачи планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="1dece-111">The number of times that the Task Scheduler will attempt to restart the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dece-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1dece-112">Remarks</span></span>

<span data-ttu-id="1dece-113">При чтении или записи XML для задачи этот параметр указывается в элементе [**Count**](taskschedulerschema-count-restarttype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="1dece-113">When reading or writing XML for a task, this setting is specified in the [**Count**](taskschedulerschema-count-restarttype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dece-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1dece-114">Requirements</span></span>



| <span data-ttu-id="1dece-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1dece-115">Requirement</span></span> | <span data-ttu-id="1dece-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1dece-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dece-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1dece-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1dece-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1dece-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1dece-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1dece-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1dece-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1dece-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1dece-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="1dece-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="1dece-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1dece-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1dece-123">DLL</span><span class="sxs-lookup"><span data-stu-id="1dece-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dece-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dece-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dece-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dece-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dece-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="1dece-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





