---
title: Сложный тип Маинтенанцесеттингстипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Маинтенанцесеттингс.
ms.assetid: CA4C452E-CA25-4E2D-B5E2-ED64C59AB3AD
keywords:
- планировщик задач сложного типа Маинтенанцесеттингстипе
topic_type:
- apiref
api_name:
- maintenanceSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f261e84fe2af1239cce1bbd377e991ede6e8506
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803221"
---
# <a name="maintenancesettingstype-complex-type"></a><span data-ttu-id="aa41a-104">Сложный тип Маинтенанцесеттингстипе</span><span class="sxs-lookup"><span data-stu-id="aa41a-104">maintenanceSettingsType Complex Type</span></span>

<span data-ttu-id="aa41a-105">Определяет дочерние элементы и сведения о последовательности для элемента [**маинтенанцесеттингс**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aa41a-105">Defines the child elements and sequencing information for the [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="maintenanceSettingsType">
    <xs:all>
        <xs:element name="Period"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Deadline"
            minOccurs="1"
            maxOccurs="1"
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
        <xs:element name="Exclusive"
            type="boolean"
            maxOccurs="1"
            minOccurs="1"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="aa41a-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="aa41a-106">Child elements</span></span>



| <span data-ttu-id="aa41a-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="aa41a-107">Element</span></span>                                                                        | <span data-ttu-id="aa41a-108">Тип</span><span class="sxs-lookup"><span data-stu-id="aa41a-108">Type</span></span>    | <span data-ttu-id="aa41a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="aa41a-109">Description</span></span>                                                                                                                                                                                    |
|--------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa41a-110">**Крайний срок**</span><span class="sxs-lookup"><span data-stu-id="aa41a-110">**Deadline**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md) |         | <span data-ttu-id="aa41a-111">Указывает период времени, по истечении которого планировщик заданий будет пытаться запустить задачу во время аварийного автоматического обслуживания, если это не удалось завершить во время регулярного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa41a-111">Specifies the amount of time after which the Task scheduler will attempt to start task during emergency Automatic maintenance, if it failed to complete during regular maintenance.</span></span><br/> |
| <span data-ttu-id="aa41a-112">**Монопольный доступ**</span><span class="sxs-lookup"><span data-stu-id="aa41a-112">**Exclusive**</span></span>                                                                  | <span data-ttu-id="aa41a-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="aa41a-113">boolean</span></span> | <span data-ttu-id="aa41a-114">Если задано значение true, задача будет запускаться только в других задачах обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa41a-114">If set to true, the task will be started exclusively among other maintenance tasks.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="aa41a-115">**Периода**</span><span class="sxs-lookup"><span data-stu-id="aa41a-115">**Period**</span></span>](taskschedulerschema-daysinterval-dailyscheduletype-element.md)   |         | <span data-ttu-id="aa41a-116">Указывает, как часто задача должна запускаться во время автоматического обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aa41a-116">Specifies how often the task needs to be started during Automatic maintenance.</span></span><br/>                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="aa41a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="aa41a-117">Requirements</span></span>



| <span data-ttu-id="aa41a-118">Требование</span><span class="sxs-lookup"><span data-stu-id="aa41a-118">Requirement</span></span> | <span data-ttu-id="aa41a-119">Значение</span><span class="sxs-lookup"><span data-stu-id="aa41a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa41a-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa41a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aa41a-121">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="aa41a-121">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="aa41a-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa41a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aa41a-123">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="aa41a-123">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa41a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa41a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa41a-125">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="aa41a-125">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="aa41a-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="aa41a-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





