---
description: Представляет событие изменения класса, которое представляет собой тип встроенного события, создаваемого при изменении класса в пространстве имен.
ms.assetid: 77e8e025-d584-495d-98f8-71e7fb2c9698
ms.tgt_platform: multiple
title: Класс __ClassModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 3634b632fa9ab66f0da3e48bf77fab5875daf12c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702381"
---
# <a name="__classmodificationevent-class"></a><span data-ttu-id="39992-103">\_\_Класс Классмодификатионевент</span><span class="sxs-lookup"><span data-stu-id="39992-103">\_\_ClassModificationEvent class</span></span>

<span data-ttu-id="39992-104">Класс System **\_ \_ классмодификатионевент** представляет событие изменения класса, которое представляет собой тип [встроенного события](determining-the-type-of-event-to-receive.md) , создаваемого при изменении класса в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="39992-104">The **\_\_ClassModificationEvent** system class represents a class modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a class is changed in the namespace.</span></span>

<span data-ttu-id="39992-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="39992-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39992-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="39992-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39992-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39992-107">Syntax</span></span>

``` syntax
class __ClassModificationEvent : __ClassOperationEvent
{
  object PreviousClass;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="39992-108">Члены</span><span class="sxs-lookup"><span data-stu-id="39992-108">Members</span></span>

<span data-ttu-id="39992-109">Класс **\_ \_ классмодификатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="39992-109">The **\_\_ClassModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="39992-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="39992-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39992-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="39992-111">Properties</span></span>

<span data-ttu-id="39992-112">Класс **\_ \_ классмодификатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="39992-112">The **\_\_ClassModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39992-113">**превиаускласс**</span><span class="sxs-lookup"><span data-stu-id="39992-113">**PreviousClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39992-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="39992-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="39992-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39992-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39992-116">Копия исходной версии класса.</span><span class="sxs-lookup"><span data-stu-id="39992-116">Copy of the original version of the class.</span></span>

</dd> <dt>

<span data-ttu-id="39992-117">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="39992-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39992-118">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="39992-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="39992-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39992-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39992-120">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="39992-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="39992-121">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="39992-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="39992-122">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="39992-122">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39992-123">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="39992-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="39992-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39992-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39992-125">Копия только что измененного класса, сообщаемого событием изменения класса.</span><span class="sxs-lookup"><span data-stu-id="39992-125">Copy of the newly modified class reported by the class modification event.</span></span> <span data-ttu-id="39992-126">Это свойство наследуется от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="39992-126">This property is inherited from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="39992-127">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="39992-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39992-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="39992-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="39992-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="39992-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="39992-130">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="39992-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="39992-131">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="39992-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="39992-132">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="39992-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="39992-133">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="39992-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="39992-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="39992-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39992-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39992-135">Remarks</span></span>

<span data-ttu-id="39992-136">Класс **\_ \_ классмодификатионевент** является производным от [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="39992-136">The **\_\_ClassModificationEvent** class is derived from [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="39992-137">Событие сообщает о новой и старой версиях определения класса.</span><span class="sxs-lookup"><span data-stu-id="39992-137">The event reports both the new and old versions of the class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="39992-138">Требования</span><span class="sxs-lookup"><span data-stu-id="39992-138">Requirements</span></span>



| <span data-ttu-id="39992-139">Требование</span><span class="sxs-lookup"><span data-stu-id="39992-139">Requirement</span></span> | <span data-ttu-id="39992-140">Значение</span><span class="sxs-lookup"><span data-stu-id="39992-140">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="39992-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39992-141">Minimum supported client</span></span><br/> | <span data-ttu-id="39992-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39992-142">Windows Vista</span></span><br/>       |
| <span data-ttu-id="39992-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39992-143">Minimum supported server</span></span><br/> | <span data-ttu-id="39992-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39992-144">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="39992-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="39992-145">Namespace</span></span><br/>                | <span data-ttu-id="39992-146">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="39992-146">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="39992-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39992-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39992-148">**\_\_классоператионевент**</span><span class="sxs-lookup"><span data-stu-id="39992-148">**\_\_ClassOperationEvent**</span></span>](/windows/desktop/WmiSdk/--classoperationevent)
</dt> <dt>

[<span data-ttu-id="39992-149">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="39992-149">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

