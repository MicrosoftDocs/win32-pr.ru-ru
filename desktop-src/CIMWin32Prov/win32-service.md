---
description: Представляет службу в компьютерной системе, на которой работает Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Класс Win32_Service
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33265b3dfc3b114d55b381a229b717e291bbd258716e8305d9995282d29b3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759264"
---
# <a name="win32_service-class"></a>\_Класс службы Win32

[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ службы Win32** представляет службу в компьютерной системе, на которой работает Windows.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a>Члены

Класс **\_ службы Win32** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

В **классе \_ службы Win32** имеются следующие методы.



| Метод                                                                               | Описание                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Изменение**](change-method-in-class-win32-service.md)                               | Изменяет службу.<br/>                                                                       |
| [**чанжестартмоде**](changestartmode-method-in-class-win32-service.md)             | Изменяет режим запуска службы.<br/>                                                     |
| [**Создание**](create-method-in-class-win32-service.md)                               | Создает новую службу.<br/>                                                                    |
| [**Удален**](delete-method-in-class-win32-service.md)                               | Удаляет существующую службу.<br/>                                                              |
| [**жетсекуритидескриптор**](getsecuritydescriptor-method-in-class-win32-service.md) | Возвращает дескриптор безопасности, управляющий доступом к службе.<br/>                      |
| [**интеррогатесервице**](interrogateservice-method-in-class-win32-service.md)       | Запрашивает обновление состояния службы до Service Manager.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Пытается перевести службу в приостановленное состояние.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Пытается перевести службу в состояние возобновления.<br/>                                         |
| [**сетсекуритидескриптор**](setsecuritydescriptor-method-in-class-win32-service.md) | Записывает обновленную версию дескриптора безопасности, которая управляет доступом к службе.<br/> |
| [**StartService**](startservice-method-in-class-win32-service.md)                   | Пытается перевести службу в состояние запуска.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Помещает службу в остановленное состояние.<br/>                                                    |
| [**усерконтролсервице**](usercontrolservice-method-in-class-win32-service.md)       | Пытается отправить в службу определенный пользователем управляющий код.<br/>                                |



 

### <a name="properties"></a>Свойства

Класс **\_ службы Win32** имеет следующие свойства.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двконтролсакцептед \| Service \_ Accept \_ Пауза \_ Continue"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("служба принимает паузу")
</dt> </dl>

Указывает, можно ли приостановить работу службы.

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

Указывает, можно ли остановить службу.

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

Краткое описание службы — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Создание**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| Двчеккпоинт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("число контрольных точек")
</dt> </dl>

Значение, которое служба периодически увеличивает, чтобы сообщить о ходе выполнения во время длительной операции запуска, остановки, приостановки или продолжения работы. Например, служба увеличивает это значение по мере завершения каждого этапа инициализации при запуске. Программа пользовательского интерфейса, вызывающая операцию в службе, использует это значение для отслеживания хода выполнения службы во время длительной операции. Это значение недопустимо и должно быть равно нулю, если у службы нет ожидающих операций запуска, остановки, приостановки или возобновления.

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

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API Service Structures" \| \| [**Service \_ delay \_ \_ Start \_ info**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| фделайедаутостарт "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" отложенный автоматический запуск ")
</dt> </dl>

Если **значение — true**, служба запускается после запуска других служб, запускающих автозапуск, и короткой задержки.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** это свойство не поддерживается до Windows Server 2016 и Windows 10.

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

Указывает, может ли служба создавать и взаимодействовать с Windows на настольном компьютере и, таким образом, взаимодействовать с пользователем. Интерактивные службы должны запускаться под локальной системной учетной записью. Большинство служб не являются интерактивными; то есть они не взаимодействуют с пользователем каким-либо образом.

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

Имя службы, отображаемое в оснастке "службы". Максимальная длина этой строки равна 256 символам. Обратите внимание, что отображаемое имя и имя службы (которые хранятся в реестре) не всегда одинаковы. Например, служба DHCP-клиента имеет имя службы DHCP, а не отображаемое имя DHCP-клиента. В диспетчере управления службами имя сохраняется с учетом регистра. Однако в сравнениях **DisplayName** всегда учитывается регистр.

Ограничение: принимает то же значение, что и свойство **Name** .

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

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| DwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("код выхода")
</dt> </dl>

Windows код ошибки, определяющий ошибки при запуске или остановке службы. Это свойство имеет значение ошибка, связанное со **\_ службой \_ \_ ошибок** (1066), если ошибка является уникальной для службы, представленной этим классом, а сведения об ошибке доступны в свойстве **сервицеспеЦифицекситкоде** . Служба задает это значение **без \_ ошибок** при выполнении и снова после нормального завершения.

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

Объект Date установлен. Для этого свойства не требуется указывать значение, указывающее, что объект установлен.

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

Уникальный идентификатор службы, который предоставляет сведения об управляемых функциях. Эти функциональные возможности описаны в свойстве **Description** объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

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

**Идентификатор**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status \_ Process**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| двпроцессид"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("идентификатор процесса")
</dt> </dl>

Идентификатор процесса службы.

Пример: 324

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

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("запущено")
</dt> </dl>

Указывает, запущена ли служба.

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

режим запуска базовой службы Windows.

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

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) . Эти службы не запускаются, пока пользователь не войдет в систему и не запустит их.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")


</dt> <dd>

Служба, которая не может быть запущена до тех пор, пока ее значение StartMode не изменится на Auto или Manual.

</dd> </dl>

Это свойство наследуется [**от \_ службы CIM**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (" \| структуры служб Win32API \| [**запрос \_ \_ конфигурации службы**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| Лпсервицестартнаме"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("начальное имя учетной записи")
</dt> </dl>

Имя учетной записи, под которой выполняется служба. В зависимости от типа службы имя учетной записи может быть указано в \\ формате имя_домена имя пользователя или имя участника-пользователя (" *Username@DomainName* "). Процесс службы заносится в журнал с использованием одной из этих двух форм при запуске. Если учетная запись принадлежит к встроенному домену, то ". \\ Можно указать имя пользователя. Для драйверов ядра или системного уровня **StartName** содержит имя объекта драйвера (то есть " \\ FileSystem \\ RDR" или " \\ Driver \\ КСНС"), которое система ввода-вывода использует для загрузки драйвера устройства. Кроме того, если указано **значение NULL** , драйвер запускается с именем объекта по умолчанию, созданным системой ввода-вывода на основе имени службы.

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

**Windows Server 2008 и Windows Vista:** это свойство доступно только для чтения до Windows 7 и Windows Server 2008 R2.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

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

Уникальное значение тега для этой службы в группе. Значение 0 (ноль) указывает, что у службы нет тега. Тег можно использовать для упорядочивания запуска службы в группе порядка загрузки, указывая в реестре вектор порядка тегов в папке:

**HKey \_ \_** \\  \\  \\  \\ **Граупордерлист** управления CurrentControlSet системы локального компьютера    

Теги оцениваются только для служб типа "драйвер ядра" и "драйвер файловой системы", которые имеют режимы загрузки или запуска системы.

Это свойство наследуется из [**Win32 \_ басесервице**](win32-baseservice.md).

</dd> <dt>

**ваисинт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**\_ Status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| двваисинт"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("предполагаемое время ожидания")
</dt> </dl>

Предполагаемое время в миллисекундах для ожидающей операции запуска, остановки, приостановки или продолжения работы. По истечении указанного времени служба выполняет следующий вызов метода **сбой SetServiceStatus** с увеличенным значением **контрольной точки** или изменением в **CurrentState**. Если время, указанное в **ваисинт** , прошло, а **контрольная точка** не была увеличена или **CurrentState** не изменилась, диспетчер управления службами или программа управления службами предполагает, что произошла ошибка.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ службы Win32** является производным от [**Win32 \_ басесервице**](win32-baseservice.md).

Способ управления конкретным компьютером сильно зависит от роли, которую играет компьютер. Например, вы обычно отслеживаете различные аспекты DNS-сервера, чем DHCP-сервер. Хотя ни одно свойство не может сообщить вам, является ли конкретный компьютер сервером базы данных, сервером электронной почты или сервером мультимедиа, часто можно определить роль, которую компьютер воспроизводит, определив установленные на нем службы.

В больших организациях только одна из основных служб (например, электронная почта), скорее всего, будет установлена на одном компьютере. почтовый сервер также будет работать как сервер для Microsoft® Windows файлы проигрывателя® технологии мультимедиа. По этой причине определение службы, установленной на компьютере, может помочь определить роль компьютера в сети. если служба Microsoft® Exchange Server установлена и запущена на компьютере, обычно можно считать, что этот компьютер работает как почтовый сервер.

Для перечисления служб, установленных на компьютере, можно использовать класс **\_ службы Win32** инструментария WMI. Кроме того, этот класс можно использовать для определения того, работают ли эти службы в данный момент, а также какие другие необходимые сведения об этой службе и как они были настроены.

приложение службы соответствует правилам интерфейса диспетчера управления службами (SCM) и может запускаться пользователем автоматически при запуске системы с помощью служебной программы панели управления "службы" или приложения, использующего функции службы, входящие в Windows API. Службы могут запускаться при отсутствии пользователей, выполнивших вход в систему.

Пользователь, подключающийся с удаленного компьютера, должен иметь разрешение **SC \_ Manager \_ Connect** , чтобы иметь возможность перечислить этот класс. Дополнительные сведения см. в разделе [Безопасность службы и права доступа](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Примеры

[Запрос PS-WMI, который возвращает службу "состояние" в](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) примере PowerShell для группы устройств в коллекции TechNet, использует **\_ службу Win32** для создания списка устройств на основе Active Directory, а затем запрашивает каждое устройство, отвечающее на пингфор определенной службы.

Пример [серверного отчета](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) PowerShell в коллекции TechNet использует **\_ службу Win32** для сбора сведений о сервере и публикации в документе Word.

В следующем образце кода VBScript отображаются все установленные в данный момент службы.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



Следующий пример кода VBScript описывает приостановленные, запущенные и остановленные службы на указанном компьютере.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



В следующем скрипте Perl показано, как получить список выполняющихся служб из экземпляров **\_ службы Win32**.


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



В следующем \# образце c используется [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) для получения всех выполняющихся служб на локальном компьютере.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



Следующий пример кода на языке C \# использует пространство имен [System. Management](/dotnet/api/system.management) для получения всех работающих служб на локальном компьютере.

> [!Note]  
> [System. Management](/dotnet/api/system.management) содержит исходные классы, используемые для доступа к WMI; Однако они считаются более медленными и обычно не масштабируются, а также их аналоги [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
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

[**\_Басесервице Win32**](win32-baseservice.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> <dt>

[Задачи WMI: службы](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
