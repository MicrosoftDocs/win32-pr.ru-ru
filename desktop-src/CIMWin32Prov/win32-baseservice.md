---
description: '\_Абстрактный класс WMI Басесервице Win32 представляет исполняемые объекты, установленные в базе данных реестра, обслуживаемой диспетчером управления службами.'
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Класс Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2ce4673b6739639475264f79a60a7fd1b1c7bc5a0f16153d22305a77812759a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504374"
---
# <a name="win32_baseservice-class"></a>\_Класс Win32 басесервице

Абстрактный [класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ басесервице Win32** представляет исполняемые объекты, установленные в базе данных реестра, обслуживаемой диспетчером управления службами. Исполняемый файл, связанный со службой, может запускаться во время загрузки программой загрузки или системой. Он также может быть запущен по запросу диспетчером управления службами. Любая служба или процесс, не принадлежащий определенному пользователю и предоставляющий интерфейс некоторой функциональности, поддерживаемой компьютерной системой, является потомком (или членом) этого класса.

пример. служба клиента DHCP на компьютере, на котором работает Windows Server.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
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

Класс **Win32 \_ басесервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ басесервице** содержит следующие методы.



| Метод                                                                             | Описание                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Изменение**](change-method-in-class-win32-baseservice.md)                         | Изменяет службу.<br/>                                                |
| [**чанжестартмоде**](changestartmode-method-in-class-win32-baseservice.md)       | Изменяет режим запуска службы.<br/>                              |
| [**Создание**](create-method-in-class-win32-baseservice.md)                         | Создает новую службу.<br/>                                             |
| [**Удален**](delete-method-in-class-win32-baseservice.md)                         | Удаляет существующую службу.<br/>                                       |
| [**интеррогатесервице**](interrogateservice-method-in-class-win32-baseservice.md) | Запрашивает обновление состояния службы до Service Manager.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-baseservice.md)             | Пытается перевести службу в состояние приостановки.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-baseservice.md)           | Пытается перевести службу в состояние возобновления.<br/>                |
| [**StartService**](startservice-method-in-class-win32-baseservice.md)             | Пытается перевести службу в состояние запуска.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-baseservice.md)               | Метод класса, который помещает службу в остановленное состояние.<br/>         |
| [**усерконтролсервице**](usercontrolservice-method-in-class-win32-baseservice.md) | Пытается отправить в службу определенный пользователем управляющий код.<br/>         |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ басесервице** имеет следующие свойства.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает паузу")
</dt> </dl>

Служба может быть приостановлена.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает" останавливается ").
</dt> </dl>

Служба может быть остановлена.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
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

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")
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

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("взаимодействует с Desktop")
</dt> </dl>

Служба может создавать Windows на рабочем столе и взаимодействовать с ними.

</dd> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("отображаемое имя")
</dt> </dl>

Отображаемое имя службы. Максимальная длина этой строки равна 256 символам. В диспетчере управления службами имя сохраняется с учетом регистра. При сравнении **DisplayName** всегда учитывается регистр.

Ограничения: принимает то же значение, что и свойство **Name** .

Пример: "Атдиск"

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("серьезность сбоя при запуске")
</dt> </dl>

Серьезность ошибки. Не удается запустить службу. Значение указывает действие, предпринимаемое программой запуска, если происходит сбой. Все ошибки записываются в журнал системой компьютера.

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

Система перезапущена с последней удачной конфигурацией.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")


</dt> <dd>

Попытка перезапустить систему в рабочей конфигурации.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")


</dt> <dd>

Не указано действие, которое было принято.

</dd> </dl>

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("код выхода")
</dt> </dl>

Определение любых проблем, возникших при запуске или остановке службы. Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** . Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
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

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях. Эти функциональные возможности более подробно описаны в свойстве « **Описание** » объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпбинарипаснаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя пути к файлу")
</dt> </dl>

Полный путь к двоичному файлу службы, реализующему службу.

Пример: " \\ СистемныйКорневойКаталог \\ system32 \\ Drivers \\afd.sys"

</dd> <dt>

**сервицеспеЦифицекситкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("специфический для сервера код выхода")
</dt> </dl>

Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы. Коды выхода определяются службой, представленной этим классом. Это значение задается только в том случае, если значение **екситкодепроперти** является **\_ \_ \_ ошибкой службы, характерной для ошибки** (1066).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип службы")
</dt> </dl>

Служба, предоставляемая для вызова процессов.

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

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")
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

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")
</dt> </dl>

режим запуска базовой службы Windows.

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

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

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-baseservice.md) .

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

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("начальное имя учетной записи")
</dt> </dl>

Имя учетной записи, под которой выполняется служба. В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя ( Username@DomainName ). Процесс службы будет заноситься в журнал с использованием одной из этих двух форм при запуске. Если учетная запись принадлежит к встроенному домену, ". \\ Можно указать имя пользователя. Если указано **значение NULL** , служба будет входить в систему как учетная запись LocalSystem. Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть \\ FileSystem \\ RDR или \\ Driver \\ КСНС), которое используется системой ввода и вывода для загрузки драйвера устройства. Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы. Пример: "ДВДОМ \\ Admin".

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двкуррентстате"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Текущее состояние базовой службы.

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

**Windows Server 2008 и Windows Vista:** Это свойство доступно только для чтения.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.

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

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")
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

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](cim-system.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
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

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор тега")
</dt> </dl>

Уникальное значение тега для этой службы в группе. Значение 0 (ноль) указывает, что службе не назначен тег. Тег можно использовать для упорядочивания службы Star тройки в группе порядка загрузки, указав в реестре вектор порядка тегов, расположенный в папке: HKEY \_ локальный \_ компьютер \\ System \\ CurrentControlSet \\ Control \\ граупордерлист. Теги оцениваются только для драйверов ядра и драйверов файловой системы, которые имеют режимы загрузки или запуска системы.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ басесервице** является производным от [**\_ службы CIM**](cim-service.md).

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

[**\_Служба CIM**](cim-service.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

