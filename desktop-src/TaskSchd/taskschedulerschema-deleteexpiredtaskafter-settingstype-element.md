---
title: Делетикспиредтаскафтер (Сеттингстипе), элемент
description: Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- планировщик задач элемента Делетикспиредтаскафтер
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cee7cfc48f62b58caf63125404fb07209b399fc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681850"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a><span data-ttu-id="e281e-104">Делетикспиредтаскафтер (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="e281e-104">DeleteExpiredTaskAfter (settingsType) Element</span></span>

<span data-ttu-id="e281e-105">Указывает период времени, в течение которого планировщик задач будет ожидать перед удалением задачи после истечения ее срока действия.</span><span class="sxs-lookup"><span data-stu-id="e281e-105">Specifies the amount of time that the Task Scheduler will wait before deleting the task after it expires.</span></span> <span data-ttu-id="e281e-106">Если для этого элемента не указано значение, то служба планировщик задач не удалит задачу.</span><span class="sxs-lookup"><span data-stu-id="e281e-106">If no value is specified for this element, then the Task Scheduler service will not delete the task.</span></span> <span data-ttu-id="e281e-107">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="e281e-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="e281e-108">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="e281e-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

<span data-ttu-id="e281e-109">Элемент **делетикспиредтаскафтер** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="e281e-109">The **DeleteExpiredTaskAfter** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="e281e-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e281e-110">Parent element</span></span>



| <span data-ttu-id="e281e-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="e281e-111">Element</span></span>                                                           | <span data-ttu-id="e281e-112">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="e281e-112">Derived from</span></span>                                                         | <span data-ttu-id="e281e-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e281e-113">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="e281e-114">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="e281e-114">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="e281e-115">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="e281e-115">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="e281e-116">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="e281e-116">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e281e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e281e-117">Remarks</span></span>

<span data-ttu-id="e281e-118">Сведения о разработке на языке C++ см. в разделе [**свойство делетикспиредтаскафтер объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span><span class="sxs-lookup"><span data-stu-id="e281e-118">For C++ development, see [**DeleteExpiredTaskAfter Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter).</span></span>

<span data-ttu-id="e281e-119">Сведения о разработке сценариев см. в разделе [**тасксеттингс. делетикспиредтаскафтер**](tasksettings-deleteexpiredtaskafter.md).</span><span class="sxs-lookup"><span data-stu-id="e281e-119">For script development, see [**TaskSettings.DeleteExpiredTaskAfter**](tasksettings-deleteexpiredtaskafter.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e281e-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="e281e-120">Examples</span></span>

<span data-ttu-id="e281e-121">Следующий XML-код определяет элемент Settings, который удаляет просроченную задачу через одну неделю.</span><span class="sxs-lookup"><span data-stu-id="e281e-121">The following XML defines a settings element that deletes an expired task after one week.</span></span>


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
</Settings>
```



## <a name="requirements"></a><span data-ttu-id="e281e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e281e-122">Requirements</span></span>



| <span data-ttu-id="e281e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e281e-123">Requirement</span></span> | <span data-ttu-id="e281e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e281e-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e281e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e281e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e281e-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e281e-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e281e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e281e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e281e-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e281e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e281e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e281e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e281e-130">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="e281e-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





