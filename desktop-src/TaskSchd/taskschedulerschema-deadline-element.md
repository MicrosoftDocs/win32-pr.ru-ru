---
title: Элемент крайний срок
description: Указывает, когда планировщик задач должен запустить задачу во время аварийного автоматического обслуживания, если это не удалось выполнить во время регулярного автоматического обслуживания.
ms.assetid: 34E33FAE-888E-4E82-83B8-059FB4A64B52
keywords:
- Элемент крайнего срока планировщик задач
topic_type:
- apiref
api_name:
- Deadline
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3e12524971e8b713d4d17817a8a7c7602017bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801774"
---
# <a name="deadline-element"></a><span data-ttu-id="0687a-104">Элемент крайний срок</span><span class="sxs-lookup"><span data-stu-id="0687a-104">Deadline Element</span></span>

<span data-ttu-id="0687a-105">Указывает, когда планировщик задач должен запустить задачу во время аварийного автоматического обслуживания, если это не удалось выполнить во время регулярного автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0687a-105">Specifies when the Task scheduler must to start the task during emergency Automatic maintenance, if it failed to complete during regular Automatic maintenance.</span></span>

<span data-ttu-id="0687a-106">Формат этой строки — *пнинмндтнхнмнс*, где *Москва* — количество лет, NM — это число *месяцев,* равное числу дней, *T* — разделителю даты и времени, *NH* — число *часов, число* минут, а значение *NS* равно числу секунд (например, "PT5M" указывает 5 минут, а "P1M4DT2H5M" — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="0687a-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="0687a-107">Минимальное значение — одна минута.</span><span class="sxs-lookup"><span data-stu-id="0687a-107">The minimum value is one minute.</span></span> <span data-ttu-id="0687a-108">Дополнительные сведения о типе длительности см. в разделе [схема XML, часть 2: тип данных Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="0687a-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span> <span data-ttu-id="0687a-109">Минимальный крайний срок, который может использовать задача, — 1 день.</span><span class="sxs-lookup"><span data-stu-id="0687a-109">Minimum Deadline a task can use is 1 day.</span></span> <span data-ttu-id="0687a-110">Значение элемента **крайнего срока** должно быть больше значения элемента [**period**](taskschedulerschema-period-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0687a-110">The value of the **Deadline** element should be greater than the value of the [**Period**](taskschedulerschema-period-element.md) element.</span></span> <span data-ttu-id="0687a-111">Если крайний срок не указан, задача не будет запущена во время аварийного автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0687a-111">If the deadline is not specified the task will not be started during emergency Automatic maintenance.</span></span>

``` syntax
<xs:element name="Deadline"
    maxOccurs="1"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="P1D"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="0687a-112">Элемент **крайнего срока** определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0687a-112">The **Deadline** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="0687a-113">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0687a-113">Parent element</span></span>



| <span data-ttu-id="0687a-114">Элемент</span><span class="sxs-lookup"><span data-stu-id="0687a-114">Element</span></span>                                                                                                                          | <span data-ttu-id="0687a-115">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="0687a-115">Derived from</span></span>                                                                               | <span data-ttu-id="0687a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0687a-116">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0687a-117">**Маинтенанцесеттингс (Маинтенанцесеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="0687a-117">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="0687a-118">**маинтенанцесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="0687a-118">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="0687a-119">Задает параметры задачи, которые планировщик задач будет использовать для запуска задачи во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="0687a-119">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0687a-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0687a-120">Remarks</span></span>

<span data-ttu-id="0687a-121">При программировании на C++ этот параметр простоя указывается с помощью свойства [**имаинтенанцесеттингс::D еадлине**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) .</span><span class="sxs-lookup"><span data-stu-id="0687a-121">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Deadline**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_deadline) property.</span></span>

## <a name="examples"></a><span data-ttu-id="0687a-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="0687a-122">Examples</span></span>

<span data-ttu-id="0687a-123">Следующий XML-код определяет календарь месяцев, который запускает задачу в марте.</span><span class="sxs-lookup"><span data-stu-id="0687a-123">The following XML defines a months calendar that runs the task in March.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
    <Deadline>P15D</Deadline>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="0687a-124">Требования</span><span class="sxs-lookup"><span data-stu-id="0687a-124">Requirements</span></span>



| <span data-ttu-id="0687a-125">Требование</span><span class="sxs-lookup"><span data-stu-id="0687a-125">Requirement</span></span> | <span data-ttu-id="0687a-126">Значение</span><span class="sxs-lookup"><span data-stu-id="0687a-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0687a-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0687a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0687a-128">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0687a-128">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="0687a-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0687a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0687a-130">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0687a-130">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0687a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0687a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0687a-132">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="0687a-132">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="0687a-133">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0687a-133">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





