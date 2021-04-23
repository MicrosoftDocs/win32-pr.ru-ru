---
description: Win32 \_ волумечанжеевент представляет событие локального диска, полученное в результате добавления буквы диска или подключенного диска в системе компьютера.
ms.assetid: 38595319-d7a1-4dcd-9ad8-a27cc484b699
ms.tgt_platform: multiple
title: Класс Win32_VolumeChangeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VolumeChangeEvent
- Win32_VolumeChangeEvent.SECURITY_DESCRIPTOR
- Win32_VolumeChangeEvent.TIME_CREATED
- Win32_VolumeChangeEvent.EventType
- Win32_VolumeChangeEvent.DriveName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7610cae8d0cc746774b99a101e3c6aaf1f8a64d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141035"
---
# <a name="win32_volumechangeevent-class"></a><span data-ttu-id="c0694-103">\_Класс Win32 волумечанжеевент</span><span class="sxs-lookup"><span data-stu-id="c0694-103">Win32\_VolumeChangeEvent class</span></span>

<span data-ttu-id="c0694-104">Класс **WMI \_ волумечанжеевент** [инструментария](../wmisdk/retrieving-a-class.md) Win32 представляет событие локального диска, полученное в результате добавления буквы диска или подключенного диска в системе компьютера.</span><span class="sxs-lookup"><span data-stu-id="c0694-104">The **Win32\_VolumeChangeEvent** [WMI class](../wmisdk/retrieving-a-class.md) represents a local drive event that results from the addition of a drive letter or mounted drive on the computer system.</span></span> <span data-ttu-id="c0694-105">Сетевые диски в настоящее время не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c0694-105">Network drives are not currently supported.</span></span>

<span data-ttu-id="c0694-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c0694-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="c0694-107">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="c0694-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0694-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0694-108">Syntax</span></span>

``` syntax
[UUID("455CE053-2552-4051-A3E4-C4200DC31B7"), AMENDMENT]
class Win32_VolumeChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
  string DriveName;
};
```

## <a name="members"></a><span data-ttu-id="c0694-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c0694-109">Members</span></span>

<span data-ttu-id="c0694-110">Класс **Win32 \_ волумечанжеевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c0694-110">The **Win32\_VolumeChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="c0694-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0694-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0694-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c0694-112">Properties</span></span>

<span data-ttu-id="c0694-113">Класс **Win32 \_ волумечанжеевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c0694-113">The **Win32\_VolumeChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0694-114">**DriveName**</span><span class="sxs-lookup"><span data-stu-id="c0694-114">**DriveName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0694-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c0694-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0694-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0694-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0694-117">Имя диска (буква), которое было добавлено или удалено из системы.</span><span class="sxs-lookup"><span data-stu-id="c0694-117">Drive name (letter) that has been added or removed from the system.</span></span>

</dd> <dt>

<span data-ttu-id="c0694-118">**EventType**</span><span class="sxs-lookup"><span data-stu-id="c0694-118">**EventType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0694-119">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c0694-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c0694-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0694-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0694-121">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("сообщения управления Win32APIDevice \| WM \_ девицечанже \| wParam", "Win32APIDevice Управление сообщениями управления \| WM \_ сеттингчанже")</span><span class="sxs-lookup"><span data-stu-id="c0694-121">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")</span></span>
</dt> </dl>

<span data-ttu-id="c0694-122">Тип произошедшего уведомления об изменении события.</span><span class="sxs-lookup"><span data-stu-id="c0694-122">Type of event change notification that has occurred.</span></span>

<span data-ttu-id="c0694-123">Это свойство наследуется из [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-123">This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

<span data-ttu-id="c0694-124">**Конфигурация изменена** (1)</span><span class="sxs-lookup"><span data-stu-id="c0694-124">**Configuration Changed** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

<span data-ttu-id="c0694-125">**Прибытие устройства** (2)</span><span class="sxs-lookup"><span data-stu-id="c0694-125">**Device Arrival** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

<span data-ttu-id="c0694-126">**Удаление устройства** (3)</span><span class="sxs-lookup"><span data-stu-id="c0694-126">**Device Removal** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

<span data-ttu-id="c0694-127">**Закрепление** (4)</span><span class="sxs-lookup"><span data-stu-id="c0694-127">**Docking** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0694-128">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="c0694-128">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0694-129">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="c0694-129">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="c0694-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0694-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0694-131">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="c0694-131">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="c0694-132">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-132">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span> <span data-ttu-id="c0694-133">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](../wmisdk/wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-133">For more information about constants used to set this security descriptor, see [WMI Security Constants](../wmisdk/wmi-security-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0694-134">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="c0694-134">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0694-135">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="c0694-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="c0694-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c0694-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0694-137">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="c0694-137">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="c0694-138">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="c0694-138">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="c0694-139">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="c0694-139">The information is in the Coordinated Universal Times (UTC) format.</span></span>

<span data-ttu-id="c0694-140">Это свойство наследуется от [**\_ \_ события**](../wmisdk/--event.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-140">This property is inherited from [**\_\_Event**](../wmisdk/--event.md).</span></span>

<span data-ttu-id="c0694-141">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0694-142">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0694-142">Remarks</span></span>

<span data-ttu-id="c0694-143">Класс **Win32 \_ волумечанжеевент** является производным от [**Win32 \_ девицечанжеевент**](win32-devicechangeevent.md).</span><span class="sxs-lookup"><span data-stu-id="c0694-143">The **Win32\_VolumeChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0694-144">Требования</span><span class="sxs-lookup"><span data-stu-id="c0694-144">Requirements</span></span>



| <span data-ttu-id="c0694-145">Требование</span><span class="sxs-lookup"><span data-stu-id="c0694-145">Requirement</span></span> | <span data-ttu-id="c0694-146">Значение</span><span class="sxs-lookup"><span data-stu-id="c0694-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0694-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0694-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c0694-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0694-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0694-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0694-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c0694-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0694-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0694-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c0694-151">Namespace</span></span><br/>                | <span data-ttu-id="c0694-152">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c0694-152">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c0694-153">MOF</span><span class="sxs-lookup"><span data-stu-id="c0694-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0694-154"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0694-154"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0694-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c0694-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0694-156"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0694-156"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0694-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0694-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0694-158">**\_Девицечанжеевент Win32**</span><span class="sxs-lookup"><span data-stu-id="c0694-158">**Win32\_DeviceChangeEvent**</span></span>](win32-devicechangeevent.md)
</dt> <dt>

[<span data-ttu-id="c0694-159">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="c0694-159">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
