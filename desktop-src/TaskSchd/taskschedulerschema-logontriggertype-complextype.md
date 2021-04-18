---
title: Сложный тип Логонтригжертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Логонтригжер.
ms.assetid: ddb1d01b-89d1-4d52-872c-4fbd90f32f4b
keywords:
- планировщик задач сложного типа Логонтригжертипе
topic_type:
- apiref
api_name:
- logonTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81a3f42eb94d14506d96348b803c8b1bc41737d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682134"
---
# <a name="logontriggertype-complex-type"></a><span data-ttu-id="0c32c-104">Сложный тип Логонтригжертипе</span><span class="sxs-lookup"><span data-stu-id="0c32c-104">logonTriggerType Complex Type</span></span>

<span data-ttu-id="0c32c-105">Определяет дочерние элементы и сведения о последовательности для элемента [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0c32c-105">Defines the child elements and sequencing information for the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="logonTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="UserId"
                    type="nonEmptyString"
                    minOccurs="0"
                 />
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

## <a name="child-elements"></a><span data-ttu-id="0c32c-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0c32c-106">Child elements</span></span>



| <span data-ttu-id="0c32c-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="0c32c-107">Element</span></span>                                                               | <span data-ttu-id="0c32c-108">Тип</span><span class="sxs-lookup"><span data-stu-id="0c32c-108">Type</span></span>                                                                    | <span data-ttu-id="0c32c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="0c32c-109">Description</span></span>                                                                                   |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c32c-110">**Задержка**</span><span class="sxs-lookup"><span data-stu-id="0c32c-110">**Delay**</span></span>](taskschedulerschema-delay-logontriggertype-element.md)   | <span data-ttu-id="0c32c-111">длительность</span><span class="sxs-lookup"><span data-stu-id="0c32c-111">duration</span></span>                                                                | <span data-ttu-id="0c32c-112">Промежуток времени между входом пользователя в систему и запуском задачи.</span><span class="sxs-lookup"><span data-stu-id="0c32c-112">Amount of time between when the user logs on and when the task is started.</span></span><br/>         |
| [<span data-ttu-id="0c32c-113">**UserId**</span><span class="sxs-lookup"><span data-stu-id="0c32c-113">**UserId**</span></span>](taskschedulerschema-userid-logontriggertype-element.md) | [<span data-ttu-id="0c32c-114">**нонемптистринг**</span><span class="sxs-lookup"><span data-stu-id="0c32c-114">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="0c32c-115">Идентификатор пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c32c-115">Identifier of the user.</span></span> <span data-ttu-id="0c32c-116">Задача запускается, когда пользователь входит в систему на компьютере.</span><span class="sxs-lookup"><span data-stu-id="0c32c-116">The task is started when this user logs onto the computer.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0c32c-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c32c-117">Remarks</span></span>

<span data-ttu-id="0c32c-118">Помимо дочерних элементов, определенных здесь, элемент [**логонтригжер**](taskschedulerschema-logontrigger-triggergroup-element.md) также использует дочерние элементы, определенные сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0c32c-118">In addition to the child elements defined here, the [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) element also uses child elements defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c32c-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0c32c-119">Requirements</span></span>



| <span data-ttu-id="0c32c-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0c32c-120">Requirement</span></span> | <span data-ttu-id="0c32c-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0c32c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0c32c-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c32c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0c32c-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c32c-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0c32c-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c32c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0c32c-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c32c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c32c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c32c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c32c-127">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="0c32c-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="0c32c-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="0c32c-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





