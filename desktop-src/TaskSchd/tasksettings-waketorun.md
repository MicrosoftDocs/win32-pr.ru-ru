---
title: Тасксеттингс. Вакеторун, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач выводит компьютер из спящего режима во время выполнения задачи.
ms.assetid: 51f83637-5bae-48c6-b750-b4467e651cec
keywords:
- планировщик задач свойства Вакеторун
- Планировщик задач свойства Вакеторун, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Вакеторун
topic_type:
- apiref
api_name:
- TaskSettings.WakeToRun
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b563fd1ecd27914e84043b85c44f0cf5262e9fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801751"
---
# <a name="tasksettingswaketorun-property"></a><span data-ttu-id="b2001-106">Тасксеттингс. Вакеторун, свойство</span><span class="sxs-lookup"><span data-stu-id="b2001-106">TaskSettings.WakeToRun property</span></span>

<span data-ttu-id="b2001-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что планировщик задач выводит компьютер из спящего режима во время выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="b2001-107">For scripting, gets or sets a Boolean value that indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

<span data-ttu-id="b2001-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b2001-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2001-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2001-109">Syntax</span></span>


```VB
TaskSettings.WakeToRun As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b2001-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b2001-110">Property value</span></span>

<span data-ttu-id="b2001-111">Если значение — true, свойство указывает, что планировщик задач будет выводить компьютер из спящего режима во время выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="b2001-111">If True, the property indicates that the Task Scheduler will wake the computer when it is time to run the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2001-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b2001-112">Remarks</span></span>

<span data-ttu-id="b2001-113">Когда служба планировщик задач пробуждает компьютер для выполнения задачи, экран может остаться недоступным, даже если компьютер больше не находится в спящем или спящем режиме.</span><span class="sxs-lookup"><span data-stu-id="b2001-113">When the Task Scheduler service wakes the computer to run a task, the screen may remain off even though the computer is no longer in the sleep or hibernate mode.</span></span> <span data-ttu-id="b2001-114">Экран будет включен, когда Windows Vista обнаружит, что пользователь вернулся на использование компьютера.</span><span class="sxs-lookup"><span data-stu-id="b2001-114">The screen will turn on when Windows Vista detects that a user has returned to use the computer.</span></span>

<span data-ttu-id="b2001-115">При чтении или записи XML для задачи этот параметр указывается в элементе [**вакеторун**](taskschedulerschema-waketorun-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="b2001-115">When reading or writing XML for a task, this setting is specified in the [**WakeToRun**](taskschedulerschema-waketorun-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2001-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b2001-116">Requirements</span></span>



| <span data-ttu-id="b2001-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b2001-117">Requirement</span></span> | <span data-ttu-id="b2001-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b2001-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2001-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b2001-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2001-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b2001-120">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b2001-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b2001-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2001-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b2001-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b2001-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b2001-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2001-124"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b2001-124"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b2001-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b2001-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2001-126"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2001-126"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2001-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b2001-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2001-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="b2001-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





