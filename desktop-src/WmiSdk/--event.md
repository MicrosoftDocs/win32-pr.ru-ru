---
description: Является абстрактным базовым классом, который служит родительским классом для всех внутренних и внешних событий.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: Класс __Event
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 39a032b3f082ed64ba7999d20366b89e8b3890c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703320"
---
# <a name="__event-class"></a><span data-ttu-id="c0459-103">\_\_Класс событий</span><span class="sxs-lookup"><span data-stu-id="c0459-103">\_\_Event class</span></span>

<span data-ttu-id="c0459-104">Класс системы **\_ \_ событий** является абстрактным базовым классом, который служит родительским классом для всех внутренних и внешних событий.</span><span class="sxs-lookup"><span data-stu-id="c0459-104">The **\_\_Event** system class is an abstract base class that serves as the parent class for all intrinsic and extrinsic events.</span></span> <span data-ttu-id="c0459-105">Все новые типы событий должны в конечном итоге быть производными от **\_ \_ события**.</span><span class="sxs-lookup"><span data-stu-id="c0459-105">All new event types must ultimately derive from **\_\_Event**.</span></span> <span data-ttu-id="c0459-106">Внутренние события наследуются непосредственно от этого класса.</span><span class="sxs-lookup"><span data-stu-id="c0459-106">Intrinsic events derive directly from this class.</span></span> <span data-ttu-id="c0459-107">Определяемые пользователем внешние события являются производными от подкласса этого класса с именем [**\_ \_ екстринсицевент**](--extrinsicevent.md).</span><span class="sxs-lookup"><span data-stu-id="c0459-107">User-defined extrinsic events derive from a subclass of this class called [**\_\_ExtrinsicEvent**](--extrinsicevent.md).</span></span>

<span data-ttu-id="c0459-108">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c0459-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c0459-109">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c0459-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0459-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0459-110">Syntax</span></span>

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="c0459-111">Члены</span><span class="sxs-lookup"><span data-stu-id="c0459-111">Members</span></span>

<span data-ttu-id="c0459-112">Класс **\_ \_ событий** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0459-112">The **\_\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="c0459-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0459-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0459-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0459-114">Properties</span></span>

<span data-ttu-id="c0459-115">Класс **\_ \_ событий** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0459-115">The **\_\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0459-116">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="c0459-116">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0459-117">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c0459-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c0459-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0459-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0459-119">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="c0459-119">Descriptor that the event provider uses to determine which users can receive the event.</span></span> <span data-ttu-id="c0459-120">Дополнительные сведения см. в разделе [константы безопасности WMI](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c0459-120">For more information, see [WMI Security Constants](wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0459-121">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="c0459-121">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0459-122">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c0459-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0459-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0459-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0459-124">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="c0459-124">Unique value that indicates the time the event is generated.</span></span> <span data-ttu-id="c0459-125">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="c0459-125">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c0459-126">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="c0459-126">The information is in the Coordinated Universal Time (UTC) format.</span></span>

<span data-ttu-id="c0459-127">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="c0459-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0459-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0459-128">Remarks</span></span>

<span data-ttu-id="c0459-129">Класс **\_ \_ событий** является производным от [**\_ \_ индикатионрелатед**](--indicationrelated.md), у которого нет свойств.</span><span class="sxs-lookup"><span data-stu-id="c0459-129">The **\_\_Event** class is derived from [**\_\_IndicationRelated**](--indicationrelated.md), which has no properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0459-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c0459-130">Requirements</span></span>



| <span data-ttu-id="c0459-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c0459-131">Requirement</span></span> | <span data-ttu-id="c0459-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c0459-132">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="c0459-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0459-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c0459-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0459-134">Windows Vista</span></span><br/>       |
| <span data-ttu-id="c0459-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0459-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c0459-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0459-136">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="c0459-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0459-137">Namespace</span></span><br/>                | <span data-ttu-id="c0459-138">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="c0459-138">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="c0459-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0459-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0459-140">**\_\_индикатионрелатед**</span><span class="sxs-lookup"><span data-stu-id="c0459-140">**\_\_IndicationRelated**</span></span>](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[<span data-ttu-id="c0459-141">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="c0459-141">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="c0459-142">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="c0459-142">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="c0459-143">**\_\_классоператионевент**</span><span class="sxs-lookup"><span data-stu-id="c0459-143">**\_\_ClassOperationEvent**</span></span>](--classoperationevent.md)
</dt> <dt>

[<span data-ttu-id="c0459-144">**\_\_инстанцеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="c0459-144">**\_\_InstanceOperationEvent**</span></span>](--instanceoperationevent.md)
</dt> <dt>

[<span data-ttu-id="c0459-145">**\_\_намеспацеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="c0459-145">**\_\_NamespaceOperationEvent**</span></span>](--namespaceoperationevent.md)
</dt> </dl>

 

