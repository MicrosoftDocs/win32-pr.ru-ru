---
title: Сложный тип Репетитионтипе
description: Определяет дочерние элементы и сведения о последовательности для элемента повторения (Тригжербасетипе).
ms.assetid: d2b4b840-3a69-4ff8-ac32-6ec76e7e8788
keywords:
- планировщик задач сложного типа Репетитионтипе
topic_type:
- apiref
api_name:
- repetitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aa9ee8c08a79f5db053b772c86929f98a72f011c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415872"
---
# <a name="repetitiontype-complex-type"></a><span data-ttu-id="ddd49-104">Сложный тип Репетитионтипе</span><span class="sxs-lookup"><span data-stu-id="ddd49-104">repetitionType Complex Type</span></span>

<span data-ttu-id="ddd49-105">Определяет дочерние элементы и сведения о последовательности для элемента [**повторения (тригжербасетипе)**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="ddd49-105">Defines the child elements and sequence information for the [**Repetition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

``` syntax
<xs:complexType name="repetitionType">
    <xs:all>
        <xs:element name="Interval">
            <xs:simpleType>
                <xs:restriction
                    base="duration"
                >
                    <xs:minInclusive
                        value="PT1M"
                     />
                    <xs:maxInclusive
                        value="P31D"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="Duration"
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
        <xs:element name="StopAtDurationEnd"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ddd49-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ddd49-106">Child elements</span></span>



| <span data-ttu-id="ddd49-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="ddd49-107">Element</span></span>                                                                                   | <span data-ttu-id="ddd49-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ddd49-108">Type</span></span>    | <span data-ttu-id="ddd49-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ddd49-109">Description</span></span>                                                                                                            |
|-------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddd49-110">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="ddd49-110">**Duration**</span></span>](taskschedulerschema-duration-repetitiontype-element.md)                   |         | <span data-ttu-id="ddd49-111">Указывает, как долго шаблон повторяется.</span><span class="sxs-lookup"><span data-stu-id="ddd49-111">Specifies how long the pattern is repeated.</span></span> <span data-ttu-id="ddd49-112">Если значение не указано, шаблон повторяется бесконечно.</span><span class="sxs-lookup"><span data-stu-id="ddd49-112">If no value is specified, the pattern is repeated indefinitely.</span></span><br/> |
| [<span data-ttu-id="ddd49-113">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="ddd49-113">**Interval**</span></span>](taskschedulerschema-interval-repetitiontype-element.md)                   |         | <span data-ttu-id="ddd49-114">Задает интервал времени между перезапусками задачи.</span><span class="sxs-lookup"><span data-stu-id="ddd49-114">Specifies the amount of time between each restart of the task.</span></span><br/>                                              |
| [<span data-ttu-id="ddd49-115">**стопатдуратионенд**</span><span class="sxs-lookup"><span data-stu-id="ddd49-115">**StopAtDurationEnd**</span></span>](taskschedulerschema-stopatdurationend-repetitiontype-element.md) | <span data-ttu-id="ddd49-116">Логическое</span><span class="sxs-lookup"><span data-stu-id="ddd49-116">boolean</span></span> | <span data-ttu-id="ddd49-117">Указывает, что выполняющийся экземпляр задачи останавливается в конце срока действия шаблона повторения.</span><span class="sxs-lookup"><span data-stu-id="ddd49-117">Specifies that a running instance of the task is stopped at the end of the repetition pattern duration.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="ddd49-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ddd49-118">Requirements</span></span>



| <span data-ttu-id="ddd49-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ddd49-119">Requirement</span></span> | <span data-ttu-id="ddd49-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ddd49-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ddd49-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddd49-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ddd49-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ddd49-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ddd49-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddd49-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ddd49-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ddd49-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddd49-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddd49-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd49-126">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="ddd49-126">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="ddd49-127">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="ddd49-127">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





