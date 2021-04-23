---
description: Представляет устройство, подключенное к компьютеру, работающему под управлением операционной системы Microsoft Windows, которое может создавать печатное изображение или текст на бумаге или на другом носителе.
ms.assetid: 58090e6a-8f13-4859-adb8-a7c6299d3efd
ms.tgt_platform: multiple
title: Класс Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer
- Win32_Printer.Reset
- Win32_Printer.SetPowerState
- Win32_Printer.Attributes
- Win32_Printer.Availability
- Win32_Printer.AvailableJobSheets
- Win32_Printer.AveragePagesPerMinute
- Win32_Printer.Capabilities
- Win32_Printer.CapabilityDescriptions
- Win32_Printer.Caption
- Win32_Printer.CharSetsSupported
- Win32_Printer.Comment
- Win32_Printer.ConfigManagerErrorCode
- Win32_Printer.ConfigManagerUserConfig
- Win32_Printer.CreationClassName
- Win32_Printer.CurrentCapabilities
- Win32_Printer.CurrentCharSet
- Win32_Printer.CurrentLanguage
- Win32_Printer.CurrentMimeType
- Win32_Printer.CurrentNaturalLanguage
- Win32_Printer.CurrentPaperType
- Win32_Printer.Default
- Win32_Printer.DefaultCapabilities
- Win32_Printer.DefaultCopies
- Win32_Printer.DefaultLanguage
- Win32_Printer.DefaultMimeType
- Win32_Printer.DefaultNumberUp
- Win32_Printer.DefaultPaperType
- Win32_Printer.DefaultPriority
- Win32_Printer.Description
- Win32_Printer.DetectedErrorState
- Win32_Printer.DeviceID
- Win32_Printer.Direct
- Win32_Printer.DoCompleteFirst
- Win32_Printer.DriverName
- Win32_Printer.EnableBIDI
- Win32_Printer.EnableDevQueryPrint
- Win32_Printer.ErrorCleared
- Win32_Printer.ErrorDescription
- Win32_Printer.ErrorInformation
- Win32_Printer.ExtendedDetectedErrorState
- Win32_Printer.ExtendedPrinterStatus
- Win32_Printer.Hidden
- Win32_Printer.HorizontalResolution
- Win32_Printer.InstallDate
- Win32_Printer.JobCountSinceLastReset
- Win32_Printer.KeepPrintedJobs
- Win32_Printer.LanguagesSupported
- Win32_Printer.LastErrorCode
- Win32_Printer.Local
- Win32_Printer.Location
- Win32_Printer.MarkingTechnology
- Win32_Printer.MaxCopies
- Win32_Printer.MaxNumberUp
- Win32_Printer.MaxSizeSupported
- Win32_Printer.MimeTypesSupported
- Win32_Printer.Name
- Win32_Printer.NaturalLanguagesSupported
- Win32_Printer.Network
- Win32_Printer.PaperSizesSupported
- Win32_Printer.PaperTypesAvailable
- Win32_Printer.Parameters
- Win32_Printer.PNPDeviceID
- Win32_Printer.PortName
- Win32_Printer.PowerManagementCapabilities
- Win32_Printer.PowerManagementSupported
- Win32_Printer.PrinterPaperNames
- Win32_Printer.PrinterState
- Win32_Printer.PrinterStatus
- Win32_Printer.PrintJobDataType
- Win32_Printer.PrintProcessor
- Win32_Printer.Priority
- Win32_Printer.Published
- Win32_Printer.Queued
- Win32_Printer.RawOnly
- Win32_Printer.SeparatorFile
- Win32_Printer.ServerName
- Win32_Printer.Shared
- Win32_Printer.ShareName
- Win32_Printer.SpoolEnabled
- Win32_Printer.StartTime
- Win32_Printer.Status
- Win32_Printer.StatusInfo
- Win32_Printer.SystemCreationClassName
- Win32_Printer.SystemName
- Win32_Printer.TimeOfLastReset
- Win32_Printer.UntilTime
- Win32_Printer.VerticalResolution
- Win32_Printer.WorkOffline
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 48fc170cb3e85d44dc3e01140fe2c881a7ec975b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262641"
---
# <a name="win32_printer-class"></a><span data-ttu-id="10940-103">\_Класс принтера Win32</span><span class="sxs-lookup"><span data-stu-id="10940-103">Win32\_Printer class</span></span>

<span data-ttu-id="10940-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ принтера Win32** представляет устройство, подключенное к компьютеру, работающему под управлением операционной системы Microsoft Windows, который может создавать печатное изображение или текст на бумаге или на другом носителе.</span><span class="sxs-lookup"><span data-stu-id="10940-104">The **Win32\_Printer** [WMI class](../wmisdk/retrieving-a-class.md) represents a device connected to a computer running on a Microsoft Windows operating system that can produce a printed image or text on paper or other medium.</span></span>

<span data-ttu-id="10940-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="10940-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="10940-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="10940-106">Syntax</span></span>

``` syntax
class Win32_Printer : CIM_Printer
{
  uint32   Attributes;
  uint16   Availability;
  string   AvailableJobSheets[];
  uint32   AveragePagesPerMinute;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  string   Comment;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  boolean  Default;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  uint32   DefaultPriority;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  Direct;
  boolean  DoCompleteFirst;
  string   DriverName;
  boolean  EnableBIDI;
  boolean  EnableDevQueryPrint;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint16   ExtendedDetectedErrorState;
  uint16   ExtendedPrinterStatus;
  boolean  Hidden;
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  boolean  KeepPrintedJobs;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  boolean  Local;
  string   Location;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  boolean  Network;
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   Parameters;
  string   PNPDeviceID;
  string   PortName;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   PrinterPaperNames[];
  uint32   PrinterState;
  uint16   PrinterStatus;
  string   PrintJobDataType;
  string   PrintProcessor;
  uint32   Priority;
  boolean  Published;
  boolean  Queued;
  boolean  RawOnly;
  string   SeparatorFile;
  string   ServerName;
  boolean  Shared;
  string   ShareName;
  boolean  SpoolEnabled;
  datetime StartTime;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  datetime UntilTime;
  uint32   VerticalResolution;
  boolean  WorkOffline;
};
```

## <a name="members"></a><span data-ttu-id="10940-107">Члены</span><span class="sxs-lookup"><span data-stu-id="10940-107">Members</span></span>

<span data-ttu-id="10940-108">Класс **\_ принтера Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="10940-108">The **Win32\_Printer** class has these types of members:</span></span>

-   [<span data-ttu-id="10940-109">Методы</span><span class="sxs-lookup"><span data-stu-id="10940-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="10940-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="10940-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="10940-111">Методы</span><span class="sxs-lookup"><span data-stu-id="10940-111">Methods</span></span>

<span data-ttu-id="10940-112">Класс **\_ принтера Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="10940-112">The **Win32\_Printer** class has these methods.</span></span>



| <span data-ttu-id="10940-113">Метод</span><span class="sxs-lookup"><span data-stu-id="10940-113">Method</span></span>                                                                               | <span data-ttu-id="10940-114">Описание</span><span class="sxs-lookup"><span data-stu-id="10940-114">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10940-115">**аддпринтерконнектион**</span><span class="sxs-lookup"><span data-stu-id="10940-115">**AddPrinterConnection**</span></span>](addprinterconnection-method-in-class-win32-printer.md)   | <span data-ttu-id="10940-116">Добавляет подключение к принтеру.</span><span class="sxs-lookup"><span data-stu-id="10940-116">Adds a connection to the printer.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="10940-117">**канцелаллжобс**</span><span class="sxs-lookup"><span data-stu-id="10940-117">**CancelAllJobs**</span></span>](cancelalljobs-method-in-class-win32-printer.md)                 | <span data-ttu-id="10940-118">Отменяет все задания.</span><span class="sxs-lookup"><span data-stu-id="10940-118">Cancels all jobs.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="10940-119">**жетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="10940-119">**GetSecurityDescriptor**</span></span>](getsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="10940-120">Возвращает дескриптор безопасности, управляющий доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="10940-120">Returns the security descriptor that controls access to the printer.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="10940-121">**Пауза**</span><span class="sxs-lookup"><span data-stu-id="10940-121">**Pause**</span></span>](pause-method-in-class-win32-printer.md)                                 | <span data-ttu-id="10940-122">Приостанавливает очередь печати.</span><span class="sxs-lookup"><span data-stu-id="10940-122">Pauses the print queue.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="10940-123">**принттестпаже**</span><span class="sxs-lookup"><span data-stu-id="10940-123">**PrintTestPage**</span></span>](printtestpage-method-in-class-win32-printer.md)                 | <span data-ttu-id="10940-124">Выводит тестовую страницу.</span><span class="sxs-lookup"><span data-stu-id="10940-124">Prints a test page.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="10940-125">**ренамепринтер**</span><span class="sxs-lookup"><span data-stu-id="10940-125">**RenamePrinter**</span></span>](renameprinter-method-in-class-win32-printer.md)                 | <span data-ttu-id="10940-126">Переименовывает принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-126">Renames a printer.</span></span><br/>                                                                                                                                                                                     |
| <span data-ttu-id="10940-127">**Сброс**</span><span class="sxs-lookup"><span data-stu-id="10940-127">**Reset**</span></span>                                                                            | <span data-ttu-id="10940-128">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="10940-128">Not implemented.</span></span> <span data-ttu-id="10940-129">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**Reset**](reset-method-in-class-cim-controller.md) в [**CIM \_ Printer**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-129">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/>                 |
| [<span data-ttu-id="10940-130">**Возобновить**</span><span class="sxs-lookup"><span data-stu-id="10940-130">**Resume**</span></span>](resume-method-in-class-win32-printer.md)                               | <span data-ttu-id="10940-131">Возобновляет приостановленную очередь печати.</span><span class="sxs-lookup"><span data-stu-id="10940-131">Resumes paused print queue.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="10940-132">**SetDefaultPrinter**</span><span class="sxs-lookup"><span data-stu-id="10940-132">**SetDefaultPrinter**</span></span>](setdefaultprinter-method-in-class-win32-printer.md)         | <span data-ttu-id="10940-133">Задает принтер по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10940-133">Sets the default printer.</span></span><br/>                                                                                                                                                                              |
| <span data-ttu-id="10940-134">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="10940-134">**SetPowerState**</span></span>                                                                    | <span data-ttu-id="10940-135">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="10940-135">Not implemented.</span></span> <span data-ttu-id="10940-136">Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) на [**\_ принтере CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-136">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_Printer**](cim-printer.md).</span></span><br/> |
| [<span data-ttu-id="10940-137">**сетсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="10940-137">**SetSecurityDescriptor**</span></span>](setsecuritydescriptor-method-in-class-win32-printer.md) | <span data-ttu-id="10940-138">Записывает обновленную версию дескриптора безопасности, которая управляет доступом к принтеру.</span><span class="sxs-lookup"><span data-stu-id="10940-138">Writes an updated version of the security descriptor that controls access to the printer.</span></span><br/>                                                                                                              |



 

### <a name="properties"></a><span data-ttu-id="10940-139">Свойства</span><span class="sxs-lookup"><span data-stu-id="10940-139">Properties</span></span>

<span data-ttu-id="10940-140">Класс **\_ принтера Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="10940-140">The **Win32\_Printer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10940-141">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="10940-141">**Attributes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-144">Битовая карта атрибутов для устройства печати на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="10940-144">Bitmap of attributes for a Windows-based printing device.</span></span>

<dt>

<span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>

<span data-ttu-id="10940-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**Принтер \_ АТРИБУТ \_ в очереди** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="10940-145"><span id="PRINTER_ATTRIBUTE_QUEUED"></span><span id="printer_attribute_queued"></span>**PRINTER\_ATTRIBUTE\_QUEUED** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="10940-146">Поставлено в очередь</span><span class="sxs-lookup"><span data-stu-id="10940-146">Queued</span></span>

<span data-ttu-id="10940-147">Задания печати буферизуются и помещаются в очередь.</span><span class="sxs-lookup"><span data-stu-id="10940-147">Print jobs are buffered and queued.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>

<span data-ttu-id="10940-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**Принтер \_ АТРИБУТ \_ Direct** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="10940-148"><span id="PRINTER_ATTRIBUTE_DIRECT"></span><span id="printer_attribute_direct"></span>**PRINTER\_ATTRIBUTE\_DIRECT** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="10940-149">Прямой доступ</span><span class="sxs-lookup"><span data-stu-id="10940-149">Direct</span></span>

<span data-ttu-id="10940-150">Документ, отправляемый непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-150">Document to be sent directly to the printer.</span></span> <span data-ttu-id="10940-151">Это значение используется, если задания печати неправильно поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="10940-151">This value is used if print jobs are not queued correctly.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>

<span data-ttu-id="10940-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**Принтер \_ АТРИБУТ \_ по умолчанию** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="10940-152"><span id="PRINTER_ATTRIBUTE_DEFAULT"></span><span id="printer_attribute_default"></span>**PRINTER\_ATTRIBUTE\_DEFAULT** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="10940-153">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="10940-153">Default</span></span>

<span data-ttu-id="10940-154">Принтер по умолчанию на компьютере.</span><span class="sxs-lookup"><span data-stu-id="10940-154">Default printer on a computer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>

<span data-ttu-id="10940-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**Принтер \_ АТРИБУТ \_ Shared** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="10940-155"><span id="PRINTER_ATTRIBUTE_SHARED"></span><span id="printer_attribute_shared"></span>**PRINTER\_ATTRIBUTE\_SHARED** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="10940-156">Совмещаемая блокировка</span><span class="sxs-lookup"><span data-stu-id="10940-156">Shared</span></span>

<span data-ttu-id="10940-157">Доступен в качестве общего сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="10940-157">Available as a shared network resource.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>

<span data-ttu-id="10940-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**Принтер \_ \_Сеть атрибутов** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="10940-158"><span id="PRINTER_ATTRIBUTE_NETWORK"></span><span id="printer_attribute_network"></span>**PRINTER\_ATTRIBUTE\_NETWORK** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="10940-159">Сеть</span><span class="sxs-lookup"><span data-stu-id="10940-159">Network</span></span>

<span data-ttu-id="10940-160">Подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="10940-160">Attached to a network.</span></span> <span data-ttu-id="10940-161">Если заданы как локальные, так и сетевые биты, это указывает на сетевой принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-161">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>

<span data-ttu-id="10940-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**Принтер \_ АТРИБУТ \_ Hidden** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="10940-162"><span id="PRINTER_ATTRIBUTE_HIDDEN"></span><span id="printer_attribute_hidden"></span>**PRINTER\_ATTRIBUTE\_HIDDEN** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="10940-163">Скрытый</span><span class="sxs-lookup"><span data-stu-id="10940-163">Hidden</span></span>

<span data-ttu-id="10940-164">Скрыто от некоторых пользователей в сети.</span><span class="sxs-lookup"><span data-stu-id="10940-164">Hidden from some users on the network.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>

<span data-ttu-id="10940-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**Принтер \_ \_Локальный атрибут** (64 (0x40))</span><span class="sxs-lookup"><span data-stu-id="10940-165"><span id="PRINTER_ATTRIBUTE_LOCAL"></span><span id="printer_attribute_local"></span>**PRINTER\_ATTRIBUTE\_LOCAL** (64 (0x40))</span></span>


</dt> <dd>

<span data-ttu-id="10940-166">Локальная</span><span class="sxs-lookup"><span data-stu-id="10940-166">Local</span></span>

<span data-ttu-id="10940-167">Непосредственное подключение к компьютеру.</span><span class="sxs-lookup"><span data-stu-id="10940-167">Directly connected to a computer.</span></span> <span data-ttu-id="10940-168">Если заданы как локальные, так и сетевые биты, это указывает на сетевой принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-168">If both Local and Network bits are set, this indicates a network printer.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>

<span data-ttu-id="10940-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**Принтер \_ АТРИБУТ \_ енабледевк** (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="10940-169"><span id="PRINTER_ATTRIBUTE_ENABLEDEVQ"></span><span id="printer_attribute_enabledevq"></span>**PRINTER\_ATTRIBUTE\_ENABLEDEVQ** (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="10940-170">енабледевк</span><span class="sxs-lookup"><span data-stu-id="10940-170">EnableDevQ</span></span>

<span data-ttu-id="10940-171">Включите очередь на принтере, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="10940-171">Enable the queue on the printer if available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>

<span data-ttu-id="10940-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**Принтер \_ АТРИБУТ \_ киппринтеджобс** (256 (0x100))</span><span class="sxs-lookup"><span data-stu-id="10940-172"><span id="PRINTER_ATTRIBUTE_KEEPPRINTEDJOBS"></span><span id="printer_attribute_keepprintedjobs"></span>**PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS** (256 (0x100))</span></span>


</dt> <dd>

<span data-ttu-id="10940-173">киппринтеджобс</span><span class="sxs-lookup"><span data-stu-id="10940-173">KeepPrintedJobs</span></span>

<span data-ttu-id="10940-174">Диспетчер очереди печати не должен удалять документы после их вывода на печать.</span><span class="sxs-lookup"><span data-stu-id="10940-174">Spooler should not delete documents after they are printed.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>

<span data-ttu-id="10940-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**Принтер \_ \_ \_ \_ Сначала необходимо выполнить атрибут** (512 (0x200))</span><span class="sxs-lookup"><span data-stu-id="10940-175"><span id="PRINTER_ATTRIBUTE_DO_COMPLETE_FIRST"></span><span id="printer_attribute_do_complete_first"></span>**PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST** (512 (0x200))</span></span>


</dt> <dd>

<span data-ttu-id="10940-176">докомплетефирст</span><span class="sxs-lookup"><span data-stu-id="10940-176">DoCompleteFirst</span></span>

<span data-ttu-id="10940-177">Запуск заданий, для которых сначала завершается буферизация.</span><span class="sxs-lookup"><span data-stu-id="10940-177">Start jobs that are finished spooling first.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>

<span data-ttu-id="10940-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**Принтер \_ АТРИБУТ \_ работает \_ автономно** (1024 (0x400))</span><span class="sxs-lookup"><span data-stu-id="10940-178"><span id="PRINTER_ATTRIBUTE_WORK_OFFLINE"></span><span id="printer_attribute_work_offline"></span>**PRINTER\_ATTRIBUTE\_WORK\_OFFLINE** (1024 (0x400))</span></span>


</dt> <dd>

<span data-ttu-id="10940-179">воркоффлине</span><span class="sxs-lookup"><span data-stu-id="10940-179">WorkOffline</span></span>

<span data-ttu-id="10940-180">Ставить в очередь задания печати, если принтер недоступен.</span><span class="sxs-lookup"><span data-stu-id="10940-180">Queue print jobs when a printer is not available.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>

<span data-ttu-id="10940-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**Принтер \_ АТРИБУТ \_ Enable \_ BIDI** (2048 (0x800))</span><span class="sxs-lookup"><span data-stu-id="10940-181"><span id="PRINTER_ATTRIBUTE_ENABLE_BIDI"></span><span id="printer_attribute_enable_bidi"></span>**PRINTER\_ATTRIBUTE\_ENABLE\_BIDI** (2048 (0x800))</span></span>


</dt> <dd>

<span data-ttu-id="10940-182">енаблебиди</span><span class="sxs-lookup"><span data-stu-id="10940-182">EnableBIDI</span></span>

<span data-ttu-id="10940-183">Включить двунаправленную печать.</span><span class="sxs-lookup"><span data-stu-id="10940-183">Enable bidirectional printing.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>

<span data-ttu-id="10940-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**Принтер \_ \_ \_ Только атрибут RAW** (4096 (0x1000))</span><span class="sxs-lookup"><span data-stu-id="10940-184"><span id="PRINTER_ATTRIBUTE_RAW_ONLY"></span><span id="printer_attribute_raw_only"></span>**PRINTER\_ATTRIBUTE\_RAW\_ONLY** (4096 (0x1000))</span></span>


</dt> <dd>

<span data-ttu-id="10940-185">Разрешить постановку в очередь только заданий с необработанными типами данных.</span><span class="sxs-lookup"><span data-stu-id="10940-185">Allow only raw data type jobs to be spooled.</span></span>

</dd> <dt>

<span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>

<span data-ttu-id="10940-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**Принтер \_ АТРИБУТ \_ опубликован** (8192 (0x2000))</span><span class="sxs-lookup"><span data-stu-id="10940-186"><span id="PRINTER_ATTRIBUTE_PUBLISHED"></span><span id="printer_attribute_published"></span>**PRINTER\_ATTRIBUTE\_PUBLISHED** (8192 (0x2000))</span></span>


</dt> <dd>

<span data-ttu-id="10940-187">Опубликован</span><span class="sxs-lookup"><span data-stu-id="10940-187">Published</span></span>

<span data-ttu-id="10940-188">Опубликовано в службе сетевых каталогов.</span><span class="sxs-lookup"><span data-stu-id="10940-188">Published in the network directory service.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-189">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="10940-189">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-190">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-190">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-192">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Оперативное состояние DMTF \| 003,5 "," MIB. \|Основной узел IETF-Resources-MIB. хрдевицестатус ")</span><span class="sxs-lookup"><span data-stu-id="10940-192">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="10940-193">Доступность и состояние устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-193">Availability and status of the device.</span></span>

<span data-ttu-id="10940-194">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-194">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-195"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-196"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="10940-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Работа/полная мощность** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-197"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10940-198">Работа или полная мощность</span><span class="sxs-lookup"><span data-stu-id="10940-198">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="10940-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-199"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="10940-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-200"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10940-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Неприменимо** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-201"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="10940-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-202"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="10940-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Не в **линии** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-203"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="10940-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>Не **обслуживает** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-204"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10940-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Снижение работоспособности** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-205"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="10940-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Не установлено** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-206"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="10940-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Ошибка установки** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-207"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="10940-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-208"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10940-209">Известно, что устройство находится в режиме энергосбережения, но его точное состояние неизвестно.</span><span class="sxs-lookup"><span data-stu-id="10940-209">The device is known to be in a power save mode, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="10940-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-210"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10940-211">Устройство находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности.</span><span class="sxs-lookup"><span data-stu-id="10940-211">The device is in a power save state but is still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="10940-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-212"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10940-213">Устройство не работает, но его можно быстро включить в полную работу.</span><span class="sxs-lookup"><span data-stu-id="10940-213">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="10940-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-214"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="10940-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-215"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="10940-216">Устройство находится в состоянии предупреждения, но также в режиме энергосбережения.</span><span class="sxs-lookup"><span data-stu-id="10940-216">The device is in a warning state, though also in a power save mode.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="10940-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Приостановлено** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-217"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="10940-218">Устройство приостановлено.</span><span class="sxs-lookup"><span data-stu-id="10940-218">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="10940-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-219"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="10940-220">Устройство не готово.</span><span class="sxs-lookup"><span data-stu-id="10940-220">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="10940-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-221"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="10940-222">Устройство не настроено.</span><span class="sxs-lookup"><span data-stu-id="10940-222">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="10940-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Заморожено** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-223"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="10940-224">Устройство находится в тихом режиме.</span><span class="sxs-lookup"><span data-stu-id="10940-224">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-225">**аваилаблежобшитс**</span><span class="sxs-lookup"><span data-stu-id="10940-225">**AvailableJobSheets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-226">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-226">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-228">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. рекуиреджобшитс")</span><span class="sxs-lookup"><span data-stu-id="10940-228">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredJobSheets")</span></span>
</dt> </dl>

<span data-ttu-id="10940-229">Массив всех листов заданий, доступных на принтере.</span><span class="sxs-lookup"><span data-stu-id="10940-229">Array of all the job sheets available on a printer.</span></span> <span data-ttu-id="10940-230">Также можно использовать для описания баннера, который принтер может предоставить в начале каждого задания, или другие параметры, заданные пользователем.</span><span class="sxs-lookup"><span data-stu-id="10940-230">Can also be used to describe the banner that a printer might provide at the beginning of each job, or other user-specified options.</span></span>

<span data-ttu-id="10940-231">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-231">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-232">**аверажепажесперминуте**</span><span class="sxs-lookup"><span data-stu-id="10940-232">**AveragePagesPerMinute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-233">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-235">Скорость печати (в среднем количестве страниц в минуту), которую принтер может выводить.</span><span class="sxs-lookup"><span data-stu-id="10940-235">Printing rate, in average number of pages per minute, that a printer can produce output.</span></span>

</dd> <dt>

<span data-ttu-id="10940-236">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="10940-236">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-237">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-237">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-238">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-239">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ принтер CIM**](cim-printer.md)". Капабилитидескриптионс "," CIM \_ PrintJob. Finished "," CIM \_ Принтсервице. Capabilities ")</span><span class="sxs-lookup"><span data-stu-id="10940-239">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).CapabilityDescriptions", "CIM\_PrintJob.Finishing", "CIM\_PrintService.Capabilities")</span></span>
</dt> </dl>

<span data-ttu-id="10940-240">Массив возможностей принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-240">Array of printer capabilities.</span></span>

<span data-ttu-id="10940-241">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-241">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-242"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-243"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="10940-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-244"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="10940-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-245"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="10940-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-246"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="10940-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-247"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="10940-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-248"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="10940-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-249"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="10940-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-250"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="10940-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-251"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="10940-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-252"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="10940-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-253"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="10940-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-254"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="10940-255">One-Sided</span><span class="sxs-lookup"><span data-stu-id="10940-255">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="10940-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-256"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10940-257">Two-Sided длинное ребро</span><span class="sxs-lookup"><span data-stu-id="10940-257">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="10940-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-258"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10940-259">Two-Sided короткий пограничная</span><span class="sxs-lookup"><span data-stu-id="10940-259">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="10940-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-260"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="10940-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-261"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="10940-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-262"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="10940-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-263"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="10940-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-264"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="10940-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-265"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="10940-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-266"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-267">**капабилитидескриптионс**</span><span class="sxs-lookup"><span data-stu-id="10940-267">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-268">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-268">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-269">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-270">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**\_ принтер CIM**](cim-printer.md)".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="10940-270">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-271">Массив строк произвольной формы, которые содержат подробные объяснения для функций принтера, указанных в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="10940-271">Array of free-form strings that provide detailed explanations for the printer features indicated in the **Capabilities** array.</span></span> <span data-ttu-id="10940-272">Каждая запись этого массива связана с записью в массиве **capabilities** , расположенном в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="10940-272">Each entry of this array is related to an entry in the **Capabilities** array that is located in the same index.</span></span>

<span data-ttu-id="10940-273">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-273">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-274">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="10940-274">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-275">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-275">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-276">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-277">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="10940-277">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="10940-278">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="10940-278">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="10940-279">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10940-279">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-280">**чарсетссуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-280">**CharSetsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-281">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-281">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-282">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-282">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-283">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. CharSet"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Принтер IETF — MIB. пртлокализатиончарактерсет ")</span><span class="sxs-lookup"><span data-stu-id="10940-283">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.CharSet"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationCharacterSet")</span></span>
</dt> </dl>

<span data-ttu-id="10940-284">Массив доступных наборов символов для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="10940-284">Array of available character sets for output.</span></span> <span data-ttu-id="10940-285">Строки, предоставленные в этом свойстве, должны соответствовать семантике и синтаксису, заданному в разделе 4.1.2 ("параметры charset") в RFC 2046 (MIME Part 2) и содержащихся в реестре набора символов IANA.</span><span class="sxs-lookup"><span data-stu-id="10940-285">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="10940-286">Примеры: "UTF-8", "US-ASCII" и "ISO-8859-1".</span><span class="sxs-lookup"><span data-stu-id="10940-286">Examples include, "UTF-8", "us-ASCII", and "iso-8859-1".</span></span>

<span data-ttu-id="10940-287">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-287">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-288">**Комментарий**</span><span class="sxs-lookup"><span data-stu-id="10940-288">**Comment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-290">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-290">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-291">Комментарий для очереди печати.</span><span class="sxs-lookup"><span data-stu-id="10940-291">Comment for a print queue.</span></span>

<span data-ttu-id="10940-292">Пример: цветной принтер</span><span class="sxs-lookup"><span data-stu-id="10940-292">Example: Color printer</span></span>

</dd> <dt>

<span data-ttu-id="10940-293">**конфигманажерерроркоде**</span><span class="sxs-lookup"><span data-stu-id="10940-293">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-294">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-294">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-295">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-296">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10940-296">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10940-297">Код ошибки Win32 Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="10940-297">Win32 Configuration Manager error code.</span></span>

<span data-ttu-id="10940-298">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-298">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="10940-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Это устройство работает правильно.**</span><span class="sxs-lookup"><span data-stu-id="10940-299"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="10940-300"> (0)</span><span class="sxs-lookup"><span data-stu-id="10940-300">(0)</span></span>


</dt> <dd>

<span data-ttu-id="10940-301">Устройство работает правильно.</span><span class="sxs-lookup"><span data-stu-id="10940-301">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="10940-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Это устройство настроено неправильно.**</span><span class="sxs-lookup"><span data-stu-id="10940-302"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="10940-303">(1)</span><span class="sxs-lookup"><span data-stu-id="10940-303">(1)</span></span>


</dt> <dd>

<span data-ttu-id="10940-304">Устройство настроено неправильно.</span><span class="sxs-lookup"><span data-stu-id="10940-304">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10940-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows не удается загрузить драйвер для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-305"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="10940-306">(2)</span><span class="sxs-lookup"><span data-stu-id="10940-306">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="10940-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Возможно, драйвер для этого устройства поврежден, или в системе недостаточно памяти или других ресурсов.**</span><span class="sxs-lookup"><span data-stu-id="10940-307"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="10940-308">(3)</span><span class="sxs-lookup"><span data-stu-id="10940-308">(3)</span></span>


</dt> <dd>

<span data-ttu-id="10940-309">Возможно, драйвер для этого устройства поврежден или системе не хватает памяти или других ресурсов.</span><span class="sxs-lookup"><span data-stu-id="10940-309">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10940-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Это устройство работает неправильно. Один из его драйверов или реестра может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="10940-310"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="10940-311">(4)</span><span class="sxs-lookup"><span data-stu-id="10940-311">(4)</span></span>


</dt> <dd>

<span data-ttu-id="10940-312">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="10940-312">Device is not working properly.</span></span> <span data-ttu-id="10940-313">Один из драйверов или реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="10940-313">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="10940-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**Драйверу для этого устройства требуется ресурс, который Windows не может управлять.**</span><span class="sxs-lookup"><span data-stu-id="10940-314"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="10940-315">(5)</span><span class="sxs-lookup"><span data-stu-id="10940-315">(5)</span></span>


</dt> <dd>

<span data-ttu-id="10940-316">Драйверу для устройства требуется ресурс, который Windows не может управлять.</span><span class="sxs-lookup"><span data-stu-id="10940-316">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="10940-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**Конфигурация загрузки для этого устройства конфликтует с другими устройствами.**</span><span class="sxs-lookup"><span data-stu-id="10940-317"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="10940-318"> (6)</span><span class="sxs-lookup"><span data-stu-id="10940-318">(6)</span></span>


</dt> <dd>

<span data-ttu-id="10940-319">Конфигурация загрузки для устройства конфликтует с другими устройствами.</span><span class="sxs-lookup"><span data-stu-id="10940-319">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="10940-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Не удается выполнить фильтрацию.**</span><span class="sxs-lookup"><span data-stu-id="10940-320"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="10940-321">(7)</span><span class="sxs-lookup"><span data-stu-id="10940-321">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="10940-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Отсутствует загрузчик драйверов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-322"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="10940-323">(8)</span><span class="sxs-lookup"><span data-stu-id="10940-323">(8)</span></span>


</dt> <dd>

<span data-ttu-id="10940-324">Отсутствует загрузчик драйверов для устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-324">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="10940-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Это устройство работает неправильно, так как встроенное по управления сообщает о неправильном использовании ресурсов для устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-325"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="10940-326">(9)</span><span class="sxs-lookup"><span data-stu-id="10940-326">(9)</span></span>


</dt> <dd>

<span data-ttu-id="10940-327">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="10940-327">Device is not working properly.</span></span> <span data-ttu-id="10940-328">Встроенное по управления неправильно сообщает ресурсы для устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-328">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="10940-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Не удается запустить устройство.**</span><span class="sxs-lookup"><span data-stu-id="10940-329"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="10940-330">(10)</span><span class="sxs-lookup"><span data-stu-id="10940-330">(10)</span></span>


</dt> <dd>

<span data-ttu-id="10940-331">Не удается запустить устройство.</span><span class="sxs-lookup"><span data-stu-id="10940-331">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="10940-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Сбой устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-332"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="10940-333">(11)</span><span class="sxs-lookup"><span data-stu-id="10940-333">(11)</span></span>


</dt> <dd>

<span data-ttu-id="10940-334">Сбой устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-334">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="10940-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Этому устройству не удается найти достаточно свободных ресурсов, которые можно использовать.**</span><span class="sxs-lookup"><span data-stu-id="10940-335"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="10940-336">(12)</span><span class="sxs-lookup"><span data-stu-id="10940-336">(12)</span></span>


</dt> <dd>

<span data-ttu-id="10940-337">Устройству не удается найти достаточно свободных ресурсов для использования.</span><span class="sxs-lookup"><span data-stu-id="10940-337">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="10940-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows не удается проверить ресурсы этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-338"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="10940-339">(13)</span><span class="sxs-lookup"><span data-stu-id="10940-339">(13)</span></span>


</dt> <dd>

<span data-ttu-id="10940-340">Windows не может проверить ресурсы устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-340">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="10940-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Это устройство не может работать должным образом, пока компьютер не будет перезагружен.**</span><span class="sxs-lookup"><span data-stu-id="10940-341"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="10940-342">(14)</span><span class="sxs-lookup"><span data-stu-id="10940-342">(14)</span></span>


</dt> <dd>

<span data-ttu-id="10940-343">Устройство не может работать должным образом, пока компьютер не будет перезагружен.</span><span class="sxs-lookup"><span data-stu-id="10940-343">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="10940-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Это устройство работает неправильно, так как, возможно, возникла проблема повторного перечисления.**</span><span class="sxs-lookup"><span data-stu-id="10940-344"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="10940-345">(15)</span><span class="sxs-lookup"><span data-stu-id="10940-345">(15)</span></span>


</dt> <dd>

<span data-ttu-id="10940-346">Устройство не работает должным образом из-за возможной проблемы повторного перечисления.</span><span class="sxs-lookup"><span data-stu-id="10940-346">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="10940-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows не удается найти все ресурсы, используемые этим устройством.**</span><span class="sxs-lookup"><span data-stu-id="10940-347"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="10940-348">(16)</span><span class="sxs-lookup"><span data-stu-id="10940-348">(16)</span></span>


</dt> <dd>

<span data-ttu-id="10940-349">Windows не удается найти все ресурсы, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="10940-349">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="10940-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Устройство запрашивает неизвестный тип ресурса.**</span><span class="sxs-lookup"><span data-stu-id="10940-350"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="10940-351">(17)</span><span class="sxs-lookup"><span data-stu-id="10940-351">(17)</span></span>


</dt> <dd>

<span data-ttu-id="10940-352">Устройство запрашивает неизвестный тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="10940-352">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10940-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Переустановите драйверы для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-353"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="10940-354">(18)</span><span class="sxs-lookup"><span data-stu-id="10940-354">(18)</span></span>


</dt> <dd>

<span data-ttu-id="10940-355">Необходимо переустановить драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="10940-355">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="10940-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Сбой при использовании загрузчика VxD.**</span><span class="sxs-lookup"><span data-stu-id="10940-356"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="10940-357">(19)</span><span class="sxs-lookup"><span data-stu-id="10940-357">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="10940-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Реестр может быть поврежден.**</span><span class="sxs-lookup"><span data-stu-id="10940-358"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="10940-359">(20)</span><span class="sxs-lookup"><span data-stu-id="10940-359">(20)</span></span>


</dt> <dd>

<span data-ttu-id="10940-360">Реестр может быть поврежден.</span><span class="sxs-lookup"><span data-stu-id="10940-360">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="10940-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию. Windows удаляет это устройство.**</span><span class="sxs-lookup"><span data-stu-id="10940-361"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="10940-362">(21)</span><span class="sxs-lookup"><span data-stu-id="10940-362">(21)</span></span>


</dt> <dd>

<span data-ttu-id="10940-363">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="10940-363">System failure.</span></span> <span data-ttu-id="10940-364">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="10940-364">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="10940-365">Windows удаляет устройство.</span><span class="sxs-lookup"><span data-stu-id="10940-365">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="10940-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Это устройство отключено.**</span><span class="sxs-lookup"><span data-stu-id="10940-366"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="10940-367">(22)</span><span class="sxs-lookup"><span data-stu-id="10940-367">(22)</span></span>


</dt> <dd>

<span data-ttu-id="10940-368">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="10940-368">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="10940-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Сбой системы: попробуйте изменить драйвер для этого устройства. Если это не поможет, см. документацию по оборудованию.**</span><span class="sxs-lookup"><span data-stu-id="10940-369"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="10940-370">(23)</span><span class="sxs-lookup"><span data-stu-id="10940-370">(23)</span></span>


</dt> <dd>

<span data-ttu-id="10940-371">Сбой системы.</span><span class="sxs-lookup"><span data-stu-id="10940-371">System failure.</span></span> <span data-ttu-id="10940-372">Если изменение драйвера устройства неэффективно, см. документацию по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="10940-372">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="10940-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Это устройство отсутствует, работает неправильно или не имеет установленных драйверов.**</span><span class="sxs-lookup"><span data-stu-id="10940-373"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="10940-374">(24)</span><span class="sxs-lookup"><span data-stu-id="10940-374">(24)</span></span>


</dt> <dd>

<span data-ttu-id="10940-375">Устройство отсутствует, не работает должным образом или не имеет установленных драйверов.</span><span class="sxs-lookup"><span data-stu-id="10940-375">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10940-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="10940-376"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10940-377">(25)</span><span class="sxs-lookup"><span data-stu-id="10940-377">(25)</span></span>


</dt> <dd>

<span data-ttu-id="10940-378">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="10940-378">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="10940-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Это устройство все еще настраивается Windows.**</span><span class="sxs-lookup"><span data-stu-id="10940-379"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="10940-380">(26)</span><span class="sxs-lookup"><span data-stu-id="10940-380">(26)</span></span>


</dt> <dd>

<span data-ttu-id="10940-381">Устройство все еще настраивается.</span><span class="sxs-lookup"><span data-stu-id="10940-381">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="10940-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Это устройство не имеет допустимой конфигурации журнала.**</span><span class="sxs-lookup"><span data-stu-id="10940-382"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="10940-383">(27)</span><span class="sxs-lookup"><span data-stu-id="10940-383">(27)</span></span>


</dt> <dd>

<span data-ttu-id="10940-384">Устройство не имеет допустимой конфигурации журнала.</span><span class="sxs-lookup"><span data-stu-id="10940-384">Device does not have a valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="10940-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Драйверы для этого устройства не установлены.**</span><span class="sxs-lookup"><span data-stu-id="10940-385"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="10940-386">(28)</span><span class="sxs-lookup"><span data-stu-id="10940-386">(28)</span></span>


</dt> <dd>

<span data-ttu-id="10940-387">Драйверы устройств не установлены.</span><span class="sxs-lookup"><span data-stu-id="10940-387">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="10940-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Это устройство отключено, так как встроенное по устройства не предоставил ему необходимые ресурсы.**</span><span class="sxs-lookup"><span data-stu-id="10940-388"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="10940-389">(29)</span><span class="sxs-lookup"><span data-stu-id="10940-389">(29)</span></span>


</dt> <dd>

<span data-ttu-id="10940-390">Устройство отключено.</span><span class="sxs-lookup"><span data-stu-id="10940-390">Device is disabled.</span></span> <span data-ttu-id="10940-391">Встроенное по устройства не предпредоставил необходимые ресурсы.</span><span class="sxs-lookup"><span data-stu-id="10940-391">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="10940-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Это устройство использует ресурс запроса на прерывание (IRQ), который используется другим устройством.**</span><span class="sxs-lookup"><span data-stu-id="10940-392"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="10940-393">(30)</span><span class="sxs-lookup"><span data-stu-id="10940-393">(30)</span></span>


</dt> <dd>

<span data-ttu-id="10940-394">Устройство использует ресурс IRQ, который используется другим устройством.</span><span class="sxs-lookup"><span data-stu-id="10940-394">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="10940-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Это устройство работает неправильно, так как Windows не может загрузить драйверы, необходимые для этого устройства.**</span><span class="sxs-lookup"><span data-stu-id="10940-395"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="10940-396">1-31</span><span class="sxs-lookup"><span data-stu-id="10940-396">(31)</span></span>


</dt> <dd>

<span data-ttu-id="10940-397">Устройство работает неправильно.</span><span class="sxs-lookup"><span data-stu-id="10940-397">Device is not working properly.</span></span> <span data-ttu-id="10940-398">Windows не может загрузить необходимые драйверы устройств.</span><span class="sxs-lookup"><span data-stu-id="10940-398">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-399">**конфигманажерусерконфиг**</span><span class="sxs-lookup"><span data-stu-id="10940-399">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-400">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-400">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-401">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-402">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10940-402">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10940-403">Если **значение — true**, устройство использует определяемую пользователем конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="10940-403">If **TRUE**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="10940-404">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-404">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-405">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="10940-405">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-406">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-407">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-408">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-408">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-409">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой для создания экземпляра.</span><span class="sxs-lookup"><span data-stu-id="10940-409">Name of the first concrete class to appear in the inheritance chain used to create an instance.</span></span> <span data-ttu-id="10940-410">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="10940-410">When used with other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="10940-411">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-411">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-412">**курренткапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="10940-412">**CurrentCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-413">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-413">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-414">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-415">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="10940-415">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-416">Массив возможностей принтера, которые сейчас используются.</span><span class="sxs-lookup"><span data-stu-id="10940-416">Array of printer capabilities that are being used currently.</span></span> <span data-ttu-id="10940-417">Запись в этом свойстве также должна быть указана в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="10940-417">An entry in this property must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="10940-418">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-418">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-419"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-420"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="10940-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-421"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="10940-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-422"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="10940-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-423"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="10940-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-424"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="10940-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-425"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="10940-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-426"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="10940-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-427"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="10940-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-428"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="10940-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-429"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="10940-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-430"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="10940-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-431"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="10940-432">One-Sided</span><span class="sxs-lookup"><span data-stu-id="10940-432">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="10940-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-433"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10940-434">Two-Sided длинное ребро</span><span class="sxs-lookup"><span data-stu-id="10940-434">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="10940-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-435"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10940-436">Two-Sided короткий пограничная</span><span class="sxs-lookup"><span data-stu-id="10940-436">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="10940-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-437"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="10940-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-438"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="10940-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-439"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="10940-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-440"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="10940-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-441"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="10940-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-442"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="10940-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-443"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-444">**куррентчарсет**</span><span class="sxs-lookup"><span data-stu-id="10940-444">**CurrentCharSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-445">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-446">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-446">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-447">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Чарсетссуппортед**")</span><span class="sxs-lookup"><span data-stu-id="10940-447">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CharSetsSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-448">Кодировка, используемая в данный момент для выходных данных.</span><span class="sxs-lookup"><span data-stu-id="10940-448">The character set currently used for output.</span></span> <span data-ttu-id="10940-449">Строки, предоставленные в этом свойстве, должны соответствовать семантике и синтаксису, заданному в разделе 4.1.2 ("параметры charset") в RFC 2046 (MIME Part 2) и содержащихся в реестре набора символов IANA.</span><span class="sxs-lookup"><span data-stu-id="10940-449">Strings provided in this property must conform to the semantics and syntax specified by section 4.1.2 ("Charset parameters") in RFC 2046 (MIME Part 2) and contained in the IANA character-set registry.</span></span> <span data-ttu-id="10940-450">Примеры: UTF-8, US-ASCII и ISO-8859-1.</span><span class="sxs-lookup"><span data-stu-id="10940-450">Examples include "utf-8", "us-ASCII", and iso-8859-1.</span></span>

<span data-ttu-id="10940-451">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-451">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-452">**куррентлангуаже**</span><span class="sxs-lookup"><span data-stu-id="10940-452">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-453">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-453">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-454">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-454">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-455">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)". Лангуажессуппортед ","**CIM \_ Printer**.**Куррентмиметипе**")</span><span class="sxs-lookup"><span data-stu-id="10940-455">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**CurrentMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-456">Используемый в настоящее время язык принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-456">Printer language currently used.</span></span> <span data-ttu-id="10940-457">Используемый язык должен быть указан в свойстве **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="10940-457">The language used must be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="10940-458">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-458">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-459"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-460"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="10940-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-461"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="10940-462"><span id="HPGL"></span><span id="hpgl"></span>**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-462"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="10940-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-463"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="10940-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-464"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="10940-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-465"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="10940-466"><span id="IPDS"></span><span id="ipds"></span>**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-466"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="10940-467"><span id="PPDS"></span><span id="ppds"></span>**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-467"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="10940-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-468"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="10940-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-469"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="10940-470"><span id="DDIF"></span><span id="ddif"></span>**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-470"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="10940-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-471"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="10940-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-472"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="10940-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-473"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10940-474">линедата</span><span class="sxs-lookup"><span data-stu-id="10940-474">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="10940-475"><span id="MODCA"></span><span id="modca"></span>**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-475"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="10940-476">додка</span><span class="sxs-lookup"><span data-stu-id="10940-476">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="10940-477"><span id="REGIS"></span><span id="regis"></span>**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-477"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="10940-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-478"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="10940-479"><span id="SPDL"></span><span id="spdl"></span>**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-479"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="10940-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-480"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="10940-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-481"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="10940-482"><span id="IGP"></span><span id="igp"></span>**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="10940-482"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="10940-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="10940-483"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="10940-484"><span id="DSCDSE"></span><span id="dscdse"></span>**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="10940-484"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="10940-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="10940-485"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="10940-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="10940-486"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="10940-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="10940-487"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="10940-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="10940-488"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="10940-489"><span id="CPAP"></span><span id="cpap"></span>**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="10940-489"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="10940-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="10940-490"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="10940-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="10940-491"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="10940-492">симплетекст</span><span class="sxs-lookup"><span data-stu-id="10940-492">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="10940-493"><span id="NPAP"></span><span id="npap"></span>**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="10940-493"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="10940-494"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="10940-494"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="10940-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="10940-495"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="10940-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="10940-496"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="10940-497"><span id="NPDL"></span><span id="npdl"></span>**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="10940-497"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="10940-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="10940-498"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="10940-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="10940-499"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="10940-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="10940-500"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="10940-501"><span id="LIPS"></span><span id="lips"></span>**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="10940-501"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="10940-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="10940-502"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="10940-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="10940-503"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="10940-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="10940-504"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="10940-505"><span id="EXCL"></span><span id="excl"></span>**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="10940-505"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="10940-506"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="10940-506"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="10940-507"><span id="XES"></span><span id="xes"></span>**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="10940-507"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="10940-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="10940-508"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="10940-509">48</span><span class="sxs-lookup"><span data-stu-id="10940-509">48</span></span>
</dt> <dd>

<span data-ttu-id="10940-510">XPS</span><span class="sxs-lookup"><span data-stu-id="10940-510">XPS</span></span>

</dd> <dt>

<span data-ttu-id="10940-511">49</span><span class="sxs-lookup"><span data-stu-id="10940-511">49</span></span>
</dt> <dd>

<span data-ttu-id="10940-512">HPGL2</span><span class="sxs-lookup"><span data-stu-id="10940-512">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="10940-513">50</span><span class="sxs-lookup"><span data-stu-id="10940-513">50</span></span>
</dt> <dd>

<span data-ttu-id="10940-514">пклксл</span><span class="sxs-lookup"><span data-stu-id="10940-514">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-515">**куррентмиметипе**</span><span class="sxs-lookup"><span data-stu-id="10940-515">**CurrentMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-516">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-516">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-517">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-517">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-518">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Куррентлангуаже**")</span><span class="sxs-lookup"><span data-stu-id="10940-518">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**CurrentLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-519">Тип MIME, используемый в настоящее время, если **куррентлангуаже** является типом MIME (value = 47).</span><span class="sxs-lookup"><span data-stu-id="10940-519">MIME type currently being used if the **CurrentLanguage** is a MIME type (value = 47).</span></span>

<span data-ttu-id="10940-520">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-520">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-521">**куррентнатураллангуаже**</span><span class="sxs-lookup"><span data-stu-id="10940-521">**CurrentNaturalLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-522">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-522">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-523">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-523">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-524">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Натураллангуажессуппортед**")</span><span class="sxs-lookup"><span data-stu-id="10940-524">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**NaturalLanguagesSupported**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-525">Язык, который используется принтером для управления в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="10940-525">Language that the printer is using for management currently.</span></span> <span data-ttu-id="10940-526">Язык, указанный здесь, также должен быть указан в свойстве **натураллангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="10940-526">The language listed here must also be listed in the **NaturalLanguagesSupported** property.</span></span>

<span data-ttu-id="10940-527">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-527">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-528">**куррентпапертипе**</span><span class="sxs-lookup"><span data-stu-id="10940-528">**CurrentPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-529">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-529">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-530">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-530">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-531">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Папертипесаваилабле**")</span><span class="sxs-lookup"><span data-stu-id="10940-531">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-532">Тип бумаги, используемой принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-532">Type of paper the printer is using.</span></span> <span data-ttu-id="10940-533">Должно быть выражено в форме, указанной в приложении для печати документов ISO/IEC 10175 (DPA), которое обобщено в приложении C из RFC 1759 (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="10940-533">Must be expressed in the form specified by the ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of RFC 1759 (Printer MIB).</span></span>

<span data-ttu-id="10940-534">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-534">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-535">**По умолчанию**</span><span class="sxs-lookup"><span data-stu-id="10940-535">**Default**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-536">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-536">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-537">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-538">**Значение true** показывает, что принтер является принтером по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10940-538">If **TRUE**, the printer is the default printer.</span></span>

</dd> <dt>

<span data-ttu-id="10940-539">**дефаулткапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="10940-539">**DefaultCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-540">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-540">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-541">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-541">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-542">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Возможности**")</span><span class="sxs-lookup"><span data-stu-id="10940-542">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-543">Массив возможностей принтера, используемый по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10940-543">Array of the printer capabilities used by default.</span></span> <span data-ttu-id="10940-544">Каждая запись в массиве **дефаулткапабилитиес** также должна быть указана в массиве **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="10940-544">Each entry in the **DefaultCapabilities** array must also be listed in the **Capabilities** array.</span></span>

<span data-ttu-id="10940-545">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-545">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-547"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span data-ttu-id="10940-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Цветная печать** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-548"><span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Color Printing** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span data-ttu-id="10940-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Дуплексная печать** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-549"><span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Duplex Printing** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span data-ttu-id="10940-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Копии** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-550"><span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Copies** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span data-ttu-id="10940-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Параметры сортировки** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-551"><span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span data-ttu-id="10940-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Сшивание** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-552"><span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span data-ttu-id="10940-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Прозрачная печать** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-553"><span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Transparency Printing** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span data-ttu-id="10940-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Дырокол** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-554"><span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Punch** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span data-ttu-id="10940-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Покрытие** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-555"><span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cover** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span data-ttu-id="10940-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**BIND** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-556"><span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span data-ttu-id="10940-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Черно-белая печать** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-557"><span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Black and White Printing** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span data-ttu-id="10940-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Одна сторона** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-558"><span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)</span></span>


</dt> <dd>

<span data-ttu-id="10940-559">One-Sided</span><span class="sxs-lookup"><span data-stu-id="10940-559">One-Sided</span></span>

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span data-ttu-id="10940-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>Двусторонняя **сторона** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-560"><span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Two Sided Long Edge** (13)</span></span>


</dt> <dd>

<span data-ttu-id="10940-561">Two-Sided длинное ребро</span><span class="sxs-lookup"><span data-stu-id="10940-561">Two-Sided Long Edge</span></span>

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span data-ttu-id="10940-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>Двусторонняя **короткая сторона** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-562"><span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Two Sided Short Edge** (14)</span></span>


</dt> <dd>

<span data-ttu-id="10940-563">Two-Sided короткий пограничная</span><span class="sxs-lookup"><span data-stu-id="10940-563">Two-Sided Short Edge</span></span>

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span data-ttu-id="10940-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Книжная** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-564"><span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Portrait** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span data-ttu-id="10940-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Альбомная** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-565"><span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Landscape** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span data-ttu-id="10940-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Обратная книжная** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-566"><span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverse Portrait** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span data-ttu-id="10940-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Обратная альбомная** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-567"><span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Reverse Landscape** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span data-ttu-id="10940-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Высокое качество** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-568"><span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Quality High** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span data-ttu-id="10940-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Нормальное качество** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-569"><span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span data-ttu-id="10940-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Низкое качество** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-570"><span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Quality Low** (21)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-571">**дефаулткопиес**</span><span class="sxs-lookup"><span data-stu-id="10940-571">**DefaultCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-572">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-572">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-573">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-573">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-574">Количество копий, созданных для одного задания, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="10940-574">Number of copies produced for one job—unless otherwise specified.</span></span>

<span data-ttu-id="10940-575">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-575">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-576">**DefaultLanguage**</span><span class="sxs-lookup"><span data-stu-id="10940-576">**DefaultLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-577">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-577">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-578">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-578">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-579">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)". Лангуажессуппортед ","**CIM \_ Printer**.**Дефаултмиметипе**")</span><span class="sxs-lookup"><span data-stu-id="10940-579">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "**CIM\_Printer**.**DefaultMimeType**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-580">Язык принтера по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="10940-580">Default printer language.</span></span> <span data-ttu-id="10940-581">Язык, указанный здесь, также должен быть указан в свойстве **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="10940-581">The language listed here must also be listed in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="10940-582">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-582">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-583"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-584"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="10940-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-585"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="10940-586"><span id="HPGL"></span><span id="hpgl"></span>**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-586"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="10940-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-587"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="10940-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-588"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="10940-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-589"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="10940-590"><span id="IPDS"></span><span id="ipds"></span>**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-590"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="10940-591"><span id="PPDS"></span><span id="ppds"></span>**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-591"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="10940-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-592"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="10940-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-593"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="10940-594"><span id="DDIF"></span><span id="ddif"></span>**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-594"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="10940-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-595"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="10940-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-596"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="10940-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-597"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10940-598">линедата</span><span class="sxs-lookup"><span data-stu-id="10940-598">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="10940-599"><span id="MODCA"></span><span id="modca"></span>**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-599"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="10940-600">додка</span><span class="sxs-lookup"><span data-stu-id="10940-600">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="10940-601"><span id="REGIS"></span><span id="regis"></span>**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-601"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="10940-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-602"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="10940-603"><span id="SPDL"></span><span id="spdl"></span>**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-603"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="10940-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-604"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="10940-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-605"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="10940-606"><span id="IGP"></span><span id="igp"></span>**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="10940-606"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="10940-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="10940-607"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="10940-608"><span id="DSCDSE"></span><span id="dscdse"></span>**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="10940-608"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="10940-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="10940-609"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="10940-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="10940-610"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="10940-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="10940-611"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="10940-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="10940-612"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="10940-613"><span id="CPAP"></span><span id="cpap"></span>**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="10940-613"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="10940-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="10940-614"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="10940-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="10940-615"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="10940-616">симплетекст</span><span class="sxs-lookup"><span data-stu-id="10940-616">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="10940-617"><span id="NPAP"></span><span id="npap"></span>**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="10940-617"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="10940-618"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="10940-618"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="10940-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="10940-619"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="10940-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="10940-620"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="10940-621"><span id="NPDL"></span><span id="npdl"></span>**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="10940-621"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="10940-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="10940-622"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="10940-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="10940-623"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="10940-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="10940-624"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="10940-625"><span id="LIPS"></span><span id="lips"></span>**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="10940-625"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="10940-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="10940-626"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="10940-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="10940-627"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="10940-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="10940-628"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="10940-629"><span id="EXCL"></span><span id="excl"></span>**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="10940-629"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="10940-630"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="10940-630"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="10940-631"><span id="XES"></span><span id="xes"></span>**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="10940-631"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="10940-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="10940-632"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span data-ttu-id="10940-633">48</span><span class="sxs-lookup"><span data-stu-id="10940-633">48</span></span>
</dt> <dd>

<span data-ttu-id="10940-634">XPS</span><span class="sxs-lookup"><span data-stu-id="10940-634">XPS</span></span>

</dd> <dt>

<span data-ttu-id="10940-635">49</span><span class="sxs-lookup"><span data-stu-id="10940-635">49</span></span>
</dt> <dd>

<span data-ttu-id="10940-636">HPGL2</span><span class="sxs-lookup"><span data-stu-id="10940-636">HPGL2</span></span>

</dd> <dt>

<span data-ttu-id="10940-637">50</span><span class="sxs-lookup"><span data-stu-id="10940-637">50</span></span>
</dt> <dd>

<span data-ttu-id="10940-638">пклксл</span><span class="sxs-lookup"><span data-stu-id="10940-638">PCLXL</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-639">**дефаултмиметипе**</span><span class="sxs-lookup"><span data-stu-id="10940-639">**DefaultMimeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-640">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-640">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-641">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-641">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-642">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**DefaultLanguage**")</span><span class="sxs-lookup"><span data-stu-id="10940-642">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DefaultLanguage**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-643">Тип MIME, используемый в настоящее время, если значение **DefaultLanguage** является типом MIME (value = 47).</span><span class="sxs-lookup"><span data-stu-id="10940-643">MIME type currently being used, if the **DefaultLanguage** value is a MIME type (value = 47).</span></span>

<span data-ttu-id="10940-644">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-644">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-645">**дефаултнумберуп**</span><span class="sxs-lookup"><span data-stu-id="10940-645">**DefaultNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-646">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-646">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-647">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-647">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-648">Количество страниц на печатном потоке, отображаемых принтером на одном листе мультимедиа, если в задании не указано иное.</span><span class="sxs-lookup"><span data-stu-id="10940-648">Number of print-stream pages that the printer renders on one media sheet—unless a job specifies otherwise.</span></span>

<span data-ttu-id="10940-649">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-649">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-650">**дефаултпапертипе**</span><span class="sxs-lookup"><span data-stu-id="10940-650">**DefaultPaperType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-651">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-651">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-652">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-652">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-653">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Папертипесаваилабле**")</span><span class="sxs-lookup"><span data-stu-id="10940-653">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**PaperTypesAvailable**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-654">Тип бумаги, используемый принтером, если задание печати не указывает другой тип бумаги.</span><span class="sxs-lookup"><span data-stu-id="10940-654">Paper type that the printer uses—unless a print job specifies a different paper type.</span></span> <span data-ttu-id="10940-655">Строка должна быть выражена в форме, заданной в приложении для печати документов ISO/IEC 1017 (DPA), которое суммируется в приложении C из [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="10940-655">The string must be expressed in the form specified by ISO/IEC 1017 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span>

<span data-ttu-id="10940-656">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-656">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-657">**дефаултприорити**</span><span class="sxs-lookup"><span data-stu-id="10940-657">**DefaultPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-658">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-658">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-659">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-659">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-660">Значение приоритета по умолчанию, назначенное каждому заданию печати.</span><span class="sxs-lookup"><span data-stu-id="10940-660">Default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="10940-661">**Описание**</span><span class="sxs-lookup"><span data-stu-id="10940-661">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-662">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-662">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-663">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-663">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-664">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="10940-664">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="10940-665">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="10940-665">Description of an object.</span></span>

<span data-ttu-id="10940-666">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10940-666">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-667">**детектедеррорстате**</span><span class="sxs-lookup"><span data-stu-id="10940-667">**DetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-668">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-668">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-669">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-669">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-670">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Ерроринформатион**"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" MIB. \|Принтер IETF — MIB. хрпринтердетектедеррорстате ")</span><span class="sxs-lookup"><span data-stu-id="10940-670">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**ErrorInformation**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterDetectedErrorState")</span></span>
</dt> </dl>

<span data-ttu-id="10940-671">Сведения об ошибках принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-671">Printer error information.</span></span>

<span data-ttu-id="10940-672">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-672">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-673">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-673">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-674">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-674">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

<span data-ttu-id="10940-675">**Без ошибок** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-675">**No Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

<span data-ttu-id="10940-676">**Мало бумаги** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-676">**Low Paper** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

<span data-ttu-id="10940-677">**Нет бумаги** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-677">**No Paper** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

<span data-ttu-id="10940-678">**Низкий тонер** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-678">**Low Toner** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

<span data-ttu-id="10940-679">**Нет тонера** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-679">**No Toner** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

<span data-ttu-id="10940-680">**Открыта дверца** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-680">**Door Open** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

<span data-ttu-id="10940-681">**Застревание бумаги** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-681">**Jammed** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="10940-682">**Вне сети** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-682">**Offline** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

<span data-ttu-id="10940-683">**Запрошенная служба** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-683">**Service Requested** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

<span data-ttu-id="10940-684">**Выходной лоток полон** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-684">**Output Bin Full** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-685">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="10940-685">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-686">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-686">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-687">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-687">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-688">Квалификаторы: [ **\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-688">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-689">Уникальный идентификатор принтера в системе.</span><span class="sxs-lookup"><span data-stu-id="10940-689">Unique identifier of the printer on a system.</span></span>

<span data-ttu-id="10940-690">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-690">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-691">**Direct**.</span><span class="sxs-lookup"><span data-stu-id="10940-691">**Direct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-692">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-692">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-693">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-693">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-694">Если задано **значение true**, задание печати отправляется непосредственно на принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-694">If **TRUE**, the print job is sent directly to the printer.</span></span> <span data-ttu-id="10940-695">Если задано **значение false**, задание печати помещается в очередь.</span><span class="sxs-lookup"><span data-stu-id="10940-695">If **FALSE**, the print job is spooled.</span></span>

</dd> <dt>

<span data-ttu-id="10940-696">**докомплетефирст**</span><span class="sxs-lookup"><span data-stu-id="10940-696">**DoCompleteFirst**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-697">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-697">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-698">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-698">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-699">Если **значение — true**, принтер запускает задания, которые завершили работу в очереди.</span><span class="sxs-lookup"><span data-stu-id="10940-699">If **TRUE**, the printer starts jobs that are finished spooling.</span></span> <span data-ttu-id="10940-700">Если задано **значение false**, принтер запускает задания в порядке получения заданий.</span><span class="sxs-lookup"><span data-stu-id="10940-700">If **FALSE**, the printer starts jobs in the order that the jobs are received.</span></span>

</dd> <dt>

<span data-ttu-id="10940-701">**Имя_драйвера**</span><span class="sxs-lookup"><span data-stu-id="10940-701">**DriverName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-702">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-702">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-703">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-703">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-704">Имя драйвера принтера Windows.</span><span class="sxs-lookup"><span data-stu-id="10940-704">Name of the Windows printer driver.</span></span>

<span data-ttu-id="10940-705">Пример: драйвер факса Windows</span><span class="sxs-lookup"><span data-stu-id="10940-705">Example: Windows Fax Driver</span></span>

</dd> <dt>

<span data-ttu-id="10940-706">**енаблебиди**</span><span class="sxs-lookup"><span data-stu-id="10940-706">**EnableBIDI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-707">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-707">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-708">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-708">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-709">Если **значение — true**, принтер может печататься с двунаправленным письмом.</span><span class="sxs-lookup"><span data-stu-id="10940-709">If **TRUE**, the printer can print bidirectionally.</span></span>

</dd> <dt>

<span data-ttu-id="10940-710">**енабледевкуерипринт**</span><span class="sxs-lookup"><span data-stu-id="10940-710">**EnableDevQueryPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-711">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-711">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-712">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-712">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-713">Если **значение — true**, принтер содержит документы в очереди, если настройки документов и принтеров не совпадают.</span><span class="sxs-lookup"><span data-stu-id="10940-713">If **TRUE**, the printer holds documents in the queue when document and printer setups do not match.</span></span>

</dd> <dt>

<span data-ttu-id="10940-714">**еррорклеаред**</span><span class="sxs-lookup"><span data-stu-id="10940-714">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-715">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-715">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-716">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-716">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-717">Если **значение — true**, ошибка, обнаруженная в **ластерроркоде** , была удалена.</span><span class="sxs-lookup"><span data-stu-id="10940-717">If **TRUE**, the error reported in **LastErrorCode** has been cleared.</span></span>

<span data-ttu-id="10940-718">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-718">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-719">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="10940-719">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-720">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-720">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-721">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-721">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-722">Сведения об ошибке, записанной в **ластерроркоде**, и сведения о корректирующих действиях, которые могут быть выполнены.</span><span class="sxs-lookup"><span data-stu-id="10940-722">Information about the error recorded in **LastErrorCode**, and information about corrective actions that can be taken.</span></span>

<span data-ttu-id="10940-723">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-723">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-724">**ерроринформатион**</span><span class="sxs-lookup"><span data-stu-id="10940-724">**ErrorInformation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-725">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-725">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-726">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-726">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="10940-727">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)".**Детектедеррорстате**")</span><span class="sxs-lookup"><span data-stu-id="10940-727">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).**DetectedErrorState**")</span></span>
</dt> </dl>

<span data-ttu-id="10940-728">Массив дополнительных сведений о текущем состоянии ошибки, указанном в **детектедеррорстате**.</span><span class="sxs-lookup"><span data-stu-id="10940-728">Array of supplemental information for the current error state indicated in **DetectedErrorState**.</span></span>

<span data-ttu-id="10940-729">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-729">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-730">**екстендеддетектедеррорстате**</span><span class="sxs-lookup"><span data-stu-id="10940-730">**ExtendedDetectedErrorState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-731">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-731">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-732">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-732">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-733">Сообщает стандартные сведения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="10940-733">Reports standard error information.</span></span> <span data-ttu-id="10940-734">Дополнительные сведения должны быть записаны в **детектедеррорстате**.</span><span class="sxs-lookup"><span data-stu-id="10940-734">Additional information should be recorded in **DetectedErrorState**.</span></span>

<span data-ttu-id="10940-735">Доступны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="10940-735">Values are:</span></span>

<dt>

<span data-ttu-id="10940-736">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="10940-736">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="10940-737">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="10940-737">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="10940-738">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="10940-738">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="10940-739">Другое</span><span class="sxs-lookup"><span data-stu-id="10940-739">Other</span></span>

</dd> <dt>

<span data-ttu-id="10940-740">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="10940-740">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="10940-741">Без ошибок</span><span class="sxs-lookup"><span data-stu-id="10940-741">No Error</span></span>

</dd> <dt>

<span data-ttu-id="10940-742">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="10940-742">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="10940-743">мало бумаги,</span><span class="sxs-lookup"><span data-stu-id="10940-743">Low Paper</span></span>

</dd> <dt>

<span data-ttu-id="10940-744">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="10940-744">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="10940-745">нет бумаги,</span><span class="sxs-lookup"><span data-stu-id="10940-745">No Paper</span></span>

</dd> <dt>

<span data-ttu-id="10940-746">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="10940-746">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="10940-747">мало тонера,</span><span class="sxs-lookup"><span data-stu-id="10940-747">Low Toner</span></span>

</dd> <dt>

<span data-ttu-id="10940-748">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="10940-748">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="10940-749">нет тонера,</span><span class="sxs-lookup"><span data-stu-id="10940-749">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="10940-750">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="10940-750">7 (0x7)</span></span>
</dt> <dd>

<span data-ttu-id="10940-751">открыта дверца,</span><span class="sxs-lookup"><span data-stu-id="10940-751">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="10940-752">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="10940-752">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="10940-753">замятие бумаги,</span><span class="sxs-lookup"><span data-stu-id="10940-753">Jammed</span></span>

</dd> <dt>

<span data-ttu-id="10940-754">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="10940-754">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="10940-755">запрошено обслуживание,</span><span class="sxs-lookup"><span data-stu-id="10940-755">Service Requested</span></span>

</dd> <dt>

<span data-ttu-id="10940-756">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="10940-756">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="10940-757">выходной лоток полон,</span><span class="sxs-lookup"><span data-stu-id="10940-757">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="10940-758">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="10940-758">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="10940-759">Проблема с бумагой</span><span class="sxs-lookup"><span data-stu-id="10940-759">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="10940-760">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="10940-760">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="10940-761">Не удается напечатать страницу</span><span class="sxs-lookup"><span data-stu-id="10940-761">Cannot Print Page</span></span>

</dd> <dt>

<span data-ttu-id="10940-762">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="10940-762">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="10940-763">Требуется вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="10940-763">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="10940-764">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="10940-764">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="10940-765">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="10940-765">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="10940-766">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="10940-766">15 (0xF)</span></span>
</dt> <dd>

<span data-ttu-id="10940-767">Сервер неизвестен</span><span class="sxs-lookup"><span data-stu-id="10940-767">Server Unknown</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-768">**екстендедпринтерстатус**</span><span class="sxs-lookup"><span data-stu-id="10940-768">**ExtendedPrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-769">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-769">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-770">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-770">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-771">Сведения о состоянии принтера, отличные от сведений, указанных в свойстве **Availability** .</span><span class="sxs-lookup"><span data-stu-id="10940-771">Status information for a printer that is different from information specified in the **Availability** property.</span></span>

<dt>

<span data-ttu-id="10940-772">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="10940-772">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="10940-773">Другое</span><span class="sxs-lookup"><span data-stu-id="10940-773">Other</span></span>

</dd> <dt>

<span data-ttu-id="10940-774">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="10940-774">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="10940-775">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="10940-775">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="10940-776">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="10940-776">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="10940-777">Бездействие</span><span class="sxs-lookup"><span data-stu-id="10940-777">Idle</span></span>

</dd> <dt>

<span data-ttu-id="10940-778">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="10940-778">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="10940-779">Печать</span><span class="sxs-lookup"><span data-stu-id="10940-779">Printing</span></span>

</dd> <dt>

<span data-ttu-id="10940-780">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="10940-780">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="10940-781">Прогрев</span><span class="sxs-lookup"><span data-stu-id="10940-781">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="10940-782">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="10940-782">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="10940-783">Печать остановлена</span><span class="sxs-lookup"><span data-stu-id="10940-783">Stopped Printing</span></span>

</dd> <dt>

<span data-ttu-id="10940-784">7</span><span class="sxs-lookup"><span data-stu-id="10940-784">7</span></span>
</dt> <dd>

<span data-ttu-id="10940-785">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="10940-785">Offline</span></span>

</dd> <dt>

<span data-ttu-id="10940-786">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="10940-786">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="10940-787">Пауза</span><span class="sxs-lookup"><span data-stu-id="10940-787">Paused</span></span>

</dd> <dt>

<span data-ttu-id="10940-788">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="10940-788">9 (0x9)</span></span>
</dt> <dd>

<span data-ttu-id="10940-789">Ошибка</span><span class="sxs-lookup"><span data-stu-id="10940-789">Error</span></span>

</dd> <dt>

<span data-ttu-id="10940-790">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="10940-790">10 (0xA)</span></span>
</dt> <dd>

<span data-ttu-id="10940-791">Занято</span><span class="sxs-lookup"><span data-stu-id="10940-791">Busy</span></span>

</dd> <dt>

<span data-ttu-id="10940-792">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="10940-792">11 (0xB)</span></span>
</dt> <dd>

<span data-ttu-id="10940-793">Недоступно</span><span class="sxs-lookup"><span data-stu-id="10940-793">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="10940-794">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="10940-794">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="10940-795">Ожидание</span><span class="sxs-lookup"><span data-stu-id="10940-795">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="10940-796">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="10940-796">13 (0xD)</span></span>
</dt> <dd>

<span data-ttu-id="10940-797">Обработка</span><span class="sxs-lookup"><span data-stu-id="10940-797">Processing</span></span>

</dd> <dt>

<span data-ttu-id="10940-798">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="10940-798">14 (0xE)</span></span>
</dt> <dd>

<span data-ttu-id="10940-799">Инициализация</span><span class="sxs-lookup"><span data-stu-id="10940-799">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="10940-800">15</span><span class="sxs-lookup"><span data-stu-id="10940-800">15</span></span>
</dt> <dd>

<span data-ttu-id="10940-801">Энергосбережение</span><span class="sxs-lookup"><span data-stu-id="10940-801">Power Save</span></span>

</dd> <dt>

<span data-ttu-id="10940-802">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="10940-802">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="10940-803">Ожидание удаления</span><span class="sxs-lookup"><span data-stu-id="10940-803">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="10940-804">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="10940-804">17 (0x11)</span></span>
</dt> <dd>

<span data-ttu-id="10940-805">Ввод-вывод активен</span><span class="sxs-lookup"><span data-stu-id="10940-805">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="10940-806">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="10940-806">18 (0x12)</span></span>
</dt> <dd>

<span data-ttu-id="10940-807">Ручная подача</span><span class="sxs-lookup"><span data-stu-id="10940-807">Manual Feed</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-808">**Скрыта**</span><span class="sxs-lookup"><span data-stu-id="10940-808">**Hidden**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-809">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-809">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-810">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-810">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-811">**Значение true** показывает, что принтер скрыт от пользователей сети.</span><span class="sxs-lookup"><span data-stu-id="10940-811">If **TRUE**, the printer is hidden from network users.</span></span>

</dd> <dt>

<span data-ttu-id="10940-812">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="10940-812">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-813">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-813">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-814">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-814">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-815">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. хоризонталресолутион"), [**Units**](../wmisdk/standard-qualifiers.md) ("пикселей на дюйм")</span><span class="sxs-lookup"><span data-stu-id="10940-815">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="10940-816">Горизонтальное разрешение принтера — в пикселях на дюйм.</span><span class="sxs-lookup"><span data-stu-id="10940-816">Horizontal resolution of the printer—in pixels per inch.</span></span>

<span data-ttu-id="10940-817">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-817">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-818">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="10940-818">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-819">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10940-819">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10940-820">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-820">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-821">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="10940-821">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="10940-822">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="10940-822">Date and time an object was installed.</span></span> <span data-ttu-id="10940-823">Объект может быть установлен без значения, записываемого в это свойство.</span><span class="sxs-lookup"><span data-stu-id="10940-823">The object may be installed without a value being written to this property.</span></span> <span data-ttu-id="10940-824">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10940-824">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-825">**жобкаунтсинцеластресет**</span><span class="sxs-lookup"><span data-stu-id="10940-825">**JobCountSinceLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-826">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-826">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-827">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-827">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-828">Квалификаторы: **Счетчик**</span><span class="sxs-lookup"><span data-stu-id="10940-828">Qualifiers: **Counter**</span></span>
</dt> </dl>

<span data-ttu-id="10940-829">Число заданий печати с момента последнего сброса принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-829">Number of print jobs since the printer was last reset.</span></span>

<span data-ttu-id="10940-830">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-830">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-831">**киппринтеджобс**</span><span class="sxs-lookup"><span data-stu-id="10940-831">**KeepPrintedJobs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-832">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-832">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-833">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-833">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-834">Если **значение — true**, диспетчер очереди печати не удаляет выполненные задания.</span><span class="sxs-lookup"><span data-stu-id="10940-834">If **TRUE**, the print spooler does not delete the completed jobs.</span></span>

</dd> <dt>

<span data-ttu-id="10940-835">**лангуажессуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-835">**LanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-836">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-836">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-837">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-837">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-838">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Принтер IETF — MIB. пртинтерпретерлангфамили "), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)". Миметипессуппортед "," CIM \_ PrintJob. Language "," CIM \_ Принтсервице. лангуажессуппортед ")</span><span class="sxs-lookup"><span data-stu-id="10940-838">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInterpreterLangFamily"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).MimeTypesSupported", "CIM\_PrintJob.Language", "CIM\_PrintService.LanguagesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="10940-839">Поддерживаемый массив языков печати.</span><span class="sxs-lookup"><span data-stu-id="10940-839">Array of the print languages natively supported.</span></span>

<span data-ttu-id="10940-840">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-840">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-841"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-842"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

<span data-ttu-id="10940-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-843"><span id="PCL"></span><span id="pcl"></span>**PCL** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

<span data-ttu-id="10940-844"><span id="HPGL"></span><span id="hpgl"></span>**Хпгл** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-844"><span id="HPGL"></span><span id="hpgl"></span>**HPGL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

<span data-ttu-id="10940-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-845"><span id="PJL"></span><span id="pjl"></span>**PJL** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

<span data-ttu-id="10940-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-846"><span id="PS"></span><span id="ps"></span>**PS** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

<span data-ttu-id="10940-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**Пспринтер** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-847"><span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>**PSPrinter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

<span data-ttu-id="10940-848"><span id="IPDS"></span><span id="ipds"></span>**ИПДС** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-848"><span id="IPDS"></span><span id="ipds"></span>**IPDS** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

<span data-ttu-id="10940-849"><span id="PPDS"></span><span id="ppds"></span>**Ппдс** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-849"><span id="PPDS"></span><span id="ppds"></span>**PPDS** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

<span data-ttu-id="10940-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**Ескапеп** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-850"><span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>**EscapeP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

<span data-ttu-id="10940-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-851"><span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>**Epson** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

<span data-ttu-id="10940-852"><span id="DDIF"></span><span id="ddif"></span>**Ддиф** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-852"><span id="DDIF"></span><span id="ddif"></span>**DDIF** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

<span data-ttu-id="10940-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Перенажатие** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-853"><span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>**Interpress** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

<span data-ttu-id="10940-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-854"><span id="ISO6429"></span><span id="iso6429"></span>**ISO6429** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

<span data-ttu-id="10940-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Данные линии** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-855"><span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>**Line Data** (15)</span></span>


</dt> <dd>

<span data-ttu-id="10940-856">линедата</span><span class="sxs-lookup"><span data-stu-id="10940-856">LineData</span></span>

</dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

<span data-ttu-id="10940-857"><span id="MODCA"></span><span id="modca"></span>**Модка** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-857"><span id="MODCA"></span><span id="modca"></span>**MODCA** (16)</span></span>


</dt> <dd>

<span data-ttu-id="10940-858">додка</span><span class="sxs-lookup"><span data-stu-id="10940-858">DODCA</span></span>

</dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

<span data-ttu-id="10940-859"><span id="REGIS"></span><span id="regis"></span>**Реджис** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-859"><span id="REGIS"></span><span id="regis"></span>**REGIS** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

<span data-ttu-id="10940-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-860"><span id="SCS"></span><span id="scs"></span>**SCS** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

<span data-ttu-id="10940-861"><span id="SPDL"></span><span id="spdl"></span>**Спдл** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-861"><span id="SPDL"></span><span id="spdl"></span>**SPDL** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

<span data-ttu-id="10940-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-862"><span id="TEK4014"></span><span id="tek4014"></span>**TEK4014** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

<span data-ttu-id="10940-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-863"><span id="PDS"></span><span id="pds"></span>**PDS** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

<span data-ttu-id="10940-864"><span id="IGP"></span><span id="igp"></span>**ИГП** (22)</span><span class="sxs-lookup"><span data-stu-id="10940-864"><span id="IGP"></span><span id="igp"></span>**IGP** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

<span data-ttu-id="10940-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**Кодев** (23)</span><span class="sxs-lookup"><span data-stu-id="10940-865"><span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>**CodeV** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

<span data-ttu-id="10940-866"><span id="DSCDSE"></span><span id="dscdse"></span>**Дскдсе** (24)</span><span class="sxs-lookup"><span data-stu-id="10940-866"><span id="DSCDSE"></span><span id="dscdse"></span>**DSCDSE** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

<span data-ttu-id="10940-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span><span class="sxs-lookup"><span data-stu-id="10940-867"><span id="WPS"></span><span id="wps"></span>**WPS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

<span data-ttu-id="10940-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span><span class="sxs-lookup"><span data-stu-id="10940-868"><span id="LN03"></span><span id="ln03"></span>**LN03** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

<span data-ttu-id="10940-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span><span class="sxs-lookup"><span data-stu-id="10940-869"><span id="CCITT"></span><span id="ccitt"></span>**CCITT** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

<span data-ttu-id="10940-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span><span class="sxs-lookup"><span data-stu-id="10940-870"><span id="QUIC"></span><span id="quic"></span>**QUIC** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

<span data-ttu-id="10940-871"><span id="CPAP"></span><span id="cpap"></span>**КПАП** (29)</span><span class="sxs-lookup"><span data-stu-id="10940-871"><span id="CPAP"></span><span id="cpap"></span>**CPAP** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

<span data-ttu-id="10940-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**Декппл** (30)</span><span class="sxs-lookup"><span data-stu-id="10940-872"><span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>**DecPPL** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

<span data-ttu-id="10940-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Простой текст** (31)</span><span class="sxs-lookup"><span data-stu-id="10940-873"><span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>**Simple Text** (31)</span></span>


</dt> <dd>

<span data-ttu-id="10940-874">симплетекст</span><span class="sxs-lookup"><span data-stu-id="10940-874">SimpleText</span></span>

</dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

<span data-ttu-id="10940-875"><span id="NPAP"></span><span id="npap"></span>**Нпап** (32)</span><span class="sxs-lookup"><span data-stu-id="10940-875"><span id="NPAP"></span><span id="npap"></span>**NPAP** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

<span data-ttu-id="10940-876"><span id="DOC"></span><span id="doc"></span>**Doc** (33)</span><span class="sxs-lookup"><span data-stu-id="10940-876"><span id="DOC"></span><span id="doc"></span>**DOC** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

<span data-ttu-id="10940-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span><span class="sxs-lookup"><span data-stu-id="10940-877"><span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>**imPress** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

<span data-ttu-id="10940-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Пинвритер** (35)</span><span class="sxs-lookup"><span data-stu-id="10940-878"><span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>**Pinwriter** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

<span data-ttu-id="10940-879"><span id="NPDL"></span><span id="npdl"></span>**НПДЛ** (36)</span><span class="sxs-lookup"><span data-stu-id="10940-879"><span id="NPDL"></span><span id="npdl"></span>**NPDL** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

<span data-ttu-id="10940-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span><span class="sxs-lookup"><span data-stu-id="10940-880"><span id="NEC201PL"></span><span id="nec201pl"></span>**NEC201PL** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="10940-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Автоматически** (38)</span><span class="sxs-lookup"><span data-stu-id="10940-881"><span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**Automatic** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

<span data-ttu-id="10940-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Страницы** (39)</span><span class="sxs-lookup"><span data-stu-id="10940-882"><span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>**Pages** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

<span data-ttu-id="10940-883"><span id="LIPS"></span><span id="lips"></span>**LIP** (40)</span><span class="sxs-lookup"><span data-stu-id="10940-883"><span id="LIPS"></span><span id="lips"></span>**LIPS** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

<span data-ttu-id="10940-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span><span class="sxs-lookup"><span data-stu-id="10940-884"><span id="TIFF"></span><span id="tiff"></span>**TIFF** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span data-ttu-id="10940-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Диагностика** (42)</span><span class="sxs-lookup"><span data-stu-id="10940-885"><span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnostic** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

<span data-ttu-id="10940-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**Cap** (43)</span><span class="sxs-lookup"><span data-stu-id="10940-886"><span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>**CaPSL** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

<span data-ttu-id="10940-887"><span id="EXCL"></span><span id="excl"></span>**Без** (44)</span><span class="sxs-lookup"><span data-stu-id="10940-887"><span id="EXCL"></span><span id="excl"></span>**EXCL** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

<span data-ttu-id="10940-888"><span id="LCDS"></span><span id="lcds"></span>**LCDs** (45)</span><span class="sxs-lookup"><span data-stu-id="10940-888"><span id="LCDS"></span><span id="lcds"></span>**LCDS** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

<span data-ttu-id="10940-889"><span id="XES"></span><span id="xes"></span>**Хранять** (46)</span><span class="sxs-lookup"><span data-stu-id="10940-889"><span id="XES"></span><span id="xes"></span>**XES** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

<span data-ttu-id="10940-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span><span class="sxs-lookup"><span data-stu-id="10940-890"><span id="MIME"></span><span id="mime"></span>**MIME** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

<span data-ttu-id="10940-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span><span class="sxs-lookup"><span data-stu-id="10940-891"><span id="XPS"></span><span id="xps"></span>**XPS** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

<span data-ttu-id="10940-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span><span class="sxs-lookup"><span data-stu-id="10940-892"><span id="HPGL2"></span><span id="hpgl2"></span>**HPGL2** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

<span data-ttu-id="10940-893"><span id="PCLXL"></span><span id="pclxl"></span>**Пклксл** (50)</span><span class="sxs-lookup"><span data-stu-id="10940-893"><span id="PCLXL"></span><span id="pclxl"></span>**PCLXL** (50)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-894">**ластерроркоде**</span><span class="sxs-lookup"><span data-stu-id="10940-894">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-895">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-895">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-896">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-896">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-897">Код последней ошибки, который сообщается на логическом устройстве.</span><span class="sxs-lookup"><span data-stu-id="10940-897">Last error code that the logical device reports.</span></span>

<span data-ttu-id="10940-898">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-898">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-899">**Локальное**</span><span class="sxs-lookup"><span data-stu-id="10940-899">**Local**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-900">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-900">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-901">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-901">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-902">Если **значение — true**, принтер не подключен к сети.</span><span class="sxs-lookup"><span data-stu-id="10940-902">If **TRUE**, the printer is not attached to a network.</span></span> <span data-ttu-id="10940-903">Если для **локальных** и **сетевых** свойств задано **значение true**, то принтер является сетевым принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-903">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="10940-904">**Расположение**</span><span class="sxs-lookup"><span data-stu-id="10940-904">**Location**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-905">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-905">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-906">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-906">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-907">Физическое расположение принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-907">Physical location of the printer.</span></span>

<span data-ttu-id="10940-908">Пример: Блдг.</span><span class="sxs-lookup"><span data-stu-id="10940-908">Example: Bldg.</span></span> <span data-ttu-id="10940-909">38, комната 1164</span><span class="sxs-lookup"><span data-stu-id="10940-909">38, Room 1164</span></span>

</dd> <dt>

<span data-ttu-id="10940-910">**маркингтечнологи**</span><span class="sxs-lookup"><span data-stu-id="10940-910">**MarkingTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-911">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-911">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-912">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-912">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-913">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Принтер IETF — MIB. пртмаркермарктеч ")</span><span class="sxs-lookup"><span data-stu-id="10940-913">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtMarkerMarkTech")</span></span>
</dt> </dl>

<span data-ttu-id="10940-914">Маркировка технологий, используемых принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-914">Marking technology the printer uses.</span></span>

<span data-ttu-id="10940-915">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-915">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-916">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-916">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-917">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-917">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

<span data-ttu-id="10940-918">**Светоиндикатор електрофотографик** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-918">**Electrophotographic LED** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

<span data-ttu-id="10940-919">**Електрофотографик лазерный** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-919">**Electrophotographic Laser** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="10940-920">**Електрофотографик** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-920">**Electrophotographic Other** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

<span data-ttu-id="10940-921">**Влияние перемещения головной точки на матрицу 9pin** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-921">**Impact Moving Head Dot Matrix 9pin** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

<span data-ttu-id="10940-922">**Влияние перемещения головной точки на матрицу 24pin** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-922">**Impact Moving Head Dot Matrix 24pin** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

<span data-ttu-id="10940-923">**Влияние перемещения головной точки на другую матрицу** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-923">**Impact Moving Head Dot Matrix Other** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

<span data-ttu-id="10940-924">**Полностью сформированный головной заголовк влияния** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-924">**Impact Moving Head Fully Formed** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

<span data-ttu-id="10940-925">**Полоса влияния** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-925">**Impact Band** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

<span data-ttu-id="10940-926">**Воздействие на другое** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-926">**Impact Other** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

<span data-ttu-id="10940-927">**Струйный акуеаус** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-927">**Inkjet Aqueous** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

<span data-ttu-id="10940-928">**Сплошная струйная** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-928">**Inkjet Solid** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

<span data-ttu-id="10940-929">**Струйная** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-929">**Inkjet Other** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

<span data-ttu-id="10940-930">**Перо** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-930">**Pen** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

<span data-ttu-id="10940-931">**Перенос тепла** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-931">**Thermal Transfer** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

<span data-ttu-id="10940-932">**С учетом температуры** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-932">**Thermal Sensitive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

<span data-ttu-id="10940-933">**Рассеяние тепла** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-933">**Thermal Diffusion** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

<span data-ttu-id="10940-934">**Прочая температура** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-934">**Thermal Other** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

<span data-ttu-id="10940-935">**Електроеросион** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-935">**Electroerosion** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

<span data-ttu-id="10940-936">**Статические** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-936">**Electrostatic** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

<span data-ttu-id="10940-937">**Фотограф микрофишей** (22)</span><span class="sxs-lookup"><span data-stu-id="10940-937">**Photographic Microfiche** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

<span data-ttu-id="10940-938">**Фотографический автомат** (23)</span><span class="sxs-lookup"><span data-stu-id="10940-938">**Photographic Imagesetter** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

<span data-ttu-id="10940-939">**Фотографическая другая** (24)</span><span class="sxs-lookup"><span data-stu-id="10940-939">**Photographic Other** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

<span data-ttu-id="10940-940">**Литий-спуск** (25)</span><span class="sxs-lookup"><span data-stu-id="10940-940">**Ion Deposition** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

<span data-ttu-id="10940-941">**ебеам** (26)</span><span class="sxs-lookup"><span data-stu-id="10940-941">**eBeam** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

<span data-ttu-id="10940-942">**Типесеттер** (27)</span><span class="sxs-lookup"><span data-stu-id="10940-942">**Typesetter** (27)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-943">**макскопиес**</span><span class="sxs-lookup"><span data-stu-id="10940-943">**MaxCopies**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-944">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-944">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-945">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-945">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-946">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. копий")</span><span class="sxs-lookup"><span data-stu-id="10940-946">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.Copies")</span></span>
</dt> </dl>

<span data-ttu-id="10940-947">Максимальное число копий, которое принтер может создать для одного задания.</span><span class="sxs-lookup"><span data-stu-id="10940-947">Maximum number of copies the printer can produce for one job.</span></span>

<span data-ttu-id="10940-948">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-948">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-949">**макснумберуп**</span><span class="sxs-lookup"><span data-stu-id="10940-949">**MaxNumberUp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-950">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-950">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-951">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-951">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-952">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. нумберуп")</span><span class="sxs-lookup"><span data-stu-id="10940-952">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NumberUp")</span></span>
</dt> </dl>

<span data-ttu-id="10940-953">Максимальное количество страниц на печать-поток, которые принтер может визуализировать на одном листе мультимедиа, например на бумаге.</span><span class="sxs-lookup"><span data-stu-id="10940-953">Maximum number of print-stream pages the printer can render on one media sheet, such as paper.</span></span>

<span data-ttu-id="10940-954">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-954">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-955">**макссизесуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-955">**MaxSizeSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-956">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-956">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-957">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-957">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-958">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. жобсизе"), [**Units**](../wmisdk/standard-qualifiers.md) ("килобайты")</span><span class="sxs-lookup"><span data-stu-id="10940-958">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.JobSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("kilobytes")</span></span>
</dt> </dl>

<span data-ttu-id="10940-959">Самое большое задание в виде потока байтов (в килобайтах), которое может принимать принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-959">Largest job as a byte stream, in kilobytes, that the printer can accept.</span></span> <span data-ttu-id="10940-960">Значение 0 (ноль) указывает, что ограничение не задано.</span><span class="sxs-lookup"><span data-stu-id="10940-960">A value of 0 (zero) indicates that no limit is set.</span></span>

<span data-ttu-id="10940-961">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-961">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-962">**миметипессуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-962">**MimeTypesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-963">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-963">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-964">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-964">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-965">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**CIM- \_ принтер**](cim-printer.md)". Лангуажессуппортед "," CIM \_ PrintJob. миметипес "," CIM \_ Принтсервице. миметипессуппортед ")</span><span class="sxs-lookup"><span data-stu-id="10940-965">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Printer**](cim-printer.md).LanguagesSupported", "CIM\_PrintJob.MimeTypes", "CIM\_PrintService.MimeTypesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="10940-966">Массив подробных пояснений к MIME-типу, поддерживаемых принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-966">Array of detailed MIME-type explanations that the printer supports.</span></span> <span data-ttu-id="10940-967">Если данные предоставлены, значение 47 ("MIME") должно быть включено в свойство **лангуажессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="10940-967">If data is provided, then the value 47 ("MIME") must be included in the **LanguagesSupported** property.</span></span>

<span data-ttu-id="10940-968">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-968">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-969">**Name**</span><span class="sxs-lookup"><span data-stu-id="10940-969">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-970">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-970">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-971">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-971">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-972">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="10940-972">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="10940-973">Имя принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-973">Name of the printer.</span></span>

<span data-ttu-id="10940-974">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10940-974">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-975">**натураллангуажессуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-975">**NaturalLanguagesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-976">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-976">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-977">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-977">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-978">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| Printer-MIB. пртлокализатионлангуаже "), [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) (" CIM \_ PrintJob. натураллангуаже ")</span><span class="sxs-lookup"><span data-stu-id="10940-978">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.NaturalLanguage")</span></span>
</dt> </dl>

<span data-ttu-id="10940-979">Массив языков, поддерживаемых для строк, используемых принтером для вывода управляющих данных.</span><span class="sxs-lookup"><span data-stu-id="10940-979">Array of languages supported for strings that the printer uses for output of management information.</span></span> <span data-ttu-id="10940-980">Должен соответствовать стандарту [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span><span class="sxs-lookup"><span data-stu-id="10940-980">Must conform to [RFC 1766](https://www.ietf.org/rfc/rfc1766.txt).</span></span> <span data-ttu-id="10940-981">Например, EN используется для английского языка.</span><span class="sxs-lookup"><span data-stu-id="10940-981">For example, "en" is used for English.</span></span>

<span data-ttu-id="10940-982">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-982">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-983">**Network**</span><span class="sxs-lookup"><span data-stu-id="10940-983">**Network**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-984">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-984">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-985">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-985">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-986">**Значение true** показывает, что принтер является сетевым принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-986">If **TRUE**, the printer is a network printer.</span></span> <span data-ttu-id="10940-987">Если для **локальных** и **сетевых** свойств задано **значение true**, то принтер является сетевым принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-987">If both the **Local** and **Network** properties are set to **TRUE**, then the printer is a network printer.</span></span>

</dd> <dt>

<span data-ttu-id="10940-988">**паперсизессуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-988">**PaperSizesSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-989">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-989">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-990">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-990">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-991">Массив типов бумаги, поддерживаемых принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-991">Array of the paper types that the printer supports.</span></span>

<span data-ttu-id="10940-992">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-992">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-993"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-994"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

<span data-ttu-id="10940-995"><span id="A"></span><span id="a"></span>**A** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-995"><span id="A"></span><span id="a"></span>**A** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="10940-996"><span id="B"></span><span id="b"></span>**Б** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-996"><span id="B"></span><span id="b"></span>**B** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

<span data-ttu-id="10940-997"><span id="C"></span><span id="c"></span>**C** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-997"><span id="C"></span><span id="c"></span>**C** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

<span data-ttu-id="10940-998"><span id="D"></span><span id="d"></span>**D** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-998"><span id="D"></span><span id="d"></span>**D** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="10940-999"><span id="E"></span><span id="e"></span>**E** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-999"><span id="E"></span><span id="e"></span>**E** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

<span data-ttu-id="10940-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-1000"><span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>**Letter** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

<span data-ttu-id="10940-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span><span class="sxs-lookup"><span data-stu-id="10940-1001"><span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>**Legal** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

<span data-ttu-id="10940-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**Na-10x13-конверт** (9)</span><span class="sxs-lookup"><span data-stu-id="10940-1002"><span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>**NA-10x13-Envelope** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

<span data-ttu-id="10940-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**Конверт Na-9x12** (10)</span><span class="sxs-lookup"><span data-stu-id="10940-1003"><span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>**NA-9x12-Envelope** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

<span data-ttu-id="10940-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**Na-Number-10-конверт** (11)</span><span class="sxs-lookup"><span data-stu-id="10940-1004"><span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>**NA-Number-10-Envelope** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

<span data-ttu-id="10940-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**Конверт Na-7x9** (12)</span><span class="sxs-lookup"><span data-stu-id="10940-1005"><span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>**NA-7x9-Envelope** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

<span data-ttu-id="10940-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**Конверт Na-9x11** (13)</span><span class="sxs-lookup"><span data-stu-id="10940-1006"><span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>**NA-9x11-Envelope** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

<span data-ttu-id="10940-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**Конверт Na-10x14** (14)</span><span class="sxs-lookup"><span data-stu-id="10940-1007"><span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>**NA-10x14-Envelope** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

<span data-ttu-id="10940-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**Na-Number-9-конверт** (15)</span><span class="sxs-lookup"><span data-stu-id="10940-1008"><span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>**NA-Number-9-Envelope** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

<span data-ttu-id="10940-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**Na-6x9-конверт** (16)</span><span class="sxs-lookup"><span data-stu-id="10940-1009"><span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>**NA-6x9-Envelope** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

<span data-ttu-id="10940-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**Конверт Na-10x15** (17)</span><span class="sxs-lookup"><span data-stu-id="10940-1010"><span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>**NA-10x15-Envelope** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

<span data-ttu-id="10940-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span><span class="sxs-lookup"><span data-stu-id="10940-1011"><span id="A0"></span><span id="a0"></span>**A0** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

<span data-ttu-id="10940-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span><span class="sxs-lookup"><span data-stu-id="10940-1012"><span id="A1"></span><span id="a1"></span>**A1** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

<span data-ttu-id="10940-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span><span class="sxs-lookup"><span data-stu-id="10940-1013"><span id="A2"></span><span id="a2"></span>**A2** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

<span data-ttu-id="10940-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span><span class="sxs-lookup"><span data-stu-id="10940-1014"><span id="A3"></span><span id="a3"></span>**A3** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

<span data-ttu-id="10940-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span><span class="sxs-lookup"><span data-stu-id="10940-1015"><span id="A4"></span><span id="a4"></span>**A4** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

<span data-ttu-id="10940-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span><span class="sxs-lookup"><span data-stu-id="10940-1016"><span id="A5"></span><span id="a5"></span>**A5** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

<span data-ttu-id="10940-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span><span class="sxs-lookup"><span data-stu-id="10940-1017"><span id="A6"></span><span id="a6"></span>**A6** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

<span data-ttu-id="10940-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span><span class="sxs-lookup"><span data-stu-id="10940-1018"><span id="A7"></span><span id="a7"></span>**A7** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

<span data-ttu-id="10940-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span><span class="sxs-lookup"><span data-stu-id="10940-1019"><span id="A8"></span><span id="a8"></span>**A8** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

<span data-ttu-id="10940-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span><span class="sxs-lookup"><span data-stu-id="10940-1020"><span id="A9A10"></span><span id="a9a10"></span>**A9A10** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

<span data-ttu-id="10940-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span><span class="sxs-lookup"><span data-stu-id="10940-1021"><span id="B0"></span><span id="b0"></span>**B0** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

<span data-ttu-id="10940-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span><span class="sxs-lookup"><span data-stu-id="10940-1022"><span id="B1"></span><span id="b1"></span>**B1** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

<span data-ttu-id="10940-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span><span class="sxs-lookup"><span data-stu-id="10940-1023"><span id="B2"></span><span id="b2"></span>**B2** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

<span data-ttu-id="10940-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span><span class="sxs-lookup"><span data-stu-id="10940-1024"><span id="B3"></span><span id="b3"></span>**B3** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

<span data-ttu-id="10940-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span><span class="sxs-lookup"><span data-stu-id="10940-1025"><span id="B4"></span><span id="b4"></span>**B4** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

<span data-ttu-id="10940-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span><span class="sxs-lookup"><span data-stu-id="10940-1026"><span id="B5"></span><span id="b5"></span>**B5** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

<span data-ttu-id="10940-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span><span class="sxs-lookup"><span data-stu-id="10940-1027"><span id="B6"></span><span id="b6"></span>**B6** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

<span data-ttu-id="10940-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span><span class="sxs-lookup"><span data-stu-id="10940-1028"><span id="B7"></span><span id="b7"></span>**B7** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

<span data-ttu-id="10940-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span><span class="sxs-lookup"><span data-stu-id="10940-1029"><span id="B8"></span><span id="b8"></span>**B8** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

<span data-ttu-id="10940-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span><span class="sxs-lookup"><span data-stu-id="10940-1030"><span id="B9"></span><span id="b9"></span>**B9** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

<span data-ttu-id="10940-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span><span class="sxs-lookup"><span data-stu-id="10940-1031"><span id="B10"></span><span id="b10"></span>**B10** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

<span data-ttu-id="10940-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span><span class="sxs-lookup"><span data-stu-id="10940-1032"><span id="C0"></span><span id="c0"></span>**C0** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

<span data-ttu-id="10940-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span><span class="sxs-lookup"><span data-stu-id="10940-1033"><span id="C1"></span><span id="c1"></span>**C1** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

<span data-ttu-id="10940-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span><span class="sxs-lookup"><span data-stu-id="10940-1034"><span id="C2C3"></span><span id="c2c3"></span>**C2C3** (41)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1035">C2</span><span class="sxs-lookup"><span data-stu-id="10940-1035">C2</span></span>

</dd> <dt>

<span id="C4"></span><span id="c4"></span>

<span data-ttu-id="10940-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span><span class="sxs-lookup"><span data-stu-id="10940-1036"><span id="C4"></span><span id="c4"></span>**C4** (42)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1037">C3</span><span class="sxs-lookup"><span data-stu-id="10940-1037">C3</span></span>

</dd> <dt>

<span id="C5"></span><span id="c5"></span>

<span data-ttu-id="10940-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span><span class="sxs-lookup"><span data-stu-id="10940-1038"><span id="C5"></span><span id="c5"></span>**C5** (43)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1039">C4</span><span class="sxs-lookup"><span data-stu-id="10940-1039">C4</span></span>

</dd> <dt>

<span id="C6"></span><span id="c6"></span>

<span data-ttu-id="10940-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span><span class="sxs-lookup"><span data-stu-id="10940-1040"><span id="C6"></span><span id="c6"></span>**C6** (44)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1041">C5</span><span class="sxs-lookup"><span data-stu-id="10940-1041">C5</span></span>

</dd> <dt>

<span id="C7"></span><span id="c7"></span>

<span data-ttu-id="10940-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span><span class="sxs-lookup"><span data-stu-id="10940-1042"><span id="C7"></span><span id="c7"></span>**C7** (45)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1043">C6</span><span class="sxs-lookup"><span data-stu-id="10940-1043">C6</span></span>

</dd> <dt>

<span id="C8"></span><span id="c8"></span>

<span data-ttu-id="10940-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span><span class="sxs-lookup"><span data-stu-id="10940-1044"><span id="C8"></span><span id="c8"></span>**C8** (46)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1045">C7</span><span class="sxs-lookup"><span data-stu-id="10940-1045">C7</span></span>

</dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

<span data-ttu-id="10940-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**Назначенный ISO** (47)</span><span class="sxs-lookup"><span data-stu-id="10940-1046"><span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>**ISO-Designated** (47)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1047">C8</span><span class="sxs-lookup"><span data-stu-id="10940-1047">C8</span></span>

</dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

<span data-ttu-id="10940-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span><span class="sxs-lookup"><span data-stu-id="10940-1048"><span id="JIS_B0"></span><span id="jis_b0"></span>**JIS B0** (48)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1049">ISO-Designated</span><span class="sxs-lookup"><span data-stu-id="10940-1049">ISO-Designated</span></span>

</dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

<span data-ttu-id="10940-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span><span class="sxs-lookup"><span data-stu-id="10940-1050"><span id="JIS_B1"></span><span id="jis_b1"></span>**JIS B1** (49)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1051">JIS B0</span><span class="sxs-lookup"><span data-stu-id="10940-1051">JIS B0</span></span>

</dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

<span data-ttu-id="10940-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span><span class="sxs-lookup"><span data-stu-id="10940-1052"><span id="JIS_B2"></span><span id="jis_b2"></span>**JIS B2** (50)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1053">JIS B1</span><span class="sxs-lookup"><span data-stu-id="10940-1053">JIS B1</span></span>

</dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

<span data-ttu-id="10940-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span><span class="sxs-lookup"><span data-stu-id="10940-1054"><span id="JIS_B3"></span><span id="jis_b3"></span>**JIS B3** (51)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1055">JIS B2</span><span class="sxs-lookup"><span data-stu-id="10940-1055">JIS B2</span></span>

</dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

<span data-ttu-id="10940-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span><span class="sxs-lookup"><span data-stu-id="10940-1056"><span id="JIS_B4"></span><span id="jis_b4"></span>**JIS B4** (52)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1057">JIS B3</span><span class="sxs-lookup"><span data-stu-id="10940-1057">JIS B3</span></span>

</dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

<span data-ttu-id="10940-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span><span class="sxs-lookup"><span data-stu-id="10940-1058"><span id="JIS_B5"></span><span id="jis_b5"></span>**JIS B5** (53)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1059">JIS B4</span><span class="sxs-lookup"><span data-stu-id="10940-1059">JIS B4</span></span>

</dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

<span data-ttu-id="10940-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span><span class="sxs-lookup"><span data-stu-id="10940-1060"><span id="JIS_B6"></span><span id="jis_b6"></span>**JIS B6** (54)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1061">JIS B5</span><span class="sxs-lookup"><span data-stu-id="10940-1061">JIS B5</span></span>

</dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

<span data-ttu-id="10940-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span><span class="sxs-lookup"><span data-stu-id="10940-1062"><span id="JIS_B7"></span><span id="jis_b7"></span>**JIS B7** (55)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1063">JIS B6</span><span class="sxs-lookup"><span data-stu-id="10940-1063">JIS B6</span></span>

</dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

<span data-ttu-id="10940-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span><span class="sxs-lookup"><span data-stu-id="10940-1064"><span id="JIS_B8"></span><span id="jis_b8"></span>**JIS B8** (56)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1065">JIS B7</span><span class="sxs-lookup"><span data-stu-id="10940-1065">JIS B7</span></span>

</dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

<span data-ttu-id="10940-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span><span class="sxs-lookup"><span data-stu-id="10940-1066"><span id="JIS_B9"></span><span id="jis_b9"></span>**JIS B9** (57)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1067">JIS B8</span><span class="sxs-lookup"><span data-stu-id="10940-1067">JIS B8</span></span>

</dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

<span data-ttu-id="10940-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span><span class="sxs-lookup"><span data-stu-id="10940-1068"><span id="JIS_B10"></span><span id="jis_b10"></span>**JIS B10** (58)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1069">JIS B9</span><span class="sxs-lookup"><span data-stu-id="10940-1069">JIS B9</span></span>

</dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

<span data-ttu-id="10940-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**Na-Letter** (59)</span><span class="sxs-lookup"><span data-stu-id="10940-1070"><span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>**NA-Letter** (59)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1071">JIS B10</span><span class="sxs-lookup"><span data-stu-id="10940-1071">JIS B10</span></span>

</dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

<span data-ttu-id="10940-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**Na-Legal** (60)</span><span class="sxs-lookup"><span data-stu-id="10940-1072"><span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>**NA-Legal** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

<span data-ttu-id="10940-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**Конверт B4** (61)</span><span class="sxs-lookup"><span data-stu-id="10940-1073"><span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>**B4-Envelope** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

<span data-ttu-id="10940-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**Конверт B5** (62)</span><span class="sxs-lookup"><span data-stu-id="10940-1074"><span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>**B5-Envelope** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

<span data-ttu-id="10940-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**Конверт C3** (63)</span><span class="sxs-lookup"><span data-stu-id="10940-1075"><span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>**C3-Envelope** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

<span data-ttu-id="10940-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**Конверт C4** (64)</span><span class="sxs-lookup"><span data-stu-id="10940-1076"><span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>**C4-Envelope** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

<span data-ttu-id="10940-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**Конверт C5** (65)</span><span class="sxs-lookup"><span data-stu-id="10940-1077"><span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>**C5-Envelope** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

<span data-ttu-id="10940-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**Конверт C6** (66)</span><span class="sxs-lookup"><span data-stu-id="10940-1078"><span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>**C6-Envelope** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

<span data-ttu-id="10940-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Назначено-Длинный конверт** (67)</span><span class="sxs-lookup"><span data-stu-id="10940-1079"><span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>**Designated-Long-Envelope** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

<span data-ttu-id="10940-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Конверт монарх** (68)</span><span class="sxs-lookup"><span data-stu-id="10940-1080"><span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>**Monarch-Envelope** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span data-ttu-id="10940-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span><span class="sxs-lookup"><span data-stu-id="10940-1081"><span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executive** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

<span data-ttu-id="10940-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Фолио** (70)</span><span class="sxs-lookup"><span data-stu-id="10940-1082"><span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>**Folio** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

<span data-ttu-id="10940-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Счет** (71)</span><span class="sxs-lookup"><span data-stu-id="10940-1083"><span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>**Invoice** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

<span data-ttu-id="10940-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Главная книга** (72)</span><span class="sxs-lookup"><span data-stu-id="10940-1084"><span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>**Ledger** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

<span data-ttu-id="10940-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Куарто** (73)</span><span class="sxs-lookup"><span data-stu-id="10940-1085"><span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>**Quarto** (73)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1086">**папертипесаваилабле**</span><span class="sxs-lookup"><span data-stu-id="10940-1086">**PaperTypesAvailable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1087">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-1087">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-1088">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1088">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1089">Квалификаторы: [**arrayType**](../wmisdk/standard-qualifiers.md) ("индексированный"), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. рекуиредпапертипе", "CIM \_ Принтсервице. папертипесаваилабле"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Принтер IETF — MIB. пртинпутмедианаме ")</span><span class="sxs-lookup"><span data-stu-id="10940-1089">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.RequiredPaperType", "CIM\_PrintService.PaperTypesAvailable"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.prtInputMediaName")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1090">Массив типов бумаги, доступных на принтере в данный момент.</span><span class="sxs-lookup"><span data-stu-id="10940-1090">Array of paper types that are currently available on the printer.</span></span> <span data-ttu-id="10940-1091">Каждая строка должна быть выражена в формате, указанном в приложении для печати документов ISO/IEC 10175 (DPA), которое суммируется в приложении C из [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (версия-MIB принтера).</span><span class="sxs-lookup"><span data-stu-id="10940-1091">Each string must be expressed in the format specified by ISO/IEC 10175 Document Printing Application (DPA), which is summarized in Appendix C of [RFC 1759](https://www.ietf.org/rfc/rfc1759.txt) (Printer MIB).</span></span> <span data-ttu-id="10940-1092">Любой размер бумаги, определенный в этом свойстве, также должен присутствовать в свойстве **паперсизессуппортед** .</span><span class="sxs-lookup"><span data-stu-id="10940-1092">Any paper size identified in this property must also appear in the **PaperSizesSupported** property.</span></span>

<span data-ttu-id="10940-1093">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1093">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<span data-ttu-id="10940-1094">Пример: ISO-A4-цветной</span><span class="sxs-lookup"><span data-stu-id="10940-1094">Example: iso-a4-colored</span></span>

</dd> <dt>

<span data-ttu-id="10940-1095">**Параметры**</span><span class="sxs-lookup"><span data-stu-id="10940-1095">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1096">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1096">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1097">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1097">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1098">Необязательные параметры обработчика заданий печати.</span><span class="sxs-lookup"><span data-stu-id="10940-1098">Optional parameters for the print processor.</span></span>

<span data-ttu-id="10940-1099">Пример: "копии = 2"</span><span class="sxs-lookup"><span data-stu-id="10940-1099">Example: "Copies=2"</span></span>

</dd> <dt>

<span data-ttu-id="10940-1100">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="10940-1100">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1101">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1101">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1102">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1102">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1103">Квалификаторы: [**схема**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="10940-1103">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1104">Идентификатор устройства Windows самонастраивающийся логического устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-1104">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="10940-1105">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1105">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="10940-1106">Пример: \* PNP030b</span><span class="sxs-lookup"><span data-stu-id="10940-1106">Example: \*PNP030b</span></span>

</dd> <dt>

<span data-ttu-id="10940-1107">**портнаме**</span><span class="sxs-lookup"><span data-stu-id="10940-1107">**PortName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1108">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1108">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1109">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1109">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1110">Порт, используемый для передачи данных на принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-1110">Port that is used to transmit data to a printer.</span></span> <span data-ttu-id="10940-1111">Если принтер подключен к более чем одному порту, имена каждого порта разделяются запятыми.</span><span class="sxs-lookup"><span data-stu-id="10940-1111">If a printer is connected to more than one port, the names of each port are separated by commas.</span></span>

<span data-ttu-id="10940-1112">Пример: LPT1:, LPT2:, LPT3:</span><span class="sxs-lookup"><span data-stu-id="10940-1112">Example: LPT1:, LPT2:, LPT3:</span></span>

</dd> <dt>

<span data-ttu-id="10940-1113">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="10940-1113">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1114">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="10940-1114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-1115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-1116">Массив конкретных возможностей логического устройства, связанных с питанием.</span><span class="sxs-lookup"><span data-stu-id="10940-1116">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="10940-1117">Это свойство наследуется **от \_ CIM**-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1117">This property is inherited from **CIM\_LogicalDevice**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="10940-1118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="10940-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-1119"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10940-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-1120"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10940-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-1121"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1122">Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.</span><span class="sxs-lookup"><span data-stu-id="10940-1122">The power management features are currently enabled, but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="10940-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="10940-1123"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1124">Устройство может изменить свое состояние электропитания на основе использования или других критериев.</span><span class="sxs-lookup"><span data-stu-id="10940-1124">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="10940-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-1125"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1126">Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="10940-1126">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="10940-1127">Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован.</span><span class="sxs-lookup"><span data-stu-id="10940-1127">This method is found on the parent **CIM\_LogicalDevice** class and can be implemented.</span></span> <span data-ttu-id="10940-1128">Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1128">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="10940-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-1129"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1130">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).</span><span class="sxs-lookup"><span data-stu-id="10940-1130">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="10940-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-1131"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1132">Поддержка по времени Power-On</span><span class="sxs-lookup"><span data-stu-id="10940-1132">Timed Power-On Supported</span></span>

<span data-ttu-id="10940-1133">Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.</span><span class="sxs-lookup"><span data-stu-id="10940-1133">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1134">**поверманажементсуппортед**</span><span class="sxs-lookup"><span data-stu-id="10940-1134">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1135">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-1137">Если **значение равно true**, мощность устройства может быть управляемой, а это означает, что его можно перевести в режим приостановки.</span><span class="sxs-lookup"><span data-stu-id="10940-1137">If **TRUE**, the power of the device can be managed, which means that it can be put into suspend mode.</span></span> <span data-ttu-id="10940-1138">Свойство не указывает на то, что функции управления питанием включены, только что логическое устройство поддерживает управление питанием.</span><span class="sxs-lookup"><span data-stu-id="10940-1138">The property does not indicate that power management features are enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="10940-1139">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1139">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1140">**принтерпапернамес**</span><span class="sxs-lookup"><span data-stu-id="10940-1140">**PrinterPaperNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1141">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="10940-1141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="10940-1142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-1143">Массив размеров бумаги, поддерживаемый принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-1143">Array of paper sizes supported by the printer.</span></span> <span data-ttu-id="10940-1144">Указанные принтером имена используются для представления поддерживаемых размеров бумаги.</span><span class="sxs-lookup"><span data-stu-id="10940-1144">The printer-specified names are used to represent supported paper sizes.</span></span>

<span data-ttu-id="10940-1145">Пример: B5 (JIS)</span><span class="sxs-lookup"><span data-stu-id="10940-1145">Example: B5 (JIS)</span></span>

</dd> <dt>

<span data-ttu-id="10940-1146">**принтерстате**</span><span class="sxs-lookup"><span data-stu-id="10940-1146">**PrinterState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-1147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1149">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-1149">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-1150">Одно из возможных состояний, связанных с этим принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-1150">One of the possible states relating to this printer.</span></span> <span data-ttu-id="10940-1151">Это свойство устарело.</span><span class="sxs-lookup"><span data-stu-id="10940-1151">This property is obsolete.</span></span> <span data-ttu-id="10940-1152">Вместо этого свойства используйте **принтерстатус**.</span><span class="sxs-lookup"><span data-stu-id="10940-1152">In place of this property, use **PrinterStatus**.</span></span>

<dt>

<span data-ttu-id="10940-1153">0</span><span class="sxs-lookup"><span data-stu-id="10940-1153">0</span></span>
</dt> <dd>

<span data-ttu-id="10940-1154">Бездействие. Дополнительные сведения см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="10940-1154">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1155">1</span><span class="sxs-lookup"><span data-stu-id="10940-1155">1</span></span>
</dt> <dd>

<span data-ttu-id="10940-1156">Пауза</span><span class="sxs-lookup"><span data-stu-id="10940-1156">Paused</span></span>

</dd> <dt>

<span data-ttu-id="10940-1157">2</span><span class="sxs-lookup"><span data-stu-id="10940-1157">2</span></span>
</dt> <dd>

<span data-ttu-id="10940-1158">Ошибка</span><span class="sxs-lookup"><span data-stu-id="10940-1158">Error</span></span>

</dd> <dt>

<span data-ttu-id="10940-1159">3</span><span class="sxs-lookup"><span data-stu-id="10940-1159">3</span></span>
</dt> <dd>

<span data-ttu-id="10940-1160">Ожидание удаления</span><span class="sxs-lookup"><span data-stu-id="10940-1160">Pending Deletion</span></span>

</dd> <dt>

<span data-ttu-id="10940-1161">4</span><span class="sxs-lookup"><span data-stu-id="10940-1161">4</span></span>
</dt> <dd>

<span data-ttu-id="10940-1162">Застревание бумаги</span><span class="sxs-lookup"><span data-stu-id="10940-1162">Paper Jam</span></span>

</dd> <dt>

<span data-ttu-id="10940-1163">5</span><span class="sxs-lookup"><span data-stu-id="10940-1163">5</span></span>
</dt> <dd>

<span data-ttu-id="10940-1164">Выдача бумаги</span><span class="sxs-lookup"><span data-stu-id="10940-1164">Paper Out</span></span>

</dd> <dt>

<span data-ttu-id="10940-1165">6</span><span class="sxs-lookup"><span data-stu-id="10940-1165">6</span></span>
</dt> <dd>

<span data-ttu-id="10940-1166">Ручная подача</span><span class="sxs-lookup"><span data-stu-id="10940-1166">Manual Feed</span></span>

</dd> <dt>

<span data-ttu-id="10940-1167">7</span><span class="sxs-lookup"><span data-stu-id="10940-1167">7</span></span>
</dt> <dd>

<span data-ttu-id="10940-1168">Проблема с бумагой</span><span class="sxs-lookup"><span data-stu-id="10940-1168">Paper Problem</span></span>

</dd> <dt>

<span data-ttu-id="10940-1169">8</span><span class="sxs-lookup"><span data-stu-id="10940-1169">8</span></span>
</dt> <dd>

<span data-ttu-id="10940-1170">Автономная миграция</span><span class="sxs-lookup"><span data-stu-id="10940-1170">Offline</span></span>

</dd> <dt>

<span data-ttu-id="10940-1171">9</span><span class="sxs-lookup"><span data-stu-id="10940-1171">9</span></span>
</dt> <dd>

<span data-ttu-id="10940-1172">Ввод-вывод активен</span><span class="sxs-lookup"><span data-stu-id="10940-1172">I/O Active</span></span>

</dd> <dt>

<span data-ttu-id="10940-1173">10</span><span class="sxs-lookup"><span data-stu-id="10940-1173">10</span></span>
</dt> <dd>

<span data-ttu-id="10940-1174">Занято</span><span class="sxs-lookup"><span data-stu-id="10940-1174">Busy</span></span>

</dd> <dt>

<span data-ttu-id="10940-1175">11</span><span class="sxs-lookup"><span data-stu-id="10940-1175">11</span></span>
</dt> <dd>

<span data-ttu-id="10940-1176">Печать</span><span class="sxs-lookup"><span data-stu-id="10940-1176">Printing</span></span>

</dd> <dt>

<span data-ttu-id="10940-1177">12</span><span class="sxs-lookup"><span data-stu-id="10940-1177">12</span></span>
</dt> <dd>

<span data-ttu-id="10940-1178">выходной лоток полон,</span><span class="sxs-lookup"><span data-stu-id="10940-1178">Output Bin Full</span></span>

</dd> <dt>

<span data-ttu-id="10940-1179">13</span><span class="sxs-lookup"><span data-stu-id="10940-1179">13</span></span>
</dt> <dd>

<span data-ttu-id="10940-1180">Недоступно</span><span class="sxs-lookup"><span data-stu-id="10940-1180">Not Available</span></span>

</dd> <dt>

<span data-ttu-id="10940-1181">14</span><span class="sxs-lookup"><span data-stu-id="10940-1181">14</span></span>
</dt> <dd>

<span data-ttu-id="10940-1182">Ожидание</span><span class="sxs-lookup"><span data-stu-id="10940-1182">Waiting</span></span>

</dd> <dt>

<span data-ttu-id="10940-1183">15</span><span class="sxs-lookup"><span data-stu-id="10940-1183">15</span></span>
</dt> <dd>

<span data-ttu-id="10940-1184">Обработка</span><span class="sxs-lookup"><span data-stu-id="10940-1184">Processing</span></span>

</dd> <dt>

<span data-ttu-id="10940-1185">16</span><span class="sxs-lookup"><span data-stu-id="10940-1185">16</span></span>
</dt> <dd>

<span data-ttu-id="10940-1186">Инициализация</span><span class="sxs-lookup"><span data-stu-id="10940-1186">Initialization</span></span>

</dd> <dt>

<span data-ttu-id="10940-1187">17</span><span class="sxs-lookup"><span data-stu-id="10940-1187">17</span></span>
</dt> <dd>

<span data-ttu-id="10940-1188">Прогрев</span><span class="sxs-lookup"><span data-stu-id="10940-1188">Warming Up</span></span>

</dd> <dt>

<span data-ttu-id="10940-1189">18</span><span class="sxs-lookup"><span data-stu-id="10940-1189">18</span></span>
</dt> <dd>

<span data-ttu-id="10940-1190">Мало тонера</span><span class="sxs-lookup"><span data-stu-id="10940-1190">Toner Low</span></span>

</dd> <dt>

<span data-ttu-id="10940-1191">19</span><span class="sxs-lookup"><span data-stu-id="10940-1191">19</span></span>
</dt> <dd>

<span data-ttu-id="10940-1192">нет тонера,</span><span class="sxs-lookup"><span data-stu-id="10940-1192">No Toner</span></span>

</dd> <dt>

<span data-ttu-id="10940-1193">20</span><span class="sxs-lookup"><span data-stu-id="10940-1193">20</span></span>
</dt> <dd>

<span data-ttu-id="10940-1194">Страница беспечатана</span><span class="sxs-lookup"><span data-stu-id="10940-1194">Page Punt</span></span>

</dd> <dt>

<span data-ttu-id="10940-1195">21</span><span class="sxs-lookup"><span data-stu-id="10940-1195">21</span></span>
</dt> <dd>

<span data-ttu-id="10940-1196">Требуется вмешательство пользователя</span><span class="sxs-lookup"><span data-stu-id="10940-1196">User Intervention Required</span></span>

</dd> <dt>

<span data-ttu-id="10940-1197">22</span><span class="sxs-lookup"><span data-stu-id="10940-1197">22</span></span>
</dt> <dd>

<span data-ttu-id="10940-1198">Недостаточно памяти</span><span class="sxs-lookup"><span data-stu-id="10940-1198">Out of Memory</span></span>

</dd> <dt>

<span data-ttu-id="10940-1199">23</span><span class="sxs-lookup"><span data-stu-id="10940-1199">23</span></span>
</dt> <dd>

<span data-ttu-id="10940-1200">открыта дверца,</span><span class="sxs-lookup"><span data-stu-id="10940-1200">Door Open</span></span>

</dd> <dt>

<span data-ttu-id="10940-1201">24</span><span class="sxs-lookup"><span data-stu-id="10940-1201">24</span></span>
</dt> <dd>

<span data-ttu-id="10940-1202">Сервер \_ неизвестен</span><span class="sxs-lookup"><span data-stu-id="10940-1202">Server\_Unknown</span></span>

</dd> <dt>

<span data-ttu-id="10940-1203">25</span><span class="sxs-lookup"><span data-stu-id="10940-1203">25</span></span>
</dt> <dd>

<span data-ttu-id="10940-1204">Энергосбережение</span><span class="sxs-lookup"><span data-stu-id="10940-1204">Power Save</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1205">**принтерстатус**</span><span class="sxs-lookup"><span data-stu-id="10940-1205">**PrinterStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1206">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-1206">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1208">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Принтер IETF — MIB. хрпринтерстатус ")</span><span class="sxs-lookup"><span data-stu-id="10940-1208">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|Printer-MIB.hrPrinterStatus")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1209">Сведения о состоянии принтера, отличные от сведений, указанных в свойстве " **доступность** логического устройства".</span><span class="sxs-lookup"><span data-stu-id="10940-1209">Status information for a printer that is different from information specified in the logical device **Availability** property.</span></span>

<span data-ttu-id="10940-1210">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1210">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-1211"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-1212"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="10940-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Бездействие** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-1213"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (3)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1214">Бездействие. Дополнительные сведения см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="10940-1214">Idle - for more information, see the Remarks section below.</span></span>

</dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

<span data-ttu-id="10940-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Печать** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-1215"><span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>**Printing** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

<span data-ttu-id="10940-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Прогрев** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-1216"><span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>**Warmup** (5)</span></span>


</dt> <dd>

<span data-ttu-id="10940-1217">Прогрев</span><span class="sxs-lookup"><span data-stu-id="10940-1217">Warming Up</span></span>

</dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

<span data-ttu-id="10940-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Печать остановлена** (6)</span><span class="sxs-lookup"><span data-stu-id="10940-1218"><span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>**Stopped Printing** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="10940-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (7)</span><span class="sxs-lookup"><span data-stu-id="10940-1219"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1220">**принтжобдататипе**</span><span class="sxs-lookup"><span data-stu-id="10940-1220">**PrintJobDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1221">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1222">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1222">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1223">Тип данных задания печати, ожидающего устройства печати под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="10940-1223">Data type of a print job waiting for the Windows-based printing device.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1224">**принтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="10940-1224">**PrintProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1227">Имя диспетчера очереди печати, обрабатывающего задания печати.</span><span class="sxs-lookup"><span data-stu-id="10940-1227">Name of the print spooler that handles print jobs.</span></span>

<span data-ttu-id="10940-1228">Пример: SPOOLSS.DLL</span><span class="sxs-lookup"><span data-stu-id="10940-1228">Example: SPOOLSS.DLL</span></span>

</dd> <dt>

<span data-ttu-id="10940-1229">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="10940-1229">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1230">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-1230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1231">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1231">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1232">Приоритет принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-1232">Priority of the printer.</span></span> <span data-ttu-id="10940-1233">Задания на принтере с более высоким приоритетом планируются первыми.</span><span class="sxs-lookup"><span data-stu-id="10940-1233">Jobs on a higher priority printer are scheduled first.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1234">**Выпущен**</span><span class="sxs-lookup"><span data-stu-id="10940-1234">**Published**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1235">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1235">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1236">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1236">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1237">Если **значение — true**, принтер публикуется в службе сетевого каталога.</span><span class="sxs-lookup"><span data-stu-id="10940-1237">If **TRUE**, the printer is published in the network directory service.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1238">**Поставлено в очередь**</span><span class="sxs-lookup"><span data-stu-id="10940-1238">**Queued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1239">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1239">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1240">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1240">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1241">**Значение true** показывает, что принтеры помещаются в буфер и помещаются в очередь заданий печати.</span><span class="sxs-lookup"><span data-stu-id="10940-1241">If **TRUE**, the printer buffers and queues print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1242">**равонли**</span><span class="sxs-lookup"><span data-stu-id="10940-1242">**RawOnly**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1243">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1243">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1244">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1244">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1245">Если **значение — true**, принтер принимает только необработанные данные для постановки в очередь.</span><span class="sxs-lookup"><span data-stu-id="10940-1245">If **TRUE**, the printer accepts only raw data to be spooled.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1246">**сепараторфиле**</span><span class="sxs-lookup"><span data-stu-id="10940-1246">**SeparatorFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1247">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1247">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1248">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1248">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1249">Имя файла, используемого для создания страницы-разделителя.</span><span class="sxs-lookup"><span data-stu-id="10940-1249">Name of the file used to create a separator page.</span></span> <span data-ttu-id="10940-1250">Эта страница используется для разделения заданий печати, отправленных на принтер.</span><span class="sxs-lookup"><span data-stu-id="10940-1250">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1251">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="10940-1251">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1253">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-1254">Имя сервера, управляющего принтером.</span><span class="sxs-lookup"><span data-stu-id="10940-1254">Name of the server that controls the printer.</span></span> <span data-ttu-id="10940-1255">Если эта строка имеет **значение NULL**, управление принтером осуществляется локально.</span><span class="sxs-lookup"><span data-stu-id="10940-1255">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1256">**Общий**</span><span class="sxs-lookup"><span data-stu-id="10940-1256">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1257">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1257">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1258">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1258">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1259">Если **значение — true**, принтер доступен в качестве общего сетевого ресурса.</span><span class="sxs-lookup"><span data-stu-id="10940-1259">If **TRUE**, the printer is available as a shared network resource.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1260">**Сетев**</span><span class="sxs-lookup"><span data-stu-id="10940-1260">**ShareName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1261">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1262">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1262">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1263">Имя общего ресурса устройства печати на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="10940-1263">Share name of the Windows-based printing device.</span></span>

<span data-ttu-id="10940-1264">Пример: " \\ \\ PRINTSERVER1 \\ PRINTER2"</span><span class="sxs-lookup"><span data-stu-id="10940-1264">Example: "\\\\PRINTSERVER1\\PRINTER2"</span></span>

</dd> <dt>

<span data-ttu-id="10940-1265">**спуленаблед**</span><span class="sxs-lookup"><span data-stu-id="10940-1265">**SpoolEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1266">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1267">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1268">Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-1268">Qualifiers: [**Deprecated**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-1269">Это свойство устарело; не используйте.</span><span class="sxs-lookup"><span data-stu-id="10940-1269">This property is obsolete; do not use.</span></span> <span data-ttu-id="10940-1270">Если **значение — true**, буферизация включена для принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-1270">If **TRUE**, spooling is enabled for printer.</span></span>

</dd> <dt>

<span data-ttu-id="10940-1271">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="10940-1271">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1272">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10940-1272">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1273">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1273">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1274">Дата и время, когда принтер может начать печать задания, если принтер ограничен печатью в определенное время.</span><span class="sxs-lookup"><span data-stu-id="10940-1274">Date and time that a printer can start to print a job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="10940-1275">Это значение выражается как время, прошедшее с 12:00 AM по ГРИНВИЧу (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="10940-1275">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1276">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="10940-1276">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1277">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1278">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1279">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="10940-1279">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1280">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="10940-1280">Current status of the object.</span></span> <span data-ttu-id="10940-1281">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="10940-1281">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="10940-1282">Рабочие состояния включают: **ОК**, **снижение работоспособности** и пред- **Ошибка** (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозируется сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="10940-1282">Operational statuses include: **OK**, **Degraded**, and **Pred Fail** (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="10940-1283">Неработающие состояния включают: **Ошибка**, **Запуск**, **Остановка** и **обслуживание**.</span><span class="sxs-lookup"><span data-stu-id="10940-1283">Nonoperational statuses include: **Error**, **Starting**, **Stopping**, and **Service**.</span></span> <span data-ttu-id="10940-1284">Последнее, **Служба**, может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="10940-1284">The latter, **Service**, could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="10940-1285">Не вся такая работа находится в режиме «в сети», но управляемый элемент не является ни « **ОК** », ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="10940-1285">Not all such work is online, yet the managed element is neither **OK** nor in one of the other states.</span></span>

<span data-ttu-id="10940-1286">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1286">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="10940-1287">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="10940-1287">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="10940-1288">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="10940-1288">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="10940-1289">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="10940-1289">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="10940-1290">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="10940-1290">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-1291">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="10940-1291">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="10940-1292">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="10940-1292">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="10940-1293">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="10940-1293">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="10940-1294">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="10940-1294">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="10940-1295">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="10940-1295">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="10940-1296">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="10940-1296">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="10940-1297">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="10940-1297">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="10940-1298">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="10940-1298">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="10940-1299">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="10940-1299">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1300">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="10940-1300">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1301">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="10940-1301">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1302">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1302">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1303">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Рабочее состояние DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="10940-1303">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1304">Состояние логического устройства.</span><span class="sxs-lookup"><span data-stu-id="10940-1304">State of the logical device.</span></span> <span data-ttu-id="10940-1305">Если это свойство не применяется к логическому устройству, следует использовать значение 5 (**неприменимо**).</span><span class="sxs-lookup"><span data-stu-id="10940-1305">If this property does not apply to the logical device, the value 5 (**Not Applicable**) should be used.</span></span>

<span data-ttu-id="10940-1306">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1306">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="10940-1307">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="10940-1307">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="10940-1308">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="10940-1308">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="10940-1309">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="10940-1309">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="10940-1310">**Отключено** (4)</span><span class="sxs-lookup"><span data-stu-id="10940-1310">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="10940-1311">**Неприменимо** (5)</span><span class="sxs-lookup"><span data-stu-id="10940-1311">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="10940-1312">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="10940-1312">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1313">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1313">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1314">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1315">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-1315">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-1316">Значение свойства **CreationClassName** компьютера.</span><span class="sxs-lookup"><span data-stu-id="10940-1316">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="10940-1317">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1317">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1318">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="10940-1318">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1319">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="10940-1319">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1320">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1320">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1321">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="10940-1321">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="10940-1322">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="10940-1322">Name of the scoping system.</span></span>

<span data-ttu-id="10940-1323">Это свойство наследуется [**от \_ CIM**](cim-logicaldevice.md)-унаследованной модели.</span><span class="sxs-lookup"><span data-stu-id="10940-1323">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1324">**тимеофластресет**</span><span class="sxs-lookup"><span data-stu-id="10940-1324">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1325">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10940-1325">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1326">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1326">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="10940-1327">Дата и время последнего сброса принтера.</span><span class="sxs-lookup"><span data-stu-id="10940-1327">Date and time the printer was last reset.</span></span>

<span data-ttu-id="10940-1328">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1328">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1329">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="10940-1329">**UntilTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1330">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="10940-1330">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1331">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1331">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1332">Дата и время, когда принтер может напечатать Последнее задание — если принтер ограничен печатью в определенное время.</span><span class="sxs-lookup"><span data-stu-id="10940-1332">Date and time that a printer can print the last job—if the printer is limited to print at specific times.</span></span> <span data-ttu-id="10940-1333">Это значение выражается как время, прошедшее с 12:00 AM по ГРИНВИЧу (время по Гринвичу).</span><span class="sxs-lookup"><span data-stu-id="10940-1333">This value is expressed as the time elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1334">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="10940-1334">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1335">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10940-1335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1336">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="10940-1336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10940-1337">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("CIM \_ PrintJob. хоризонталресолутион"), [**Units**](../wmisdk/standard-qualifiers.md) ("пикселей на дюйм")</span><span class="sxs-lookup"><span data-stu-id="10940-1337">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("CIM\_PrintJob.HorizontalResolution"), [**Units**](../wmisdk/standard-qualifiers.md) ("pixels per inch")</span></span>
</dt> </dl>

<span data-ttu-id="10940-1338">Вертикальное разрешение принтера (в пикселях на дюйм).</span><span class="sxs-lookup"><span data-stu-id="10940-1338">Vertical resolution, in pixels-per-inch, of the printer.</span></span>

<span data-ttu-id="10940-1339">Это свойство наследуется [**от \_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1339">This property is inherited from [**CIM\_Printer**](cim-printer.md).</span></span>

</dd> <dt>

<span data-ttu-id="10940-1340">**воркоффлине**</span><span class="sxs-lookup"><span data-stu-id="10940-1340">**WorkOffline**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10940-1341">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="10940-1341">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="10940-1342">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="10940-1342">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="10940-1343">Если **значение — true**, можно поместить задания печати в очередь на компьютере, когда принтер находится в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="10940-1343">If **TRUE**, you can queue print jobs on the computer when the printer is offline.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10940-1344">Комментарии</span><span class="sxs-lookup"><span data-stu-id="10940-1344">Remarks</span></span>

<span data-ttu-id="10940-1345">Класс **\_ принтера Win32** является производным от [**\_ принтера CIM**](cim-printer.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1345">The **Win32\_Printer** class is derived from [**CIM\_Printer**](cim-printer.md).</span></span> <span data-ttu-id="10940-1346">Перед вызовом [**SWbemObject. \_**](../wmisdk/swbemobject-put-.md) WHERE или [**IWbemServices::P Утинстанце**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) для **экземпляра \_ принтера Win32** , необходимо включить привилегию **селоаддриверпривилеже** (**вбемпривилежелоаддривер** для Visual Basic и лоаддривер для моникеров скрипта).</span><span class="sxs-lookup"><span data-stu-id="10940-1346">Before calling [**SWbemObject.Put\_**](../wmisdk/swbemobject-put-.md) or [**IWbemServices::PutInstance**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstance) for a **Win32\_Printer** instance, the **SeLoadDriverPrivilege** privilege (**wbemPrivilegeLoadDriver** for Visual Basic and LoadDriver for scripting monikers) must be enabled.</span></span> <span data-ttu-id="10940-1347">Дополнительные сведения см. в статьях [**константы прав**](../wmisdk/privilege-constants.md) и [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="10940-1347">For more information, see [**Privilege Constants**](../wmisdk/privilege-constants.md) and [Executing Privileged Operations](../wmisdk/executing-privileged-operations.md).</span></span> <span data-ttu-id="10940-1348">В следующем примере кода VBScript показано, как включить привилегию **сетлоаддриверпривилеже** в скрипте.</span><span class="sxs-lookup"><span data-stu-id="10940-1348">The following VBScript code example shows how to enable the **SetLoadDriverPrivilege** privilege in script.</span></span>

<span data-ttu-id="10940-1349">Для работы с кластерами принтеров MSCS используйте prnadmin.dll сборку или другое платформа .NET Framework [System. Printing](/dotnet/api/system.printing) Namespace.</span><span class="sxs-lookup"><span data-stu-id="10940-1349">For working with MSCS Printer clusters, use the prnadmin.dll assembly, or else the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>


```VB
Set objPrinter = GetObject("winmgmts:{impersonationLevel=Impersonate,(LoadDriver)}!//./Root/CIMv2:Win32_Printer")
```



<span data-ttu-id="10940-1350">Для определения доступных принтеров Windows использует учетные данные пользователя, запустившего сценарий.</span><span class="sxs-lookup"><span data-stu-id="10940-1350">Windows uses the credentials of the user running the script to determine what the available printers are.</span></span> <span data-ttu-id="10940-1351">Таким образом, если сценарий выполняется удаленно, вы можете получить доступ только к принтеру, доступному для вашей учетной записи пользователя в этой удаленной системе.</span><span class="sxs-lookup"><span data-stu-id="10940-1351">Therefore, if you are running a script remotely, you may only be able to access any printer that is available to your user account on that remote system.</span></span>

<span data-ttu-id="10940-1352">Класс **\_ принтеров Win32** нельзя использовать для принтеров на кластере на печати MSCS.</span><span class="sxs-lookup"><span data-stu-id="10940-1352">You cannot use the **Win32\_Printer** class for printers on an MSCS print cluster.</span></span> <span data-ttu-id="10940-1353">Вместо этого может потребоваться использовать средство Принтерадмин (PrnAdmin.dll) или пространство имен платформа .NET Framework [System. Printing](/dotnet/api/system.printing) .</span><span class="sxs-lookup"><span data-stu-id="10940-1353">Instead, you may need to use either the PrinterAdmin tool (PrnAdmin.dll) or the .NET Framework [System.Printing](/dotnet/api/system.printing) namespace.</span></span>

> [!Note]  
> <span data-ttu-id="10940-1354">При извлечении **принтерстатус** = 3 или **принтерстате** = 0 драйвер принтера не может подавать точную информацию в WMI.</span><span class="sxs-lookup"><span data-stu-id="10940-1354">If you are retrieving **PrinterStatus** = 3 or **PrinterState** = 0, the printer driver may not be feeding accurate information into WMI.</span></span> <span data-ttu-id="10940-1355">Инструментарий WMI извлекает сведения о принтерах из spoolsv.exe процесса.</span><span class="sxs-lookup"><span data-stu-id="10940-1355">WMI retrieves the printer information from the spoolsv.exe process.</span></span> <span data-ttu-id="10940-1356">Возможно, драйвер принтера не сообщает о своем состоянии диспетчеру очереди печати.</span><span class="sxs-lookup"><span data-stu-id="10940-1356">It is possible the printer driver does not report its status to the spooler.</span></span> <span data-ttu-id="10940-1357">В этом случае принтер **Win32 \_** сообщает принтеру о **состоянии простоя**.</span><span class="sxs-lookup"><span data-stu-id="10940-1357">In this case, **Win32\_Printer** reports the printer as **Idle**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="10940-1358">Примеры</span><span class="sxs-lookup"><span data-stu-id="10940-1358">Examples</span></span>

<span data-ttu-id="10940-1359">С [помощью примера Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell в коллекции TechNet для взаимодействия с моделью автоматизации Visio для создания рисунка Visio используется **\_ принтер Win32** .</span><span class="sxs-lookup"><span data-stu-id="10940-1359">The [PS Create a Computer Configuration Drawing using Visio](https://Gallery.TechNet.Microsoft.Com/84e2c31a-e644-4f79-83cd-e2b1a0ef8557) PowerShell sample on TechNet Gallery uses **Win32\_Printer** to interact with Visio automation model to create a Visio drawing.</span></span>

<span data-ttu-id="10940-1360">Для получения сведений об удаленном компьютере в [сценарии PowerShell для удаленного](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) компьютера используется ряд классов, включая **\_ принтер Win32**.</span><span class="sxs-lookup"><span data-stu-id="10940-1360">The [Powershell Remote PC Info Script](https://Gallery.TechNet.Microsoft.Com/2a8a008c-ee30-4b50-a81a-1b7545ef3436) uses a number of classes, including **Win32\_Printer**, to retrieve information about a remote computer.</span></span>

<span data-ttu-id="10940-1361">В следующем образце кода PowerShell показано, как определить принтер по умолчанию для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="10940-1361">The following PowerShell code sample shows how to determine the default printer of the local computer.</span></span>


```PowerShell
Get-WmiObject win32_printer | %{if ($_.default) {$_}}
```



<span data-ttu-id="10940-1362">Следующий пример кода VBScript описывает, как получить статистику принтера из экземпляров **\_ принтера Win32**.</span><span class="sxs-lookup"><span data-stu-id="10940-1362">The following VBScript code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```VB
Set PrinterSet = GetObject("winmgmts:").InstancesOf ("Win32_Printer")
If (PrinterSet.Count = 0 ) Then WScript.Echo "No Printers Installed!"
for each Printer in PrinterSet
   if Printer.PrinterStatus = 3 then WScript.Echo Printer.Name & Chr(13) & "Status:  Idle"
   if Printer.PrinterStatus = 4 then WScript.Echo Printer.Name & Chr(13) & "Status:  Printing"
   
next
```



<span data-ttu-id="10940-1363">В следующем образце кода Perl описывается получение статистики принтера из экземпляров **\_ принтера Win32**.</span><span class="sxs-lookup"><span data-stu-id="10940-1363">The following Perl code sample describes how to retrieve printer stats from instances of **Win32\_Printer**.</span></span>


```
use strict;
use Win32::OLE;

my $PrinterSet;

eval { $PrinterSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf ("Win32_Printer"); };
unless($@)
{
   if ($PrinterSet->{Count} == 0) 
   {
      print "No Printers Installed!\n";
   }

   foreach my $PrinterInst (in $PrinterSet)
   {
      if ($PrinterInst->{PrinterStatus} == 3) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Idle\n";
      }
      if ($PrinterInst->{PrinterStatus} == 4) 
      {
         print "\n$PrinterInst->{Name}\nStatus:  Printing\n";
      }
   }
}
else
{
   print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="10940-1364">В следующем примере кода VBScript показано, как получить имя принтера по умолчанию для компьютера.</span><span class="sxs-lookup"><span data-stu-id="10940-1364">The following VBScript code example shows how to obtain the name of the default printer for a computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( "winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colInstalledPrinters =  objWMIService.ExecQuery ("Select * from Win32_Printer")
For Each objPrinter in colInstalledPrinters

    If objPrinter.Default = "True" Then 
      Wscript.Echo "Name: " & objPrinter.Name
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="10940-1365">Требования</span><span class="sxs-lookup"><span data-stu-id="10940-1365">Requirements</span></span>



| <span data-ttu-id="10940-1366">Требование</span><span class="sxs-lookup"><span data-stu-id="10940-1366">Requirement</span></span> | <span data-ttu-id="10940-1367">Значение</span><span class="sxs-lookup"><span data-stu-id="10940-1367">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10940-1368">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="10940-1368">Minimum supported client</span></span><br/> | <span data-ttu-id="10940-1369">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10940-1369">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="10940-1370">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="10940-1370">Minimum supported server</span></span><br/> | <span data-ttu-id="10940-1371">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10940-1371">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="10940-1372">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="10940-1372">Namespace</span></span><br/>                | <span data-ttu-id="10940-1373">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10940-1373">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="10940-1374">MOF</span><span class="sxs-lookup"><span data-stu-id="10940-1374">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10940-1375"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10940-1375"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="10940-1376">DLL</span><span class="sxs-lookup"><span data-stu-id="10940-1376">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10940-1377"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10940-1377"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="10940-1378">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="10940-1378">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10940-1379">**\_Принтер CIM**</span><span class="sxs-lookup"><span data-stu-id="10940-1379">**CIM\_Printer**</span></span>](cim-printer.md)
</dt> <dt>

[<span data-ttu-id="10940-1380">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="10940-1380">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="10940-1381">Задачи WMI: принтеры и печать</span><span class="sxs-lookup"><span data-stu-id="10940-1381">WMI Tasks: Printers and Printing</span></span>](../wmisdk/wmi-tasks--printers-and-printing.md)
</dt> </dl>

 

 
