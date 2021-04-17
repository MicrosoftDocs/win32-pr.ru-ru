---
description: Является базовым классом для всех внутренних событий, связанных с классом.
ms.assetid: 554bbabd-2639-40f5-8786-6df2188db0ec
ms.tgt_platform: multiple
title: Класс __ClassOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0c7a78219cec5c014e289dad4bf1cc29f0466a06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703395"
---
# <a name="__classoperationevent-class"></a><span data-ttu-id="de321-103">\_\_Класс Классоператионевент</span><span class="sxs-lookup"><span data-stu-id="de321-103">\_\_ClassOperationEvent class</span></span>

<span data-ttu-id="de321-104">Класс System **\_ \_ классоператионевент** является базовым классом для всех внутренних событий, связанных с классом.</span><span class="sxs-lookup"><span data-stu-id="de321-104">The **\_\_ClassOperationEvent** system class is a base class for all intrinsic events that relate to a class.</span></span>

<span data-ttu-id="de321-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="de321-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="de321-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="de321-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="de321-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de321-107">Syntax</span></span>

``` syntax
class __ClassOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetClass;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="de321-108">Члены</span><span class="sxs-lookup"><span data-stu-id="de321-108">Members</span></span>

<span data-ttu-id="de321-109">Класс **\_ \_ классоператионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="de321-109">The **\_\_ClassOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="de321-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="de321-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="de321-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="de321-111">Properties</span></span>

<span data-ttu-id="de321-112">Класс **\_ \_ классоператионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="de321-112">The **\_\_ClassOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de321-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="de321-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de321-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="de321-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="de321-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de321-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de321-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="de321-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="de321-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="de321-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="de321-118">**TargetClass**</span><span class="sxs-lookup"><span data-stu-id="de321-118">**TargetClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de321-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="de321-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="de321-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de321-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de321-121">Класс, затронутый событием.</span><span class="sxs-lookup"><span data-stu-id="de321-121">Class affected by the event.</span></span> <span data-ttu-id="de321-122">Для событий создания это только что созданный класс.</span><span class="sxs-lookup"><span data-stu-id="de321-122">For creation events, this is the newly created class.</span></span> <span data-ttu-id="de321-123">Для событий изменения это новая версия измененного класса.</span><span class="sxs-lookup"><span data-stu-id="de321-123">For modification events, this is the new version of the changed class.</span></span> <span data-ttu-id="de321-124">Для событий удаления это удаленный класс.</span><span class="sxs-lookup"><span data-stu-id="de321-124">For deletion events, this is the deleted class.</span></span>

</dd> <dt>

<span data-ttu-id="de321-125">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="de321-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de321-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="de321-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="de321-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="de321-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de321-128">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="de321-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="de321-129">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="de321-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="de321-130">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="de321-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="de321-131">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="de321-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="de321-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="de321-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de321-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="de321-133">Remarks</span></span>

<span data-ttu-id="de321-134">Класс **\_ \_ классоператионевент** является производным от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="de321-134">The **\_\_ClassOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="de321-135">Экземпляры **\_ \_ классоператионевент** не создаются; создаются только экземпляры его подклассов.</span><span class="sxs-lookup"><span data-stu-id="de321-135">Instances of **\_\_ClassOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="de321-136">Следующие классы являются производными от **\_ \_ классоператионевент**:</span><span class="sxs-lookup"><span data-stu-id="de321-136">The following classes derive from **\_\_ClassOperationEvent**:</span></span>

[<span data-ttu-id="de321-137">**\_\_класскреатионевент**</span><span class="sxs-lookup"><span data-stu-id="de321-137">**\_\_ClassCreationEvent**</span></span>](--classcreationevent.md)

[<span data-ttu-id="de321-138">**\_\_классмодификатионевент**</span><span class="sxs-lookup"><span data-stu-id="de321-138">**\_\_ClassModificationEvent**</span></span>](--classmodificationevent.md)

[<span data-ttu-id="de321-139">**\_\_классделетионевент**</span><span class="sxs-lookup"><span data-stu-id="de321-139">**\_\_ClassDeletionEvent**</span></span>](--classdeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="de321-140">Требования</span><span class="sxs-lookup"><span data-stu-id="de321-140">Requirements</span></span>



| <span data-ttu-id="de321-141">Требование</span><span class="sxs-lookup"><span data-stu-id="de321-141">Requirement</span></span> | <span data-ttu-id="de321-142">Значение</span><span class="sxs-lookup"><span data-stu-id="de321-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="de321-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de321-143">Minimum supported client</span></span><br/> | <span data-ttu-id="de321-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de321-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="de321-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de321-145">Minimum supported server</span></span><br/> | <span data-ttu-id="de321-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de321-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="de321-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de321-147">Namespace</span></span><br/>                | <span data-ttu-id="de321-148">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="de321-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="de321-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de321-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de321-150">**\_\_Событие**</span><span class="sxs-lookup"><span data-stu-id="de321-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="de321-151">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="de321-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="de321-152">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="de321-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

