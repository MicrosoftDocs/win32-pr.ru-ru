---
title: Сложный тип Буттригжертипе
description: Определяет дочерний элемент и сведения о последовательности для элемента Буттригжер.
ms.assetid: 36ade928-7640-4f91-ab76-18398b0cd65f
keywords:
- планировщик задач сложного типа Буттригжертипе
topic_type:
- apiref
api_name:
- bootTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d16634cacb9c17e5027ac9e6b6dd7abb26b78007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492084"
---
# <a name="boottriggertype-complex-type"></a><span data-ttu-id="82986-104">Сложный тип Буттригжертипе</span><span class="sxs-lookup"><span data-stu-id="82986-104">bootTriggerType Complex Type</span></span>

<span data-ttu-id="82986-105">Определяет дочерний элемент и сведения о последовательности для элемента [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="82986-105">Defines the child element and sequencing information for the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="bootTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="Delay"
                    type="duration"
                    default="PT0M"
                    minOccurs="0"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="82986-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="82986-106">Child elements</span></span>



| <span data-ttu-id="82986-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="82986-107">Element</span></span>                                                            | <span data-ttu-id="82986-108">Тип</span><span class="sxs-lookup"><span data-stu-id="82986-108">Type</span></span>     | <span data-ttu-id="82986-109">Описание</span><span class="sxs-lookup"><span data-stu-id="82986-109">Description</span></span>                                                                                 |
|--------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82986-110">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="82986-110">**Delay**</span></span>](taskschedulerschema-delay-boottriggertype-element.md) | <span data-ttu-id="82986-111">длительность</span><span class="sxs-lookup"><span data-stu-id="82986-111">duration</span></span> | <span data-ttu-id="82986-112">Промежуток времени между загрузкой системы и срабатыванием триггера.</span><span class="sxs-lookup"><span data-stu-id="82986-112">Amount of time between when the system is booted and when the trigger is fired.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="82986-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="82986-113">Remarks</span></span>

<span data-ttu-id="82986-114">Помимо дочернего элемента, определенного здесь, элемент [**буттригжер**](taskschedulerschema-boottrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="82986-114">In addition to the child element defined here, the [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="82986-115">Требования</span><span class="sxs-lookup"><span data-stu-id="82986-115">Requirements</span></span>



| <span data-ttu-id="82986-116">Требование</span><span class="sxs-lookup"><span data-stu-id="82986-116">Requirement</span></span> | <span data-ttu-id="82986-117">Значение</span><span class="sxs-lookup"><span data-stu-id="82986-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="82986-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82986-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82986-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="82986-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="82986-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82986-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82986-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="82986-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="82986-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82986-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82986-123">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="82986-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="82986-124">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="82986-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





