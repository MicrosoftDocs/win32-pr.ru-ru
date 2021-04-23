---
description: Сообщает о событии создания экземпляра, которое представляет собой тип внутреннего события, создаваемого при добавлении нового экземпляра в пространство имен.
ms.assetid: 41976479-70e3-4914-a56a-fa94a1fd31c7
ms.tgt_platform: multiple
title: Класс __InstanceCreationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 29bdefbe1db20cd8b55b74433061b6c0cf152378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272239"
---
# <a name="__instancecreationevent-class"></a><span data-ttu-id="f57dc-103">\_\_Класс Инстанцекреатионевент</span><span class="sxs-lookup"><span data-stu-id="f57dc-103">\_\_InstanceCreationEvent class</span></span>

<span data-ttu-id="f57dc-104">Класс System **\_ \_ инстанцекреатионевент** сообщает о событии создания экземпляра, которое представляет собой тип [внутреннего события](determining-the-type-of-event-to-receive.md) , создаваемого при добавлении нового экземпляра в пространство имен.</span><span class="sxs-lookup"><span data-stu-id="f57dc-104">The **\_\_InstanceCreationEvent** system class reports an instance creation event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) that is generated when a new instance is added to the namespace.</span></span>

<span data-ttu-id="f57dc-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f57dc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f57dc-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f57dc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f57dc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f57dc-107">Syntax</span></span>

``` syntax
class __InstanceCreationEvent : __InstanceOperationEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="f57dc-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f57dc-108">Members</span></span>

<span data-ttu-id="f57dc-109">Класс **\_ \_ инстанцекреатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f57dc-109">The **\_\_InstanceCreationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="f57dc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f57dc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f57dc-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f57dc-111">Properties</span></span>

<span data-ttu-id="f57dc-112">Класс **\_ \_ инстанцекреатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f57dc-112">The **\_\_InstanceCreationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f57dc-113">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="f57dc-113">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f57dc-114">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="f57dc-114">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f57dc-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f57dc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f57dc-116">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="f57dc-116">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="f57dc-117">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f57dc-117">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="f57dc-118">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="f57dc-118">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f57dc-119">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="f57dc-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f57dc-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f57dc-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f57dc-121">Копия созданного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f57dc-121">Copy of the instance that was created.</span></span> <span data-ttu-id="f57dc-122">Это свойство наследуется от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="f57dc-122">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f57dc-123">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="f57dc-123">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f57dc-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f57dc-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f57dc-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f57dc-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f57dc-126">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="f57dc-126">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="f57dc-127">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="f57dc-127">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="f57dc-128">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="f57dc-128">The information is in the Coordinated Universal Time (UTC) format.</span></span> <span data-ttu-id="f57dc-129">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="f57dc-129">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="f57dc-130">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f57dc-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f57dc-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f57dc-131">Remarks</span></span>

<span data-ttu-id="f57dc-132">Класс **\_ \_ инстанцекреатионевент** является производным от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="f57dc-132">The **\_\_InstanceCreationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="f57dc-133">**Создание ресурса: \_ \_ инстанцекреатионевент**</span><span class="sxs-lookup"><span data-stu-id="f57dc-133">**Creation of a resource: \_\_InstanceCreationEvent**</span></span>

<span data-ttu-id="f57dc-134">Предположим, вы заинтересованы в получении уведомления, если на определенном компьютере запущен Блокнот.</span><span class="sxs-lookup"><span data-stu-id="f57dc-134">Suppose you are interested in receiving a notification if Notepad is run on a certain computer.</span></span> <span data-ttu-id="f57dc-135">При запуске блокнота создается соответствующий процесс.</span><span class="sxs-lookup"><span data-stu-id="f57dc-135">When Notepad runs, a corresponding process is created.</span></span> <span data-ttu-id="f57dc-136">Управление процессами осуществляется с помощью инструментария WMI и представляется \_ классом процесса Win32.</span><span class="sxs-lookup"><span data-stu-id="f57dc-136">Processes can be managed by using WMI and are represented by the Win32\_Process class.</span></span> <span data-ttu-id="f57dc-137">Когда запускается блокнот, соответствующий экземпляр \_ класса процесса Win32 станет доступен через инструментарий WMI.</span><span class="sxs-lookup"><span data-stu-id="f57dc-137">When Notepad starts running, a corresponding instance of the Win32\_Process class becomes available through WMI.</span></span> <span data-ttu-id="f57dc-138">Если вы зарегистрировали интерес в этом событии (выполнив соответствующий запрос уведомления о событиях), доступность этого экземпляра приведет к созданию экземпляра класса **\_ \_ инстанцекреатионевент** .</span><span class="sxs-lookup"><span data-stu-id="f57dc-138">If you have registered your interest in this event (by issuing the appropriate event notification query), the availability of this instance results in the creation of an instance of the **\_\_InstanceCreationEvent** class.</span></span>

<span data-ttu-id="f57dc-139">Запросы уведомлений, которые запрашивают уведомление о создании ресурса и используют встроенные события, используют синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="f57dc-139">Notification queries that request notification of the creation of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceCreationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Process' and TargetInstance.Name = 'notepad.exe'`

<span data-ttu-id="f57dc-140">Более подробное обсуждение использования **\_ \_ инстанцекреатионевент** в качестве способа мониторинга файловых систем см. в разделе [инструментарий WMI и мониторинг файловой системы](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) в кодепрожект.</span><span class="sxs-lookup"><span data-stu-id="f57dc-140">For a larger discussion of using **\_\_InstanceCreationEvent** as a way to monitor file systems, see [WMI and File System Monitoring](https://www.codeproject.com/Articles/42212/WMI-and-File-System-Monitoring) on CodeProject.</span></span>

## <a name="examples"></a><span data-ttu-id="f57dc-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="f57dc-141">Examples</span></span>

<span data-ttu-id="f57dc-142">[Процедура создания постоянной регистрации событий WMI для мониторинга файлов](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) в коллекции TechNet использует **\_ \_ инстанцекреатионевент** в составе сложного сценария для настройки постоянной регистрации событий WMI.</span><span class="sxs-lookup"><span data-stu-id="f57dc-142">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a complex script to set up a permanent WMI event registration.</span></span>

<span data-ttu-id="f57dc-143">Пример PowerShell для [постоянных событий PowerShell](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) в коллекции TechNet использует **\_ \_ инстанцекреатионевент** как часть демонстрационного сценария для настройки постоянной регистрации событий.</span><span class="sxs-lookup"><span data-stu-id="f57dc-143">The [PowerShell WMI Permanent Events](https://Gallery.TechNet.Microsoft.Com/PowerShell-WMI-Permanent-7e17f262) PowerShell example on TechNet Gallery uses **\_\_InstanceCreationEvent** as part of a demonstration script for setting up a permanent event registration.</span></span>

<span data-ttu-id="f57dc-144">Пример сценария VBScript для [создания процесса](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) на сайте TechNet использует **\_ \_ инстанцекреатионевент** для мониторинга первого события создания экземпляра WMI для [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="f57dc-144">The [Monitor process creation event](https://Gallery.TechNet.Microsoft.Com/6f137d9e-f00a-4f0a-ad07-7d752ff5251d) VBScript sample on TechNet uses **\_\_InstanceCreationEvent** to monitors the first WMI instance creation event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="f57dc-145">Требования</span><span class="sxs-lookup"><span data-stu-id="f57dc-145">Requirements</span></span>



| <span data-ttu-id="f57dc-146">Требование</span><span class="sxs-lookup"><span data-stu-id="f57dc-146">Requirement</span></span> | <span data-ttu-id="f57dc-147">Значение</span><span class="sxs-lookup"><span data-stu-id="f57dc-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f57dc-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f57dc-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f57dc-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f57dc-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f57dc-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f57dc-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f57dc-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f57dc-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f57dc-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f57dc-152">Namespace</span></span><br/>                | <span data-ttu-id="f57dc-153">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="f57dc-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f57dc-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f57dc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f57dc-155">**\_\_инстанцеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="f57dc-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="f57dc-156">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="f57dc-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

