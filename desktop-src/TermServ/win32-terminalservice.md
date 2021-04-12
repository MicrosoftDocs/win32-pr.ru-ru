---
title: Класс Win32_TerminalService
description: Подкласс \_ класса службы Win32. Win32 \_ терминалсервице представляет свойство element \_ ассоциации Win32 терминалсервицетосеттинг.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalService службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalService, описание
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba5646c6ac9abf41fddc023ad39884e611681a71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492735"
---
# <a name="win32_terminalservice-class"></a>\_Класс Win32 терминалсервице

Класс **WMI \_ Терминалсервице для Win32** является подклассом класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) . **Win32 \_ Терминалсервице** представляет свойство **element** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
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
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ терминалсервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ терминалсервице** содержит следующие методы.



| Метод                                                                       | Описание                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Change**](win32-terminalservice-change.md)                               | Изменяет службу.<br/>                                                                       |
| [**чанжестартмоде**](win32-terminalservice-changestartmode.md)             | Изменяет режим запуска службы.<br/>                                                     |
| [**Создать**](win32-terminalservice-create.md)                               | Создает новую службу.<br/>                                                                    |
| [**Удалить**](win32-terminalservice-delete.md)                               | Удаляет существующую службу.<br/>                                                              |
| [**жетсекуритидескриптор**](win32-terminalservice-getsecuritydescriptor.md) | Возвращает дескриптор безопасности, управляющий доступом к службе.<br/>                      |
| [**интеррогатесервице**](win32-terminalservice-interrogateservice.md)       | Запрашивает обновление состояния службы до Service Manager.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Пытается перевести службу в приостановленное состояние.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Пытается перевести службу в состояние возобновления.<br/>                                         |
| [**сетсекуритидескриптор**](win32-terminalservice-setsecuritydescriptor.md) | Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.<br/> |
| [**StartService**](win32-terminalservice-startservice.md)                   | Пытается перевести службу в состояние запуска.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Помещает службу в остановленное состояние.<br/>                                                    |
| [**усерконтролсервице**](win32-terminalservice-usercontrolservice.md)       | Пытается отправить в службу определенный пользователем управляющий код.<br/>                                |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ терминалсервице** имеет следующие свойства.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает паузу")
</dt> </dl>

Указывает, можно ли приостановить работу службы.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("служба принимает" останавливается ").
</dt> </dl>

Указывает, можно ли остановить службу.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое описание службы — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Создание**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| Двчеккпоинт"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("число контрольных точек")
</dt> </dl>

Значение, которое служба периодически увеличивает, чтобы сообщить о ходе выполнения во время длительной операции запуска, остановки, приостановки или продолжения работы. Например, служба увеличивает это значение по мере завершения каждого этапа инициализации при запуске. Программа пользовательского интерфейса, вызывающая операцию в службе, использует это значение для отслеживания хода выполнения службы во время длительной операции. Это значение недопустимо и должно быть равно нулю, если у службы нет ожидающих операций запуска, остановки, приостановки или возобновления.

Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя класса")
</dt> </dl>

Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра. При использовании с другими ключевыми свойствами класса это свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.

Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API Service Structures" \| \| [**Service \_ delay \_ \_ Start \_ info**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| фделайедаутостарт "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" отложенный автоматический запуск ")
</dt> </dl>

Если **значение — true**, служба запускается после запуска других служб, запускающих автозапуск, и короткой задержки.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows Server 2016 и Windows 10.

Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).

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

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa)службы \| двсервицетипе \| \_ Интерактивный \_ процесс"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("взаимодействует с Desktop")
</dt> </dl>

Указывает, может ли служба создавать и взаимодействовать с Windows на настольном компьютере и, таким образом, взаимодействовать с пользователем. Интерактивные службы должны запускаться под локальной системной учетной записью. Большинство служб не являются интерактивными; то есть они не взаимодействуют с пользователем каким-либо образом.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**дисконнектедсессионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Число отключенных сеансов на текущем сервере. Эти сеансы по-прежнему могут активно потреблять ресурсы сервера, но в настоящее время они не имеют сетевого подключения к клиенту.

</dd> <dt>

**Отображаемое имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпдисплайнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("отображаемое имя")
</dt> </dl>

Имя службы, отображаемое в оснастке "службы". Максимальная длина этой строки равна 256 символам. Обратите внимание, что отображаемое имя и имя службы (которые хранятся в реестре) не всегда одинаковы. Например, служба DHCP-клиента имеет имя службы DHCP, а не отображаемое имя DHCP-клиента. В диспетчере управления службами имя сохраняется с учетом регистра. Однако в сравнениях [**DisplayName**](/windows/desktop/CIMWin32Prov/win32-service) всегда учитывается регистр.

Ограничение: принимает то же значение, что и свойство [**Name**](/windows/desktop/CIMWin32Prov/win32-service) .

Пример: "Атдиск"

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Дверрорконтрол"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("серьезность сбоя при запуске")
</dt> </dl>

Серьезность ошибки, если не удается запустить службу во время запуска. Значение указывает действие, предпринимаемое программой запуска, если происходит сбой. Все ошибки записываются в журнал системой компьютера.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Игнорировать** ("ignore")


</dt> <dd>

Пользователь не получает уведомление.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Обычная** ("Обычная")


</dt> <dd>

Пользователь получает уведомление. Обычно это будет окно сообщения с уведомлением пользователя о проблеме.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Серьезная** ("серьезная")


</dt> <dd>

Система перезапускается в последней известной рабочей конфигурации.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** ("критическая")


</dt> <dd>

Попытка перезапустить систему в рабочей конфигурации. Если служба не запускается второй раз, происходит сбой запуска.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** ("неизвестно")


</dt> <dd>

Серьезность ошибки неизвестна.

</dd> </dl>

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("код выхода")
</dt> </dl>

Код ошибки Windows, определяющий ошибки, возникающие при запуске или остановке службы. Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве [**сервицеспеЦифицекситкоде**](/windows/desktop/CIMWin32Prov/win32-service) . Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Объект Date установлен. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях. Эти функциональные возможности описаны в свойстве [**Description**](/windows/desktop/CIMWin32Prov/win32-service) объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

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

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status \_ Process**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| двпроцессид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор процесса")
</dt> </dl>

Идентификатор процесса службы.

Пример: 324

Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> <dt>

**сервицеспеЦифицекситкоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двсервицеспеЦифицекситкоде"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("специфический для сервера код выхода")
</dt> </dl>

Код ошибки, зависящей от службы, для ошибок, возникающих во время запуска или остановки службы. Коды выхода определяются службой, представленной этим классом. Это значение задается только в том случае, если значение свойства [**ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) — ошибка, связанная со **\_ службой ошибок \_ \_** (1066).

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двсервицетипе"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип службы")
</dt> </dl>

Тип службы, предоставленной для вызывающих процессов.

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

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("запущено")
</dt> </dl>

Указывает, запущена ли служба.

Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("режим запуска")
</dt> </dl>

Режим запуска базовой службы Windows.

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

Служба запускается автоматически диспетчером управления службами во время запуска системы. Автоматические службы запускаются, даже если пользователь не входит в систему.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Вручную** ("вручную")


</dt> <dd>

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Эти службы не запускаются, пока пользователь не войдет в систему и не запустит их.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")


</dt> <dd>

Служба, которая не может быть запущена до тех пор, пока ее значение StartMode не изменится на Auto или Manual.

</dd> </dl>

Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("начальное имя учетной записи")
</dt> </dl>

Имя учетной записи, под которой выполняется служба. В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя (" *Username@DomainName* "). Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске. Если учетная запись принадлежит к встроенному домену, то ". \\ Можно указать имя пользователя. Для драйверов ядра или системного уровня [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) содержит имя объекта драйвера (то есть " \\ FileSystem \\ RDR" или " \\ Driver \\ КСНС"), которое система ввода-вывода использует для загрузки драйвера устройства. Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.

Пример: "ДВДОМ \\ Admin"

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

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

**Windows Server 2008 и Windows Vista:** Это свойство доступно только для чтения до Windows 7 и Windows Server 2008 R2.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

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

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName "), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" имя класса системы ")
</dt> </dl>

Имя типа системы, в которой размещена эта служба.

Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**распространено**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ система CIM**](/windows/desktop/CIMWin32Prov/cim-system). Name "), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" System Name ")
</dt> </dl>

Имя системы, в которой размещена эта служба.

Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| двтагид"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("идентификатор тега")
</dt> </dl>

Уникальное значение тега для этой службы в группе. Значение 0 (ноль) указывает, что у службы нет тега. Тег можно использовать для упорядочивания запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:

**HKey \_ \_** \\  \\  \\  \\ **Граупордерлист** управления CurrentControlSet системы локального компьютера    

Теги оцениваются только для служб типа "драйвер ядра" и "драйвер файловой системы", которые имеют режимы загрузки или запуска системы.

Это свойство наследуется из [**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).

</dd> <dt>

**тоталсессионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Общее число сеансов на текущем сервере. Сюда входят подключенные и отключенные сеансы.

</dd> <dt>

**ваисинт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**\_ Status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| двваисинт"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("предполагаемое время ожидания")
</dt> </dl>

Предполагаемое время в миллисекундах для ожидающей операции запуска, остановки, приостановки или продолжения работы. По истечении указанного времени служба выполняет следующий вызов метода **сбой SetServiceStatus** с увеличенным значением [**контрольной точки**](/windows/desktop/CIMWin32Prov/win32-service) или изменением в **CurrentState**. Если время, указанное в **ваисинт** , прошло, а **контрольная точка** не была увеличена или **CurrentState** не изменилась, диспетчер управления службами или программа управления службами предполагает, что произошла ошибка.

Это свойство наследуется [**от \_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> </dl>

## <a name="remarks"></a>Комментарии

Поскольку класс **Win32 \_ терминалсервице** является подклассом класса [**\_ службы Win32**](/windows/desktop/CIMWin32Prov/win32-service) , класс наследует все свойства и методы **\_ службы Win32**.

[**Win32 \_ Терминалсервицесеттинг**](win32-terminalservicesetting.md) связан с **Win32 \_ терминалсервице** в качестве свойства **Setting** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .

[**Win32 \_ Тссессиондиректори**](win32-tssessiondirectory.md) связан с **Win32 \_ терминалсервице** в качестве свойства **Setting** ассоциации [**Win32 \_ тссессиондиректорисеттинг**](win32-tssessiondirectorysetting.md) .

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Root\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_Терминалсервицетосеттинг Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_Тссессиондиректори Win32**](win32-tssessiondirectory.md)
</dt> <dt>

[**\_Басесервице Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_Служба CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

