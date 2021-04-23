---
title: Period, элемент
description: Указывает, как часто задача должна запускаться во время автоматического обслуживания.
ms.assetid: E4BE2466-3119-41F8-8238-4627C28B26E5
keywords:
- Элемент period планировщик задач
topic_type:
- apiref
api_name:
- Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a507a9b0a8f97d1ae4e6c8df654a45d67b77767
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493122"
---
# <a name="period-element"></a><span data-ttu-id="c553d-104">Period, элемент</span><span class="sxs-lookup"><span data-stu-id="c553d-104">Period Element</span></span>

<span data-ttu-id="c553d-105">Указывает, как часто задача должна запускаться во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c553d-105">Specifies how often the task needs to be started during Automatic maintenance.</span></span>

<span data-ttu-id="c553d-106">Формат этой строки — *пнинмндтнхнмнс*, где *Москва* — количество лет, NM — это число *месяцев,* равное числу дней, *T* — разделителю даты и времени, *NH* — число *часов, число* минут, а значение *NS* равно числу секунд (например, "PT5M" указывает 5 минут, а "P1M4DT2H5M" — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="c553d-106">The format for this string is *PnYnMnDTnHnMnS*, where *nY* is the number of years, nM is the number of months, *nD* is the number of days, *T* is the date/time separator, *nH* is the number of hours, *nM* is the number of minutes, and *nS* is the number of seconds (for example, "PT5M" specifies 5 minutes and "P1M4DT2H5M" specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="c553d-107">Минимальное значение — одна минута.</span><span class="sxs-lookup"><span data-stu-id="c553d-107">The minimum value is one minute.</span></span> <span data-ttu-id="c553d-108">Дополнительные сведения о типе длительности см. в разделе [схема XML, часть 2: тип данных Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span><span class="sxs-lookup"><span data-stu-id="c553d-108">For more information about the duration type, see [XML Schema Part 2: Datatypes Second Edition](https://www.w3.org/TR/xmlschema-2/#duration).</span></span>

``` syntax
<xs:element name="Period"
    maxOccurs="1"
    minOccurs="1"
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

<span data-ttu-id="c553d-109">Элемент **period** определяется сложным типом [**маинтенанцесеттингстипе**](taskschedulerschema-maintenancesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c553d-109">The **Period** element is defined by the [**maintenanceSettingsType**](taskschedulerschema-maintenancesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c553d-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="c553d-110">Parent element</span></span>



| <span data-ttu-id="c553d-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="c553d-111">Element</span></span>                                                                                                                          | <span data-ttu-id="c553d-112">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="c553d-112">Derived from</span></span>                                                                               | <span data-ttu-id="c553d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="c553d-113">Description</span></span>                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c553d-114">**Маинтенанцесеттингс (Маинтенанцесеттингстипе)**</span><span class="sxs-lookup"><span data-stu-id="c553d-114">**MaintenanceSettings (maintenanceSettingsType)**</span></span>](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) | [<span data-ttu-id="c553d-115">**маинтенанцесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="c553d-115">**maintenanceSettingsType**</span></span>](taskschedulerschema-maintenancesettingstype-complextype.md) | <span data-ttu-id="c553d-116">Задает параметры задачи, которые планировщик задач будет использовать для запуска задачи во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c553d-116">Specifies the task settings the Task scheduler will use to start task during Automatic maintenance.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c553d-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c553d-117">Remarks</span></span>

<span data-ttu-id="c553d-118">При программировании на C++ этот параметр простоя указывается с помощью свойства [**имаинтенанцесеттингс::P ериод**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) .</span><span class="sxs-lookup"><span data-stu-id="c553d-118">For C++ programming, this idle setting is specified using the [**IMaintenanceSettings::Period**](/windows/desktop/api/Taskschd/nf-taskschd-imaintenancesettings-get_period) property.</span></span>

## <a name="examples"></a><span data-ttu-id="c553d-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="c553d-119">Examples</span></span>

<span data-ttu-id="c553d-120">Следующий код XML определяет задачу обслуживания с требованием периодичности, равным 5 дням.</span><span class="sxs-lookup"><span data-stu-id="c553d-120">The following XML defines maintenance task with periodicity requirement set to 5 days.</span></span>


```XML
<MaintenanceSettings>
    <Period>P5D</Period>
</MaintenanceSettings>
```



## <a name="requirements"></a><span data-ttu-id="c553d-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c553d-121">Requirements</span></span>



| <span data-ttu-id="c553d-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c553d-122">Requirement</span></span> | <span data-ttu-id="c553d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c553d-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c553d-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c553d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c553d-125">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c553d-125">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="c553d-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c553d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c553d-127">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c553d-127">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c553d-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c553d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c553d-129">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="c553d-129">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c553d-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="c553d-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





