---
description: '\_Класс WMI принтердривер для Win32 представляет драйверы для \_ экземпляра принтера Win32.'
ms.assetid: baf48bbf-60a3-4d9b-93b7-c1b22518a9c1
ms.tgt_platform: multiple
title: Класс Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver
- Win32_PrinterDriver.Caption
- Win32_PrinterDriver.ConfigFile
- Win32_PrinterDriver.CreationClassName
- Win32_PrinterDriver.DataFile
- Win32_PrinterDriver.DefaultDataType
- Win32_PrinterDriver.DependentFiles
- Win32_PrinterDriver.Description
- Win32_PrinterDriver.DriverPath
- Win32_PrinterDriver.FilePath
- Win32_PrinterDriver.HelpFile
- Win32_PrinterDriver.InfName
- Win32_PrinterDriver.InstallDate
- Win32_PrinterDriver.MonitorName
- Win32_PrinterDriver.Name
- Win32_PrinterDriver.OEMUrl
- Win32_PrinterDriver.Started
- Win32_PrinterDriver.StartMode
- Win32_PrinterDriver.Status
- Win32_PrinterDriver.SupportedPlatform
- Win32_PrinterDriver.SystemCreationClassName
- Win32_PrinterDriver.SystemName
- Win32_PrinterDriver.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 615d6561e12f67edee34e0de84dade12f250e0f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895941"
---
# <a name="win32_printerdriver-class"></a><span data-ttu-id="658df-103">\_Класс Win32 принтердривер</span><span class="sxs-lookup"><span data-stu-id="658df-103">Win32\_PrinterDriver class</span></span>

<span data-ttu-id="658df-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ принтердривер для Win32** представляет драйверы для экземпляра [**\_ принтера Win32**](win32-printer.md) .</span><span class="sxs-lookup"><span data-stu-id="658df-104">The **Win32\_PrinterDriver** [WMI class](../wmisdk/retrieving-a-class.md) represents the drivers for a [**Win32\_Printer**](win32-printer.md) instance.</span></span>

<span data-ttu-id="658df-105">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все наследуемые свойства, но исключает методы.</span><span class="sxs-lookup"><span data-stu-id="658df-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties, but excludes methods.</span></span> <span data-ttu-id="658df-106">Справочные сведения о методах см. в таблице методов в этой статье.</span><span class="sxs-lookup"><span data-stu-id="658df-106">For reference information about methods, see the table of methods in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="658df-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="658df-107">Syntax</span></span>

``` syntax
class Win32_PrinterDriver : CIM_Service
{
  string   Caption;
  string   ConfigFile;
  string   CreationClassName;
  string   DataFile;
  string   DefaultDataType;
  string   DependentFiles[];
  string   Description;
  string   DriverPath;
  string   FilePath;
  string   HelpFile;
  string   InfName;
  datetime InstallDate;
  string   MonitorName;
  string   Name;
  string   OEMUrl;
  boolean  Started;
  string   StartMode;
  string   Status;
  string   SupportedPlatform;
  string   SystemCreationClassName;
  string   SystemName;
  uint16   Version;
};
```

## <a name="members"></a><span data-ttu-id="658df-108">Члены</span><span class="sxs-lookup"><span data-stu-id="658df-108">Members</span></span>

<span data-ttu-id="658df-109">Класс **Win32 \_ принтердривер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="658df-109">The **Win32\_PrinterDriver** class has these types of members:</span></span>

-   [<span data-ttu-id="658df-110">Методы</span><span class="sxs-lookup"><span data-stu-id="658df-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="658df-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="658df-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="658df-112">Методы</span><span class="sxs-lookup"><span data-stu-id="658df-112">Methods</span></span>

<span data-ttu-id="658df-113">Класс **Win32 \_ принтердривер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="658df-113">The **Win32\_PrinterDriver** class has these methods.</span></span>



| <span data-ttu-id="658df-114">Метод</span><span class="sxs-lookup"><span data-stu-id="658df-114">Method</span></span>                                                                           | <span data-ttu-id="658df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="658df-115">Description</span></span>                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="658df-116">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="658df-116">**AddPrinterDriver**</span></span>](addprinterdriver-method-in-class-win32-printerdriver.md) | <span data-ttu-id="658df-117">Создает новый драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-117">Creates a new printer driver.</span></span><br/> |
| [<span data-ttu-id="658df-118">**StartService**</span><span class="sxs-lookup"><span data-stu-id="658df-118">**StartService**</span></span>](startservice-method-in-class-win32-printerdriver.md)         | <span data-ttu-id="658df-119">Запускает службу печати.</span><span class="sxs-lookup"><span data-stu-id="658df-119">Starts print service.</span></span><br/>         |
| [<span data-ttu-id="658df-120">**StopService**</span><span class="sxs-lookup"><span data-stu-id="658df-120">**StopService**</span></span>](stopservice-method-in-class-win32-printerdriver.md)           | <span data-ttu-id="658df-121">Останавливает службу печати.</span><span class="sxs-lookup"><span data-stu-id="658df-121">Stops print service.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="658df-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="658df-122">Properties</span></span>

<span data-ttu-id="658df-123">Класс **Win32 \_ принтердривер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="658df-123">The **Win32\_PrinterDriver** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="658df-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="658df-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-127">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="658df-127">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="658df-128">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="658df-128">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="658df-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="658df-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-130">**ConfigFile**</span><span class="sxs-lookup"><span data-stu-id="658df-130">**ConfigFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-133">Файл конфигурации для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-133">Configuration file for this printer driver.</span></span>

<span data-ttu-id="658df-134">Пример: "pscrptui.dll"</span><span class="sxs-lookup"><span data-stu-id="658df-134">Example: "pscrptui.dll"</span></span>

</dd> <dt>

<span data-ttu-id="658df-135">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="658df-135">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-138">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")</span><span class="sxs-lookup"><span data-stu-id="658df-138">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="658df-139">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="658df-139">Name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="658df-140">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="658df-140">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="658df-141">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="658df-141">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-142">**DataFile**</span><span class="sxs-lookup"><span data-stu-id="658df-142">**DataFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-145">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) (CIM \_ File. filename)</span><span class="sxs-lookup"><span data-stu-id="658df-145">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.FileName)</span></span>
</dt> </dl>

<span data-ttu-id="658df-146">Файл данных для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-146">Data file for this printer driver.</span></span>

<span data-ttu-id="658df-147">Пример: "qms810. PPD"</span><span class="sxs-lookup"><span data-stu-id="658df-147">Example: "qms810.ppd"</span></span>

</dd> <dt>

<span data-ttu-id="658df-148">**дефаултдататипе**</span><span class="sxs-lookup"><span data-stu-id="658df-148">**DefaultDataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-151">Тип данных по умолчанию для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-151">Default data type for this printer driver.</span></span>

<span data-ttu-id="658df-152">Пример: "EMF"</span><span class="sxs-lookup"><span data-stu-id="658df-152">Example: "EMF"</span></span>

</dd> <dt>

<span data-ttu-id="658df-153">**депендентфилес**</span><span class="sxs-lookup"><span data-stu-id="658df-153">**DependentFiles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-154">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="658df-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="658df-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-156">Массив зависимых файлов для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-156">Array of dependent files for this printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="658df-157">**Описание**</span><span class="sxs-lookup"><span data-stu-id="658df-157">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-160">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="658df-160">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="658df-161">Комментарий, описывающий ссылку.</span><span class="sxs-lookup"><span data-stu-id="658df-161">Comment that describes the link.</span></span>

<span data-ttu-id="658df-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="658df-162">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-163">**DriverPath**</span><span class="sxs-lookup"><span data-stu-id="658df-163">**DriverPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-164">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-166">Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) (CIM- \_ файл. путь)</span><span class="sxs-lookup"><span data-stu-id="658df-166">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) (CIM\_DataFile.Path)</span></span>
</dt> </dl>

<span data-ttu-id="658df-167">Путь для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-167">Path for this printer driver.</span></span>

<span data-ttu-id="658df-168">Пример: "C: \\ \\ drivers \\ \\pscript.dll"</span><span class="sxs-lookup"><span data-stu-id="658df-168">Example: "C:\\\\drivers\\\\pscript.dll"</span></span>

</dd> <dt>

<span data-ttu-id="658df-169">**Равно**</span><span class="sxs-lookup"><span data-stu-id="658df-169">**FilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-170">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="658df-171">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="658df-172">Путь к используемому INF-файлу.</span><span class="sxs-lookup"><span data-stu-id="658df-172">Path to the INF file being used.</span></span>

<span data-ttu-id="658df-173">Пример: "c: \\ \\ temp \\ \\ Driver"</span><span class="sxs-lookup"><span data-stu-id="658df-173">Example: "c:\\\\temp\\\\driver"</span></span>

</dd> <dt>

<span data-ttu-id="658df-174">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="658df-174">**HelpFile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-177">Файл справки для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-177">Help file for this printer driver.</span></span>

<span data-ttu-id="658df-178">Пример: "пскрптуи. hlp"</span><span class="sxs-lookup"><span data-stu-id="658df-178">Example: "pscrptui.hlp"</span></span>

</dd> <dt>

<span data-ttu-id="658df-179">**инфнаме**</span><span class="sxs-lookup"><span data-stu-id="658df-179">**InfName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-180">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="658df-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="658df-182">Имя используемого INF-файла.</span><span class="sxs-lookup"><span data-stu-id="658df-182">Name of the INF file being used.</span></span> <span data-ttu-id="658df-183">По умолчанию используется указанный в операционной системе INF-файл принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-183">The default is to use an operating system provided printer INF file.</span></span> <span data-ttu-id="658df-184">Если драйвер предоставляется непосредственно изготовителем принтера, а не операционной системой, используется другое имя файла.</span><span class="sxs-lookup"><span data-stu-id="658df-184">A different file name is used if the driver is provided directly by the manufacturer of the printer and not the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="658df-185">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="658df-185">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-186">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="658df-186">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="658df-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-188">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="658df-188">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="658df-189">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="658df-189">Date and time the object is installed.</span></span> <span data-ttu-id="658df-190">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="658df-190">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="658df-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="658df-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-192">**мониторнаме**</span><span class="sxs-lookup"><span data-stu-id="658df-192">**MonitorName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-195">Имя монитора для этого драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-195">Name of the monitor for this printer driver.</span></span>

<span data-ttu-id="658df-196">Пример: "монитор PJL"</span><span class="sxs-lookup"><span data-stu-id="658df-196">Example: "PJL monitor"</span></span>

</dd> <dt>

<span data-ttu-id="658df-197">**Name**</span><span class="sxs-lookup"><span data-stu-id="658df-197">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-198">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-198">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-199">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-199">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-200">Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="658df-200">Qualifiers: [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="658df-201">Имя драйвера для этого принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-201">Driver name for this printer.</span></span> <span data-ttu-id="658df-202">Это составной ключ, состоящий из значений **Name**, **Version** и **суппортедплатформ** .</span><span class="sxs-lookup"><span data-stu-id="658df-202">This is a compound key composed of the **Name**, **Version**, and **SupportedPlatform** values.</span></span>

<span data-ttu-id="658df-203">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) и переопределяет определение **имени** в этом классе.</span><span class="sxs-lookup"><span data-stu-id="658df-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) and overrides the **Name** definition in that class.</span></span>

</dd> <dt>

<span data-ttu-id="658df-204">**оемурл**</span><span class="sxs-lookup"><span data-stu-id="658df-204">**OEMUrl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-205">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-206">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="658df-207">Ссылка на веб-сайт изготовителя принтера (WWW).</span><span class="sxs-lookup"><span data-stu-id="658df-207">World Wide Web (WWW) link to the printer manufacturer's website.</span></span> <span data-ttu-id="658df-208">Обратите внимание, что это свойство не заполняется при использовании файла Win32. INF и применимо только к драйверам, предоставленным непосредственно производителем.</span><span class="sxs-lookup"><span data-stu-id="658df-208">Note that this property is not populated when the Win32.inf file is used, and is only applicable for drivers provided directly from the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="658df-209">**Запуск**</span><span class="sxs-lookup"><span data-stu-id="658df-209">**Started**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-210">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="658df-210">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="658df-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-212">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")</span><span class="sxs-lookup"><span data-stu-id="658df-212">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Started")</span></span>
</dt> </dl>

<span data-ttu-id="658df-213">Если **значение равно true**, то служба запущена.</span><span class="sxs-lookup"><span data-stu-id="658df-213">If **TRUE**, the service is started.</span></span> <span data-ttu-id="658df-214">Если задано **значение false**, служба остановлена.</span><span class="sxs-lookup"><span data-stu-id="658df-214">If **FALSE**, the service is stopped.</span></span>

<span data-ttu-id="658df-215">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="658df-215">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-216">**StartMode**</span><span class="sxs-lookup"><span data-stu-id="658df-216">**StartMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-218">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-219">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("режим запуска")</span><span class="sxs-lookup"><span data-stu-id="658df-219">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Start Mode")</span></span>
</dt> </dl>

<span data-ttu-id="658df-220">Режим запуска службы автоматически запускается операционной системой или запускается только по требованию.</span><span class="sxs-lookup"><span data-stu-id="658df-220">Start mode of the service is automatically started by an operating system, or only started when requested.</span></span>

<span data-ttu-id="658df-221">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="658df-221">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

<span data-ttu-id="658df-222">Возможные следующие значения.</span><span class="sxs-lookup"><span data-stu-id="658df-222">The following are possible values:</span></span>

<dl> <dd><span data-ttu-id="658df-223">Автоматическое</span><span class="sxs-lookup"><span data-stu-id="658df-223">"Automatic"</span></span></dd> <dd><span data-ttu-id="658df-224">Документации</span><span class="sxs-lookup"><span data-stu-id="658df-224">"Manual"</span></span></dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span data-ttu-id="658df-225">**Автоматически** ("автоматически")</span><span class="sxs-lookup"><span data-stu-id="658df-225">**Automatic** ("Automatic")</span></span>


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span data-ttu-id="658df-226">**Вручную** ("вручную")</span><span class="sxs-lookup"><span data-stu-id="658df-226">**Manual** ("Manual")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="658df-227">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="658df-227">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-228">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-228">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-229">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-229">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-230">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="658df-230">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="658df-231">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="658df-231">Current status of the object.</span></span> <span data-ttu-id="658df-232">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="658df-232">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="658df-233">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="658df-233">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="658df-234">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="658df-234">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="658df-235">Последняя, «служба», может применяться при зеркальном переносе диска, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="658df-235">The latter, "Service", can apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="658df-236">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="658df-236">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="658df-237">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="658df-237">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="658df-238">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="658df-238">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="658df-239">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="658df-239">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="658df-240">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="658df-240">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="658df-241">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="658df-241">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="658df-242">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="658df-242">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="658df-243">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="658df-243">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="658df-244">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="658df-244">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="658df-245">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="658df-245">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="658df-246">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="658df-246">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="658df-247">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="658df-247">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="658df-248">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="658df-248">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="658df-249">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="658df-249">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="658df-250">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="658df-250">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="658df-251">**суппортедплатформ**</span><span class="sxs-lookup"><span data-stu-id="658df-251">**SupportedPlatform**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-252">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-253">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="658df-253">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="658df-254">Операционные среды, для которых предназначен драйвер.</span><span class="sxs-lookup"><span data-stu-id="658df-254">Operating environments that the driver is intended for.</span></span>

<span data-ttu-id="658df-255">Пример: "Windows NT x86".</span><span class="sxs-lookup"><span data-stu-id="658df-255">Example: "Windows NT x86".</span></span>

</dd> <dt>

<span data-ttu-id="658df-256">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="658df-256">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-257">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-258">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-259">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы ")</span><span class="sxs-lookup"><span data-stu-id="658df-259">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Class Name")</span></span>
</dt> </dl>

<span data-ttu-id="658df-260">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="658df-260">Scoping system's creation class name.</span></span>

<span data-ttu-id="658df-261">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="658df-261">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-262">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="658df-262">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="658df-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="658df-264">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="658df-264">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="658df-265">Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")</span><span class="sxs-lookup"><span data-stu-id="658df-265">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("System Name")</span></span>
</dt> </dl>

<span data-ttu-id="658df-266">Имя системы, в которой размещена эта служба.</span><span class="sxs-lookup"><span data-stu-id="658df-266">Name of the system that hosts this service.</span></span>

<span data-ttu-id="658df-267">Это свойство наследуется [**от \_ службы CIM**](cim-service.md).</span><span class="sxs-lookup"><span data-stu-id="658df-267">This property is inherited from [**CIM\_Service**](cim-service.md).</span></span>

</dd> <dt>

<span data-ttu-id="658df-268">**Version**</span><span class="sxs-lookup"><span data-stu-id="658df-268">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="658df-269">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="658df-269">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="658df-270">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="658df-270">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="658df-271">Версия операционной системы для драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-271">Operating system version for the printer driver.</span></span>

<dt>

<span id="3"></span>

<span data-ttu-id="658df-272"><span id="3"></span>**3-5**</span><span class="sxs-lookup"><span data-stu-id="658df-272"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="658df-273">2000</span><span class="sxs-lookup"><span data-stu-id="658df-273">Win2k</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="658df-274">Комментарии</span><span class="sxs-lookup"><span data-stu-id="658df-274">Remarks</span></span>

<span data-ttu-id="658df-275">Класс **Win32 \_ принтердривер** является производным от [**\_ службы CIM**](cim-service.md) , которая является производной от [**CIM \_ логикалелемент**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="658df-275">The **Win32\_PrinterDriver** class is derived from [**CIM\_Service**](cim-service.md) which derives from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="658df-276">Пользователи могут удалить драйвер принтера, удалив соответствующий экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="658df-276">Users can uninstall a printer driver by deleting a corresponding instance of this class.</span></span> <span data-ttu-id="658df-277">Для этого вызывающий процесс должен иметь набор прав **селоаддриверпривилеже** для удаления экземпляра этого класса.</span><span class="sxs-lookup"><span data-stu-id="658df-277">To do so, the calling process must have the **SeLoadDriverPrivilege** privilege set to delete an instance of this class.</span></span>

## <a name="examples"></a><span data-ttu-id="658df-278">Примеры</span><span class="sxs-lookup"><span data-stu-id="658df-278">Examples</span></span>

<span data-ttu-id="658df-279">Пример " [Управление драйверами принтера и принтерами](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) " позволяет управлять драйверами принтера и портами принтера.</span><span class="sxs-lookup"><span data-stu-id="658df-279">The [Manage Printer and Printer Drivers](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) VBScript sample manages printer drivers and printer ports.</span></span>

<span data-ttu-id="658df-280">В следующем [обсуждении на форумах TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) описано, как создать принтер и загрузить драйверы с сервера.</span><span class="sxs-lookup"><span data-stu-id="658df-280">The following [discussion on the TechNet forums](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) describes how to create a printer and upload drivers from a server.</span></span>

<span data-ttu-id="658df-281">В следующем примере сценария VBScript перечислены все драйверы принтеров, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="658df-281">The following VBScript sample lists all the printer drivers that have been installed on a computer.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
Set colInstalledPrinters =  objWMIService.ExecQuery _ 
    ("Select * from Win32_PrinterDriver") 
 
For each objPrinter in colInstalledPrinters 
    Wscript.Echo "Configuration File: " & objPrinter.ConfigFile 
    Wscript.Echo "Data File: " & objPrinter.DataFile 
    Wscript.Echo "Description: " & objPrinter.Description 
    Wscript.Echo "Driver Path: " & objPrinter.DriverPath 
    Wscript.Echo "File Path: " & objPrinter.FilePath 
    Wscript.Echo "Help File: " & objPrinter.HelpFile 
    Wscript.Echo "INF Name: " & objPrinter.InfName 
    Wscript.Echo "Monitor Name: " & objPrinter.MonitorName 
    Wscript.Echo "Name: " & objPrinter.Name 
    Wscript.Echo "OEM Url: " & objPrinter.OEMUrl 
    Wscript.Echo "Supported Platform: " & objPrinter.SupportedPlatform 
    Wscript.Echo "Version: " & objPrinter.Version 
Next 
```



## <a name="requirements"></a><span data-ttu-id="658df-282">Требования</span><span class="sxs-lookup"><span data-stu-id="658df-282">Requirements</span></span>



| <span data-ttu-id="658df-283">Требование</span><span class="sxs-lookup"><span data-stu-id="658df-283">Requirement</span></span> | <span data-ttu-id="658df-284">Значение</span><span class="sxs-lookup"><span data-stu-id="658df-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="658df-285">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="658df-285">Minimum supported client</span></span><br/> | <span data-ttu-id="658df-286">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="658df-286">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="658df-287">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="658df-287">Minimum supported server</span></span><br/> | <span data-ttu-id="658df-288">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="658df-288">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="658df-289">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="658df-289">Namespace</span></span><br/>                | <span data-ttu-id="658df-290">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="658df-290">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="658df-291">MOF</span><span class="sxs-lookup"><span data-stu-id="658df-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="658df-292"><dt>Win32 \_ Printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="658df-292"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="658df-293">DLL</span><span class="sxs-lookup"><span data-stu-id="658df-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="658df-294"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="658df-294"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="658df-295">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="658df-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658df-296">**\_Служба CIM**</span><span class="sxs-lookup"><span data-stu-id="658df-296">**CIM\_Service**</span></span>](./cim-service.md)
</dt> <dt>

[<span data-ttu-id="658df-297">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="658df-297">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
