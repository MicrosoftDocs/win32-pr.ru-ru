---
description: Сообщает о событии создания пространства имен, которое представляет собой тип встроенного события, создаваемого при добавлении нового пространства имен к текущему пространству имен.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: Класс __NamespaceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 8432bcfb2c96c70b91a7f0d187297217082e2d28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673955"
---
# <a name="__namespacecreationevent-class"></a><span data-ttu-id="94e50-103">\_\_Класс Намеспацекреатионевент</span><span class="sxs-lookup"><span data-stu-id="94e50-103">\_\_NamespaceCreationEvent class</span></span>

<span data-ttu-id="94e50-104">Класс System **\_ \_ намеспацекреатионевент** сообщает о событии создания пространства имен, которое представляет собой тип [встроенного события](determining-the-type-of-event-to-receive.md) , создаваемого при добавлении нового пространства имен к текущему пространству имен.</span><span class="sxs-lookup"><span data-stu-id="94e50-104">The **\_\_NamespaceCreationEvent** system class reports a namespace creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when a new namespace is added to the current namespace.</span></span>

<span data-ttu-id="94e50-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="94e50-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="94e50-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="94e50-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e50-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94e50-107">Syntax</span></span>

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="94e50-108">Члены</span><span class="sxs-lookup"><span data-stu-id="94e50-108">Members</span></span>

<span data-ttu-id="94e50-109">Класс **\_ \_ намеспацекреатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="94e50-109">The **\_\_NamespaceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="94e50-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="94e50-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="94e50-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="94e50-111">Properties</span></span>

<span data-ttu-id="94e50-112">Класс **\_ \_ намеспацекреатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="94e50-112">The **\_\_NamespaceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="94e50-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="94e50-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e50-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="94e50-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="94e50-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94e50-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e50-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="94e50-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="94e50-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="94e50-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="94e50-118">**Имен**</span><span class="sxs-lookup"><span data-stu-id="94e50-118">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e50-119">Тип данных: **\_ \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="94e50-119">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="94e50-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94e50-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e50-121">Копия созданного экземпляра [**\_ \_ пространства имен**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="94e50-121">Copy of the [**\_\_Namespace**](--namespace.md) instance that was created.</span></span> <span data-ttu-id="94e50-122">Свойство **Name** экземпляра **\_ \_ пространства имен** указывает, какое пространство имен было создано.</span><span class="sxs-lookup"><span data-stu-id="94e50-122">The **Name** property of the **\_\_Namespace** instance indicates which namespace was created.</span></span> <span data-ttu-id="94e50-123">Это свойство наследуется от [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="94e50-123">This property is inherited from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="94e50-124">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="94e50-124">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="94e50-125">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="94e50-125">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="94e50-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="94e50-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="94e50-127">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="94e50-127">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="94e50-128">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="94e50-128">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="94e50-129">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="94e50-129">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="94e50-130">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="94e50-130">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="94e50-131">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="94e50-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="94e50-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94e50-132">Remarks</span></span>

<span data-ttu-id="94e50-133">Класс **\_ \_ намеспацекреатионевент** является производным от [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="94e50-133">The **\_\_NamespaceCreationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="94e50-134">Требования</span><span class="sxs-lookup"><span data-stu-id="94e50-134">Requirements</span></span>



| <span data-ttu-id="94e50-135">Требование</span><span class="sxs-lookup"><span data-stu-id="94e50-135">Requirement</span></span> | <span data-ttu-id="94e50-136">Значение</span><span class="sxs-lookup"><span data-stu-id="94e50-136">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94e50-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94e50-137">Minimum supported client</span></span><br/> | <span data-ttu-id="94e50-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94e50-138">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94e50-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94e50-139">Minimum supported server</span></span><br/> | <span data-ttu-id="94e50-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94e50-140">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="94e50-141">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="94e50-141">Namespace</span></span><br/>                | <span data-ttu-id="94e50-142">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="94e50-142">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="94e50-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94e50-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e50-144">**\_\_намеспацеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="94e50-144">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="94e50-145">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="94e50-145">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

