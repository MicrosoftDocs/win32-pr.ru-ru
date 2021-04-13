---
title: Ваиттимеаут (Идлесеттингстипе), элемент
description: Указывает период времени, в течение которого планировщик задач будет ожидать наступления условия простоя.
ms.assetid: 6a4cc80d-adc2-47a7-946f-a9f12eeb35a4
keywords:
- планировщик задач элемента Ваиттимеаут
topic_type:
- apiref
api_name:
- WaitTimeout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16f71a014358a8e0520274d1ff853cf6146aa05d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534865"
---
# <a name="waittimeout-idlesettingstype-element"></a><span data-ttu-id="d7ab2-104">Ваиттимеаут (Идлесеттингстипе), элемент</span><span class="sxs-lookup"><span data-stu-id="d7ab2-104">WaitTimeout (idleSettingsType) Element</span></span>

<span data-ttu-id="d7ab2-105">Указывает период времени, в течение которого планировщик задач будет ожидать наступления условия простоя.</span><span class="sxs-lookup"><span data-stu-id="d7ab2-105">Specifies the amount of time that the Task Scheduler will wait for an idle condition to occur.</span></span> <span data-ttu-id="d7ab2-106">Если для этого элемента не указано значение, то служба планировщик задач будет ждать неопределенное время, пока не произойдет условие простоя.</span><span class="sxs-lookup"><span data-stu-id="d7ab2-106">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span> <span data-ttu-id="d7ab2-107">Формат этой строки — Пнинмндтнхнмнс, где Нью-то число лет, nM — это количество месяцев, а — число дней, равное, т. е. в качестве разделителя даты и времени, nH — это количество часов, а в качестве значения nS — количество секунд (например, PT5M указывает 5 минут, а P1M4DT2H5M — один месяц, четыре дня, два часа и пять минут).</span><span class="sxs-lookup"><span data-stu-id="d7ab2-107">The format for this string is PnYnMnDTnHnMnS, where nY is the number of years, nM is the number of months, nD is the number of days, 'T' is the date/time separator, nH is the number of hours, nM is the number of minutes, and nS is the number of seconds (for example, PT5M specifies 5 minutes and P1M4DT2H5M specifies one month, four days, two hours, and five minutes).</span></span> <span data-ttu-id="d7ab2-108">Дополнительные сведения о типе длительности см. в разделе <https://go.microsoft.com/fwlink/p/?linkid=106886> .</span><span class="sxs-lookup"><span data-stu-id="d7ab2-108">For more information about the duration type, see <https://go.microsoft.com/fwlink/p/?linkid=106886>.</span></span> <span data-ttu-id="d7ab2-109">Минимальное допустимое время — 1 минута.</span><span class="sxs-lookup"><span data-stu-id="d7ab2-109">The minimum time allowed is 1 minute.</span></span>

``` syntax
<xs:element name="WaitTimeout"
    default="PT1H"
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

<span data-ttu-id="d7ab2-110">Элемент определяется сложным типом [**идлесеттингстипе**](taskschedulerschema-idlesettingstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ab2-110">The element is defined by the [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="d7ab2-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d7ab2-111">Parent element</span></span>



| <span data-ttu-id="d7ab2-112">Элемент</span><span class="sxs-lookup"><span data-stu-id="d7ab2-112">Element</span></span>                                                                       | <span data-ttu-id="d7ab2-113">Унаследован от</span><span class="sxs-lookup"><span data-stu-id="d7ab2-113">Derived from</span></span>                                                                 | <span data-ttu-id="d7ab2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d7ab2-114">Description</span></span>                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7ab2-115">**идлесеттингс**</span><span class="sxs-lookup"><span data-stu-id="d7ab2-115">**IdleSettings**</span></span>](taskschedulerschema-idlesettings-settingstype-element.md) | [<span data-ttu-id="d7ab2-116">**идлесеттингстипе**</span><span class="sxs-lookup"><span data-stu-id="d7ab2-116">**idleSettingsType**</span></span>](taskschedulerschema-idlesettingstype-complextype.md) | <span data-ttu-id="d7ab2-117">Указывает, как планировщик задач выполняет задачи, когда компьютер находится в состоянии простоя.</span><span class="sxs-lookup"><span data-stu-id="d7ab2-117">Specifies how the Task Scheduler performs tasks when the computer is in an idle state.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d7ab2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7ab2-118">Remarks</span></span>

<span data-ttu-id="d7ab2-119">Для разработки скриптов этот параметр простоя указывается с помощью свойства [**идлесеттингс. ваиттимеаут**](idlesettings-waittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="d7ab2-119">For script development, this idle setting is specified using the [**IdleSettings.WaitTimeout**](idlesettings-waittimeout.md) property.</span></span>

<span data-ttu-id="d7ab2-120">Для разработки на C++ этот параметр простоя указывается с помощью свойства [**иидлесеттингс:: ваиттимеаут**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) .</span><span class="sxs-lookup"><span data-stu-id="d7ab2-120">For C++ development, this idle setting is specified using the [**IIdleSettings::WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) property.</span></span>

## <a name="examples"></a><span data-ttu-id="d7ab2-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="d7ab2-121">Examples</span></span>

<span data-ttu-id="d7ab2-122">Следующий XML-код определяет параметр простоя, который ждет 24 часа при возникновении условия простоя.</span><span class="sxs-lookup"><span data-stu-id="d7ab2-122">The following XML defines an idle setting that waits 24 hours for an idle condition to occur.</span></span>


```XML
<IdleSettings>
    <WaitTimeout>PT24H</WaitTimeout>
</IdleSettings>
```



## <a name="requirements"></a><span data-ttu-id="d7ab2-123">Требования</span><span class="sxs-lookup"><span data-stu-id="d7ab2-123">Requirements</span></span>



| <span data-ttu-id="d7ab2-124">Требование</span><span class="sxs-lookup"><span data-stu-id="d7ab2-124">Requirement</span></span> | <span data-ttu-id="d7ab2-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d7ab2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d7ab2-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7ab2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ab2-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7ab2-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d7ab2-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7ab2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ab2-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d7ab2-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d7ab2-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7ab2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ab2-131">планировщик задач элементы схемы</span><span class="sxs-lookup"><span data-stu-id="d7ab2-131">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d7ab2-132">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="d7ab2-132">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





