---
description: представляет операционную систему на основе Windows, установленную на компьютере.
ms.assetid: eb6a8cff-20a0-4211-b46a-3084e9c39246
ms.tgt_platform: multiple
title: Класс Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem
- Win32_OperatingSystem.BootDevice
- Win32_OperatingSystem.BuildNumber
- Win32_OperatingSystem.BuildType
- Win32_OperatingSystem.Caption
- Win32_OperatingSystem.CodeSet
- Win32_OperatingSystem.CountryCode
- Win32_OperatingSystem.CreationClassName
- Win32_OperatingSystem.CSCreationClassName
- Win32_OperatingSystem.CSDVersion
- Win32_OperatingSystem.CSName
- Win32_OperatingSystem.CurrentTimeZone
- Win32_OperatingSystem.DataExecutionPrevention_Available
- Win32_OperatingSystem.DataExecutionPrevention_32BitApplications
- Win32_OperatingSystem.DataExecutionPrevention_Drivers
- Win32_OperatingSystem.DataExecutionPrevention_SupportPolicy
- Win32_OperatingSystem.Debug
- Win32_OperatingSystem.Description
- Win32_OperatingSystem.Distributed
- Win32_OperatingSystem.EncryptionLevel
- Win32_OperatingSystem.ForegroundApplicationBoost
- Win32_OperatingSystem.FreePhysicalMemory
- Win32_OperatingSystem.FreeSpaceInPagingFiles
- Win32_OperatingSystem.FreeVirtualMemory
- Win32_OperatingSystem.InstallDate
- Win32_OperatingSystem.LargeSystemCache
- Win32_OperatingSystem.LastBootUpTime
- Win32_OperatingSystem.LocalDateTime
- Win32_OperatingSystem.Locale
- Win32_OperatingSystem.Manufacturer
- Win32_OperatingSystem.MaxNumberOfProcesses
- Win32_OperatingSystem.MaxProcessMemorySize
- Win32_OperatingSystem.MUILanguages
- Win32_OperatingSystem.Name
- Win32_OperatingSystem.NumberOfLicensedUsers
- Win32_OperatingSystem.NumberOfProcesses
- Win32_OperatingSystem.NumberOfUsers
- Win32_OperatingSystem.OperatingSystemSKU
- Win32_OperatingSystem.Organization
- Win32_OperatingSystem.OSArchitecture
- Win32_OperatingSystem.OSLanguage
- Win32_OperatingSystem.OSProductSuite
- Win32_OperatingSystem.OSType
- Win32_OperatingSystem.OtherTypeDescription
- Win32_OperatingSystem.PAEEnabled
- Win32_OperatingSystem.PlusProductID
- Win32_OperatingSystem.PlusVersionNumber
- Win32_OperatingSystem.PortableOperatingSystem
- Win32_OperatingSystem.Primary
- Win32_OperatingSystem.ProductType
- Win32_OperatingSystem.RegisteredUser
- Win32_OperatingSystem.SerialNumber
- Win32_OperatingSystem.ServicePackMajorVersion
- Win32_OperatingSystem.ServicePackMinorVersion
- Win32_OperatingSystem.SizeStoredInPagingFiles
- Win32_OperatingSystem.Status
- Win32_OperatingSystem.SuiteMask
- Win32_OperatingSystem.SystemDevice
- Win32_OperatingSystem.SystemDirectory
- Win32_OperatingSystem.SystemDrive
- Win32_OperatingSystem.TotalSwapSpaceSize
- Win32_OperatingSystem.TotalVirtualMemorySize
- Win32_OperatingSystem.TotalVisibleMemorySize
- Win32_OperatingSystem.Version
- Win32_OperatingSystem.WindowsDirectory
- Win32_OperatingSystem.QuantumLength
- Win32_OperatingSystem.QuantumType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1df0da4cadf0cd610803b2f456f22049471b28bc5653bc400f4c730cb0c47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972534"
---
# <a name="win32_operatingsystem-class"></a>\_Класс операционной системы Win32

[класс WMI](../wmisdk/retrieving-a-class.md) **\_ операционной системы Win32** , представляющий собой операционную систему на основе Windows, установленную на компьютере.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Singleton, Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4DE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_OperatingSystem : CIM_OperatingSystem
{
  string   BootDevice;
  string   BuildNumber;
  string   BuildType;
  string   Caption;
  string   CodeSet;
  string   CountryCode;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSDVersion;
  string   CSName;
  sint16   CurrentTimeZone;
  boolean  DataExecutionPrevention_Available;
  boolean  DataExecutionPrevention_32BitApplications;
  boolean  DataExecutionPrevention_Drivers;
  uint8    DataExecutionPrevention_SupportPolicy;
  boolean  Debug;
  string   Description;
  boolean  Distributed;
  uint32   EncryptionLevel;
  uint8    ForegroundApplicationBoost = 2;
  uint64   FreePhysicalMemory;
  uint64   FreeSpaceInPagingFiles;
  uint64   FreeVirtualMemory;
  datetime InstallDate;
  uint32   LargeSystemCache;
  datetime LastBootUpTime;
  datetime LocalDateTime;
  string   Locale;
  string   Manufacturer;
  uint32   MaxNumberOfProcesses;
  uint64   MaxProcessMemorySize;
  string   MUILanguages[];
  string   Name;
  uint32   NumberOfLicensedUsers;
  uint32   NumberOfProcesses;
  uint32   NumberOfUsers;
  uint32   OperatingSystemSKU;
  string   Organization;
  string   OSArchitecture;
  uint32   OSLanguage;
  uint32   OSProductSuite;
  uint16   OSType;
  string   OtherTypeDescription;
  Boolean  PAEEnabled;
  string   PlusProductID;
  string   PlusVersionNumber;
  boolean  PortableOperatingSystem;
  boolean  Primary;
  uint32   ProductType;
  string   RegisteredUser;
  string   SerialNumber;
  uint16   ServicePackMajorVersion;
  uint16   ServicePackMinorVersion;
  uint64   SizeStoredInPagingFiles;
  string   Status;
  uint32   SuiteMask;
  string   SystemDevice;
  string   SystemDirectory;
  string   SystemDrive;
  uint64   TotalSwapSpaceSize;
  uint64   TotalVirtualMemorySize;
  uint64   TotalVisibleMemorySize;
  string   Version;
  string   WindowsDirectory;
  uint8    QuantumLength;
  uint8    QuantumType;
};
```

## <a name="members"></a>Члены

Класс **\_ операционной системы Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **\_ операционной системы Win32** имеет следующие методы.



| Метод                                                                                     | Описание                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Перезагрузка**](reboot-method-in-class-win32-operatingsystem.md)                             | Завершает работу и перезапускает компьютерную систему.<br/>                                                                                                                                                                                                           |
| [**сетдатетиме**](setdatetime-method-in-class-win32-operatingsystem.md)                   | Позволяет задать дату и время компьютера.<br/>                                                                                                                                                                                                                |
| [**Завершение работы**](shutdown-method-in-class-win32-operatingsystem.md)                         | Выгружает программы и библиотеки DLL до точки, в которой можно отключить компьютер.<br/>                                                                                                                                                                           |
| [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md)               | предоставляет полный набор параметров завершения работы, поддерживаемых операционными системами Windows.<br/>                                                                                                                                                                           |
| [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) | Предоставляет тот же набор параметров завершения работы, который поддерживает метод [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) в **Win32 \_ операционной** системы, но также позволяет указать комментарии, причину завершения работы или время ожидания.<br/> |



 

### <a name="properties"></a>Свойства

Класс **\_ операционной системы Win32** имеет следующие свойства.

<dl> <dt>

**BootDevice**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| \_ сведения о сопоставлении дисков \_ \| btInt13Unit")
</dt> </dl>

имя диска, с которого запускается операционная система Windows.

Пример: " \\ \\ \\ Harddisk0 устройства"

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе структуры \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| двбуилднумбер")
</dt> </dl>

Номер сборки операционной системы. Его можно использовать для более точных сведений о версии, чем номера выпускаемой версии продукта.

Пример: "1381"

</dd> <dt>

**буилдтипе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| курренттипе")
</dt> </dl>

Тип сборки, используемой для операционной системы.

Примеры: "" Розничная Сборка "", "" проверенная сборка ""

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка. Строка включает версию операционной системы. например, "Microsoft Windows 7 Корпоративная". Это свойство может быть локализовано.

**Windows Vista и Windows 7:** Это свойство может содержать конечные символы. например, для получения сведений с помощью этого свойства может потребоваться строка "Microsoft Windows 7 Корпоративная" (конечная пробел).

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Исходный код**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (6), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| locale \_ идефаултансикодепаже")
</dt> </dl>

Значение кодовой страницы, используемой операционной системой. Кодовая страница содержит таблицу символов, которую операционная система использует для преобразования строк для разных языков. В Американский национальный институт стандартов (ANSI) (ANSI) перечислены значения, представляющие определенные кодовые страницы. Если операционная система не использует кодовую страницу ANSI, для этого элемента устанавливается значение 0 (ноль). Для определения значения кодовой страницы в строке **набора кода** может использоваться не более шести символов.

Пример: "1255"

</dd> <dt>

**каунтрикоде**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| язык \_ икаунтри")
</dt> </dl>

Код для страны или региона, который использует операционная система. Значения основаны на международных префиксах телефонных номеров, которые также называются кодами страны и региона IBM. Это свойство может использовать не более шести символов для определения значения кода страны или региона.

Пример: "1" (США)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**кскреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя класса создания для системы компьютера с областями.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**CSDVersion**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе структуры \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **сзксдверсион**")
</dt> </dl>

Строка **, заканчивающаяся нулем и** указывающая на последний пакет обновления, установленный на компьютере. Если пакет обновления не установлен, строка имеет **значение NULL**.

Пример: "пакет обновления 3"

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Имя системы области компьютера.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**курренттимезоне**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("минуты")
</dt> </dl>

Число (в минутах), в течение которого операционная система смещается от среднего времени по Гринвичу (GMT). Число может быть положительным, отрицательным или нулевым.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**Датаексекутионпревентион \_ 32BitApplications**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Если функция предотвращения выполнения данных доступна, это свойство указывает, что эта функция настроена для работы в 32-разрядных приложениях, если **значение true**. На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище [данные конфигурации загрузки (BCD)](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal) , а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.

</dd> <dt>

**Датаексекутионпревентион \_ доступно**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Предотвращение выполнения данных — это аппаратная функция для предотвращения атак переполнения буфера путем остановки выполнения кода на страницах памяти типа данных. Если **значение — true**, эта функция доступна. На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище BCD, а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.

</dd> <dt>

**\_Драйверы датаексекутионпревентион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Если функция предотвращения выполнения данных доступна, это свойство указывает, что эта функция настроена для работы с драйверами, если имеет **значение true**. На 64-разрядных компьютерах функция предотвращения выполнения данных настраивается в хранилище BCD, а свойства в **Win32 версии \_ операционной** системы устанавливаются соответствующим образом.

</dd> <dt>

**Датаексекутионпревентион \_ суппортполици**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Указывает, какой параметр предотвращения выполнения данных (DEP) применяется. Параметр DEP определяет степень применения DEP к 32-разрядным приложениям в системе. функция DEP всегда применяется к ядру Windows.

<dt>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>

<span id="Always_Off"></span><span id="always_off"></span><span id="ALWAYS_OFF"></span>**Всегда выкл** . (0)


</dt> <dd>

Функция DEP отключена для всех 32-разрядных приложений на компьютере без исключений. Этот параметр недоступен для пользовательского интерфейса.

</dd> <dt>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>

<span id="Always_On"></span><span id="always_on"></span><span id="ALWAYS_ON"></span>**Always on** (1)


</dt> <dd>

Функция DEP включена для всех 32-разрядных приложений на компьютере. Этот параметр недоступен для пользовательского интерфейса.

</dd> <dt>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>

<span id="Opt_In"></span><span id="opt_in"></span><span id="OPT_IN"></span>**Согласие на участие** (2)


</dt> <dd>

функция DEP включена для ограниченного числа двоичных файлов, ядра и всех служб на основе Windows. Однако он по умолчанию отключен для всех 32-разрядных приложений. Пользователь или администратор должен явно выбрать параметр **Always on** или **отказаться от согласия** , прежде чем DEP можно будет применить к 32-разрядным приложениям.

</dd> <dt>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>

<span id="Opt_Out"></span><span id="opt_out"></span><span id="OPT_OUT"></span>**Отказ от участия** (3)


</dt> <dd>

Функция DEP включена по умолчанию для всех 32-разрядных приложений. Пользователь или администратор может явно удалить поддержку 32-разрядного приложения, добавив приложение в список исключений.

</dd> </dl>

</dd> <dt>

**Отладка**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| [**жетсистемметрикс**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ Debug")
</dt> </dl>

Операционная система — это проверенная (Отладка) сборка. Если **значение — true**, устанавливается версия отладки. Проверенные сборки предоставляют проверку ошибок, проверку аргументов и код отладки системы. Дополнительный код в проверяемом двоичном файле создает сообщение об ошибке отладчика ядра и разбивается на отладчик. Это позволяет немедленно определить причину ошибки и ее расположение. На производительность может повлиять в проверенной сборке из-за дополнительного выполняемого кода.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Описание"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

описание операционной системы Windows. Некоторые пользовательские интерфейсы, например, позволяющие изменять это описание, ограничивают его длину до 48 символов.

</dd> <dt>

**Распределенные**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **значение равно true**, операционная система распространяется на несколько узлов системы компьютера. В этом случае эти узлы должны быть сгруппированы как кластер.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**EncryptionLevel**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уровень шифрования для безопасных транзакций: 40-разрядная, 128-разрядная или *n*-разрядная.

<dt>

<span id="40-bit"></span><span id="40-BIT"></span>

**40-разрядная** (0)


</dt> <dd></dd> <dt>

<span id="128-bit"></span><span id="128-BIT"></span>

**128-разрядная** (1)


</dt> <dd></dd> <dt>

<span id="n-bit"></span><span id="N-BIT"></span>

**n-разрядная** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**фореграундаппликатионбуст**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ приоритиконтрол \| Win32PrioritySeparation")
</dt> </dl>

Повышение приоритета назначается для приложения переднего плана. Повышение производительности приложения реализуется путем предоставления приложению дополнительных срезов времени выполнения (длина тактовой задержки).

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (0)


</dt> <dd>

Система увеличивает тактовую длину на 6.

</dd> <dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>**Минимум** (1)


</dt> <dd>

Система увеличивает тактовую длину на 12.

</dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (2)


</dt> <dd>

Система увеличивает тактовую длину на 18.

</dd> </dl>

</dd> <dt>

**фрифисикалмемори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Число (в килобайтах) физической памяти, неиспользуемой и доступной в данный момент.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**фриспацеинпагингфилес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Memory Параметры \| 001,4 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")
</dt> </dl>

Число (в килобайтах), которое можно сопоставить с файлами подкачки операционной системы, не заставляя другие страницы.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**фривиртуалмемори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Число (в килобайтах) виртуальной памяти, неиспользуемой и доступной в данный момент.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Объект Date установлен. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**ларжесистемкаче**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Это свойство устарело и не поддерживается.

<dt>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>

<span id="Optimize_for_Applications"></span><span id="optimize_for_applications"></span><span id="OPTIMIZE_FOR_APPLICATIONS"></span>**Оптимизировать для приложений** (0)


</dt> <dd>

Оптимизируйте память для приложений.

</dd> <dt>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>

<span id="Optimize_for_System_Performance"></span><span id="optimize_for_system_performance"></span><span id="OPTIMIZE_FOR_SYSTEM_PERFORMANCE"></span>**Оптимизировать для производительности системы** (1)


</dt> <dd>

Оптимизируйте память для повышения производительности системы.

</dd> </dl>

</dd> <dt>

**LastBootUpTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время последнего перезапуска операционной системы.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**LocalDateTime**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. В файле IETF \| Host-Resources-MIB. хрсистемдате "," MIF. \|Общие сведения о DMTF \| 001,6 ")
</dt> </dl>

Версия операционной системы для локальной даты и времени суток.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**Локаль**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции поддержки национального языка \| [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) \| язык \_ илангуаже")
</dt> </dl>

Идентификатор языка, используемый операционной системой. Идентификатор языка — это стандартное Международный цифровой сокращенный номер страны или региона. Каждый язык имеет уникальный идентификатор языка (LANGID), 16-разрядное значение, состоящее из основного идентификатора языка и вторичного идентификатора языка.

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Имя производителя операционной системы. для систем на основе Windows это значение равно «корпорация майкрософт».

</dd> <dt>

**макснумберофпроцессес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистеммакспроцессес ")
</dt> </dl>

Максимальное число контекстов процессов, которое может поддерживать операционная система. Значение по умолчанию, заданное поставщиком, — 4294967295 (0xFFFFFFFF). Если фиксированного максимума нет, значение должно быть равно 0 (нулю). В системах с фиксированным максимальным значением этот объект может помочь в диагностике сбоев, возникающих при достижении максимального значения (если неизвестно, введите 4294967295 (0xFFFFFFFF)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**макспроцессмеморисизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Максимальное число (в килобайтах) памяти, которое может быть выделено процессу. Для операционных систем без виртуальной памяти обычно это значение равно общему объему физической памяти за вычетом памяти, используемой BIOS и операционной системой. Для некоторых операционных систем это значение может быть бесконечным, в этом случае следует указать 0 (нуль). В других случаях это значение может быть константой, например 2G или 4G.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**муилангуажес**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

многоязычный пользовательский интерфейс Языки пакета MUI, установленные на компьютере. Например, "en-US". Языки пакета MUI — это файлы ресурсов, которые можно установить в английской версии операционной системы. При установке пакета MUI можно изменить язык пользовательского интерфейса на один из поддерживаемых языков 33.

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Экземпляр операционной системы в системе компьютера.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**нумберофлиценседусерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число пользовательских лицензий для операционной системы. Если значение не ограничено, введите 0 (ноль). Если значение неизвестно, введите-1.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**нумберофпроцессес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемпроцессес ")
</dt> </dl>

Количество контекстов процессов, загруженных или выполняемых в операционной системе в данный момент.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**нумберофусерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIB. \|Основной узел IETF-Resources-MIB. хрсистемнумусерс ")
</dt> </dl>

Число пользовательских сеансов, для которых в настоящее время хранятся сведения о состоянии операционной системы.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**оператингсистемску**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Номер SKU для операционной системы. Эти значения совпадают с константами **Product \_ \** _, определенными в Winnt. h, которые используются с функцией [_ *жетпродуктинфо* *](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .

В следующем списке перечислены возможные значения номера SKU.

<dt>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>

<span id="PRODUCT_UNDEFINED"></span><span id="product_undefined"></span>**Продукт \_ Не ОПРЕДЕЛЕНо** (0)


</dt> <dd>

Не определено.

</dd> <dt>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>

<span id="PRODUCT_ULTIMATE"></span><span id="product_ultimate"></span>**Продукт \_ ULTIMATE** (1)


</dt> <dd>

ultimate Edition, например Windows Vista Ultimate.

</dd> <dt>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>

<span id="PRODUCT_HOME_BASIC"></span><span id="product_home_basic"></span>**Продукт \_ ДОМАШНяя \_ Базовая** (2)


</dt> <dd>

Выпуск Home Basic

</dd> <dt>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>

<span id="PRODUCT_HOME_PREMIUM"></span><span id="product_home_premium"></span>**Продукт \_ ДОМАШНяя \_ Расширенная** (3)


</dt> <dd>

выпуск Home Premium

</dd> <dt>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>

<span id="PRODUCT_ENTERPRISE"></span><span id="product_enterprise"></span>**Продукт \_ ENTERPRISE** (4)


</dt> <dd>

Выпуск Enterprise

</dd> <dt>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>

<span id="PRODUCT_BUSINESS"></span><span id="product_business"></span>**Продукт \_ Бизнес** (6)


</dt> <dd>

Business Edition

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>

<span id="PRODUCT_STANDARD_SERVER"></span><span id="product_standard_server"></span>**Продукт \_ Стандартный \_ сервер** (7)


</dt> <dd>

Windows выпуск Standard сервера (установка возможностей рабочего стола)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>

<span id="PRODUCT_DATACENTER_SERVER"></span><span id="product_datacenter_server"></span>**Продукт \_ Сервер DATACENTER \_ Server** (8)


</dt> <dd>

Windows Server Datacenter Edition (Установка возможностей рабочего стола)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER"></span><span id="product_smallbusiness_server"></span>**Продукт \_ \_Сервер смаллбусинесс** (9)


</dt> <dd>

Выпуск Small Business Server

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>

<span id="PRODUCT_ENTERPRISE_SERVER"></span><span id="product_enterprise_server"></span>**Продукт \_ \_Сервер предприятия** (10)


</dt> <dd>

Enterprise Выпуск сервера

</dd> <dt>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>

<span id="PRODUCT_STARTER"></span><span id="product_starter"></span>**Продукт \_ НАЧАЛЬная** (11)


</dt> <dd>

 Starter Edition

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE"></span><span id="product_datacenter_server_core"></span>**Продукт \_ Ядро DATACENTER \_ Server \_ Core** (12)


</dt> <dd>

Выпуск Datacenter Server Core

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE"></span><span id="product_standard_server_core"></span>**Продукт \_ STANDARD \_ Server \_ Core** (13)


</dt> <dd>

Выпуск Standard Server Core

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE"></span><span id="product_enterprise_server_core"></span>**Продукт \_ ENTERPRISE \_ Server \_ Core** (14)


</dt> <dd>

Enterprise Выпуск Server Core

</dd> <dt>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>

<span id="PRODUCT_WEB_SERVER"></span><span id="product_web_server"></span>**Продукт \_ ВЕБ- \_ сервер** (17)


</dt> <dd>

Выпуск Web Server

</dd> <dt>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>

<span id="PRODUCT_HOME_SERVER"></span><span id="product_home_server"></span>**Продукт \_ ДОМАШНИЙ \_ сервер** (19)


</dt> <dd>

Выпуск Home Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER"></span><span id="product_storage_express_server"></span>**Продукт \_ \_Сервер Storage Express \_ Server** (20)


</dt> <dd>

служба хранилища Выпуск Express Server

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER"></span><span id="product_storage_standard_server"></span>**Продукт \_ \_Стандартный \_ сервер хранилища** (21)


</dt> <dd>

Windows служба хранилища Server выпуск Standard (установка возможностей рабочего стола)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER"></span><span id="product_storage_workgroup_server"></span>**Продукт \_ STORAGE \_ Workgroup \_ Server** (22)


</dt> <dd>

Windows служба хранилища Server Workgroup Edition (установка возможностей рабочего стола)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></span><span id="product_storage_enterprise_server"></span>**Продукт \_ \_Сервер хранилища Enterprise \_ Server** (23)


</dt> <dd>

выпуск служба хранилища Enterprise Server

</dd> <dt>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>

<span id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></span><span id="product_server_for_smallbusiness"></span>**Продукт \_ СЕРВЕР \_ для \_ смаллбусинесс** (24)


</dt> <dd>

Сервер для Small Business Edition

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></span><span id="product_smallbusiness_server_premium"></span>**Продукт \_ СМАЛЛБУСИНЕСС \_ Server \_ Premium** (25)


</dt> <dd>

выпуск Small Business Server Premium Edition

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>

<span id="PRODUCT_ENTERPRISE_N"></span><span id="product_enterprise_n"></span>**Продукт \_ Корпоративный \_ N** (27)


</dt> <dd>

Windows выпуск Enterprise

</dd> <dt>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>

<span id="PRODUCT_ULTIMATE_N"></span><span id="product_ultimate_n"></span>**Продукт \_ ULTIMATE \_ N** (28)


</dt> <dd>

Windows Выпуск Ultimate

</dd> <dt>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>

<span id="PRODUCT_WEB_SERVER_CORE"></span><span id="product_web_server_core"></span>**Продукт \_ \_ \_ Ядро веб-сервера** (29)


</dt> <dd>

Windows Серверный выпуск Web Server (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>

<span id="PRODUCT_STANDARD_SERVER_V"></span><span id="product_standard_server_v"></span>**Продукт \_ Стандартный \_ сервер \_ V** (36)


</dt> <dd>

Windows выпуск Standard сервера без Hyper-V

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_V"></span><span id="product_datacenter_server_v"></span>**Продукт \_ DATACENTER \_ Server \_ V** (37)


</dt> <dd>

Windows Выпуск Server Datacenter без Hyper-V (полная установка)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_V"></span><span id="product_enterprise_server_v"></span>**Продукт \_ ENTERPRISE \_ Server \_ V** (38)


</dt> <dd>

Windows серверная выпуск Enterprise без Hyper-V (полная установка)

</dd> <dt>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>

<span id="PRODUCT_DATACENTER_SERVER_CORE_V"></span><span id="product_datacenter_server_core_v"></span>**Продукт \_ Ядро DATACENTER \_ Server \_ Core \_ V** (39)


</dt> <dd>

Windows Выпуск Server Datacenter без Hyper-V (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>

<span id="PRODUCT_STANDARD_SERVER_CORE_V"></span><span id="product_standard_server_core_v"></span>**Продукт \_ STANDARD \_ Server \_ Core \_ V** (40)


</dt> <dd>

Windows серверная выпуск Standard без Hyper-V (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>

<span id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></span><span id="product_enterprise_server_core_v"></span>**Продукт \_ ENTERPRISE \_ Server \_ Core \_ V** (41)


</dt> <dd>

Windows серверная выпуск Enterprise без Hyper-V (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>

<span id="PRODUCT_HYPERV"></span><span id="product_hyperv"></span>**Продукт \_ HYPERV** (42)


</dt> <dd>

Microsoft Hyper-V Server

</dd> <dt>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>

<span id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></span><span id="product_storage_express_server_core"></span>**Продукт \_ STORAGE \_ Express \_ Server \_ Core** (43)


</dt> <dd>

служба хранилища Server Express Edition (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>

<span id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></span><span id="product_storage_standard_server_core"></span>**Продукт \_ ХРАНИЛИЩЕ \_ Standard \_ Server \_ Core** (44)


</dt> <dd>

служба хранилища выпуск Standard сервера (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>

<span id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></span><span id="product_storage_workgroup_server_core"></span>**Продукт \_ ХРАНИЛИЩЕ \_ Server Workgroup, \_ \_ ядро** (45)


</dt> <dd>

служба хранилища Server Workgroup Edition (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>

<span id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></span><span id="product_storage_enterprise_server_core"></span>**Продукт \_ \_ \_ \_ Ядро хранилища ENTERPRISE Server** (46)


</dt> <dd>

служба хранилища Server Workgroup Edition (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>

<span id="PRODUCT_PROFESSIONAL"></span><span id="product_professional"></span>**Продукт \_ Профессиональная** (48)


</dt> <dd>

Windows Professional

</dd> <dt>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>

<span id="PRODUCT_SB_SOLUTION_SERVER"></span><span id="product_sb_solution_server"></span>**Продукт \_ \_ \_ Сервер решений SB** (50)


</dt> <dd>

Windows Server Essentials (Установка возможностей рабочего стола)

</dd> <dt>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>

<span id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></span><span id="product_smallbusiness_server_premium_core"></span>**Продукт \_ СМАЛЛБУСИНЕСС \_ Server \_ Premium \_ Core** (63)


</dt> <dd>

Small Business server Premium (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>

<span id="PRODUCT_CLUSTER_SERVER_V"></span><span id="product_cluster_server_v"></span>**Продукт \_ Сервер КЛАСТЕРов версии \_ \_ V** (64)


</dt> <dd>

Windows Сервер вычислений кластера без Hyper-V

</dd> <dt>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>

<span id="PRODUCT_CORE_ARM"></span><span id="product_core_arm"></span>**Продукт \_ ЯДЕРная \_ ARM** (97)


</dt> <dd>

Windows RT

</dd> <dt>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>

<span id="PRODUCT_CORE"></span><span id="product_core"></span>**Продукт \_ ЯДРО** (101)


</dt> <dd>

Windows Домом

</dd> <dt>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>

<span id="PRODUCT_PROFESSIONAL_WMC"></span><span id="product_professional_wmc"></span>**Продукт \_ Профессиональная \_ WMC** (103)


</dt> <dd>

Windows Professional с Media Center

</dd> <dt>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>

<span id="PRODUCT_MOBILE_CORE"></span><span id="product_mobile_core"></span>**Продукт \_ Мобильные \_ ядра** (104)


</dt> <dd>

Windows Mobile

</dd> <dt>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>

<span id="PRODUCT_IOTUAP"></span><span id="product_iotuap"></span>**Продукт \_ ИОТУАП** (123)


</dt> <dd>

Windows Основные компоненты IoT (Интернет вещей)

</dd> <dt>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>

<span id="PRODUCT_DATACENTER_NANO_SERVER"></span><span id="product_datacenter_nano_server"></span>**Продукт \_ \_Nano \_ Server datacenter** (143)


</dt> <dd>

Windows Server Datacenter Edition (установка Nano Server)

</dd> <dt>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>

<span id="PRODUCT_STANDARD_NANO_SERVER"></span><span id="product_standard_nano_server"></span>**Продукт \_ Стандартный \_ Nano \_ SERVER** (144)


</dt> <dd>

Windows серверная выпуск Standard (установка Nano Server)

</dd> <dt>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>

<span id="PRODUCT_DATACENTER_WS_SERVER_CORE"></span><span id="product_datacenter_ws_server_core"></span>**Продукт \_ Ядро DATACENTER \_ WS \_ Server \_ Core** (147)


</dt> <dd>

Windows Server Datacenter Edition (установка основных серверных компонентов)

</dd> <dt>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>

<span id="PRODUCT_STANDARD_WS_SERVER_CORE"></span><span id="product_standard_ws_server_core"></span>**Продукт \_ СТАНДАРТНОЕ \_ \_ \_ ядро WS Server** (148)


</dt> <dd>

Windows выпуск Standard сервера (установка основных серверных компонентов)

</dd> </dl>

</dd> <dt>

**Организация**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows \\ \\ CurrentVersion \| RegisteredOrganization")
</dt> </dl>

Название компании для зарегистрированного пользователя операционной системы.

Пример: "Корпорация Майкрософт"

</dd> <dt>

**OSArchitecture**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Архитектура операционной системы, в отличие от процессора. Это свойство может быть локализовано.

Пример: 32-bit

</dd> <dt>

**OSLanguage**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| умолчанию панель управления" язык и \\ \\ \\ \\ региональные \| стандарты ")
</dt> </dl>

Языковая версия установленной операционной системы. В следующем списке перечислены возможные значения. Пример: 0x0807 (немецкий, Швейцария).

<dt>

1 (0x1)
</dt> <dd>

Арабский

</dd> <dt>

4 (0x4)
</dt> <dd>

Китайский (упрощенное письмо) — Китай

</dd> <dt>

9 (0x9)
</dt> <dd>

Английский

</dd> <dt>

1025 (0x401)
</dt> <dd>

Арабский — Саудовская Аравия

</dd> <dt>

1026 (0x402)
</dt> <dd>

Болгарский

</dd> <dt>

1027 (0x403)
</dt> <dd>

Каталонский

</dd> <dt>

1028 (0x404)
</dt> <dd>

Китайский (традиционное письмо) — Тайвань

</dd> <dt>

1029 (0x405)
</dt> <dd>

Чешский

</dd> <dt>

1030 (0x406)
</dt> <dd>

Датский

</dd> <dt>

1031 (0x407)
</dt> <dd>

Немецкий (Германия)

</dd> <dt>

1032 (0x408)
</dt> <dd>

Греческий

</dd> <dt>

1033 (0x409)
</dt> <dd>

Английский — США

</dd> <dt>

1034 (0x40A)
</dt> <dd>

Испанский — традиционная сортировка

</dd> <dt>

1035 (0x40B)
</dt> <dd>

Финский

</dd> <dt>

1036 (0x40C)
</dt> <dd>

Французский (Франция)

</dd> <dt>

1037 (0x40D)
</dt> <dd>

Иврит

</dd> <dt>

1038 (0x40E)
</dt> <dd>

Венгерский

</dd> <dt>

1039 (0x40F)
</dt> <dd>

Исландский

</dd> <dt>

1040 (0x410)
</dt> <dd>

Итальянский (Италия)

</dd> <dt>

1041 (0x411)
</dt> <dd>

Японский

</dd> <dt>

1042 (0x412)
</dt> <dd>

Корейский

</dd> <dt>

1043 (0x413)
</dt> <dd>

Голландский (Нидерланды)

</dd> <dt>

1044 (0x414)
</dt> <dd>

Норвежский — букмол

</dd> <dt>

1045 (0x415)
</dt> <dd>

Польский

</dd> <dt>

1046 (0x416)
</dt> <dd>

Португальский (Бразилия)

</dd> <dt>

1047 (0x417)
</dt> <dd>

Rhaeto-Romanic

</dd> <dt>

1048 (0x418)
</dt> <dd>

Румынский

</dd> <dt>

1049 (0x419)
</dt> <dd>

Русский

</dd> <dt>

1050 (0x41A)
</dt> <dd>

Хорватский

</dd> <dt>

1051 (0x41B)
</dt> <dd>

Словацкий

</dd> <dt>

1052 (0x41C)
</dt> <dd>

Албанский

</dd> <dt>

1053 (0x41D)
</dt> <dd>

Шведский

</dd> <dt>

1054 (0x41E)
</dt> <dd>

Тайский

</dd> <dt>

1055 (0x41F)
</dt> <dd>

Турецкий

</dd> <dt>

1056 (0x420)
</dt> <dd>

Урду

</dd> <dt>

1057 (0x421)
</dt> <dd>

Индонезийский

</dd> <dt>

1058 (0x422)
</dt> <dd>

Украинский

</dd> <dt>

1059 (0x423)
</dt> <dd>

Белорусский

</dd> <dt>

1060 (0x424)
</dt> <dd>

Словенский

</dd> <dt>

1061 (0x425)
</dt> <dd>

Эстонский

</dd> <dt>

1062 (0x426)
</dt> <dd>

Латышский

</dd> <dt>

1063 (0x427)
</dt> <dd>

Литовский

</dd> <dt>

1065 (0x429)
</dt> <dd>

Персидский

</dd> <dt>

1066 (0x42A)
</dt> <dd>

Вьетнамский

</dd> <dt>

1069 (0x42D)
</dt> <dd>

Баскский

</dd> <dt>

1070 (0x42E)
</dt> <dd>

Сербский

</dd> <dt>

1071 (0x42F)
</dt> <dd>

Македонский (Северная Македония)

</dd> <dt>

1072 (0x430)
</dt> <dd>

суту

</dd> <dt>

1073 (0x431)
</dt> <dd>

Тсонга

</dd> <dt>

1074 (0x432)
</dt> <dd>

Тсвана

</dd> <dt>

1076 (0x434)
</dt> <dd>

Коса

</dd> <dt>

1077 (0x435)
</dt> <dd>

Зулу

</dd> <dt>

1078 (0x436)
</dt> <dd>

Африкаанс

</dd> <dt>

1080 (0x438)
</dt> <dd>

Фарерского

</dd> <dt>

1081 (0x439)
</dt> <dd>

Hindi

</dd> <dt>

1082 (0x43A)
</dt> <dd>

Мальтийский

</dd> <dt>

1084 (0x43C)
</dt> <dd>

Шотландский гэльский (Великобритания)

</dd> <dt>

1085 (0x43D)
</dt> <dd>

Идиш

</dd> <dt>

1086 (со значением 0x43e)
</dt> <dd>

Малайский — Малайзия

</dd> <dt>

2049 (0x801)
</dt> <dd>

Арабский — Ирак

</dd> <dt>

2052 (0x804)
</dt> <dd>

Китайский (упрощенное письмо) — КНР

</dd> <dt>

2055 (0x807)
</dt> <dd>

Немецкий — Швейцария

</dd> <dt>

2057 (0x809)
</dt> <dd>

Английский — Великобритания

</dd> <dt>

2058 (0x80)
</dt> <dd>

Испанский — Мексика

</dd> <dt>

2060 (0x80C)
</dt> <dd>

Французский — Бельгия

</dd> <dt>

2064 (0x810)
</dt> <dd>

Итальянский — Швейцария

</dd> <dt>

2067 (0x813)
</dt> <dd>

Голландский — Бельгия

</dd> <dt>

2068 (0x814)
</dt> <dd>

Норвежский — нюнорск

</dd> <dt>

2070 (0x816)
</dt> <dd>

Португальский (Португалия)

</dd> <dt>

2072 (0x818)
</dt> <dd>

Румынский — Молдова

</dd> <dt>

2073 (0x819)
</dt> <dd>

Русский — Молдова

</dd> <dt>

2074 (0x81A)
</dt> <dd>

Сербский — латиница

</dd> <dt>

2077 (0x81D)
</dt> <dd>

Шведский — Финляндия

</dd> <dt>

3073 (0xC01)
</dt> <dd>

Арабский — Египет

</dd> <dt>

3076 (0xC04)
</dt> <dd>

Китайский (традиционное письмо) — Гонконг Гонконг

</dd> <dt>

3079 (0xC07)
</dt> <dd>

Немецкий — Австрия

</dd> <dt>

3081 (0xC09)
</dt> <dd>

Английский — Австралия

</dd> <dt>

3082 (0xC0A)
</dt> <dd>

Испанский — Международная сортировка

</dd> <dt>

3084 (0xC0C)
</dt> <dd>

Французский — Канада

</dd> <dt>

3098 (0xC1A)
</dt> <dd>

Сербский — кириллица

</dd> <dt>

4097 (0x1001)
</dt> <dd>

Арабский — Ливия

</dd> <dt>

4100 (0x1004)
</dt> <dd>

Китайский (упрощенное письмо) — Сингапур

</dd> <dt>

4103 (0x1007)
</dt> <dd>

Немецкий — Люксембург

</dd> <dt>

4105 (0x1009)
</dt> <dd>

Английский — Канада

</dd> <dt>

4106 (0x100A)
</dt> <dd>

Испанский — Гватемала

</dd> <dt>

4108 (0x100C)
</dt> <dd>

Французский — Швейцария

</dd> <dt>

5121 (0x1401)
</dt> <dd>

Арабский — Алжир

</dd> <dt>

5127 (0x1407)
</dt> <dd>

Немецкий — Лихтенштейн

</dd> <dt>

5129 (0x1409)
</dt> <dd>

Английский — Новая Зеландия

</dd> <dt>

5130 (0x140A)
</dt> <dd>

Испанский — Коста-Рика

</dd> <dt>

5132 (0x140C)
</dt> <dd>

Французский — Люксембург

</dd> <dt>

6145 (0x1801)
</dt> <dd>

Арабский — Марокко

</dd> <dt>

6153 (0x1809)
</dt> <dd>

Английский — Ирландия

</dd> <dt>

6154 (0x180A)
</dt> <dd>

Испанский — Панама

</dd> <dt>

7169 (0x1C01)
</dt> <dd>

Арабский — Тунис

</dd> <dt>

7177 (0x1C09)
</dt> <dd>

Английский — Южная Африка

</dd> <dt>

7178 (0x1C0A)
</dt> <dd>

Испанский — Доминиканская Республика

</dd> <dt>

8193 (0x2001)
</dt> <dd>

Арабский — Оман

</dd> <dt>

8201 (0x2009)
</dt> <dd>

Английский — Ямайка

</dd> <dt>

8202 (0x200A)
</dt> <dd>

Испанский — Венесуэла

</dd> <dt>

9217 (0x2401)
</dt> <dd>

Арабский — Йемен

</dd> <dt>

9226 (0x240A)
</dt> <dd>

Испанский — Колумбия

</dd> <dt>

10241 (0x2801)
</dt> <dd>

Арабский — Сирия

</dd> <dt>

10249 (0x2809)
</dt> <dd>

Английский — Белиз

</dd> <dt>

10250 (0x280A)
</dt> <dd>

Испанский — Перу

</dd> <dt>

11265 (0x2C01)
</dt> <dd>

Арабский — Иордания

</dd> <dt>

11273 (0x2C09)
</dt> <dd>

Английский — Тринидад

</dd> <dt>

11274 (0x2C0A)
</dt> <dd>

Испанский — Аргентина

</dd> <dt>

12289 (0x3001)
</dt> <dd>

Арабский — Ливан

</dd> <dt>

12298 (0x300A)
</dt> <dd>

Испанский — Эквадор

</dd> <dt>

13313 (0x3401)
</dt> <dd>

Арабский — Кувейт

</dd> <dt>

13322 (0x340A)
</dt> <dd>

Испанский — Чили

</dd> <dt>

14337 (0x3801)
</dt> <dd>

Арабский — ОАЭ

</dd> <dt>

14346 (0x380A)
</dt> <dd>

Испанский — Уругвай

</dd> <dt>

15361 (0x3C01)
</dt> <dd>

Арабский — Бахрейн

</dd> <dt>

15370 (0x3C0A)
</dt> <dd>

Испанский — Парагвай

</dd> <dt>

16385 (0x4001)
</dt> <dd>

Арабский — Катар

</dd> <dt>

16394 (0x400A)
</dt> <dd>

Испанский — Боливия

</dd> <dt>

17418 (0x440A)
</dt> <dd>

Испанский — Эль-Сальвадор

</dd> <dt>

18442 (0x480A)
</dt> <dd>

Испанский — Гондурас

</dd> <dt>

19466 (0x4C0A)
</dt> <dd>

Испанский — Никарагуа

</dd> <dt>

20490 (0x500A)
</dt> <dd>

Испанский — Пуэрто-Рико

</dd> </dl>

</dd> <dt>

**OSProductSuite**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control \\ \\ продуктоптионс \| продуктсуите"), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("малый бизнес", "Enterprise", "backoffice", "коммуникационный сервер", "сервер терминалов", "малый бизнес (ограниченный)", "Embedded NT", "центр обработки данных")
</dt> </dl>

Установленные и лицензированные дополнения системных продуктов в операционной системе. например, значение 146 (0x92) для **оспродуктсуите** указывает Enterprise, службы терминалов и центр обработки данных (биты 1, 4 и семь наборов). В следующем списке перечислены возможные значения.

<dt>

1 (0x1)
</dt> <dd>

Microsoft Small Business Server был установлен, но может быть обновлен до другой версии Windows.

</dd> <dt>

2 (0x2)
</dt> <dd>

Windows сервер 2008 Enterprise установлен.

</dd> <dt>

4 (0x4)
</dt> <dd>

Windows Компоненты BackOffice установлены.

</dd> <dt>

8 (0x8)
</dt> <dd>

Коммуникационный сервер установлен.

</dd> <dt>

16 (0x10)
</dt> <dd>

Службы терминалов установлены.

</dd> <dt>

32 (0x20)
</dt> <dd>

Microsoft Small Business Server устанавливается с помощью клиентской лицензии с лицензией.

</dd> <dt>

64 (0x40)
</dt> <dd>

Windows Внедрена установка.

</dd> <dt>

128 (0x80)
</dt> <dd>

Установлен выпуск Datacenter.

</dd> <dt>

256 (0x100)
</dt> <dd>

Службы терминалов установлены, но поддерживается только один интерактивный сеанс.

</dd> <dt>

512 (0x200)
</dt> <dd>

Windows Установлен выпуск Home Edition.

</dd> <dt>

1024 (0x400)
</dt> <dd>

Установлен выпуск Web Server.

</dd> <dt>

8192 (0x2000)
</dt> <dd>

служба хранилища Установлен выпуск Server.

</dd> <dt>

16384 (0x4000)
</dt> <dd>

Установлен выпуск Compute Cluster Edition.

</dd> </dl>

</dd> <dt>

**OSType**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**система \_ CIM**](cim-operatingsystem.md)".**Осертипедескриптион**")
</dt> </dl>

Тип операционной системы. В следующем списке указаны возможные значения.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span id="MACOS"></span><span id="macos"></span>**MACOS** (2)


</dt> <dd>

МАКРОКОМАНД

</dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span id="ATTUNIX"></span><span id="attunix"></span>**Аттуникс** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span id="DGUX"></span><span id="dgux"></span>**Дгукс** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span id="DECNT"></span><span id="decnt"></span>**Декнт** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>**Цифровая UNIX** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>**Опенвмс** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span id="HPUX"></span><span id="hpux"></span>**Hpux** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span id="AIX"></span><span id="aix"></span>**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span id="MVS"></span><span id="mvs"></span>**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span id="OS400"></span><span id="os400"></span>**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span id="OS_2"></span><span id="os_2"></span>**ОС/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>**Жававм** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span id="MSDOS"></span><span id="msdos"></span>**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span id="WIN95"></span><span id="win95"></span>**Win95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span id="WIN98"></span><span id="win98"></span>**Win98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span id="WINNT"></span><span id="winnt"></span>**WinNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span id="WINCE"></span><span id="wince"></span>**Wince** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span id="NCR3000"></span><span id="ncr3000"></span>**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span id="OSF"></span><span id="osf"></span>**Использование** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span id="DC_OS"></span><span id="dc_os"></span>**DC/OS** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>**зависящие UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>**SCO опенсервер** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>**Секуент** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span id="IRIX"></span><span id="irix"></span>**Ирикс** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>**Solaris** (29)


</dt> <dd>

Solaris

</dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>**Сунос** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span id="U6000"></span><span id="u6000"></span>**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span id="ASERIES"></span><span id="aseries"></span>**Асериес** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>**Тандемнск** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>**Тандемнт** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span id="BS2000"></span><span id="bs2000"></span>**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span id="LINUX"></span><span id="linux"></span>**Linux** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>**Линкс** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span id="XENIX"></span><span id="xenix"></span>**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span id="VM_ESA"></span><span id="vm_esa"></span>**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>**интерактивный UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span id="BSDUNIX"></span><span id="bsdunix"></span>**Бсдуникс** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>**Нетбсд** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>**GNU Хурд** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span id="OS9"></span><span id="os9"></span>**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>**Ядро машинного ядра** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>**Inferno адский** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span id="QNX"></span><span id="qnx"></span>**Кнкс** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span id="EPOC"></span><span id="epoc"></span>**Епок** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>**Иксворкс** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>**Вксворкс** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>**Mint** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>**Беос** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span id="HP_MPE"></span><span id="hp_mpe"></span>**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>**NeXTSTEP** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>**Палмпилот** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>**Рапсодии** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Выделенный** (59)


</dt> <dd></dd> <dt>

<span id="OS_390"></span><span id="os_390"></span>

<span id="OS_390"></span><span id="os_390"></span>**ОС/390** (60)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span id="VSE"></span><span id="vse"></span>**VSE** (61)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span id="TPF"></span><span id="tpf"></span>**ТПФ** (62)


</dt> <dd></dd> </dl>

</dd> <dt>

**осертипедескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**Моделкорреспонденце**](../wmisdk/standard-qualifiers.md) ("[**модель \_ CIM**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Дополнительное описание текущей версии операционной системы.

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**паинаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

При **значении true** расширения физических адресов (PAE) включаются операционной системой, работающей на процессорах Intel. PAE позволяет приложениям обращаться к более чем 4 ГБ физической памяти. При включении PAE операционная система использует линейное преобразование адресов трех уровней, а не два уровня. Предоставление приложению большего объема физической памяти снижает необходимость перекачки памяти в файл подкачки и повышает производительность. Чтобы включить, PAE, используйте параметр "/PAE" в файле Boot.ini. Дополнительные сведения о расширении физических адресов см. в разделе <https://Go.Microsoft.Com/FWLink/p/?LinkID=45912> .

</dd> <dt>

**плуспродуктид**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! ProductId ")
</dt> </dl>

Не поддерживается.

</dd> <dt>

**плусверсионнумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| Plus! VersionNumber ")
</dt> </dl>

Не поддерживается.

</dd> <dt>

**портаблеоператингсистем**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, загружена ли операционная система с внешнего USB-устройства. Если значение равно true, операционная система обнаружила, что она загружается на поддерживаемом локально подключенном запоминающем устройстве.

**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** это свойство не поддерживается до Windows 8 и Windows Server 2012.

</dd> <dt>

**Источник**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Указывает, является ли это основной операционной системой.

</dd> <dt>

**продукттипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополнительные сведения о системе.

<dt>

<span id="Work_Station"></span><span id="work_station"></span><span id="WORK_STATION"></span>

**Рабочая станция** (1)


</dt> <dd></dd> <dt>

<span id="Domain_Controller"></span><span id="domain_controller"></span><span id="DOMAIN_CONTROLLER"></span>

**Контроллер домена** (2)


</dt> <dd></dd> <dt>

<span id="Server"></span><span id="server"></span><span id="SERVER"></span>

**Сервер** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**куантумленгс**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ приоритиконтрол \| Win32PrioritySeparation")
</dt> </dl>

Не поддерживается

* * Windows Server 2008 и Windows Vista: * *

Свойство **куантумленгс** определяет число тактов часов в такте. Такт — это единица времени выполнения, которую планировщик может предоставить приложению, прежде чем переходить к другим приложениям. Когда поток запускается в течение одного такта, ядро загружает его и перемещает в конец очереди для приложений с равными приоритетами. фактическая длина такта потока различается в разных Windowsных платформах. только для Windows NT/Windows 2000.

Возможные значения:.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="One_tick"></span><span id="one_tick"></span><span id="ONE_TICK"></span>

**Один такт** (1)


</dt> <dd></dd> <dt>

<span id="Two_ticks"></span><span id="two_ticks"></span><span id="TWO_TICKS"></span>

**Два кванта** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**куантумтипе**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Не поддерживается

* * Windows Server 2008 и Windows Vista: * *

Свойство **куантумтипе** указывает либо фиксированные, либо такты переменной длины. Windows значение по умолчанию — такты переменной длины, где приложение переднего плана имеет более длительный такт, чем фоновые приложения. Windows Сервер по умолчанию принимает такты фиксированной длины. Такт — это единица времени выполнения, которую планировщик может предоставить приложению перед переключением на другое приложение. Когда поток запускается в течение одного такта, ядро загружает его и перемещает в конец очереди для приложений с равными приоритетами. фактическая длина такта потока различается в разных Windowsных платформах.

Возможные значения:.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Исправлено** (1)


</dt> <dd></dd> <dt>

<span id="Variable"></span><span id="variable"></span><span id="VARIABLE"></span>

**Переменная** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**регистередусер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| регистередовнер")
</dt> </dl>

Имя зарегистрированного пользователя операционной системы.

Пример: "Бен Смит"

</dd> <dt>

**Номер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \| ProductId")
</dt> </dl>

Серийный идентификационный номер продукта операционной системы.

Пример: "10497-OEM-0031416-71674"

</dd> <dt>

**сервицепаккмажорверсион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе структуры \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **всервицепаккмажор**")
</dt> </dl>

Основной номер версии пакета обновления, установленного в системе компьютера. Если пакет обновления не установлен, значение равно 0 (ноль).

</dd> <dt>

**сервицепаккминорверсион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе структуры \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| **всервицепаккминор**")
</dt> </dl>

Дополнительный номер версии пакета обновления, установленного в системе компьютера. Если пакет обновления не установлен, значение равно 0 (ноль).

</dd> <dt>

**сизесторединпагингфилес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| Memory Параметры \| 001,3 "), [**единицы**](../wmisdk/standard-qualifiers.md) (" килобайтах ")
</dt> </dl>

Общее число килобайтов, которые могут храниться в файлах подкачки операционной системы — 0 (ноль) указывает на отсутствие файлов подкачки. Имейте в виду, что это число не представляет фактический физический размер файла подкачки на диске.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например, жесткий диск с поддержкой SMART может работать правильно, но прогнозирует сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Состояние службы применяется к административной работе, например к зеркальному переносу диска, перезагрузке списка разрешений пользователя или другой административной работе. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

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

**суитемаск**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**битовые карты**](../wmisdk/standard-qualifiers.md) ("0", "1", "2", "3", "4", "5", "6", "7", "8", "9", "10"), [**битвалуес**](../wmisdk/standard-qualifiers.md) ("Windows Server, Small Business Edition", "Windows server, выпуск Enterprise", "Windows server, backoffice edition", "Windows Server, Communications edition", "службы терминалов майкрософт", "Windows server, Small Business edition ограничен", "Windows Embedded", "Windows server, datacenter edition", "один пользователь", "Windows Home Edition", "Windows server, Web Edition")
</dt> </dl>

Битовые флаги, которые обозначают наборы продуктов, доступные в системе.

Например, чтобы указать как личное, так и BackOffice, задайте для **суитемаск** значение `4 | 512` или `516` .

<dt>

1
</dt> <dd>

Малый бизнес

</dd> <dt>

2
</dt> <dd>

Предприятие

</dd> <dt>

4
</dt> <dd>

BackOffice

</dd> <dt>

8
</dt> <dd>

Коммуникации

</dd> <dt>

16
</dt> <dd>

Службы терминалов

</dd> <dt>

32
</dt> <dd>

Ограничено малым предприятием

</dd> <dt>

64
</dt> <dd>

Выпуск Embedded

</dd> <dt>

128
</dt> <dd>

Datacenter Edition

</dd> <dt>

256
</dt> <dd>

Один пользователь

</dd> <dt>

512
</dt> <dd>

Выпуск Home Edition

</dd> <dt>

1024
</dt> <dd>

Выпуск Web Server

</dd> </dl>

</dd> <dt>

**системдевице**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| функции реестра Win32API \| [**жетприватепрофилестринг**](/windows/win32/api/winbase/nf-winbase-getprivateprofilestring) \| paths \| целевое устройство")
</dt> </dl>

Раздел физического диска, на котором установлена операционная система.

</dd> <dt>

**системдиректори**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе functions [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya))
</dt> </dl>

Системный каталог операционной системы.

Пример: "C: \\ Windows \\ System32"

</dd> <dt>

**SystemDrive**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Буква диска, на котором находится операционная система. Пример: "C:"

</dd> <dt>

**тоталсвапспацесизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Общий объем области подкачки в килобайтах. Это значение может быть **равно NULL** (не указано), если область подкачки не отличается от файлов страниц. Однако некоторые операционные системы отличают эти понятия. например, в UNIX все процессы можно переключать, когда список свободных страниц опускается и остается ниже заданного значения.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**тоталвиртуалмеморисизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Число (в килобайтах) виртуальной памяти. Например, это можно рассчитать, добавив общий объем ОЗУ к объему пространства для разбиения на страницы, то есть добавив объем памяти, выданный компьютером или агрегированный системой, в свойство **сизесторединпагингфилес**.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**тоталвисиблемеморисизе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**единицы**](../wmisdk/standard-qualifiers.md) ("килобайтах")
</dt> </dl>

Общий объем физической памяти, доступной операционной системе, в килобайтах. Это значение не обязательно указывает на истинный объем физической памяти, но сообщает операционной системе, как она доступна.

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).

Это свойство наследуется от системы [**CIM \_**](cim-operatingsystem.md).

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**Override**](../wmisdk/standard-qualifiers.md) ("версия"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе структуры \| [**осверсионинфоекс**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) \| двмажорверсион, двминорверсион")
</dt> </dl>

Номер версии операционной системы.

Пример: "4,0"

</dd> <dt>

**WindowsDirectory**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Сведения о системе functions \| [**жетвиндовсдиректори**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)")
</dt> </dl>

Windows каталог операционной системы.

Пример: "C: \\ Windows"

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ операционной** системы является производным [**от \_ модели CIM**](cim-operatingsystem.md).

любая операционная система, которая может быть установлена на компьютере, на котором может работать операционная система на основе Windows, является потомком или членом этого класса. **Win32 \_ Операционная** система — это одноэлементный класс. Чтобы получить единственный экземпляр, используйте "@" для ключа.

В отличие от большинства других классов WMI, создаваемых MgmtClassGen, метод **. CreateInstance**() возвратит пустой объект **операционной** системы. Поэтому, если вы используете C \# с MgmtClassGen, можно использовать следующий код:


```CSharp
WMI.OperatingSystem os = new ROOT.CIMV2.win32.OperatingSystem();
```



## <a name="examples"></a>Примеры

Пример на языке VBScript, который получает данные о операционной системе и процессоре из [**Win32 \_ ComputerSystem**](win32-computersystem.md), [**\_ процессора Win32**](win32-processor.md)и Win32 Operating, можно найти в примерах, посвященных [**\_ процессору Win32**](win32-processor.md) . **\_**

в разделе [создание отчетов о среде Exchange с помощью powershell](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Generate-Exchange-2388e7c9) powershell в коллекции TechNet используется класс **\_ операционной системы Win32** для создания отчетов среды Exchange.

Пример " [Получение времени работы сервера с помощью WMI](https://Gallery.TechNet.Microsoft.Com/Get-Server-Uptime-Using-WMI-15aaa8ac) " в коллекции TechNet использует свойство **LastBootupTime** , чтобы определить, как долго работает сервер. В этом примере также используется параметр timeout, чтобы предотвратить зависание вызова WMI.

Пример кода VBScript для надстройки [WMI](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) в коллекции TechNet использует класс операционной системы **Win32 \_** для получения сведений о ОС с нескольких удаленных компьютеров.

Следующий скрипт получает экземпляры **Win32 \_ операционной** системы в пространстве имен root CIMv2 по умолчанию \\ , а затем отображает сведения об операционной системе.


```VB
On Error Resume Next
' Connect to WMI and obtain instances of Win32_OperatingSystem
For Each objOS in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

WScript.Echo "Name = " & objOS.Caption & "Version = " & objOS.Version &VBCR _
           & "Registered User = " & objOS.RegisteredUser &VBCR _
           & "Manufacturer = " & objOS.Manufacturer      
Next

if Err <> 0 Then
    WScript.Echo Err.Description
    Err.Clear
End if
```



В следующем образце кода PowerShell отображаются все рабочие сведения о текущей ОС.


```PowerShell
# get instance
$os = Get-WmiObject Win32_OperatingSystem

# output information:
"The class has {0} properties" -f $os.properties.count
"Details on this class:"
$os | Format-List *
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Операционная система CIM \_**](cim-operatingsystem.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[Задачи WMI: операционные системы](../wmisdk/wmi-tasks--operating-systems.md)
</dt> <dt>

[Задачи WMI: оборудование компьютера](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> <dt>

[Задачи WMI: управление рабочим столом](../wmisdk/wmi-tasks--desktop-management.md)
</dt> </dl>

 

 
