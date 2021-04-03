---
title: простой тип Гуидтипе (планировщик задач)
description: Определяет шаблон для допустимых идентификаторов GUID.
ms.assetid: 1aa3f08b-4b3e-4e72-8ac4-d859a8da4c32
keywords:
- планировщик задач простого типа Гуидтипе
topic_type:
- apiref
api_name:
- guidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b95d5b8ad7a4158dbe449fb28cf3324499488f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137027"
---
# <a name="guidtype-simple-type-task-scheduler"></a><span data-ttu-id="74d2d-104">простой тип Гуидтипе (планировщик задач)</span><span class="sxs-lookup"><span data-stu-id="74d2d-104">guidType simple type (Task Scheduler)</span></span>

<span data-ttu-id="74d2d-105">Определяет шаблон для допустимых идентификаторов GUID.</span><span class="sxs-lookup"><span data-stu-id="74d2d-105">Defines the pattern for valid GUIDs.</span></span>

``` syntax
<xs:simpleType name="guidType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="74d2d-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="74d2d-106">Patterns</span></span>

<span data-ttu-id="74d2d-107">Простой тип **гуидтипе** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="74d2d-107">The **guidType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `\{([0-9a-fA-F]){8}(\-[0-9a-fA-F]{4}){3}\-[0-9a-fA-F]{12}\}`

    <span data-ttu-id="74d2d-108">Уникальное 128-разрядное число.</span><span class="sxs-lookup"><span data-stu-id="74d2d-108">A unique 128-bit number.</span></span>

## <a name="requirements"></a><span data-ttu-id="74d2d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="74d2d-109">Requirements</span></span>



| <span data-ttu-id="74d2d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="74d2d-110">Requirement</span></span> | <span data-ttu-id="74d2d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="74d2d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="74d2d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74d2d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="74d2d-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="74d2d-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="74d2d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74d2d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="74d2d-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="74d2d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74d2d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74d2d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74d2d-117">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="74d2d-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="74d2d-118">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="74d2d-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





