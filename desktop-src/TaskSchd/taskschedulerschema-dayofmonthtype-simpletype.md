---
title: Простой тип Дайофмонстипе
description: Определяет возможные значения для указания дня месяца.
ms.assetid: 13497cf4-e1e5-4d54-9dff-0fe89be1fed8
keywords:
- планировщик задач простого типа Дайофмонстипе
topic_type:
- apiref
api_name:
- dayOfMonthType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a8428688ff429809c7509bae42adb156efe00ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533890"
---
# <a name="dayofmonthtype-simple-type"></a><span data-ttu-id="9d466-104">Простой тип Дайофмонстипе</span><span class="sxs-lookup"><span data-stu-id="9d466-104">dayOfMonthType Simple Type</span></span>

<span data-ttu-id="9d466-105">Определяет возможные значения для указания дня месяца.</span><span class="sxs-lookup"><span data-stu-id="9d466-105">Defines the possible values for specifying a day of the month.</span></span>

``` syntax
<xs:simpleType name="dayOfMonthType">
    <xs:restriction
        base="string"
    >
        <xs:pattern
            value="[1-9]|[1-2][0-9]|3[0-1]|Last"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="patterns"></a><span data-ttu-id="9d466-106">Шаблоны</span><span class="sxs-lookup"><span data-stu-id="9d466-106">Patterns</span></span>

<span data-ttu-id="9d466-107">Простой тип **дайофмонстипе** — это **строка** , которая ограничена следующим шаблоном:</span><span class="sxs-lookup"><span data-stu-id="9d466-107">The **dayOfMonthType** simple type is a **string** that is restricted by the following pattern:</span></span>

-   `[1-9]|[1-2][0-9]|3[0-1]|Last`

    <span data-ttu-id="9d466-108">Указывает первый из 31-дневного дня месяца или всегда последний день месяца.</span><span class="sxs-lookup"><span data-stu-id="9d466-108">Specifies the 1st through the 31st day of the month, or always the last day of the month.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d466-109">Требования</span><span class="sxs-lookup"><span data-stu-id="9d466-109">Requirements</span></span>



| <span data-ttu-id="9d466-110">Требование</span><span class="sxs-lookup"><span data-stu-id="9d466-110">Requirement</span></span> | <span data-ttu-id="9d466-111">Значение</span><span class="sxs-lookup"><span data-stu-id="9d466-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9d466-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d466-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9d466-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9d466-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9d466-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d466-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9d466-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9d466-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d466-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d466-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d466-117">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="9d466-117">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="9d466-118">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="9d466-118">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





