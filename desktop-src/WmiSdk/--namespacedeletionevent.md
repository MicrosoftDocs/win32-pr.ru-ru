---
description: Сообщает о событии удаления пространства имен, которое представляет собой тип внутреннего события, создаваемого при удалении подпространства имен из текущего пространства имен.
ms.assetid: f7160a90-562d-40d9-9189-32aaabcd81d0
ms.tgt_platform: multiple
title: Класс __NamespaceDeletionEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceDeletionEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6e23f909718167760c02bbdb38e2a075d04bc516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647658"
---
# <a name="__namespacedeletionevent-class"></a><span data-ttu-id="dc0c0-103">\_\_Класс Намеспацеделетионевент</span><span class="sxs-lookup"><span data-stu-id="dc0c0-103">\_\_NamespaceDeletionEvent class</span></span>

<span data-ttu-id="dc0c0-104">Класс System **\_ \_ намеспацеделетионевент** сообщает о событии удаления пространства имен, которое представляет собой тип [внутреннего события](determining-the-type-of-event-to-receive.md) , создаваемого при удалении подпространства имен из текущего пространства имен.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-104">The **\_\_NamespaceDeletionEvent** system class reports a namespace deletion event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a sub-namespace is removed from the current namespace.</span></span>

<span data-ttu-id="dc0c0-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="dc0c0-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc0c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc0c0-107">Syntax</span></span>

``` syntax
class __NamespaceDeletionEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="dc0c0-108">Члены</span><span class="sxs-lookup"><span data-stu-id="dc0c0-108">Members</span></span>

<span data-ttu-id="dc0c0-109">Класс **\_ \_ намеспацеделетионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc0c0-109">The **\_\_NamespaceDeletionEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="dc0c0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc0c0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc0c0-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc0c0-111">Properties</span></span>

<span data-ttu-id="dc0c0-112">Класс **\_ \_ намеспацеделетионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-112">The **\_\_NamespaceDeletionEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc0c0-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc0c0-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="dc0c0-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc0c0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc0c0-116">Дескриптор, используемый поставщиком событий для определения пользователей, которые могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-116">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="dc0c0-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc0c0-118">**Имен**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc0c0-119">Тип данных: **\_ \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="dc0c0-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc0c0-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc0c0-121">Копия удаляемого экземпляра [**\_ \_ пространства имен**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="dc0c0-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that is deleted.</span></span> <span data-ttu-id="dc0c0-122">Свойство **Name** экземпляра **\_ \_ пространства имен** определяет пространство имен, которое удаляется.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-122">The **Name** property of the **\_\_Namespace** instance identifies the namespace that is deleted.</span></span> <span data-ttu-id="dc0c0-123">Это свойство наследуется от [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="dc0c0-124">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc0c0-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="dc0c0-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc0c0-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc0c0-127">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-127">Unique value that indicates the time an event is generated.</span></span> <span data-ttu-id="dc0c0-128">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="dc0c0-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="dc0c0-129">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="dc0c0-130">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="dc0c0-131">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc0c0-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc0c0-132">Remarks</span></span>

<span data-ttu-id="dc0c0-133">Класс **\_ \_ намеспацеделетионевент** является производным от [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="dc0c0-133">The **\_\_NamespaceDeletionEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc0c0-134">Требования</span><span class="sxs-lookup"><span data-stu-id="dc0c0-134">Requirements</span></span>



| <span data-ttu-id="dc0c0-135">Требование</span><span class="sxs-lookup"><span data-stu-id="dc0c0-135">Requirement</span></span> | <span data-ttu-id="dc0c0-136">Значение</span><span class="sxs-lookup"><span data-stu-id="dc0c0-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dc0c0-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc0c0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="dc0c0-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc0c0-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dc0c0-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc0c0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="dc0c0-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc0c0-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="dc0c0-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc0c0-141">Namespace</span></span><br/>                | <span data-ttu-id="dc0c0-142">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="dc0c0-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="dc0c0-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc0c0-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc0c0-144">**\_\_намеспацеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="dc0c0-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="dc0c0-145">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="dc0c0-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

