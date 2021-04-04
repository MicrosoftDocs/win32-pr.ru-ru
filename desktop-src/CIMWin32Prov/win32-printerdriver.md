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
# <a name="win32_printerdriver-class"></a>\_Класс Win32 принтердривер

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ принтердривер для Win32** представляет драйверы для экземпляра [**\_ принтера Win32**](win32-printer.md) .

Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все наследуемые свойства, но исключает методы. Справочные сведения о методах см. в таблице методов в этой статье.

## <a name="syntax"></a>Синтаксис

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

## <a name="members"></a>Члены

Класс **Win32 \_ принтердривер** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ принтердривер** содержит следующие методы.



| Метод                                                                           | Описание                              |
|:---------------------------------------------------------------------------------|:-----------------------------------------|
| [**аддпринтердривер**](addprinterdriver-method-in-class-win32-printerdriver.md) | Создает новый драйвер принтера.<br/> |
| [**StartService**](startservice-method-in-class-win32-printerdriver.md)         | Запускает службу печати.<br/>         |
| [**StopService**](stopservice-method-in-class-win32-printerdriver.md)           | Останавливает службу печати.<br/>          |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ принтердривер** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ConfigFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Файл конфигурации для этого драйвера принтера.

Пример: "pscrptui.dll"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**DataFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) (CIM \_ File. filename)
</dt> </dl>

Файл данных для этого драйвера принтера.

Пример: "qms810. PPD"

</dd> <dt>

**дефаултдататипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип данных по умолчанию для этого драйвера принтера.

Пример: "EMF"

</dd> <dt>

**депендентфилес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив зависимых файлов для этого драйвера принтера.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Комментарий, описывающий ссылку.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**DriverPath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) (CIM- \_ файл. путь)
</dt> </dl>

Путь для этого драйвера принтера.

Пример: "C: \\ \\ drivers \\ \\pscript.dll"

</dd> <dt>

**Равно**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Путь к используемому INF-файлу.

Пример: "c: \\ \\ temp \\ \\ Driver"

</dd> <dt>

**HelpFile**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Файл справки для этого драйвера принтера.

Пример: "пскрптуи. hlp"

</dd> <dt>

**инфнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Имя используемого INF-файла. По умолчанию используется указанный в операционной системе INF-файл принтера. Если драйвер предоставляется непосредственно изготовителем принтера, а не операционной системой, используется другое имя файла.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Дата и время установки объекта. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**мониторнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя монитора для этого драйвера принтера.

Пример: "монитор PJL"

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)
</dt> </dl>

Имя драйвера для этого принтера. Это составной ключ, состоящий из значений **Name**, **Version** и **суппортедплатформ** .

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) и переопределяет определение **имени** в этом классе.

</dd> <dt>

**оемурл**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на веб-сайт изготовителя принтера (WWW). Обратите внимание, что это свойство не заполняется при использовании файла Win32. INF и применимо только к драйверам, предоставленным непосредственно производителем.

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")
</dt> </dl>

Если **значение равно true**, то служба запущена. Если задано **значение false**, служба остановлена.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("режим запуска")
</dt> </dl>

Режим запуска службы автоматически запускается операционной системой или запускается только по требованию.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

Возможные следующие значения.

<dl> <dd>Автоматическое</dd> <dd>Документации</dd> </dl>

<dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Автоматически** ("автоматически")


</dt> <dd></dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

**Вручную** ("вручную")


</dt> <dd></dd> </dl>

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться при зеркальном переносе диска, перезагрузке списка разрешений пользователя или выполнении других административных задач. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

В эти значения входят:

<dt>

<span id="OK"></span><span id="ok"></span>

**ОК** ("ОК")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Ошибка** ("ошибка")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Пониженная работоспособность** (пониженная работоспособность)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Пред-ошибка** ("пред Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Запуск** ("Запуск")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Остановка** ("остановка")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Служба** ("служба")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Пренапряжению** ("напряжению")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Невосстановление** ("невосстановление")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Нет контакта** ("нет контакта")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Потеря** связи ("потеря связи")


</dt> <dd></dd> </dl>

</dd> <dt>

**суппортедплатформ**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Операционные среды, для которых предназначен драйвер.

Пример: "Windows NT x86".

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы ")
</dt> </dl>

Имя класса создания системы области.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" System Name ")
</dt> </dl>

Имя системы, в которой размещена эта служба.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Версия операционной системы для драйвера принтера.

<dt>

<span id="3"></span>

<span id="3"></span>**3-5**


</dt> <dd>

2000

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ принтердривер** является производным от [**\_ службы CIM**](cim-service.md) , которая является производной от [**CIM \_ логикалелемент**](cim-logicalelement.md).

Пользователи могут удалить драйвер принтера, удалив соответствующий экземпляр этого класса. Для этого вызывающий процесс должен иметь набор прав **селоаддриверпривилеже** для удаления экземпляра этого класса.

## <a name="examples"></a>Примеры

Пример " [Управление драйверами принтера и принтерами](https://Gallery.TechNet.Microsoft.Com/710bb2ad-9a8d-42cb-b142-cda2c1452548) " позволяет управлять драйверами принтера и портами принтера.

В следующем [обсуждении на форумах TechNet](https://social.technet.microsoft.com/Forums/scriptcenter/6210fa0b-0c32-4bce-a79c-dfe835922613/create-printers-in-powershell-with-wmi-win32printer-createinstance?forum=ITCG) описано, как создать принтер и загрузить драйверы с сервера.

В следующем примере сценария VBScript перечислены все драйверы принтеров, установленные на компьютере.


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](./cim-service.md)
</dt> <dt>

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> </dl>

 

 
