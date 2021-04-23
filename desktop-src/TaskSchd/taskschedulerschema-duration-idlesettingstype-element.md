---
title: Duration (Идлесеттингстипе), элемент
description: Указывает, как долго компьютер должен находиться в состоянии простоя перед выполнением задачи.
ms.assetid: 89584694-0685-44e2-b8b7-69e47ee28d5d
keywords:
- Элемент Duration планировщик задач
topic_type:
- apiref
api_name:
- Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31ad092693c72dcc33357f4b7e21436e2cba8af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533950"
---
# <a name="duration-idlesettingstype-element"></a><span data-ttu-id="381b3-104">Duration (Идлесеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="381b3-104">Duration (idleSettingsType) Element</span></span>

<span data-ttu-id="381b3-105">Указывает, как долго компьютер должен находиться в состоянии простоя перед выполнением задачи.</span><span class="sxs-lookup"><span data-stu-id="381b3-105">Specifies how long the computer must be in an idle state before the task is run.</span></span> <span data-ttu-id="381b3-106">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="381b3-106">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="381b3-107">Минимальное значение — одна минута.</span><span class="sxs-lookup"><span data-stu-id="381b3-107">The minimum value is one minute.</span></span> <span data-ttu-id="381b3-108">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="381b3-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span>

``` syntax
<xs:element name="Duration"
    default="PT10M"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="duration"
        >
            <xs:minInclusive
                value="PT1M"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="381b3-109">Элемент определяется сложным типом [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="381b3-109">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="381b3-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="381b3-110">Parent element</span></span>



| <span data-ttu-id="381b3-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="381b3-111">Element</span></span>                                                                       | <span data-ttu-id="381b3-112">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="381b3-112">Derived from</span></span>                                                                 | <span data-ttu-id="381b3-113">Описание</span><span class="sxs-lookup"><span data-stu-id="381b3-113">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="381b3-114">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="381b3-114">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="381b3-115">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="381b3-115">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="381b3-116">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="381b3-116">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="381b3-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="381b3-117">Remarks</span></span>

<span data-ttu-id="381b3-118">Для программирования скриптов этот параметр простоя указывается с помощью свойства [**идлесеттингс. идледуратион**](idlesettings-idleduration.md) .</span><span class="sxs-lookup"><span data-stu-id="381b3-118">For script programming, this idle setting is specified using the [**IdleSettings.IdleDuration**](idlesettings-idleduration.md) property.</span></span>

<span data-ttu-id="381b3-119">При программировании на C++ этот параметр простоя указывается с помощью свойства [**иидлесеттингс:: идледуратион**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) .</span><span class="sxs-lookup"><span data-stu-id="381b3-119">For C++ programming, this idle setting is specified using the [**IIdleSettings::IdleDuration**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_idleduration) property.</span></span>

## <a name="examples"></a><span data-ttu-id="381b3-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="381b3-120">Examples</span></span>

<span data-ttu-id="381b3-121">Следующий XML-код определяет параметр бездействия, который разрешает запуск задачи в течение 5 минут.</span><span class="sxs-lookup"><span data-stu-id="381b3-121">The following XML defines an idle setting that allows 5 minutes for the task to start.</span></span>


```XML
<IdleSettings>
    <Duration>PT5M</Duration>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="381b3-122">Требования</span><span class="sxs-lookup"><span data-stu-id="381b3-122">Requirements</span></span>



| <span data-ttu-id="381b3-123">Требование</span><span class="sxs-lookup"><span data-stu-id="381b3-123">Requirement</span></span> | <span data-ttu-id="381b3-124">Значение</span><span class="sxs-lookup"><span data-stu-id="381b3-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="381b3-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="381b3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="381b3-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="381b3-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="381b3-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="381b3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="381b3-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="381b3-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="381b3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="381b3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381b3-130">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="381b3-130">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="381b3-131">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="381b3-131">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





