---
title: Простой тип Мултиплеинстанцесполицитипе
description: Определяет константы политики экземпляра для элемента Мултиплеинстанцесполици (Сеттингстипе).
ms.assetid: 6e3f83b0-b71e-49c9-9c27-5a37f996746b
keywords:
- планировщик задач простого типа Мултиплеинстанцесполицитипе
topic_type:
- apiref
api_name:
- multipleInstancesPolicyType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 29a3523ef16224836ada474fb32265084453479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988870"
---
# <a name="multipleinstancespolicytype-simple-type"></a><span data-ttu-id="f3d7e-104">Простой тип Мултиплеинстанцесполицитипе</span><span class="sxs-lookup"><span data-stu-id="f3d7e-104">multipleInstancesPolicyType Simple Type</span></span>

<span data-ttu-id="f3d7e-105">Определяет константы политики экземпляра для элемента [**мултиплеинстанцесполици (сеттингстипе)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f3d7e-105">Defines the instance policy constants for the [**MultipleInstancesPolicy (settingsType)**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md) element.</span></span>

``` syntax
<xs:simpleType name="multipleInstancesPolicyType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="Parallel"
         />
        <xs:enumeration
            value="Queue"
         />
        <xs:enumeration
            value="IgnoreNew"
         />
        <xs:enumeration
            value="StopExisting"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a><span data-ttu-id="f3d7e-106">Значения перечисления</span><span class="sxs-lookup"><span data-stu-id="f3d7e-106">Enumeration values</span></span>

<span data-ttu-id="f3d7e-107">Простой тип **мултиплеинстанцесполицитипе** определяет следующие значения.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-107">The **multipleInstancesPolicyType** simple type defines the following values.</span></span>



| <span data-ttu-id="f3d7e-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f3d7e-108">Value</span></span>        | <span data-ttu-id="f3d7e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f3d7e-109">Description</span></span>                                                                                     |
|--------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3d7e-110">Параллельные</span><span class="sxs-lookup"><span data-stu-id="f3d7e-110">Parallel</span></span>     | <span data-ttu-id="f3d7e-111">Запускает новый экземпляр во время работы существующего экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-111">Starts new instance while an existing instance is running.</span></span><br/>                           |
| <span data-ttu-id="f3d7e-112">Очередь</span><span class="sxs-lookup"><span data-stu-id="f3d7e-112">Queue</span></span>        | <span data-ttu-id="f3d7e-113">Запускает новый экземпляр Task после завершения всех остальных экземпляров задачи.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-113">Starts new instance of task after all other instances of the task are complete.</span></span><br/>      |
| <span data-ttu-id="f3d7e-114">игноренев</span><span class="sxs-lookup"><span data-stu-id="f3d7e-114">IgnoreNew</span></span>    | <span data-ttu-id="f3d7e-115">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-115">Default.</span></span> <span data-ttu-id="f3d7e-116">Не запускает новый экземпляр, если запущен существующий экземпляр задачи.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-116">Does not start new instance if an existing instance of the task is running.</span></span><br/> |
| <span data-ttu-id="f3d7e-117">стопексистинг</span><span class="sxs-lookup"><span data-stu-id="f3d7e-117">StopExisting</span></span> | <span data-ttu-id="f3d7e-118">Останавливает существующий экземпляр задачи перед запуском нового экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f3d7e-118">Stops an existing instance of the task before it starts new instance.</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="f3d7e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f3d7e-119">Requirements</span></span>



| <span data-ttu-id="f3d7e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f3d7e-120">Requirement</span></span> | <span data-ttu-id="f3d7e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f3d7e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3d7e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3d7e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f3d7e-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3d7e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3d7e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3d7e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f3d7e-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3d7e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3d7e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3d7e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3d7e-127">Простые типы схемы планировщик задач</span><span class="sxs-lookup"><span data-stu-id="f3d7e-127">Task Scheduler Schema Simple Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="f3d7e-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="f3d7e-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





