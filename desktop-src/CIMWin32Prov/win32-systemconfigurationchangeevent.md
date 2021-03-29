---
description: '&Win32 \_ системконфигуратиончанжеевент \# 8194; Класс WMI указывает, что список устройств в системе обновлен (устройство было добавлено или удалено, или изменена конфигурация).'
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Класс Win32_SystemConfigurationChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0bc479d3415906a6536c6df1d163056e94e2af76
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142442"
---
# <a name="win32_systemconfigurationchangeevent-class"></a><span data-ttu-id="6c328-103">\_Класс Win32 системконфигуратиончанжеевент</span><span class="sxs-lookup"><span data-stu-id="6c328-103">Win32\_SystemConfigurationChangeEvent class</span></span>

<span data-ttu-id="6c328-104"> [Класс WMI](../wmisdk/retrieving-a-class.md) *\*\_ системконфигуратиончанжеевент для Win32** указывает, что список устройств в системе обновлен (устройство было добавлено или удалено, или изменена конфигурация).</span><span class="sxs-lookup"><span data-stu-id="6c328-104">The **Win32\_SystemConfigurationChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).</span></span> <span data-ttu-id="6c328-105">Возникает событие, и экземпляр этого класса создается при отправке сообщения "Девмгррефрешон<*ComputerName*>".</span><span class="sxs-lookup"><span data-stu-id="6c328-105">An event is fired and an instance of this is class created when the "DevMgrRefreshOn<*ComputerName*>" message is sent.</span></span> <span data-ttu-id="6c328-106">Точное изменение списка устройств не содержится в сообщении, поэтому для получения текущих системных настроек требуется обновление устройства.</span><span class="sxs-lookup"><span data-stu-id="6c328-106">The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings.</span></span> <span data-ttu-id="6c328-107">Примеры изменений конфигурации: параметры IRQ, COM-порты и версии BIOS.</span><span class="sxs-lookup"><span data-stu-id="6c328-107">Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.</span></span>

<span data-ttu-id="6c328-108">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="6c328-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6c328-109">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="6c328-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c328-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6c328-110">Syntax</span></span>

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a><span data-ttu-id="6c328-111">Члены</span><span class="sxs-lookup"><span data-stu-id="6c328-111">Members</span></span>

<span data-ttu-id="6c328-112">Класс **Win32 \_ системконфигуратиончанжеевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6c328-112">The **Win32\_SystemConfigurationChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="6c328-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c328-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6c328-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c328-114">Properties</span></span>

<span data-ttu-id="6c328-115">Класс **Win32 \_ системконфигуратиончанжеевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6c328-115">The **Win32\_SystemConfigurationChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6c328-116">**EventType**</span><span class="sxs-lookup"><span data-stu-id="6c328-116">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c328-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6c328-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6c328-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c328-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6c328-119">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("сообщения управления Win32APIDevice \| WM \_ девицечанже \| wParam", "Win32APIDevice Управление сообщениями управления \| WM \_ сеттингчанже")</span><span class="sxs-lookup"><span data-stu-id="6c328-119">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="6c328-120">Тип произошедшего уведомления об изменении события.</span><span class="sxs-lookup"><span data-stu-id="6c328-120">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="6c328-121">Это свойство наследуется из [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-121">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="6c328-122">**Конфигурация изменена** (1)</span><span class="sxs-lookup"><span data-stu-id="6c328-122">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="6c328-123">**Прибытие устройства** (2)</span><span class="sxs-lookup"><span data-stu-id="6c328-123">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="6c328-124">**Удаление устройства** (3)</span><span class="sxs-lookup"><span data-stu-id="6c328-124">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="6c328-125">**Закрепление** (4)</span><span class="sxs-lookup"><span data-stu-id="6c328-125">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6c328-126">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="6c328-126">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c328-127">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="6c328-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="6c328-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c328-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c328-129">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="6c328-129">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="6c328-130">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-130">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="6c328-131">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-131">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="6c328-132">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="6c328-132">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6c328-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6c328-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6c328-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6c328-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6c328-135">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="6c328-135">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="6c328-136">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="6c328-136">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="6c328-137">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="6c328-137">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="6c328-138">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-138">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="6c328-139">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c328-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c328-140">Remarks</span></span>

<span data-ttu-id="6c328-141">Класс **Win32 \_ системконфигуратиончанжеевент** является производным от [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="6c328-141">The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c328-142">Требования</span><span class="sxs-lookup"><span data-stu-id="6c328-142">Requirements</span></span>



| <span data-ttu-id="6c328-143">Требование</span><span class="sxs-lookup"><span data-stu-id="6c328-143">Requirement</span></span> | <span data-ttu-id="6c328-144">Значение</span><span class="sxs-lookup"><span data-stu-id="6c328-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c328-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c328-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6c328-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c328-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c328-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c328-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6c328-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c328-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c328-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6c328-149">Namespace</span></span><br/>                | <span data-ttu-id="6c328-150">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6c328-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6c328-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6c328-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c328-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c328-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c328-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6c328-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c328-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c328-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c328-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c328-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c328-156">**\_Девицечанжеевент Win32**</span><span class="sxs-lookup"><span data-stu-id="6c328-156">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="6c328-157">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="6c328-157">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
