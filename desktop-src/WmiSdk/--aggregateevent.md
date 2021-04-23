---
description: Представляет статистическое событие нескольких отдельных внутренних или внешних событий.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: Класс __AggregateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684314"
---
# <a name="__aggregateevent-class"></a><span data-ttu-id="fcb9f-103">\_\_Класс Аггрегативент</span><span class="sxs-lookup"><span data-stu-id="fcb9f-103">\_\_AggregateEvent class</span></span>

<span data-ttu-id="fcb9f-104">Класс System **\_ \_ аггрегативент** представляет агрегатное событие нескольких отдельных внутренних или внешних событий.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-104">The **\_\_AggregateEvent** system class represents an aggregate event of several individual intrinsic or extrinsic events.</span></span> <span data-ttu-id="fcb9f-105">Инструментарий WMI создает экземпляр **\_ \_ аггрегативент** , а не [**\_ \_ событие**](--event.md) , когда потребители регистрируются с предложением [Group Within](group-clause.md) в своем запросе события.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-105">WMI generates an instance of **\_\_AggregateEvent** rather than [**\_\_Event**](--event.md) when consumers register with the [GROUP WITHIN](group-clause.md) clause in their event query.</span></span>

<span data-ttu-id="fcb9f-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fcb9f-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcb9f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcb9f-108">Syntax</span></span>

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a><span data-ttu-id="fcb9f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="fcb9f-109">Members</span></span>

<span data-ttu-id="fcb9f-110">Класс **\_ \_ аггрегативент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fcb9f-110">The **\_\_AggregateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="fcb9f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcb9f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcb9f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcb9f-112">Properties</span></span>

<span data-ttu-id="fcb9f-113">Класс **\_ \_ аггрегативент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-113">The **\_\_AggregateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcb9f-114">**NumberOfEvents**</span><span class="sxs-lookup"><span data-stu-id="fcb9f-114">**NumberOfEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb9f-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcb9f-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcb9f-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcb9f-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcb9f-117">Число событий, собранных для создания этого одного сводного события.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-117">Number of events combined to produce this single summary event.</span></span>

</dd> <dt>

<span data-ttu-id="fcb9f-118">**Representative**</span><span class="sxs-lookup"><span data-stu-id="fcb9f-118">**Representative**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcb9f-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="fcb9f-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="fcb9f-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcb9f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcb9f-121">Копия одного из событий, доставленных в рамках интервала статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-121">Copy of one of the events delivered within the aggregation interval.</span></span> <span data-ttu-id="fcb9f-122">Например, если потребитель зарегистрировался для событий изменения раздела реестра от поставщика событий реестра, то в качестве **представителя** будет храниться экземпляр класса **регистрикэйчанжеевент** .</span><span class="sxs-lookup"><span data-stu-id="fcb9f-122">For example, if a consumer has registered for registry key change events from the Registry Event provider, **Representative** would hold an instance of the **RegistryKeyChangeEvent** class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fcb9f-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fcb9f-123">Remarks</span></span>

<span data-ttu-id="fcb9f-124">Класс **\_ \_ аггрегативент** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-124">The **\_\_AggregateEvent** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

<span data-ttu-id="fcb9f-125">Поставщики событий никогда не создают статистических событий.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-125">Event providers never generate aggregate events.</span></span> <span data-ttu-id="fcb9f-126">Они должны игнорировать предложение GROUP в рамках обработки запросов событий.</span><span class="sxs-lookup"><span data-stu-id="fcb9f-126">They must ignore the GROUP WITHIN clause in their processing of event queries.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcb9f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="fcb9f-127">Requirements</span></span>



| <span data-ttu-id="fcb9f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="fcb9f-128">Requirement</span></span> | <span data-ttu-id="fcb9f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="fcb9f-129">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fcb9f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcb9f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="fcb9f-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fcb9f-131">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fcb9f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcb9f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="fcb9f-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fcb9f-133">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="fcb9f-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fcb9f-134">Namespace</span></span><br/>                | <span data-ttu-id="fcb9f-135">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="fcb9f-135">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="fcb9f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcb9f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcb9f-137">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="fcb9f-137">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="fcb9f-138">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="fcb9f-138">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="fcb9f-139">Запросы с помощью WQL</span><span class="sxs-lookup"><span data-stu-id="fcb9f-139">Querying with WQL</span></span>](querying-with-wql.md)
</dt> </dl>

 

