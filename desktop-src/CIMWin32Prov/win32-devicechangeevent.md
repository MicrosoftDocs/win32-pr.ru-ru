---
description: '\_Абстрактный класс WMI Девицечанжеевент Win32 представляет события изменения устройства, которые вызваны добавлением, удалением или изменением устройств в компьютерной системе.'
ms.assetid: 78155357-4231-4ded-980e-89feeb864ef2
ms.tgt_platform: multiple
title: Класс Win32_DeviceChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceChangeEvent
- Win32_DeviceChangeEvent.SECURITY_DESCRIPTOR
- Win32_DeviceChangeEvent.TIME_CREATED
- Win32_DeviceChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f97ab262d95b70a69b06e15202a78d5c1364f90
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807924"
---
# <a name="win32_devicechangeevent-class"></a><span data-ttu-id="09045-103">\_Класс Win32 девицечанжеевент</span><span class="sxs-lookup"><span data-stu-id="09045-103">Win32\_DeviceChangeEvent class</span></span>

<span data-ttu-id="09045-104">Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ девицечанжеевент Win32** представляет события изменения устройства, которые вызваны добавлением, удалением или изменением устройств в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="09045-104">The **Win32\_DeviceChangeEvent** abstract [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents device change events that result from the addition, removal, or modification of devices on the computer system.</span></span> <span data-ttu-id="09045-105">К ним относятся изменения конфигурации оборудования (закрепление и Отстыковка), состояние оборудования или новые сопоставленные устройства (сопоставление сетевого диска).</span><span class="sxs-lookup"><span data-stu-id="09045-105">This includes changes in the hardware configuration (docking and undocking), the hardware state, or newly mapped devices (mapping of a network drive).</span></span> <span data-ttu-id="09045-106">Например, устройство изменилось при \_ отправке сообщения WM девицечанже.</span><span class="sxs-lookup"><span data-stu-id="09045-106">For example, a device has changed when a WM\_DEVICECHANGE message is sent.</span></span>

<span data-ttu-id="09045-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="09045-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="09045-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="09045-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="09045-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="09045-109">Syntax</span></span>

``` syntax
[UUID("0DE6AAF8-49F1-4868-B3D4-61CB69BA4322"), AMENDMENT]
class Win32_DeviceChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="09045-110">Члены</span><span class="sxs-lookup"><span data-stu-id="09045-110">Members</span></span>

<span data-ttu-id="09045-111">Класс **Win32 \_ девицечанжеевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="09045-111">The **Win32\_DeviceChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="09045-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="09045-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09045-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="09045-113">Properties</span></span>

<span data-ttu-id="09045-114">Класс **Win32 \_ девицечанжеевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="09045-114">The **Win32\_DeviceChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="09045-115">**EventType**</span><span class="sxs-lookup"><span data-stu-id="09045-115">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09045-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="09045-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="09045-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09045-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="09045-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("сообщения управления Win32APIDevice \| WM \_ девицечанже \| wParam", "Win32APIDevice Управление сообщениями управления \| WM \_ сеттингчанже")</span><span class="sxs-lookup"><span data-stu-id="09045-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="09045-119">Тип произошедшего уведомления об изменении события.</span><span class="sxs-lookup"><span data-stu-id="09045-119">Type of event change notification that has occurred.</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="09045-120">**Конфигурация изменена** (1)</span><span class="sxs-lookup"><span data-stu-id="09045-120">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="09045-121">**Прибытие устройства** (2)</span><span class="sxs-lookup"><span data-stu-id="09045-121">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="09045-122">**Удаление устройства** (3)</span><span class="sxs-lookup"><span data-stu-id="09045-122">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="09045-123">**Закрепление** (4)</span><span class="sxs-lookup"><span data-stu-id="09045-123">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="09045-124">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="09045-124">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09045-125">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="09045-125">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="09045-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09045-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09045-127">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="09045-127">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="09045-128">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="09045-128">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="09045-129">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="09045-129">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="09045-130">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="09045-130">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="09045-131">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="09045-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="09045-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="09045-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="09045-133">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="09045-133">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="09045-134">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="09045-134">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="09045-135">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="09045-135">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="09045-136">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="09045-136">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="09045-137">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="09045-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="09045-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09045-138">Remarks</span></span>

<span data-ttu-id="09045-139">**\_ Девицечанжеевент Win32** является абстрактным классом, производным от [**\_ \_ екстринсицевент**](/windows/desktop/WmiSdk/--extrinsicevent).</span><span class="sxs-lookup"><span data-stu-id="09045-139">The **Win32\_DeviceChangeEvent** is an abstract class derived from [**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="09045-140">Требования</span><span class="sxs-lookup"><span data-stu-id="09045-140">Requirements</span></span>



| <span data-ttu-id="09045-141">Требование</span><span class="sxs-lookup"><span data-stu-id="09045-141">Requirement</span></span> | <span data-ttu-id="09045-142">Значение</span><span class="sxs-lookup"><span data-stu-id="09045-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="09045-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09045-143">Minimum supported client</span></span><br/> | <span data-ttu-id="09045-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="09045-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="09045-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09045-145">Minimum supported server</span></span><br/> | <span data-ttu-id="09045-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="09045-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="09045-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="09045-147">Namespace</span></span><br/>                | <span data-ttu-id="09045-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="09045-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="09045-149">MOF</span><span class="sxs-lookup"><span data-stu-id="09045-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="09045-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="09045-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="09045-151">DLL</span><span class="sxs-lookup"><span data-stu-id="09045-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09045-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09045-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09045-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09045-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09045-154">**\_\_екстринсицевент**</span><span class="sxs-lookup"><span data-stu-id="09045-154">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> <dt>

<span data-ttu-id="09045-155">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="09045-155">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

