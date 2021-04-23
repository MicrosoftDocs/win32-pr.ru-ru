---
title: Тасксеттингс. Делетикспиредтаскафтер, свойство
description: Для создания скриптов Возвращает или задает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.
ms.assetid: c57d736c-e3ce-44b8-809e-44f7c0321d70
keywords:
- планировщик задач свойства Делетикспиредтаскафтер
- Планировщик задач свойства Делетикспиредтаскафтер, объект Тасксеттингс
- Планировщик задач объекта Тасксеттингс, свойство Делетикспиредтаскафтер
topic_type:
- apiref
api_name:
- TaskSettings.DeleteExpiredTaskAfter
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9005ff7988353daa902b1bc3151c539713bb94ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489849"
---
# <a name="tasksettingsdeleteexpiredtaskafter-property"></a><span data-ttu-id="4c5b2-106">Тасксеттингс. Делетикспиредтаскафтер, свойство</span><span class="sxs-lookup"><span data-stu-id="4c5b2-106">TaskSettings.DeleteExpiredTaskAfter property</span></span>

<span data-ttu-id="4c5b2-107">Для создания скриптов Возвращает или задает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-107">For scripting, gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="4c5b2-108">Если для этого свойства не указано значение, то служба планировщик задач не удалит задачу.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-108">If no value is specified for this property, then the Task Scheduler service will not delete the task.</span></span>

<span data-ttu-id="4c5b2-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5b2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c5b2-110">Syntax</span></span>


```VB
TaskSettings.DeleteExpiredTaskAfter As String
```



## <a name="property-value"></a><span data-ttu-id="4c5b2-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4c5b2-111">Property value</span></span>

<span data-ttu-id="4c5b2-112">Строка, которая возвращает или задает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-112">A string that gets or sets the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="4c5b2-113">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="4c5b2-113">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c5b2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c5b2-114">Remarks</span></span>

<span data-ttu-id="4c5b2-115">Срок действия задачи истекает после того, как превышена конечная граница для всех триггеров, связанных с задачей.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-115">A task expires after the end boundary has been exceeded for all triggers associated with the task.</span></span> <span data-ttu-id="4c5b2-116">Конечная граница триггера задается свойством [ендбаундари](trigger-endboundary.md) , унаследованным всеми объектами Trigger.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-116">The end boundary for a trigger is specified by the [EndBoundary](trigger-endboundary.md) property inherited by all trigger objects.</span></span>

<span data-ttu-id="4c5b2-117">При чтении или записи XML для задачи этот параметр указывается в элементе [**делетикспиредтаскафтер (сеттингстипе)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="4c5b2-117">When reading or writing XML for a task, this setting is specified in the [**DeleteExpiredTaskAfter (settingsType)**](taskschedulerschema-deleteexpiredtaskafter-settingstype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5b2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="4c5b2-118">Requirements</span></span>



| <span data-ttu-id="4c5b2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="4c5b2-119">Requirement</span></span> | <span data-ttu-id="4c5b2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="4c5b2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5b2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c5b2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5b2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c5b2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="4c5b2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c5b2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5b2-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c5b2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c5b2-125">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4c5b2-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c5b2-126"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c5b2-126"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c5b2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5b2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5b2-128"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5b2-128"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5b2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c5b2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5b2-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="4c5b2-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





