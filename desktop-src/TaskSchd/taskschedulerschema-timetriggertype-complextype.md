---
title: Сложный тип Тиметригжертипе
description: Определяет базовый тип для элемента Тиметригжер.
ms.assetid: 3aabfb7a-3e11-4b67-8345-cc5088f11efc
keywords:
- планировщик задач сложного типа Тиметригжертипе
topic_type:
- apiref
api_name:
- timeTriggerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ca21464df967ff473a767e814b9ce6969a56c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672528"
---
# <a name="timetriggertype-complex-type"></a><span data-ttu-id="53a90-104">Сложный тип Тиметригжертипе</span><span class="sxs-lookup"><span data-stu-id="53a90-104">timeTriggerType Complex Type</span></span>

<span data-ttu-id="53a90-105">Определяет базовый тип для элемента [**тиметригжер**](taskschedulerschema-timetrigger-triggergroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="53a90-105">Defines the base type for the [**TimeTrigger**](taskschedulerschema-timetrigger-triggergroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="timeTriggerType">
    <xs:complexContent>
        <xs:extension
            base="triggerBaseType"
        >
            <xs:sequence>
                <xs:element name="RandomDelay"
                    type="duration"
                    default="PT0M"
                 />
            </xs:sequence>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="53a90-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="53a90-106">Child elements</span></span>



| <span data-ttu-id="53a90-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="53a90-107">Element</span></span>                                                                        | <span data-ttu-id="53a90-108">Тип</span><span class="sxs-lookup"><span data-stu-id="53a90-108">Type</span></span>     | <span data-ttu-id="53a90-109">Описание</span><span class="sxs-lookup"><span data-stu-id="53a90-109">Description</span></span>                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a90-110">**рандомделай**</span><span class="sxs-lookup"><span data-stu-id="53a90-110">**RandomDelay**</span></span>](taskschedulerschema-randomdelay-timetriggertype-element.md) | <span data-ttu-id="53a90-111">длительность</span><span class="sxs-lookup"><span data-stu-id="53a90-111">duration</span></span> | <span data-ttu-id="53a90-112">Указывает время задержки, которое добавляется случайным образом к времени начала триггера.</span><span class="sxs-lookup"><span data-stu-id="53a90-112">Specifies the delay time that is randomly added to the start time of the trigger.</span></span> <span data-ttu-id="53a90-113">Формат этой строки — P <days> DT <hours> H <minutes> <seconds> S (например, P2DT5S — 2 дня, задержка 5 секунд).</span><span class="sxs-lookup"><span data-stu-id="53a90-113">The format for this string is P<days>DT<hours>H<minutes>M<seconds>S (for example, P2DT5S is a 2 day, 5 second delay).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="53a90-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53a90-114">Remarks</span></span>

<span data-ttu-id="53a90-115">Обратите внимание, что этот элемент не добавляет никаких дочерних элементов к элементам, определенным сложным типом [**тригжербасетипе**](taskschedulerschema-triggerbasetype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="53a90-115">Note that this element does not add any child elements to those defined by the [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="53a90-116">Требования</span><span class="sxs-lookup"><span data-stu-id="53a90-116">Requirements</span></span>



| <span data-ttu-id="53a90-117">Требование</span><span class="sxs-lookup"><span data-stu-id="53a90-117">Requirement</span></span> | <span data-ttu-id="53a90-118">Значение</span><span class="sxs-lookup"><span data-stu-id="53a90-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="53a90-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53a90-119">Minimum supported client</span></span><br/> | <span data-ttu-id="53a90-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="53a90-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="53a90-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53a90-121">Minimum supported server</span></span><br/> | <span data-ttu-id="53a90-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="53a90-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="53a90-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53a90-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53a90-124">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="53a90-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="53a90-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="53a90-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





