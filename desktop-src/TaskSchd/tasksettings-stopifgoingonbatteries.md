---
title: Тасксеттингс. Стопифгоингонбаттериес, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача будет остановлена, если компьютер перейдет в аккумулятор.
ms.assetid: a133cba0-c93e-4963-83a3-7587e323fc6e
keywords:
- планировщик задач свойства Стопифгоингонбаттериес
- Планировщик задач свойства Стопифгоингонбаттериес, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Стопифгоингонбаттериес
topic_type:
- apiref
api_name:
- TaskSettings.StopIfGoingOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aced436d653b6bbc02b4b36edea9046e3ac62392
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492246"
---
# <a name="tasksettingsstopifgoingonbatteries-property"></a><span data-ttu-id="63573-106">Тасксеттингс. Стопифгоингонбаттериес, свойство</span><span class="sxs-lookup"><span data-stu-id="63573-106">TaskSettings.StopIfGoingOnBatteries property</span></span>

<span data-ttu-id="63573-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача будет остановлена, если компьютер перейдет в аккумулятор.</span><span class="sxs-lookup"><span data-stu-id="63573-107">For scripting, gets or sets a Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span>

<span data-ttu-id="63573-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="63573-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63573-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63573-109">Syntax</span></span>


```VB
TaskSettings.StopIfGoingOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="63573-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="63573-110">Property value</span></span>

<span data-ttu-id="63573-111">Логическое значение, указывающее, что задача будет остановлена при переходе компьютера на питание.</span><span class="sxs-lookup"><span data-stu-id="63573-111">A Boolean value that indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="63573-112">Если значение — true, свойство указывает, что задача будет остановлена при переходе компьютера на питание.</span><span class="sxs-lookup"><span data-stu-id="63573-112">If True, the property indicates that the task will be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="63573-113">Если значение равно false, свойство указывает, что задача не будет остановлена, если компьютер переходит в аккумулятор.</span><span class="sxs-lookup"><span data-stu-id="63573-113">If False, the property indicates that the task will not be stopped if the computer is going onto batteries.</span></span> <span data-ttu-id="63573-114">Значение по умолчанию равно True.</span><span class="sxs-lookup"><span data-stu-id="63573-114">The default is True.</span></span> <span data-ttu-id="63573-115">Дополнительные сведения см. в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="63573-115">See Remarks for more details.</span></span>

## <a name="remarks"></a><span data-ttu-id="63573-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63573-116">Remarks</span></span>

<span data-ttu-id="63573-117">При чтении или записи XML для задачи этот параметр указывается в элементе [**стопифгоингонбаттериес**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="63573-117">When reading or writing XML for a task, this setting is specified in the [**StopIfGoingOnBatteries**](taskschedulerschema-stopifgoingonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="63573-118">Требования</span><span class="sxs-lookup"><span data-stu-id="63573-118">Requirements</span></span>



| <span data-ttu-id="63573-119">Требование</span><span class="sxs-lookup"><span data-stu-id="63573-119">Requirement</span></span> | <span data-ttu-id="63573-120">Значение</span><span class="sxs-lookup"><span data-stu-id="63573-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63573-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63573-121">Minimum supported client</span></span><br/> | <span data-ttu-id="63573-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63573-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="63573-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63573-123">Minimum supported server</span></span><br/> | <span data-ttu-id="63573-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63573-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63573-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="63573-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="63573-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63573-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63573-127">DLL</span><span class="sxs-lookup"><span data-stu-id="63573-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63573-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63573-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63573-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63573-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63573-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="63573-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





