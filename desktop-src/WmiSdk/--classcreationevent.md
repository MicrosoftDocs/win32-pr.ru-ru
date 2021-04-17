---
description: Представляет событие создания класса, которое представляет собой тип встроенного события, создаваемого при добавлении нового класса в пространство имен.
ms.assetid: a946a8eb-498c-4104-b80f-e520b0e62e36
ms.tgt_platform: multiple
title: Класс __ClassCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 18994ee7067e44a9199de9b62f7ff278a8bece00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702383"
---
# <a name="__classcreationevent-class"></a><span data-ttu-id="ef67b-103">\_\_Класс Класскреатионевент</span><span class="sxs-lookup"><span data-stu-id="ef67b-103">\_\_ClassCreationEvent class</span></span>

<span data-ttu-id="ef67b-104">Класс System **\_ \_ класскреатионевент** представляет событие создания класса, которое представляет собой тип [встроенного события](determining-the-type-of-event-to-receive.md) , создаваемого при добавлении нового класса в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ef67b-104">The **\_\_ClassCreationEvent** system class represents a class creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new class is added to the namespace.</span></span>

<span data-ttu-id="ef67b-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ef67b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ef67b-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ef67b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef67b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef67b-107">Syntax</span></span>

``` syntax
class __ClassCreationEvent : __ClassOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="ef67b-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ef67b-108">Members</span></span>

<span data-ttu-id="ef67b-109">Класс **\_ \_ класскреатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ef67b-109">The **\_\_ClassCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="ef67b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef67b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ef67b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ef67b-111">Properties</span></span>

<span data-ttu-id="ef67b-112">Класс **\_ \_ класскреатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ef67b-112">The **\_\_ClassCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ef67b-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="ef67b-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef67b-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ef67b-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ef67b-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef67b-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef67b-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="ef67b-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="ef67b-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ef67b-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef67b-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="ef67b-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef67b-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="ef67b-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ef67b-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef67b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef67b-121">Копия только что созданного класса, сообщаемого событием создания класса.</span><span class="sxs-lookup"><span data-stu-id="ef67b-121">Copy of the newly created class reported by the class creation event.</span></span> <span data-ttu-id="ef67b-122">Это свойство наследуется от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="ef67b-122">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef67b-123">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="ef67b-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ef67b-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ef67b-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ef67b-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef67b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ef67b-126">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="ef67b-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="ef67b-127">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="ef67b-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="ef67b-128">Эти сведения находятся в формате универсальных координат времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="ef67b-128">The information is in the Universal Time Coordinates (UTC) format.</span></span> <span data-ttu-id="ef67b-129">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="ef67b-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="ef67b-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="ef67b-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef67b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef67b-131">Remarks</span></span>

<span data-ttu-id="ef67b-132">Класс **\_ \_ класскреатионевент** является производным от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="ef67b-132">The **\_\_ClassCreationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef67b-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ef67b-133">Requirements</span></span>



| <span data-ttu-id="ef67b-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ef67b-134">Requirement</span></span> | <span data-ttu-id="ef67b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ef67b-135">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="ef67b-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef67b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ef67b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef67b-137">Windows Vista</span></span><br/>       |
| <span data-ttu-id="ef67b-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef67b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ef67b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef67b-139">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="ef67b-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef67b-140">Namespace</span></span><br/>                | <span data-ttu-id="ef67b-141">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="ef67b-141">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="ef67b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef67b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef67b-143">**\_\_классоператионевент**</span><span class="sxs-lookup"><span data-stu-id="ef67b-143">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="ef67b-144">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="ef67b-144">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

