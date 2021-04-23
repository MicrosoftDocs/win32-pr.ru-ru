---
title: Сложный тип Идлесеттингстипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Идлесеттингс (Сеттингстипе).
ms.assetid: 0f50c4d6-fda9-42cc-8dab-4c9439fbea4b
keywords:
- планировщик задач сложного типа Идлесеттингстипе
topic_type:
- apiref
api_name:
- idleSettingsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba5ffa3acb879aad095b5b136d882bb817eb0ab0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681846"
---
# <a name="idlesettingstype-complex-type"></a><span data-ttu-id="94ecf-104">Сложный тип Идлесеттингстипе</span><span class="sxs-lookup"><span data-stu-id="94ecf-104">idleSettingsType Complex Type</span></span>

<span data-ttu-id="94ecf-105">Определяет дочерние элементы и сведения о последовательности для элемента [**идлесеттингс (сеттингстипе)**](taskschedulerschema-idlesettings-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="94ecf-105">Defines the child elements and sequencing information for the [**IdleSettings (settingsType)**](taskschedulerschema-idlesettings-settingstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="idleSettingsType">
    <xs:all>
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
        <xs:element name="StopOnIdleEnd"
            type="boolean"
            default="true"
            minOccurs="0"
         />
        <xs:element name="RestartOnIdle"
            type="boolean"
            default="false"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="94ecf-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="94ecf-106">Child elements</span></span>



| <span data-ttu-id="94ecf-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="94ecf-107">Element</span></span>                                                                                  | <span data-ttu-id="94ecf-108">Тип</span><span class="sxs-lookup"><span data-stu-id="94ecf-108">Type</span></span>    | <span data-ttu-id="94ecf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="94ecf-109">Description</span></span>                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94ecf-110">**Длительность**</span><span class="sxs-lookup"><span data-stu-id="94ecf-110">**Duration**</span></span>](taskschedulerschema-duration-idlesettingstype-element.md)                |         | <span data-ttu-id="94ecf-111">Указывает время, отведенное на запуск задачи в условиях простоя.</span><span class="sxs-lookup"><span data-stu-id="94ecf-111">Specifies the amount of time allowed to start the task while in an idle condition.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="94ecf-112">**рестартонидле**</span><span class="sxs-lookup"><span data-stu-id="94ecf-112">**RestartOnIdle**</span></span>](taskschedulerschema-restartonidle-idlesettingstype-element.md)      | <span data-ttu-id="94ecf-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="94ecf-113">boolean</span></span> | <span data-ttu-id="94ecf-114">Задача перезапускается сразу же после запуска условия простоя.</span><span class="sxs-lookup"><span data-stu-id="94ecf-114">The task is restarted as soon as an idle condition starts.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="94ecf-115">**стопонидлинд**</span><span class="sxs-lookup"><span data-stu-id="94ecf-115">**StopOnIdleEnd**</span></span>](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) | <span data-ttu-id="94ecf-116">Логическое</span><span class="sxs-lookup"><span data-stu-id="94ecf-116">boolean</span></span> | <span data-ttu-id="94ecf-117">Указывает, что задача завершается, если условие простоя заканчивается до превышения длительности простоя.</span><span class="sxs-lookup"><span data-stu-id="94ecf-117">Specifies that the task is terminated if the idle condition ends before the idle duration is exceeded.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="94ecf-118">**ваиттимеаут**</span><span class="sxs-lookup"><span data-stu-id="94ecf-118">**WaitTimeout**</span></span>](taskschedulerschema-waittimeout-idlesettingstype-element.md)          |         | <span data-ttu-id="94ecf-119">Указывает период времени, в течение которого ожидается запуск условия простоя.</span><span class="sxs-lookup"><span data-stu-id="94ecf-119">Specifies the amount of time to wait for an idle condition to start.</span></span> <span data-ttu-id="94ecf-120">Если для этого элемента не указано значение, то служба планировщик задач будет ждать неопределенное время, пока не произойдет условие простоя.</span><span class="sxs-lookup"><span data-stu-id="94ecf-120">If no value is specified for this element, then the Task Scheduler service will wait indefinitely for an idle condition to occur.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="94ecf-121">Требования</span><span class="sxs-lookup"><span data-stu-id="94ecf-121">Requirements</span></span>



| <span data-ttu-id="94ecf-122">Требование</span><span class="sxs-lookup"><span data-stu-id="94ecf-122">Requirement</span></span> | <span data-ttu-id="94ecf-123">Значение</span><span class="sxs-lookup"><span data-stu-id="94ecf-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94ecf-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94ecf-124">Minimum supported client</span></span><br/> | <span data-ttu-id="94ecf-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="94ecf-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94ecf-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94ecf-126">Minimum supported server</span></span><br/> | <span data-ttu-id="94ecf-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="94ecf-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94ecf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94ecf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ecf-129">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="94ecf-129">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="94ecf-130">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="94ecf-130">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





