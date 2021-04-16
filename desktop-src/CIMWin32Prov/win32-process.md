---
Description: Процесс Win32 \_&\# 32; Класс WMI представляет процесс в операционной системе.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Класс Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657201"
---
# <a name="win32_process-class"></a>\_Класс процесса Win32

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ процесса Win32** представляет процесс в операционной системе.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

> [!NOTE]
> Общие сведения о процессах и потоках в Windows см. в разделе [процессы и потоки](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Члены

Класс **\_ процесса Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ процесса Win32** содержит следующие методы.



| Метод                                                                   | Описание                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аттачдебугжер**](attachdebugger-method-in-class-win32-process.md)   | Запускает зарегистрированный в данный момент отладчик для процесса.<br/>                                                                                                                                                                                                                      |
| [**Создать**](create-method-in-class-win32-process.md)                   | Создает новый процесс.<br/>                                                                                                                                                                                                                                                         |
| [**жетаваилаблевиртуалсизе**](getavailablevirtualsize-win32-process.md) | Получает текущий размер (в байтах) свободного виртуального адресного пространства, доступного процессу.<br/> **Windows server 2012, Windows 8, Windows 7, Windows server 2008 и Windows Vista:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Возвращает имя пользователя и доменное имя, под которым выполняется процесс.<br/>                                                                                                                                                                                                    |
| [**жетовнерсид**](getownersid-method-in-class-win32-process.md)         | Возвращает идентификатор безопасности (SID) для владельца процесса.<br/>                                                                                                                                                                                                            |
| [**SetPriority**](setpriority-method-in-class-win32-process.md)         | Изменяет приоритет выполнения процесса.<br/>                                                                                                                                                                                                                                   |
| [**Завершение**](terminate-method-in-class-win32-process.md)             | Завершает процесс и все его потоки.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Свойства

Класс **\_ процесса Win32** имеет следующие свойства.

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

**CommandLine**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Командная строка для запуска процесса")
</dt> </dl>

Командная строка, используемая для запуска определенного процесса, если это применимо.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Дата начала выполнения процесса.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**кскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Кскреатионкласснаме**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы компьютера ")
</dt> </dl>

Имя класса создания для системы компьютера с областями.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CSName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя системы компьютера ")
</dt> </dl>

Имя системы области компьютера.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**привилегии**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры справки по инструментам Win32API \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| Сзексепас"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("путь к исполняемому файлу")
</dt> </dl>

Путь к исполняемому файлу процесса.

Пример: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние выполнения")
</dt> </dl>

Текущее рабочее состояние процесса.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd>

Неизвестно

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd>

Другое

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Готово** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Работает** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Заблокировано** (4)


</dt> <dd>

Блокировано

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Блокировка приостановлена** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Приостановлено** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Завершено** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Растет** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Дескриптор**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")
</dt> </dl>

Идентификатор процесса.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("количество маркеров")
</dt> </dl>

Общее число открытых дескрипторов, принадлежащих процессу. **HandleCount** — это сумма дескрипторов, которые в настоящее время открыты каждым потоком в этом процессе. Для проверки или изменения системных ресурсов используется маркер. Каждый обработчик имеет запись в таблице, которая поддерживается внутренним образом. Записи содержат адреса ресурсов и данных для обнаружения типа ресурса.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Дата установки объекта. Объект может быть установлен без значения, записываемого в это свойство.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**кернелмодетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("кернелмодетиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")
</dt> </dl>

Время в режиме ядра (в миллисекундах). Если эта информация недоступна, используйте значение 0 (ноль).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**максимумворкингсетсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. \|Ограничения квоты H \_ \| максимумворкингсетсизе "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" максимальный размер рабочего множества "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")
</dt> </dl>

Максимальный размер рабочего множества процесса. Рабочий набор процесса — это набор страниц памяти, видимых для процесса в физической оперативной памяти. Эти страницы являются резидентными и доступны для использования приложением без активации ошибки страницы.

Пример: 1413120

</dd> <dt>

**минимумворкингсетсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. \|Ограничения квоты H \_ \| минимумворкингсетсизе "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" минимальный размер рабочего набора "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")
</dt> </dl>

Минимальный размер рабочего множества процесса. Рабочий набор процесса — это набор страниц памяти, видимых для процесса в физической оперативной памяти. Эти страницы являются резидентными и доступны для использования приложением без активации ошибки страницы.

Пример: 20480

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")
</dt> </dl>

Имя исполняемого файла, ответственного за процесс, эквивалентное свойству имя образа в диспетчере задач.

При наследовании подклассом свойство может быть переопределено как ключевое свойство. Имя жестко запрограммировано в самом приложении и не влияет на изменение имени файла. Например, даже если переименовать Calc.exe, имя Calc.exe будет по-прежнему отображаться в диспетчере задач и в любых скриптах WMI, которые извлекают имя процесса.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**оскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса операционной системы ")
</dt> </dl>

Имя класса создания для операционной системы области.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ Операционная система CIM**](cim-operatingsystem.md)".**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя операционной системы ")
</dt> </dl>

Имя операционной системы области.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**осероператионкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Осероператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Счетчик других операций")
</dt> </dl>

Количество выполненных операций ввода-вывода, которые не являются операциями чтения или записи.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**осертрансферкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Осертрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("другие счетчики передач"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Объем данных, передаваемых во время операций, которые не являются операциями чтения или записи.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**пажефаултс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пажефаулткаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число ошибок страниц")
</dt> </dl>

Количество ошибок страниц, создаваемых процессом.

Пример: 10

</dd> <dt>

**пажефилеусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пажефилеусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("использование файла подкачки"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Количество места в файле подкачки, которое используется процессом в данный момент. Это значение согласуется со значением **VMSize** в TaskMgr.exe.

Пример: 102435

</dd> <dt>

**парентпроцессид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Инхеритедфромуникуепроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор родительского процесса")
</dt> </dl>

Уникальный идентификатор процесса, который создает процесс. Идентификаторы процессов используются повторно, поэтому они определяют только процесс времени существования этого процесса. Возможно, процесс, идентифицированный **парентпроцессид** , завершается, поэтому **парентпроцессид** может не ссылаться на выполняющийся процесс. Также возможно, что **парентпроцессид** неправильно ссылается на процесс, который повторно использует идентификатор процесса. Свойство **CreationDate** можно использовать для определения того, был ли создан указанный родительский объект после создания процесса, представленного этим экземпляром **\_ процесса Win32** .

</dd> <dt>

**пеакпажефилеусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеакпажефилеусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковое использование файла подкачки"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Максимальный объем пространства файла подкачки, используемый в течение всего процесса.

Пример: 102367

</dd> <dt>

**пеаквиртуалсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеаквиртуалсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковое использование адресного пространства виртуальной"), [**единицы**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Максимальное виртуальное адресное пространство, используемое процессом в любой момент времени. Использование виртуального адресного пространства не обязательно подразумевает соответствующее использование страниц диска или основной памяти. Однако виртуальное пространство ограничено, и чрезмерное использование процесса может привести к невозможности загрузки библиотек.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**пеакворкингсетсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Пеакворкингсетсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("пиковый размер рабочего набора"), [**единиц**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Пиковый размер рабочего множества процесса.

Пример: 1413120

</dd> <dt>

**Приоритет**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("приоритет"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| басеприорити"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("приоритет")
</dt> </dl>

Планирование приоритета процесса в операционной системе. Чем выше значение, тем выше приоритет, получаемый процессом. Значения приоритета могут находиться в диапазоне от 0 (ноль), который является наименьшим приоритетом до 31, что является высшим приоритетом.

Пример: 7

</dd> <dt>

**приватепажекаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Приватепажекаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число частных страниц")
</dt> </dl>

Текущее количество выделенных страниц, которые доступны только для процесса, представленного этим экземпляром **\_ процесса Win32** .

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структуры потоков \| [**\_ сведения о процессе**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| Двпроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор процесса")
</dt> </dl>

Числовой идентификатор, используемый для различения одного процесса от другого. Процессидс действительны из времени создания процесса до завершения процесса. После завершения работы этот же числовой идентификатор можно применить к новому процессу.

Это означает, что нельзя использовать только ProcessID для мониторинга определенного процесса. Например, приложение может иметь идентификатор процесса 7, а затем завершиться с ошибкой. При запуске нового процесса новому процессу может быть назначен идентификатор процесса 7. Сценарий, проверенный только для указанного ProcessID, может быть «обманным», чтобы подумать о том, что исходное приложение все еще запущено.

</dd> <dt>

**куотанонпажедпулусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотанонпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("квота использования невыгружаемого пула")
</dt> </dl>

Квота объема использования невыгружаемого пула для процесса.

Пример: 15

</dd> <dt>

**куотапажедпулусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("квота на использование выгружаемого пула")
</dt> </dl>

Объем использования выгружаемого пула для процесса в квоте.

Пример: 22

</dd> <dt>

**куотапеакнонпажедпулусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапеакнонпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Пиковая квота использования невыгружаемого пула")
</dt> </dl>

Пиковая квота использования невыгружаемого пула для процесса.

Пример: 31

</dd> <dt>

**куотапеакпажедпулусаже**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Куотапеакпажедпулусаже"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Пиковая квота использования выгружаемого пула")
</dt> </dl>

Пиковая квота использования выгружаемого пула для процесса.

Пример: 31

</dd> <dt>

**реадоператионкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Реадоператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число операций чтения")
</dt> </dl>

Число выполненных операций чтения.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**реадтрансферкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Реадтрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число передач чтения"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Объем считанных данных.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесс состояние \| процесса \_ системы \_ \| SessionID"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор сеанса")
</dt> </dl>

Уникальный идентификатор, создаваемый операционной системой при создании сеанса. Сеанс охватывает период времени от входа до выхода из определенной системы.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Это свойство не реализовано и не заполняется ни одним экземпляром этого класса. Всегда имеет **значение NULL**.

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

**TerminationDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Дата завершения")
</dt> </dl>

Процесс остановлен или прерван. Чтобы получить время завершения, необходимо удерживать маркер процесса открытым. В противном случае это свойство возвращает **значение NULL**.

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число потоков")
</dt> </dl>

Число активных потоков в процессе. Инструкция — это базовая единица выполнения в процессоре, а поток — это объект, выполняющий инструкцию. Каждый выполняющийся процесс имеет по крайней мере один поток.

</dd> <dt>

**усермодетиме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("усермодетиме"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 наносекунд")
</dt> </dl>

Время в пользовательском режиме, в единицах 100 нс. Если эта информация недоступна, используйте значение 0 (ноль).

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**виртуалсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| процесса состояние \| системного \_ процесса \_ \| Виртуалсизе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("использование виртуального адресного пространства"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Текущий размер виртуального адресного пространства, используемого процессом, а не физическая или виртуальная память, фактически используемая процессом. Использование виртуального адресного пространства не обязательно подразумевает соответствующее использование страниц диска или основной памяти. Виртуальное пространство, конечное, и слишком много, процесс может не суметь загрузить библиотеки. Это значение согласуется с тем, что отображается в Perfmon.exe.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и функции потока \| Жетпроцессверсион"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("версия Windows")
</dt> </dl>

Версия Windows, в которой выполняется процесс.

Пример: 4,0

</dd> <dt>

**воркингсетсизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("размер рабочего множества"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Объем памяти в байтах, который должен эффективно выполняться процессом — для операционной системы, использующей управление памятью на основе страниц. Если в системе недостаточно памяти (меньше размера рабочего набора), пробуксовка происходит. Если размер рабочего набора неизвестен, используйте **значение NULL** или 0 (ноль). Если предоставлены данные рабочего набора, можно отслеживать эти сведения, чтобы понять, как изменяются требования к памяти для процесса.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

Это свойство наследуется [**от \_ процесса CIM**](cim-process.md).

</dd> <dt>

**вритеоператионкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессе в системе \_ \| Вритеоператионкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число операций записи")
</dt> </dl>

Число выполненных операций записи.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**вритетрансферкаунт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| процесс Win32API и структура потоков \| \_ сведения о процессах \_ \| Вритетрансферкаунт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число передач записи"), [**единиц**](../wmisdk/standard-qualifiers.md) ("байт")
</dt> </dl>

Объем записанных данных.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **\_ процесса Win32** является производным от [**\_ процесса CIM**](cim-process.md). Вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ Name** на компьютере, где размещается реестр. Дополнительные сведения см. в разделе [выполнение привилегированных операций](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Обзор

Процессы лежат практически на всех компьютерах, происходящих на компьютере. На самом деле, основная причина большинства проблем с компьютером может быть отслежена на процессах. Например, на компьютере может быть запущено слишком много процессов (и зависит от ограниченного набора ресурсов), или же один процесс может использовать больше ресурсов, чем общий ресурс. Эти факторы важны для того, чтобы следить за процессами, выполняемыми на компьютере. Наблюдение за процессом, главное действие в управлении процессами, позволяет определить, что компьютер действительно делает, какие приложения работают и каким образом влияют изменения в вычислительной среде.

### <a name="monitoring-a-process"></a>Мониторинг процесса

Мониторинг процессов на регулярной основе помогает убедиться, что компьютер работает с пиковой эффективностью и что он выполняет свои задачи надлежащим образом. Например, мониторинг процессов позволяет немедленно получить уведомления о любом приложении, которое перестало отвечать, а затем выполнить действия по завершению этого процесса. Кроме того, мониторинг процессов позволяет выявление проблем до их возникновения. Например, при многократной проверке объема памяти, используемой процессом, можно выявлять утечку памяти. Затем можно остановить процесс, чтобы приложение аномального использовало всю доступную память и переведет компьютер в остановленное расположение.

Мониторинг процессов также помогает минимизировать перерывы, вызванные запланированными простои для обновления и обслуживания. Например, проверка состояния приложения базы данных, выполняющегося на клиентских компьютерах, позволяет определить влияние перевода базы данных в режим «вне сети» для обновления программного обеспечения.

Наблюдение за доступностью процесса. Измеряет процент времени, в течение которого доступен процесс. Доступность обычно отслеживается с помощью простой проверки, которая сообщает, работает ли процесс. Отслеживая результаты каждой пробы, можно вычислить доступность процесса. Например, процесс, проверенный 100 раз и отвечающий на 95 из этих событий, имеет уровень доступности 95%. Этот тип мониторинга обычно зарезервирован для баз данных, почтовых программ и других приложений, которые должны выполняться в любое время. Он не подходит для программ обработки текста, электронных таблиц или других приложений, которые обычно запускаются и останавливаются несколько раз в день.

Для настройки процесса можно создать экземпляр класса [**Win32 \_ процессстартуп**](win32-processstartup.md) .

Производительность процесса можно отслеживать с помощью класса [**\_ \_ \_ процесса Win32 перфформаттеддата PERFPROC**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) и объекта обновления WMI, например [**свбемрефрешер**](../wmisdk/swbemrefresher.md). Дополнительные сведения см. в разделе [наблюдение за данными производительности](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Примеры

В [списке свойств классов WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) . пример кода PowerShell в коллекции TechNet описывается класс **\_ процесса Win32** и результаты выводятся в формате Excel.

Процесс [завершения процесса на нескольких серверах](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) прерывает процесс, выполняющийся на одном или нескольких компьютерах.

В примере в разделе [вызов метода поставщика](../wmisdk/example--calling-a-provider-method.md) код использует C++ для вызова **\_ процесса Win32** для создания процесса.

Доступность — это простейшая форма мониторинга процессов. при таком подходе вы просто убедитесь, что процесс выполняется. При наблюдении за доступностью процессов обычно извлекается список процессов, запущенных на компьютере, а затем проверяется, активен ли конкретный процесс. Если процесс активен, он считается доступным. Если процесс неактивен, он недоступен. Следующий пример сценария VBScript отслеживает доступность процесса, проверяя список запущенных на компьютере процессов и выдавая уведомление, если процесс Database.exe не найден.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



Следующий пример VBScript отслеживает создание процессов с помощью временного потребителя событий.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



Следующая команда VBScript отслеживает сведения о производительности процесса.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



В следующем примере кода VBScript показано, как получить сведения о владельце каждого процесса на локальном компьютере. Этот сценарий можно использовать для получения данных с удаленного компьютера, например, чтобы определить, какие пользователи имеют процессы, выполняющие сервер терминалов, подставьте имя удаленного компьютера для "." в первой строке. Кроме того, необходимо быть администратором на удаленном компьютере.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



В следующем примере кода VBScript показано, как получить сеанс входа, связанный с выполняющимся процессом. Процесс должен выполняться Notepad.exe перед запуском скрипта. В примере находятся экземпляры [**Win32 \_ LogonSession**](win32-logonsession.md) , связанные с **\_ процессом Win32** , который представляет Notepad.exe. [**Win32 \_ Сессионпроцесс**](win32-sessionprocess.md) указывается в качестве класса ассоциации. Дополнительные сведения см. в разделе [соединители оператора.](../wmisdk/associators-of-statement.md).


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Процесс CIM**](cim-process.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[Задачи WMI: процессы](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
