---
title: Ексекутионтимелимит (Сеттингстипе), элемент
description: Количество времени, отведенное на выполнение задачи.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- планировщик задач элемента Ексекутионтимелимит
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891581"
---
# <a name="executiontimelimit-settingstype-element"></a><span data-ttu-id="f538a-104">Ексекутионтимелимит (Сеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="f538a-104">ExecutionTimeLimit (settingsType) Element</span></span>

<span data-ttu-id="f538a-105">Количество времени, отведенное на выполнение задачи. Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="f538a-105">Amount of time allowed to complete the task.The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="f538a-106">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="f538a-106">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="f538a-107">Значение PT0S позволит задаче выполняться неограниченное время.</span><span class="sxs-lookup"><span data-stu-id="f538a-107">A value of PT0S will enable the task to run indefinitely.</span></span>

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

<span data-ttu-id="f538a-108">Элемент **ексекутионтимелимит** определяется сложным типом [**сеттингстипе**](taskschedulerschema-settingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f538a-108">The **ExecutionTimeLimit** element is defined by the [**settingsType**](taskschedulerschema-settingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f538a-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f538a-109">Parent element</span></span>



| <span data-ttu-id="f538a-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="f538a-110">Element</span></span>                                                           | <span data-ttu-id="f538a-111">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="f538a-111">Derived from</span></span>                                                         | <span data-ttu-id="f538a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f538a-112">Description</span></span>                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="f538a-113">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="f538a-113">**Settings**</span></span>](taskschedulerschema-settings-tasktype-element.md) | [<span data-ttu-id="f538a-114">**сеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="f538a-114">**settingsType**</span></span>](taskschedulerschema-settingstype-complextype.md) | <span data-ttu-id="f538a-115">Содержит параметры, которые планировщик задач использует для выполнения задачи.</span><span class="sxs-lookup"><span data-stu-id="f538a-115">Contains the settings that the Task Scheduler uses to perform the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f538a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f538a-116">Remarks</span></span>

<span data-ttu-id="f538a-117">Сведения о разработке на языке C++ см. в разделе [**свойство ексекутионтимелимит объекта итасксеттингс**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span><span class="sxs-lookup"><span data-stu-id="f538a-117">For C++ development, see [**ExecutionTimeLimit Property of ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).</span></span>

<span data-ttu-id="f538a-118">Сведения о разработке сценариев см. в разделе [**TaskSettings.Exeкутионтимелимит**](tasksettings-executiontimelimit.md).</span><span class="sxs-lookup"><span data-stu-id="f538a-118">For script development, see [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f538a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f538a-119">Requirements</span></span>



| <span data-ttu-id="f538a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f538a-120">Requirement</span></span> | <span data-ttu-id="f538a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f538a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f538a-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f538a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f538a-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f538a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f538a-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f538a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f538a-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f538a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f538a-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f538a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f538a-127">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="f538a-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





