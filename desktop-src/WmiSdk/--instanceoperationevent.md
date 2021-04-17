---
description: Служит базовым классом для всех внутренних событий, связанных с экземпляром.
ms.assetid: f6d2b6e5-0dca-4cb5-95a5-33b45cd76807
ms.tgt_platform: multiple
title: Класс __InstanceOperationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceOperationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 1d3111b74c876cc7ffedb959eca7f46812ed92e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703016"
---
# <a name="__instanceoperationevent-class"></a><span data-ttu-id="991c4-103">\_\_Класс Инстанцеоператионевент</span><span class="sxs-lookup"><span data-stu-id="991c4-103">\_\_InstanceOperationEvent class</span></span>

<span data-ttu-id="991c4-104">Системный класс **\_ \_ инстанцеоператионевент** выступает в качестве базового класса для всех внутренних событий, связанных с экземпляром.</span><span class="sxs-lookup"><span data-stu-id="991c4-104">The **\_\_InstanceOperationEvent** system class serves as a base class for all intrinsic events that relate to an instance.</span></span>

<span data-ttu-id="991c4-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="991c4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="991c4-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="991c4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="991c4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="991c4-107">Syntax</span></span>

``` syntax
class __InstanceOperationEvent : __Event
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="991c4-108">Члены</span><span class="sxs-lookup"><span data-stu-id="991c4-108">Members</span></span>

<span data-ttu-id="991c4-109">Класс **\_ \_ инстанцеоператионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="991c4-109">The **\_\_InstanceOperationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="991c4-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="991c4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="991c4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="991c4-111">Properties</span></span>

<span data-ttu-id="991c4-112">Класс **\_ \_ инстанцеоператионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="991c4-112">The **\_\_InstanceOperationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="991c4-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="991c4-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991c4-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="991c4-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="991c4-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="991c4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="991c4-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="991c4-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="991c4-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="991c4-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="991c4-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="991c4-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991c4-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="991c4-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="991c4-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="991c4-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="991c4-121">Экземпляр, затронутый событием.</span><span class="sxs-lookup"><span data-stu-id="991c4-121">Instance affected by the event.</span></span> <span data-ttu-id="991c4-122">Для событий создания это только что созданный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="991c4-122">For creation events, this is the newly created instance.</span></span> <span data-ttu-id="991c4-123">Для событий изменения это новая версия измененного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="991c4-123">For modification events, this is the new version of the changed instance.</span></span> <span data-ttu-id="991c4-124">Для событий удаления это удаленный экземпляр.</span><span class="sxs-lookup"><span data-stu-id="991c4-124">For deletion events, this is the deleted instance.</span></span>

</dd> <dt>

<span data-ttu-id="991c4-125">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="991c4-125">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="991c4-126">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="991c4-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="991c4-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="991c4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="991c4-128">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="991c4-128">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="991c4-129">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="991c4-129">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="991c4-130">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="991c4-130">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="991c4-131">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="991c4-131">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="991c4-132">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="991c4-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="991c4-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="991c4-133">Remarks</span></span>

<span data-ttu-id="991c4-134">Класс **\_ \_ инстанцеоператионевент** является производным от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="991c4-134">The **\_\_InstanceOperationEvent** class is derived from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="991c4-135">Экземпляры **\_ \_ инстанцеоператионевент** не создаются; создаются только экземпляры его подклассов.</span><span class="sxs-lookup"><span data-stu-id="991c4-135">Instances of **\_\_InstanceOperationEvent** are not created; only instances of its subclasses are created.</span></span> <span data-ttu-id="991c4-136">Следующие классы являются производными от **\_ \_ инстанцеоператионевент**:</span><span class="sxs-lookup"><span data-stu-id="991c4-136">The following classes derive from **\_\_InstanceOperationEvent**:</span></span>

[<span data-ttu-id="991c4-137">**\_\_инстанцекреатионевент**</span><span class="sxs-lookup"><span data-stu-id="991c4-137">**\_\_InstanceCreationEvent**</span></span>](--instancecreationevent.md)

[<span data-ttu-id="991c4-138">**\_\_инстанцемодификатионевент**</span><span class="sxs-lookup"><span data-stu-id="991c4-138">**\_\_InstanceModificationEvent**</span></span>](--instancemodificationevent.md)

[<span data-ttu-id="991c4-139">**\_\_инстанцеделетионевент**</span><span class="sxs-lookup"><span data-stu-id="991c4-139">**\_\_InstanceDeletionEvent**</span></span>](--instancedeletionevent.md)

<span data-ttu-id="991c4-140">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="991c4-140">**Overview**</span></span>

<span data-ttu-id="991c4-141">Так же, как и класс WMI, представляющий каждый тип системного ресурса, который может управляться с помощью WMI, существует класс WMI, представляющий каждый тип события WMI.</span><span class="sxs-lookup"><span data-stu-id="991c4-141">Just as there is a WMI class that represents each type of system resource that can be managed using WMI, there is a WMI class that represents each type of WMI event.</span></span> <span data-ttu-id="991c4-142">При возникновении события, которое может отслеживаться WMI, создается экземпляр соответствующего класса событий WMI.</span><span class="sxs-lookup"><span data-stu-id="991c4-142">When an event that can be monitored by WMI occurs, an instance of the corresponding WMI event class is created.</span></span> <span data-ttu-id="991c4-143">Событие WMI возникает при создании этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="991c4-143">A WMI event occurs when that instance is created.</span></span>

<span data-ttu-id="991c4-144">Существует три основных типа классов событий WMI, которые являются производными от класса WMI [**\_ \_ событий**](--event.md) : внутренние события, внешние события и события таймера.</span><span class="sxs-lookup"><span data-stu-id="991c4-144">There are three major types of WMI event classes, all of which are derived from the [**\_\_Event**](--event.md) WMI class: Intrinsic Events, Extrinsic Events, and Timer Events.</span></span> <span data-ttu-id="991c4-145">Внутренние события, в свою очередь, представляются тремя разными классами, производными от класса **\_ \_ событий** : [**\_ \_ намеспацеоператионевент**](--namespaceoperationevent.md), **\_ \_ инстанцеоператионевент** и [**\_ \_ классоператионевент**](--classoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="991c4-145">Intrinsic Events, in turn, are represented by three distinct classes derived from the **\_\_Event** class: [**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md), **\_\_InstanceOperationEvent**, and [**\_\_ClassOperationEvent**](--classoperationevent.md).</span></span>

<span data-ttu-id="991c4-146">Внутренние события</span><span class="sxs-lookup"><span data-stu-id="991c4-146">Intrinsic Events</span></span>

<span data-ttu-id="991c4-147">Внутренние события используются для мониторинга ресурса, представленного классом в репозитории CIM.</span><span class="sxs-lookup"><span data-stu-id="991c4-147">Intrinsic events are used to monitor a resource represented by a class in the CIM repository.</span></span> <span data-ttu-id="991c4-148">Каждый ресурс представлен экземпляром класса.</span><span class="sxs-lookup"><span data-stu-id="991c4-148">Each resource is represented by an instance of a class.</span></span> <span data-ttu-id="991c4-149">Это означает, что наблюдение за ресурсом с помощью WMI на самом деле включает наблюдение за экземплярами, которые соответствуют ресурсу.</span><span class="sxs-lookup"><span data-stu-id="991c4-149">This means that monitoring a resource using WMI actually involves monitoring the instances that correspond to the resource.</span></span>

<span data-ttu-id="991c4-150">Внутренние события также можно использовать для отслеживания изменений в пространстве имен или классе в репозитории.</span><span class="sxs-lookup"><span data-stu-id="991c4-150">Intrinsic events can also be used to monitor changes to a namespace or class in the repository.</span></span> <span data-ttu-id="991c4-151">Однако наблюдение за изменениями пространств имен или классов имеет ограниченное значение для системных администраторов.</span><span class="sxs-lookup"><span data-stu-id="991c4-151">However, monitoring changes to namespaces or classes is of limited value to system administrators.</span></span>

<span data-ttu-id="991c4-152">Внутреннее событие представлено экземпляром класса, производного от \_ \_ инстанцеоператионевент, \_ \_ намеспацеоператионевент или \_ \_ классоператионевент.</span><span class="sxs-lookup"><span data-stu-id="991c4-152">An intrinsic event is represented by an instance of a class derived from \_\_InstanceOperationEvent, \_\_NamespaceOperationEvent, or \_\_ClassOperationEvent.</span></span> <span data-ttu-id="991c4-153">Любые изменения в экземплярах WMI представлены \_ \_ классом инстанцеоператионевент и производными от него классами: \_ \_ инстанцекреатионевент, \_ \_ инстанцемодификатионевент и \_ \_ инстанцеделетионевент.</span><span class="sxs-lookup"><span data-stu-id="991c4-153">Any changes to instances in WMI are represented by the \_\_InstanceOperationEvent class and the classes derived from it: \_\_InstanceCreationEvent, \_\_InstanceModificationEvent, and \_\_InstanceDeletionEvent.</span></span>

<span data-ttu-id="991c4-154">Мониторинг ресурсов с помощью WMI включает в себя наблюдение за экземплярами, а все изменения экземпляров представляются \_ \_ инстанцеоператионевент и производными от него классами.</span><span class="sxs-lookup"><span data-stu-id="991c4-154">Monitoring resources using WMI involves monitoring instances and all changes to instances are represented by \_\_InstanceOperationEvent and the classes derived from it.</span></span> <span data-ttu-id="991c4-155">Это означает, что в конечном счете ресурсы мониторинга требуют наблюдения за экземплярами \_ \_ классов, производных от инстанцеоператионевент.</span><span class="sxs-lookup"><span data-stu-id="991c4-155">This means that monitoring resources ultimately involves monitoring instances of \_\_InstanceOperationEvent-derived classes.</span></span>

<span data-ttu-id="991c4-156">Вы регистрируете интерес в экземплярах одного из этих классов, выполнив запрос уведомления, выраженный в WQL.</span><span class="sxs-lookup"><span data-stu-id="991c4-156">You register interest in instances of one of these classes by issuing a notification query expressed in WQL.</span></span> <span data-ttu-id="991c4-157">Запрос использует синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="991c4-157">The query uses syntax similar to the following:</span></span>

`SELECT * FROM __InstanceOperationEventOrDerivedClass WITHIN PollingInterval WHERE TargetInstance ISA WMIClassName AND TargetInstance.WMIClassPropertyName = Value`

<span data-ttu-id="991c4-158">Более подробное описание использования событий экземпляра WMI для мониторинга активности компьютера см. в разделе [как можно отслеживать различные типы событий с помощью всего одного сценария?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span><span class="sxs-lookup"><span data-stu-id="991c4-158">For a longer discussion of using the WMI instance events to monitor computer activity, see [How Can I Monitor for Different Types of Events With Just One Script?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/04/04/how-can-i-monitor-for-different-types-of-events-with-just-one-script.aspx)</span></span>

## <a name="examples"></a><span data-ttu-id="991c4-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="991c4-159">Examples</span></span>

<span data-ttu-id="991c4-160">Пример кода VBScript [Processing](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) в коллекции TechNet использует **\_ \_ инстанцеоператионевент** для мониторинга первого события экземпляра WMI для [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="991c4-160">The [Monitor process event](https://Gallery.TechNet.Microsoft.Com/94c7dc4c-813a-411d-aa3f-f98982cd2a2f) VBScript code sample on TechNet Gallery uses **\_\_InstanceOperationEvent** to monitors the first WMI instance event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="991c4-161">Требования</span><span class="sxs-lookup"><span data-stu-id="991c4-161">Requirements</span></span>



| <span data-ttu-id="991c4-162">Требование</span><span class="sxs-lookup"><span data-stu-id="991c4-162">Requirement</span></span> | <span data-ttu-id="991c4-163">Значение</span><span class="sxs-lookup"><span data-stu-id="991c4-163">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="991c4-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="991c4-164">Minimum supported client</span></span><br/> | <span data-ttu-id="991c4-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="991c4-165">Windows Vista</span></span><br/>       |
| <span data-ttu-id="991c4-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="991c4-166">Minimum supported server</span></span><br/> | <span data-ttu-id="991c4-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="991c4-167">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="991c4-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="991c4-168">Namespace</span></span><br/>                | <span data-ttu-id="991c4-169">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="991c4-169">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="991c4-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="991c4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="991c4-171">**\_\_Событие**</span><span class="sxs-lookup"><span data-stu-id="991c4-171">**\_\_Event**</span></span>](/windows/desktop/WmiSdk/--event)
</dt> <dt>

[<span data-ttu-id="991c4-172">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="991c4-172">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="991c4-173">Определение типа получаемого события</span><span class="sxs-lookup"><span data-stu-id="991c4-173">Determining the Type of Event to Receive</span></span>](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[<span data-ttu-id="991c4-174">Запись в файл журнала на основе события</span><span class="sxs-lookup"><span data-stu-id="991c4-174">Writing to a Log File Based on an Event</span></span>](writing-to-a-log-file-based-on-an-event.md)
</dt> </dl>

 

