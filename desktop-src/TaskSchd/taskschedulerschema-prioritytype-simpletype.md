---
title: Простой тип Приорититипе
description: Определяет минимальное и максимальное значения для элемента Priority (Сеттингстипе).
ms.assetid: 44e97d78-f035-4db9-a557-f24960518628
keywords:
- планировщик задач простого типа Приорититипе
topic_type:
- apiref
api_name:
- priorityType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 05b3c6d04adf557242438c813dab4f10d48cdb9d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071867"
---
# <a name="prioritytype-simple-type"></a><span data-ttu-id="b7b0e-104">Простой тип Приорититипе</span><span class="sxs-lookup"><span data-stu-id="b7b0e-104">priorityType Simple Type</span></span>

<span data-ttu-id="b7b0e-105">Определяет минимальное и максимальное значения для элемента [**Priority (сеттингстипе)**](taskschedulerschema-priority-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="b7b0e-105">Defines the minimum and maximum values for the [**Priority (settingsType)**](taskschedulerschema-priority-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="priorityType">
    <xs:restriction
        base="byte"
    >
        <xs:enumeration
            value="0"
         />
        <xs:enumeration
            value="10"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="b7b0e-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="b7b0e-106">Enumeration values</span></span>

<span data-ttu-id="b7b0e-107">Простой тип **приорититипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b7b0e-107">The **priorityType** simple type defines the following values.</span></span>



| <span data-ttu-id="b7b0e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b7b0e-108">Value</span></span> | <span data-ttu-id="b7b0e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b7b0e-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="b7b0e-110">0</span><span class="sxs-lookup"><span data-stu-id="b7b0e-110">0</span></span>     | <span data-ttu-id="b7b0e-111">Минимальное допустимое целое число.</span><span class="sxs-lookup"><span data-stu-id="b7b0e-111">Minimum integer allowed.</span></span><br/> |
| <span data-ttu-id="b7b0e-112">10</span><span class="sxs-lookup"><span data-stu-id="b7b0e-112">10</span></span>    | <span data-ttu-id="b7b0e-113">Максимально допустимое целое число.</span><span class="sxs-lookup"><span data-stu-id="b7b0e-113">Maximum integer allowed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b7b0e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b7b0e-114">Requirements</span></span>



| <span data-ttu-id="b7b0e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b7b0e-115">Requirement</span></span> | <span data-ttu-id="b7b0e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b7b0e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b7b0e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b7b0e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b7b0e-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b7b0e-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b7b0e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b7b0e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b7b0e-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b7b0e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7b0e-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b7b0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7b0e-122">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="b7b0e-122">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="b7b0e-123">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="b7b0e-123">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





