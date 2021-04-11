---
title: Тасксеттингс. Дисалловстартифонбаттериес, свойство
description: Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача не будет запущена, если компьютер работает от батарей.
ms.assetid: 5e13f168-a396-495f-a486-e64e8524c8cd
keywords:
- планировщик задач свойства Дисалловстартифонбаттериес
- Планировщик задач свойства Дисалловстартифонбаттериес, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Дисалловстартифонбаттериес
topic_type:
- apiref
api_name:
- TaskSettings.DisallowStartIfOnBatteries
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35a7fde3012b25dfeab65e6e6088bb1d950892d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137010"
---
# <a name="tasksettingsdisallowstartifonbatteries-property"></a><span data-ttu-id="978e0-106">Тасксеттингс. Дисалловстартифонбаттериес, свойство</span><span class="sxs-lookup"><span data-stu-id="978e0-106">TaskSettings.DisallowStartIfOnBatteries property</span></span>

<span data-ttu-id="978e0-107">Для создания скриптов Возвращает или задает логическое значение, указывающее, что задача не будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="978e0-107">For scripting, gets or sets a Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span>

<span data-ttu-id="978e0-108">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="978e0-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="978e0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="978e0-109">Syntax</span></span>


```VB
TaskSettings.DisallowStartIfOnBatteries As Boolean
```



## <a name="property-value"></a><span data-ttu-id="978e0-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="978e0-110">Property value</span></span>

<span data-ttu-id="978e0-111">Логическое значение, указывающее, что задача не будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="978e0-111">A Boolean value that indicates that the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="978e0-112">Если задано значение true, задача не будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="978e0-112">If True, the task will not be started if the computer is running on batteries.</span></span> <span data-ttu-id="978e0-113">Если задано значение false, задача будет запущена, если компьютер работает от батарей.</span><span class="sxs-lookup"><span data-stu-id="978e0-113">If False, the task will be started if the computer is running on batteries.</span></span> <span data-ttu-id="978e0-114">Значение по умолчанию равно True.</span><span class="sxs-lookup"><span data-stu-id="978e0-114">The default is True.</span></span>

## <a name="remarks"></a><span data-ttu-id="978e0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="978e0-115">Remarks</span></span>

<span data-ttu-id="978e0-116">При чтении или записи XML для задачи этот параметр указывается в элементе [**дисалловстартифонбаттериес**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="978e0-116">When reading or writing XML for a task, this setting is specified in the [**DisallowStartIfOnBatteries**](taskschedulerschema-disallowstartifonbatteries-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="978e0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="978e0-117">Requirements</span></span>



| <span data-ttu-id="978e0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="978e0-118">Requirement</span></span> | <span data-ttu-id="978e0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="978e0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="978e0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="978e0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="978e0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="978e0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="978e0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="978e0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="978e0-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="978e0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="978e0-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="978e0-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="978e0-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="978e0-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="978e0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="978e0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="978e0-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="978e0-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="978e0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="978e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978e0-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="978e0-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





