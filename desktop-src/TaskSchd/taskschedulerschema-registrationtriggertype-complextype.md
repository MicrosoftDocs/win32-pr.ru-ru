---
title: Сложный тип Регистратионтригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Регистратионтригжер.
ms.assetid: 3663c015-67cf-4775-a1a6-4429cce93b96
keywords:
- планировщик задач сложного типа Регистратионтригжертипе
topic_type:
- apiref
api_name:
- registrationTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2ddb55436a0a6980a8909da636a02ca59244ca85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415873"
---
# <a name="registrationtriggertype-complex-type"></a><span data-ttu-id="31391-104">Сложный тип Регистратионтригжертипе</span><span class="sxs-lookup"><span data-stu-id="31391-104">registrationTriggerType Complex Type</span></span>

<span data-ttu-id="31391-105">Определяет дочерние элементы и сведения о последовательности для элемента [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="31391-105">Defines child elements and sequencing information for the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="registrationTriggerType">
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

## <a name="child-elements"></a><span data-ttu-id="31391-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31391-106">Child elements</span></span>



| <span data-ttu-id="31391-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="31391-107">Element</span></span>                                                                    | <span data-ttu-id="31391-108">Тип</span><span class="sxs-lookup"><span data-stu-id="31391-108">Type</span></span>     | <span data-ttu-id="31391-109">Описание</span><span class="sxs-lookup"><span data-stu-id="31391-109">Description</span></span>                                                                                               |
|----------------------------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31391-110">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="31391-110">**Delay**</span></span>](taskschedulerschema-delay-registrationtriggertype-element.md) | <span data-ttu-id="31391-111">длительность</span><span class="sxs-lookup"><span data-stu-id="31391-111">duration</span></span> | <span data-ttu-id="31391-112">Указывает промежуток времени между регистрацией задачи и началом задачи.</span><span class="sxs-lookup"><span data-stu-id="31391-112">Specifies the amount of time between when the task is registered and when the task is started.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31391-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="31391-113">Remarks</span></span>

<span data-ttu-id="31391-114">Помимо дочерних элементов, определенных здесь, элемент [**регистратионтригжер**](taskschedulerschema-registrationtrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="31391-114">In addition to the child elements defined here, the [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="31391-115">Требования</span><span class="sxs-lookup"><span data-stu-id="31391-115">Requirements</span></span>



| <span data-ttu-id="31391-116">Требование</span><span class="sxs-lookup"><span data-stu-id="31391-116">Requirement</span></span> | <span data-ttu-id="31391-117">Значение</span><span class="sxs-lookup"><span data-stu-id="31391-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31391-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="31391-118">Minimum supported client</span></span><br/> | <span data-ttu-id="31391-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31391-119">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31391-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="31391-120">Minimum supported server</span></span><br/> | <span data-ttu-id="31391-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31391-121">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31391-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="31391-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31391-123">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="31391-123">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="31391-124">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="31391-124">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





