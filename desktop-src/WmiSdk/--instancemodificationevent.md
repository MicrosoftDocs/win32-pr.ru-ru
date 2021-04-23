---
description: Сообщает о событии изменения экземпляра, которое представляет собой тип внутреннего события, создаваемого при изменении экземпляра в пространстве имен.
ms.assetid: aa35f349-8b57-435f-bf82-76daf2b43ec9
ms.tgt_platform: multiple
title: Класс __InstanceModificationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceModificationEvent
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: e644db16b6638bbc87006819e186540a9ce1874e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911523"
---
# <a name="__instancemodificationevent-class"></a><span data-ttu-id="927e3-103">\_\_Класс Инстанцемодификатионевент</span><span class="sxs-lookup"><span data-stu-id="927e3-103">\_\_InstanceModificationEvent class</span></span>

<span data-ttu-id="927e3-104">Класс System **\_ \_ инстанцемодификатионевент** сообщает о событии изменения экземпляра, которое представляет собой тип [внутреннего события](determining-the-type-of-event-to-receive.md) , создаваемого при изменении экземпляра в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="927e3-104">The **\_\_InstanceModificationEvent** system class reports an instance modification event, which is a type of [intrinsic event](determining-the-type-of-event-to-receive.md) generated when an instance changes in the namespace.</span></span>

<span data-ttu-id="927e3-105">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="927e3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="927e3-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="927e3-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="927e3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="927e3-107">Syntax</span></span>

``` syntax
class __InstanceModificationEvent : __InstanceOperationEvent
{
  object PreviousInstance;
  uint8  SECURITY_DESCRIPTOR[];
  object TargetInstance;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a><span data-ttu-id="927e3-108">Члены</span><span class="sxs-lookup"><span data-stu-id="927e3-108">Members</span></span>

<span data-ttu-id="927e3-109">Класс **\_ \_ инстанцемодификатионевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="927e3-109">The **\_\_InstanceModificationEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="927e3-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="927e3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="927e3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="927e3-111">Properties</span></span>

<span data-ttu-id="927e3-112">Класс **\_ \_ инстанцемодификатионевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="927e3-112">The **\_\_InstanceModificationEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="927e3-113">**PreviousInstance**</span><span class="sxs-lookup"><span data-stu-id="927e3-113">**PreviousInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="927e3-114">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="927e3-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="927e3-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="927e3-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="927e3-116">Копия экземпляра перед изменением.</span><span class="sxs-lookup"><span data-stu-id="927e3-116">Copy of the instance prior to modification.</span></span>

</dd> <dt>

<span data-ttu-id="927e3-117">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="927e3-117">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="927e3-118">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="927e3-118">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="927e3-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="927e3-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="927e3-120">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="927e3-120">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="927e3-121">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="927e3-121">This property is inherited from [**\_\_Event**](--event.md).</span></span>

</dd> <dt>

<span data-ttu-id="927e3-122">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="927e3-122">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="927e3-123">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="927e3-123">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="927e3-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="927e3-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="927e3-125">Новая версия измененного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="927e3-125">New version of the changed instance.</span></span> <span data-ttu-id="927e3-126">Это свойство наследуется от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="927e3-126">This property is inherited from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

</dd> <dt>

<span data-ttu-id="927e3-127">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="927e3-127">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="927e3-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="927e3-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="927e3-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="927e3-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="927e3-130">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="927e3-130">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="927e3-131">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="927e3-131">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="927e3-132">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="927e3-132">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="927e3-133">Это свойство наследуется от [**\_ \_ события**](--event.md).</span><span class="sxs-lookup"><span data-stu-id="927e3-133">This property is inherited from [**\_\_Event**](--event.md).</span></span>

<span data-ttu-id="927e3-134">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="927e3-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="927e3-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="927e3-135">Remarks</span></span>

<span data-ttu-id="927e3-136">Класс **\_ \_ инстанцемодификатионевент** является производным от [**\_ \_ инстанцеоператионевент**](--instanceoperationevent.md).</span><span class="sxs-lookup"><span data-stu-id="927e3-136">The **\_\_InstanceModificationEvent** class is derived from [**\_\_InstanceOperationEvent**](--instanceoperationevent.md).</span></span>

<span data-ttu-id="927e3-137">**Изменение ресурса: \_ \_ инстанцемодификатионевент**</span><span class="sxs-lookup"><span data-stu-id="927e3-137">**Modification of a resource: \_\_InstanceModificationEvent**</span></span>

<span data-ttu-id="927e3-138">Предположим, вы подозреваете, что используемое приложение управления ошибочно изменяет тип запуска службы на одном из серверов.</span><span class="sxs-lookup"><span data-stu-id="927e3-138">Suppose you suspect that a management application you are using is erroneously changing the startup type of a service on one of your servers.</span></span> <span data-ttu-id="927e3-139">Необходимо написать сценарий WMI для отслеживания изменений, внесенных в конфигурацию службы.</span><span class="sxs-lookup"><span data-stu-id="927e3-139">You want to write a WMI script to monitor any modifications made to the configuration of the service.</span></span> <span data-ttu-id="927e3-140">Как только изменения вносятся в службу, ее соответствующий TargetInstance отражает изменение.</span><span class="sxs-lookup"><span data-stu-id="927e3-140">As soon as a modification is made to a service, its corresponding TargetInstance reflects the modification.</span></span>

<span data-ttu-id="927e3-141">Если вы регистрируете интерес в этом событии, изменение конфигурации службы приводит к созданию экземпляра класса **\_ \_ инстанцемодификатионевент** .</span><span class="sxs-lookup"><span data-stu-id="927e3-141">If you register your interest in this event, a modification to the configuration of the service results in the creation of an instance of the **\_\_InstanceModificationEvent** class.</span></span>

<span data-ttu-id="927e3-142">Запросы уведомлений, которые запрашивают уведомление об изменении ресурса и используют встроенные события, используют синтаксис, аналогичный приведенному ниже.</span><span class="sxs-lookup"><span data-stu-id="927e3-142">Notification queries that request notification of the modification of a resource and use intrinsic events all use syntax similar to the following:</span></span>

`SELECT * FROM __InstanceModificationEvent WITHIN PollingInterval WHERE TargetInstance ISA 'Win32_Service' and TargetInstance.Name = 'alerter'`

## <a name="examples"></a><span data-ttu-id="927e3-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="927e3-143">Examples</span></span>

<span data-ttu-id="927e3-144">Пример скрипта VBScript для [события изменения процесса](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) в коллекции TechNet использует **\_ \_ инстанцемодификатионевент** для отслеживания первого вхождения события изменения экземпляра WMI для [**\_ процесса Win32**](/windows/desktop/CIMWin32Prov/win32-process).</span><span class="sxs-lookup"><span data-stu-id="927e3-144">The [Monitor process modification event](https://Gallery.TechNet.Microsoft.Com/daa06cdd-c1d9-4179-ba67-83aef2b9a079) VBScript sample on TechNet Gallery uses **\_\_InstanceModificationEvent** to monitor the first occurrence of a WMI instance modification event for [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process).</span></span>

## <a name="requirements"></a><span data-ttu-id="927e3-145">Требования</span><span class="sxs-lookup"><span data-stu-id="927e3-145">Requirements</span></span>



| <span data-ttu-id="927e3-146">Требование</span><span class="sxs-lookup"><span data-stu-id="927e3-146">Requirement</span></span> | <span data-ttu-id="927e3-147">Значение</span><span class="sxs-lookup"><span data-stu-id="927e3-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="927e3-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="927e3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="927e3-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="927e3-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="927e3-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="927e3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="927e3-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="927e3-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="927e3-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="927e3-152">Namespace</span></span><br/>                | <span data-ttu-id="927e3-153">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="927e3-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="927e3-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="927e3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="927e3-155">**\_\_инстанцеоператионевент**</span><span class="sxs-lookup"><span data-stu-id="927e3-155">**\_\_InstanceOperationEvent**</span></span>](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[<span data-ttu-id="927e3-156">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="927e3-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

