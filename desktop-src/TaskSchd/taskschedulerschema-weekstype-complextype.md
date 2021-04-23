---
title: Сложный тип Викстипе
description: Определяет дочерний элемент и сведения о последовательности для элемента Week.
ms.assetid: c9e8814c-b8f9-426d-943d-ca3efa5d914b
keywords:
- планировщик задач сложного типа Викстипе
topic_type:
- apiref
api_name:
- weeksType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 597cc72c043a478a414187f63a9aa89516dee658
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137011"
---
# <a name="weekstype-complex-type"></a><span data-ttu-id="a4c59-104">Сложный тип Викстипе</span><span class="sxs-lookup"><span data-stu-id="a4c59-104">weeksType Complex Type</span></span>

<span data-ttu-id="a4c59-105">Определяет дочерний элемент и сведения о последовательности для элемента [**Week**](taskschedulerschema-week-weekstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c59-105">Defines the child element and sequencing information for the [**Week**](taskschedulerschema-week-weekstype-element.md) element.</span></span>

``` syntax
<xs:complexType name="weeksType">
    <xs:sequence>
        <xs:element name="Week"
            type="weekType"
            minOccurs="0"
            maxOccurs="5"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a4c59-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a4c59-106">Child elements</span></span>



| <span data-ttu-id="a4c59-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a4c59-107">Element</span></span>                                                    | <span data-ttu-id="a4c59-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a4c59-108">Type</span></span>                                                        | <span data-ttu-id="a4c59-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a4c59-109">Description</span></span>                                             |
|------------------------------------------------------------|-------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="a4c59-110">**Неделя**</span><span class="sxs-lookup"><span data-stu-id="a4c59-110">**Week**</span></span>](taskschedulerschema-week-weekstype-element.md) | [<span data-ttu-id="a4c59-111">**виктипе**</span><span class="sxs-lookup"><span data-stu-id="a4c59-111">**weekType**</span></span>](taskschedulerschema-weektype-simpletype.md) | <span data-ttu-id="a4c59-112">Указывает неделю, в которой выполняется задача.</span><span class="sxs-lookup"><span data-stu-id="a4c59-112">Specifies the week in which the task is run.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a4c59-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a4c59-113">Requirements</span></span>



| <span data-ttu-id="a4c59-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a4c59-114">Requirement</span></span> | <span data-ttu-id="a4c59-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a4c59-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a4c59-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4c59-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c59-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a4c59-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a4c59-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4c59-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c59-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a4c59-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a4c59-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4c59-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c59-121">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="a4c59-121">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





