---
title: Тасксеттингс. Hidden, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача не будет отображаться в пользовательском интерфейсе.
ms.assetid: 84a3d0b3-30f0-4356-b6cf-9bee3091612f
keywords:
- планировщик задач скрытого свойства
- Планировщик задач скрытого свойства, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, скрытое свойство
topic_type:
- apiref
api_name:
- TaskSettings.Hidden
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057a3d920ba70260d23ad13a5888072ab5b07767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803203"
---
# <a name="tasksettingshidden-property"></a><span data-ttu-id="ddacf-106">Тасксеттингс. Hidden, свойство</span><span class="sxs-lookup"><span data-stu-id="ddacf-106">TaskSettings.Hidden property</span></span>

<span data-ttu-id="ddacf-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача не будет отображаться в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ddacf-107">For scripting, gets or sets a Boolean value that indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="ddacf-108">Однако администраторы могут переопределить этот параметр с помощью "главного коммутатора", который делает все задачи видимыми в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ddacf-108">However, administrators can override this setting through the use of a "master switch" that makes all tasks visible in the UI.</span></span>

<span data-ttu-id="ddacf-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ddacf-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddacf-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ddacf-110">Syntax</span></span>


```VB
TaskSettings.Hidden As Boolean
```



## <a name="property-value"></a><span data-ttu-id="ddacf-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ddacf-111">Property value</span></span>

<span data-ttu-id="ddacf-112">Значение **true** показывает, что задача не будет видима в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ddacf-112">If **True**, the value indicates that the task will not be visible in the UI.</span></span> <span data-ttu-id="ddacf-113">Если задано **значение false**, задача будет видима в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="ddacf-113">If **False**, the task will be visible in the UI.</span></span> <span data-ttu-id="ddacf-114">По умолчанию **False**.</span><span class="sxs-lookup"><span data-stu-id="ddacf-114">The default is **False**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddacf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ddacf-115">Remarks</span></span>

<span data-ttu-id="ddacf-116">При чтении или записи XML для задачи этот параметр указывается в [**скрытом элементе (сеттингстипе)**](taskschedulerschema-hidden-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="ddacf-116">When reading or writing XML for a task, this setting is specified in the [**Hidden (settingsType)**](taskschedulerschema-hidden-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddacf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ddacf-117">Requirements</span></span>



| <span data-ttu-id="ddacf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ddacf-118">Requirement</span></span> | <span data-ttu-id="ddacf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ddacf-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddacf-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddacf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ddacf-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ddacf-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ddacf-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddacf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ddacf-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ddacf-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ddacf-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="ddacf-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddacf-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ddacf-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ddacf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="ddacf-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddacf-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddacf-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddacf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddacf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddacf-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ddacf-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





