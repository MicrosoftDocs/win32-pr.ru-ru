---
description: Базовый класс для всех внутренних событий, связанных с пространством имен.
ms.assetid: 168637b1-217e-4b6d-bd07-25127b9e9f6c
ms.tgt_platform: multiple
title: Класс __NamespaceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: d263af0eab5fc3899b45659bc8409a5e68776fe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647657"
---
# <a name="__namespaceoperationevent-class"></a><span data-ttu-id="249dd-103">\_\_Класс Намеспацеоператионевент</span><span class="sxs-lookup"><span data-stu-id="249dd-103">\_\_NamespaceOperationEvent class</span></span>

<span data-ttu-id="249dd-104">Класс System **\_ \_ намеспацеоператионевент** является базовым классом для всех внутренних событий, связанных с пространством имен.</span><span class="sxs-lookup"><span data-stu-id="249dd-104">The **\_\_NamespaceOperationEvent** system class is a base class for all intrinsic events that relate to a namespace.</span></span>

<span data-ttu-id="249dd-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="249dd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="249dd-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="249dd-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="249dd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="249dd-107">Syntax</span></span>

``` syntax
class __NamespaceOperationEvent : __Event
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="249dd-108">Члены</span><span class="sxs-lookup"><span data-stu-id="249dd-108">Members</span></span>

<span data-ttu-id="249dd-109">Класс **\_ \_ намеспацеоператионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="249dd-109">The **\_\_NamespaceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="249dd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="249dd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="249dd-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="249dd-111">Properties</span></span>

<span data-ttu-id="249dd-112">Класс **\_ \_ намеспацеоператионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="249dd-112">The **\_\_NamespaceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="249dd-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="249dd-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249dd-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="249dd-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="249dd-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="249dd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249dd-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="249dd-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="249dd-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="249dd-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="249dd-118">**Имен**</span><span class="sxs-lookup"><span data-stu-id="249dd-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249dd-119">Тип данных: **\_ \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="249dd-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="249dd-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="249dd-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249dd-121">Пространство имен, затронутое событием.</span><span class="sxs-lookup"><span data-stu-id="249dd-121">Namespace affected by the event.</span></span> <span data-ttu-id="249dd-122">Для событий создания это только что созданное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="249dd-122">For creation events, this is the newly created namespace.</span></span> <span data-ttu-id="249dd-123">Для событий изменения это измененное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="249dd-123">For modification events, this is the changed namespace.</span></span> <span data-ttu-id="249dd-124">Для событий удаления это удаленное пространство имен.</span><span class="sxs-lookup"><span data-stu-id="249dd-124">For deletion events, this is the deleted namespace.</span></span>

</dd> <dt>

<span data-ttu-id="249dd-125">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="249dd-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="249dd-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="249dd-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="249dd-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="249dd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="249dd-128">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="249dd-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="249dd-129">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="249dd-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="249dd-130">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="249dd-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="249dd-131">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="249dd-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="249dd-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="249dd-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="249dd-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="249dd-133">Remarks</span></span>

<span data-ttu-id="249dd-134">Класс **\_ \_ намеспацеоператионевент** является производным от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="249dd-134">The **\_\_NamespaceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="249dd-135">Экземпляры этого класса не создаются.</span><span class="sxs-lookup"><span data-stu-id="249dd-135">Instances of this class are not created.</span></span> <span data-ttu-id="249dd-136">Инструментарий WMI создает экземпляры одного из следующих классов, производных от этого класса:</span><span class="sxs-lookup"><span data-stu-id="249dd-136">WMI creates instances of one of the following classes derived from this class:</span></span>

[<span data-ttu-id="249dd-137">**\_\_намеспацекреатионевент**</span><span class="sxs-lookup"><span data-stu-id="249dd-137">**\_\_NamespaceCreationEvent**</span></span>](--namespacecreationevent.md)

[<span data-ttu-id="249dd-138">**\_\_намеспацемодификатионевент**</span><span class="sxs-lookup"><span data-stu-id="249dd-138">**\_\_NamespaceModificationEvent**</span></span>](--namespacemodificationevent.md)

[<span data-ttu-id="249dd-139">**\_\_намеспацеделетионевент**</span><span class="sxs-lookup"><span data-stu-id="249dd-139">**\_\_NamespaceDeletionEvent**</span></span>](--namespacedeletionevent.md)

## <a name="requirements"></a><span data-ttu-id="249dd-140">Требования</span><span class="sxs-lookup"><span data-stu-id="249dd-140">Requirements</span></span>



| <span data-ttu-id="249dd-141">Требование</span><span class="sxs-lookup"><span data-stu-id="249dd-141">Requirement</span></span> | <span data-ttu-id="249dd-142">Значение</span><span class="sxs-lookup"><span data-stu-id="249dd-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="249dd-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="249dd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="249dd-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="249dd-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="249dd-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="249dd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="249dd-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="249dd-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="249dd-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="249dd-147">Namespace</span></span><br/>                | <span data-ttu-id="249dd-148">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="249dd-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="249dd-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="249dd-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="249dd-150">**\_\_Событие**</span><span class="sxs-lookup"><span data-stu-id="249dd-150">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="249dd-151">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="249dd-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="249dd-152">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="249dd-152">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> </dl>

 

