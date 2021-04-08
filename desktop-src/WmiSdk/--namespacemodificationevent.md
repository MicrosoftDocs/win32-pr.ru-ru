---
description: Сообщает о событии изменения пространства имен, которое представляет собой тип внутреннего события, создаваемого при изменении пространства имен.
ms.assetid: 168505d7-4677-4f41-935e-149f22de2cb5
ms.tgt_platform: multiple
title: Класс __NamespaceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceModificationEvent
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5af5783d3ebfbfb4b7842cb86b1919f8dbed1365
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817616"
---
# <a name="__namespacemodificationevent-class"></a><span data-ttu-id="523d6-103">\_\_Класс Намеспацемодификатионевент</span><span class="sxs-lookup"><span data-stu-id="523d6-103">\_\_NamespaceModificationEvent class</span></span>

<span data-ttu-id="523d6-104">Класс System **\_ \_ намеспацемодификатионевент** сообщает о событии изменения пространства имен, которое представляет собой тип [внутреннего события](determining-the-type-of-event-to-receive.md) , создаваемого при изменении пространства имен.</span><span class="sxs-lookup"><span data-stu-id="523d6-104">The **\_\_NamespaceModificationEvent** system class reports a namespace modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a namespace is modified.</span></span>

<span data-ttu-id="523d6-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="523d6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="523d6-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="523d6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="523d6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="523d6-107">Syntax</span></span>

``` syntax
class __NamespaceModificationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace PreviousNamespace;
  uint8       SECURITY_DESCRIPTOR [];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="523d6-108">Члены</span><span class="sxs-lookup"><span data-stu-id="523d6-108">Members</span></span>

<span data-ttu-id="523d6-109">Класс **\_ \_ намеспацемодификатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="523d6-109">The **\_\_NamespaceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="523d6-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="523d6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="523d6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="523d6-111">Properties</span></span>

<span data-ttu-id="523d6-112">Класс **\_ \_ намеспацемодификатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="523d6-112">The **\_\_NamespaceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="523d6-113">**превиауснамеспаце**</span><span class="sxs-lookup"><span data-stu-id="523d6-113">**PreviousNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523d6-114">Тип данных: **\_ \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="523d6-114">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="523d6-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523d6-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="523d6-116">Копия исходной версии экземпляра [**\_ \_ пространства имен**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="523d6-116">Copy of the original version of a [**\_\_Namespace**](--namespace.md) instance.</span></span> <span data-ttu-id="523d6-117">Свойство **Name** этого экземпляра определяет пространство имен, которое изменяется.</span><span class="sxs-lookup"><span data-stu-id="523d6-117">The **Name** property of this instance identifies the namespace that is modified.</span></span>

</dd> <dt>

<span data-ttu-id="523d6-118">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="523d6-118">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523d6-119">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="523d6-119">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="523d6-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523d6-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="523d6-121">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="523d6-121">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="523d6-122">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-122">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="523d6-123">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="523d6-123">**SECURITY\_DESCRIPTOR**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="523d6-124">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="523d6-124">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="523d6-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523d6-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="523d6-126">Дескриптор, используемый поставщиком событий для определения пользователей, которые могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="523d6-126">Descriptor that the event provider uses to determine the users that can receive an event.</span></span> <span data-ttu-id="523d6-127">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-127">This property is inherited from [**\_\_Event**](--event.md).</span></span>

> [!Note]  
> <span data-ttu-id="523d6-128">**Пустой** список управления доступом (ACL) в [**\_ дескрипторе безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) предоставляет всем всем времени неограниченный доступ.</span><span class="sxs-lookup"><span data-stu-id="523d6-128">A **NULL** access control list (ACL) in the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) grants unlimited access to everyone all the time.</span></span> <span data-ttu-id="523d6-129">Дополнительные сведения см. в разделе [Создание дескриптора безопасности для нового объекта](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="523d6-129">For more information, see [Creating a Security Descriptor for a New Object](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="523d6-130">**Имен**</span><span class="sxs-lookup"><span data-stu-id="523d6-130">**TargetNamespace**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523d6-131">Тип данных: **\_ \_ пространство имен**</span><span class="sxs-lookup"><span data-stu-id="523d6-131">Data type: **\_\_Namespace**</span></span>
</dt> <dt>

<span data-ttu-id="523d6-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523d6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="523d6-133">Копия изменяемого экземпляра [**\_ \_ пространства имен**](--namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="523d6-133">Copy of the [**\_\_Namespace**](--namespace.md) instance that is modified.</span></span> <span data-ttu-id="523d6-134">Свойство **Name** экземпляра **\_ \_ пространства имен** указывает на изменяемое пространство имен.</span><span class="sxs-lookup"><span data-stu-id="523d6-134">The **Name** property of the **\_\_Namespace** instance indicates the namespace that is modified.</span></span> <span data-ttu-id="523d6-135">Это свойство наследуется от класса [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-135">This property is inherited from class [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="523d6-136">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="523d6-136">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="523d6-137">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="523d6-137">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="523d6-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="523d6-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="523d6-139">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="523d6-139">Unique value that indicates the time that an event is generated.</span></span> <span data-ttu-id="523d6-140">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="523d6-140">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="523d6-141">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="523d6-141">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="523d6-142">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-142">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="523d6-143">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="523d6-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="523d6-144">Комментарии</span><span class="sxs-lookup"><span data-stu-id="523d6-144">Remarks</span></span>

<span data-ttu-id="523d6-145">Класс **\_ \_ намеспацемодификатионевент** является производным от [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-145">The **\_\_NamespaceModificationEvent** class is derived from [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md).</span></span>

<span data-ttu-id="523d6-146">Единственным различием между целевым пространством имен и предыдущим пространством имен являются квалификаторы и свойства, кроме [**Name**](--namespace.md).</span><span class="sxs-lookup"><span data-stu-id="523d6-146">The only differences between the target namespace and the previous namespace is the qualifiers and properties except [**Name**](--namespace.md).</span></span>

<span data-ttu-id="523d6-147">Обратите внимание, что свойство [**Name**](--namespace.md) экземпляра **\_ \_ пространства имен** не может быть изменено, так как пространства имен не могут быть переименованы.</span><span class="sxs-lookup"><span data-stu-id="523d6-147">Note that the [**Name**](--namespace.md) property of a **\_\_Namespace** instance cannot change because namespaces cannot be renamed.</span></span> <span data-ttu-id="523d6-148">Чтобы изменить имя пространства имен, необходимо удалить экземпляр **\_ \_ пространства имен** и создать его повторно с новым именем.</span><span class="sxs-lookup"><span data-stu-id="523d6-148">To modify the name of a namespace, the **\_\_Namespace** instance must be deleted and re-created with a new name.</span></span> <span data-ttu-id="523d6-149">Поэтому события изменения пространства имен создаются при возникновении изменений в квалификаторах и свойствах, отличных от **Name**.</span><span class="sxs-lookup"><span data-stu-id="523d6-149">Therefore, namespace modification events are generated when a change occurs to qualifiers and properties other than **Name**.</span></span> <span data-ttu-id="523d6-150">Событие изменения пространства имен не создается при возникновении какого-либо изменения в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="523d6-150">A namespace modification event is not generated when any kind of change occurs within the namespace.</span></span> <span data-ttu-id="523d6-151">Событие изменения пространства имен создается только при изменении экземпляра пространства имен.</span><span class="sxs-lookup"><span data-stu-id="523d6-151">A namespace modification event is generated only when a namespace instance is modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="523d6-152">Требования</span><span class="sxs-lookup"><span data-stu-id="523d6-152">Requirements</span></span>



| <span data-ttu-id="523d6-153">Требование</span><span class="sxs-lookup"><span data-stu-id="523d6-153">Requirement</span></span> | <span data-ttu-id="523d6-154">Значение</span><span class="sxs-lookup"><span data-stu-id="523d6-154">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="523d6-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="523d6-155">Minimum supported client</span></span><br/> | <span data-ttu-id="523d6-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="523d6-156">Windows Vista</span></span><br/>       |
| <span data-ttu-id="523d6-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="523d6-157">Minimum supported server</span></span><br/> | <span data-ttu-id="523d6-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="523d6-158">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="523d6-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="523d6-159">Namespace</span></span><br/>                | <span data-ttu-id="523d6-160">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="523d6-160">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="523d6-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="523d6-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523d6-162">**\_\_намеспацеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="523d6-162">**\_\_NamespaceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[<span data-ttu-id="523d6-163">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="523d6-163">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

