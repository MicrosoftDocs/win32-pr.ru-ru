---
description: Представляет системный драйвер для базовой службы.
ms.assetid: 67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2
ms.tgt_platform: multiple
title: Класс Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver
- Win32_SystemDriver.AcceptPause
- Win32_SystemDriver.AcceptStop
- Win32_SystemDriver.Caption
- Win32_SystemDriver.CreationClassName
- Win32_SystemDriver.Description
- Win32_SystemDriver.DesktopInteract
- Win32_SystemDriver.DisplayName
- Win32_SystemDriver.ErrorControl
- Win32_SystemDriver.ExitCode
- Win32_SystemDriver.InstallDate
- Win32_SystemDriver.Name
- Win32_SystemDriver.PathName
- Win32_SystemDriver.ServiceSpecificExitCode
- Win32_SystemDriver.ServiceType
- Win32_SystemDriver.Started
- Win32_SystemDriver.StartMode
- Win32_SystemDriver.StartName
- Win32_SystemDriver.State
- Win32_SystemDriver.Status
- Win32_SystemDriver.SystemCreationClassName
- Win32_SystemDriver.SystemName
- Win32_SystemDriver.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7533e5d1e842e6794a9f9c386103b781afa0404ee181354c420770358f7e8a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751224"
---
# <a name="win32_systemdriver-class"></a>\_Класс Win32 SystemDriver

 [Класс WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriver для Win32** представляет системный драйвер для базовой службы.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4C5-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemDriver : Win32_BaseService
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ SystemDriver** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ SystemDriver** содержит следующие методы.



| Метод                                                                              | Описание                                                                                     |
|:------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Изменение**](change-method-in-class-win32-systemdriver.md)                         | Метод класса, который изменяет службу.<br/>                                                |
| [**чанжестартмоде**](changestartmode-method-in-class-win32-systemdriver.md)       | Метод класса, который изменяет режим запуска службы.<br/>                              |
| [**Создание**](create-method-in-class-win32-systemdriver.md)                         | Метод класса, который создает новую службу.<br/>                                             |
| [**Удален**](delete-method-in-class-win32-systemdriver.md)                         | Метод класса, который удаляет существующую службу.<br/>                                       |
| [**интеррогатесервице**](interrogateservice-method-in-class-win32-systemdriver.md) | Метод класса, запрашивающий обновление состояния службы до Service Manager.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-systemdriver.md)             | Метод класса, который пытается перевести службу в приостановленное состояние.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-systemdriver.md)           | Метод класса, который пытается перевести службу в состояние возобновления.<br/>                |
| [**StartService**](startservice-method-in-class-win32-systemdriver.md)             | Метод класса, который пытается перевести службу в состояние запуска.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-systemdriver.md)               | Метод класса, который помещает службу в остановленное состояние.<br/>                           |
| [**усерконтролсервице**](usercontrolservice-method-in-class-win32-systemdriver.md) | Метод класса, который пытается отправить в службу определяемый пользователем код элемента управления.<br/>         |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ SystemDriver** имеет следующие свойства.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает паузу")
</dt> </dl>

Служба может быть приостановлена.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает" останавливается ").
</dt> </dl>

Служба может быть остановлена.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Краткое описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя класса")
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

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

**DesktopInteract**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("взаимодействует с Desktop")
</dt> </dl>

Эта служба может создавать Windows на рабочем столе и взаимодействовать с ними.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("отображаемое имя")
</dt> </dl>

Отображаемое имя службы. Максимальная длина этой строки равна 256 символам. В диспетчере управления службами имя сохраняется с учетом регистра. В сравнениях **DisplayName** всегда учитывается регистр.

Ограничения: принимает то же значение, что и свойство **Name** .

Пример: "Атдиск"

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("серьезность сбоя при запуске")
</dt> </dl>

Серьезность ошибки, если не удается запустить службу во время запуска. Это значение указывает на действие, предпринимаемое программой запуска, если происходит сбой. Все ошибки записываются в журнал системой компьютера.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")


</dt> <dd>

Пользователь не получает уведомление.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")


</dt> <dd>

Пользователь получает уведомление.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")


</dt> <dd>

Система перезапускается в последней известной рабочей конфигурации.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")


</dt> <dd>

Попытка перезапустить систему в рабочей конфигурации.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")


</dt> <dd>

Причина сбоя неизвестна.

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("код выхода")
</dt> </dl>

Windows код ошибки, определяющий проблемы при запуске или остановке службы. Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** . Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")
</dt> </dl>

Объект был установлен. Для этого свойства не требуется значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](../wmisdk/key-qualifier.md)
</dt> </dl>

Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях. Эти функциональные возможности более подробно описаны в свойстве **Описание** объекта.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя пути к файлу")
</dt> </dl>

Полный путь к двоичному файлу службы, реализующему службу.

Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**сервицеспеЦифицекситкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("специфический для сервера код выхода")
</dt> </dl>

Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы. Коды выхода определяются службой, представленной этим классом. Это значение задается только в том случае, если значение свойства **ExitCode** — ошибка, связанная со **\_ службой ошибок \_ \_** (1066).

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("тип службы")
</dt> </dl>

Тип службы, предоставленной для вызывающих процессов.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

Значения качества производительности:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Драйвер ядра** ("драйвер ядра")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Драйвер файловой системы** ("драйвер файловой системы")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Адаптер** ("адаптер")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Драйвер распознавателя** ("драйвер распознавателя")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Собственный процесс** ("собственный процесс")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Общий процесс** ("общий процесс")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Интерактивный процесс** (интерактивный процесс)


</dt> <dd></dd> </dl>

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")
</dt> </dl>

Служба запущена.

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

Режим запуска драйвера системы.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Boot** (Загрузка)


</dt> <dd>

Драйвер устройства запущен загрузчиком операционной системы (действует только для служб драйверов).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")


</dt> <dd>

Драйвер устройства запущен процессом инициализации операционной системы. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Авто** ("Auto")


</dt> <dd>

Служба запускается автоматически диспетчером управления службами во время запуска системы.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")


</dt> <dd>

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-systemdriver.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")


</dt> <dd>

Служба, которая больше не может быть запущена.

</dd> </dl>

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("начальное имя учетной записи")
</dt> </dl>

Имя учетной записи, под которой выполняется служба. В зависимости от типа службы имя учетной записи может иметь формат имя_домена \\ имя пользователя. Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске. Если учетная запись принадлежит к встроенному домену,. \\ Можно указать имя пользователя. Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem. Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства. Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.

Пример: "ДВДОМ \\ Admin"

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
</dt> </dl>

Текущее состояние базовой службы.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

Значения качества производительности:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Остановлено** ("остановлено")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Ожидание запуска** ("Ожидание запуска")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Ожидание ожидания** ("ожидание завершения")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Работает** ("работает")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Ожидание продолжения** ("Ожидание продолжения")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Ожидание приостановки** ("ожидание приостановки")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Приостановлено** ("приостановлено")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


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

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

Значения качества производительности:

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

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](../wmisdk/standard-qualifiers.md) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" имя класса системы ")
</dt> </dl>

Имя типа системы, в которой размещена эта служба.

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

**TagId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор тега")
</dt> </dl>

Уникальное значение тега для этой службы в группе. Значение 0 (ноль) указывает, что службе не назначен тег. Тег можно использовать для упорядочения запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

**HKey \_ \_ \\ \\ \\ \\ Граупордерлист управления CurrentControlSet системы локального компьютера**.

Теги оцениваются только для драйверов ядра и драйверов файловой системы, которые имеют режимы загрузки или запуска системы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ SystemDriver** является производным от [**Win32 \_ басесервице**](win32-baseservice.md).

## <a name="examples"></a>Примеры

В примере [List Drivers](https://Gallery.TechNet.Microsoft.Com/5629cc13-cefc-4e51-a24f-aac6db23d141) VBScript в файле HTML отображаются установленные системные драйверы.

В следующем примере PowerShell извлекается ряд свойств из выполняемых системных драйверов на компьютере.


```PowerShell
Get-WmiObject -Class Win32_SystemDriver | Where-Object -FilterScript {$_.State -eq "Running"} | Where-Object -FilterScript {$_.StartMode -eq "Manual"} | Format-Table -Property Name,DisplayName
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

[**\_Басесервице Win32**](win32-baseservice.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
