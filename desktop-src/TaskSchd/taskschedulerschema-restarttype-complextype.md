---
title: Сложный тип Рестарттипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Рестартонфаилуре.
ms.assetid: 3a192955-8a33-42b9-a974-faa9a3789f58
keywords:
- планировщик задач сложного типа Рестарттипе
topic_type:
- apiref
api_name:
- restartType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f83dcac376fcdd8d2059649350502111f5a732f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535495"
---
# <a name="restarttype-complex-type"></a><span data-ttu-id="aad5e-104">Сложный тип Рестарттипе</span><span class="sxs-lookup"><span data-stu-id="aad5e-104">restartType Complex Type</span></span>

<span data-ttu-id="aad5e-105">Определяет дочерние элементы и сведения о последовательности для элемента [рестартонфаилуре](taskschedulerschema-restartonfailure-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aad5e-105">Defines the child elements and sequence information for the [RestartOnFailure](taskschedulerschema-restartonfailure-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="restartType">
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
        <xs:element name="Count">
            <xs:simpleType>
                <xs:restriction
                    base="unsignedByte"
                >
                    <xs:minInclusive
                        value="1"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="aad5e-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aad5e-106">Child elements</span></span>



| <span data-ttu-id="aad5e-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="aad5e-107">Element</span></span>                                                              | <span data-ttu-id="aad5e-108">Тип</span><span class="sxs-lookup"><span data-stu-id="aad5e-108">Type</span></span> | <span data-ttu-id="aad5e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aad5e-109">Description</span></span>                                        |
|----------------------------------------------------------------------|------|----------------------------------------------------|
| [<span data-ttu-id="aad5e-110">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="aad5e-110">**Count**</span></span>](taskschedulerschema-count-restarttype-element.md)       |      | <span data-ttu-id="aad5e-111">Число попыток перезапуска задачи.</span><span class="sxs-lookup"><span data-stu-id="aad5e-111">Number of attempts to restart the task.</span></span><br/> |
| [<span data-ttu-id="aad5e-112">**Пределах**</span><span class="sxs-lookup"><span data-stu-id="aad5e-112">**Interval**</span></span>](taskschedulerschema-interval-restarttype-element.md) |      | <span data-ttu-id="aad5e-113">Длительность попытки запуска задачи.</span><span class="sxs-lookup"><span data-stu-id="aad5e-113">How long to try to start the task.</span></span><br/>      |



## <a name="requirements"></a><span data-ttu-id="aad5e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="aad5e-114">Requirements</span></span>



| <span data-ttu-id="aad5e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="aad5e-115">Requirement</span></span> | <span data-ttu-id="aad5e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="aad5e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aad5e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aad5e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="aad5e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aad5e-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="aad5e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aad5e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="aad5e-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aad5e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aad5e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aad5e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad5e-122">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="aad5e-122">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="aad5e-123">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="aad5e-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





