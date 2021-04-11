---
description: Управляет репликацией для виртуальной машины.
ms.assetid: 0335fb94-5f2b-43be-bfb4-bc6811c5b507
title: Класс Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService
- Msvm_ReplicationService.InstanceID
- Msvm_ReplicationService.Caption
- Msvm_ReplicationService.Description
- Msvm_ReplicationService.ElementName
- Msvm_ReplicationService.InstallDate
- Msvm_ReplicationService.Name
- Msvm_ReplicationService.OperationalStatus
- Msvm_ReplicationService.StatusDescriptions
- Msvm_ReplicationService.Status
- Msvm_ReplicationService.HealthState
- Msvm_ReplicationService.CommunicationStatus
- Msvm_ReplicationService.DetailedStatus
- Msvm_ReplicationService.OperatingStatus
- Msvm_ReplicationService.PrimaryStatus
- Msvm_ReplicationService.EnabledState
- Msvm_ReplicationService.OtherEnabledState
- Msvm_ReplicationService.RequestedState
- Msvm_ReplicationService.EnabledDefault
- Msvm_ReplicationService.TimeOfLastStateChange
- Msvm_ReplicationService.AvailableRequestedStates
- Msvm_ReplicationService.TransitioningToState
- Msvm_ReplicationService.SystemCreationClassName
- Msvm_ReplicationService.SystemName
- Msvm_ReplicationService.CreationClassName
- Msvm_ReplicationService.PrimaryOwnerName
- Msvm_ReplicationService.PrimaryOwnerContact
- Msvm_ReplicationService.StartMode
- Msvm_ReplicationService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86e9140e2fe9b047c57c762be2e0fba048511993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265056"
---
# <a name="msvm_replicationservice-class"></a>\_Класс мсвм репликатионсервице

Управляет репликацией для виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationService : CIM_Service
{
  string   InstanceID;
  string   Caption = "Hyper-V Replica Service";
  string   Description = "Replication Service";
  string   ElementName;
  datetime InstallDate;
  string   Name = "replicasvc";
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_ComputerSystem";
  string   SystemName;
  string   CreationClassName = "Msvm_ReplicationService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ репликатионсервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ репликатионсервице** содержит следующие методы.



| Метод                                                                                                 | Описание                                                                                                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддаусоризатионентри**](addauthorizationentry-msvm-replicationservice.md)                         | Добавляет запись авторизации на сервер.<br/>                                                                                                                                                                                                                                           |
| [**чанжерепликатионмодетопримари**](changereplicationmodetoprimary-msvm-replicationservice.md)       | Изменяет отношение расширенной репликации на основное отношение для реплики виртуальной машины. Виртуальная машина реплики должна находиться в состоянии фиксации отработки отказа.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/> |
| [**коммитфаиловер**](commitfailover-msvm-replicationservice.md)                                       | Фиксирует моментальный снимок восстановления, который метод [**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md) использовал для отработки отказа.<br/>                                                                                                                                        |
| [**CreateReplicationRelationship**](createreplicationrelationship-msvm-replicationservice.md)         | Создает новое отношение репликации для виртуальной машины.<br/>                                                                                                                                                                                                                      |
| [**жетрепликатионстатистикс**](getreplicationstatistics-msvm-replicationservice.md)                   | Извлекает статистику репликации для виртуальной машины.<br/>                                                                                                                                                                                                                            |
| [**жетрепликатионстатистиксекс**](getreplicationstatisticsex-msvm-replicationservice.md)               | Извлекает статистику репликации, связанную с указанным отношением репликации виртуальной машины.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/>                                                    |
| [**жетсистемцертификатес**](getsystemcertificates-msvm-replicationservice.md)                         | Получает системные сертификаты в системе узла.<br/>                                                                                                                                                                                                                                |
| [**импортинитиалреплика**](importinitialreplica-msvm-replicationservice.md)                           | Импортирует начальную репликацию для виртуальной машины.<br/>                                                                                                                                                                                                                             |
| [**инитиатефаилбакк**](initiatefailback-msvm-replicationservice.md)                                   | Инициирует восстановление размещения для виртуальной машины восстановления. Это значит, что задает для виртуальной машины отработку отказа с помощью образа приложения или сбоя.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/>                              |
| [**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md)                                   | Инициирует отработку отказа для виртуальной машины в приложение или образ точки репликации уровня "Стандартный".<br/>                                                                                                                                                                                  |
| [**модифяусоризатионентри**](modifyauthorizationentry-msvm-replicationservice.md)                   | Изменяет запись авторизации на сервере.<br/>                                                                                                                                                                                                                                       |
| [**модифирепликатионсеттингс**](modifyreplicationsettings-msvm-replicationservice.md)                 | Изменяет параметры репликации для виртуальной машины.<br/>                                                                                                                                                                                                                           |
| [**модифисервицесеттингс**](modifyservicesettings-msvm-replicationservice.md)                         | Изменяет параметры службы реплики Hyper-V.<br/>                                                                                                                                                                                                                             |
| [**ремовеаусоризатионентри**](removeauthorizationentry-msvm-replicationservice.md)                   | Удаляет запись авторизации с сервера.<br/>                                                                                                                                                                                                                                     |
| [**ремоверепликатионрелатионшип**](removereplicationrelationship-msvm-replicationservice.md)         | Удаляет отношение репликации виртуальной машины.<br/>                                                                                                                                                                                                                                |
| [**ремоверепликатионрелатионшипекс**](removereplicationrelationshipex-msvm-replicationservice.md)     | Удаляет указанное отношение репликации виртуальной машины. Для виртуальной машины реплики невозможно удалить первичную репликацию, если включена расширенная репликация.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/>     |
| [**Равен**](msvm-replicationservice-requeststatechange.md)                               | Запрашивает изменение состояния.<br/>                                                                                                                                                                                                                                                           |
| [**ресетрепликатионстатистикс**](resetreplicationstatistics-msvm-replicationservice.md)               | Сбрасывает статистику репликации для виртуальной машины.<br/>                                                                                                                                                                                                                           |
| [**ресетрепликатионстатистиксекс**](resetreplicationstatisticsex-msvm-replicationservice.md)           | Сбрасывает статистику репликации, связанную с указанным отношением репликации виртуальной машины.<br/> **Windows 8.1:** Этот метод не поддерживается до Windows 8.1 и Windows Server 2012 R2.<br/>                                                         |
| [**Повторная синхронизация**](resynchronize-msvm-replicationservice.md)                                         | Выполняет операцию повторной синхронизации на указанной виртуальной машине.<br/>                                                                                                                                                                                                           |
| [**реверсерепликатионрелатионшип**](reversereplicationrelationship-msvm-replicationservice.md)       | Реплицирует отработку отказа виртуальной машины обратно на сервер-источник.<br/>                                                                                                                                                                                                               |
| [**ревертфаиловер**](revertfailover-msvm-replicationservice.md)                                       | Отменяет текущую отработку отказа для виртуальной машины, удаляя текущий диск отработки отказа.<br/>                                                                                                                                                                                        |
| [**сетаусоризатионентри**](setauthorizationentry-msvm-replicationservice.md)                         | Задает запись авторизации репликации для виртуальной машины.<br/>                                                                                                                                                                                                                    |
| [**сетфаиловернетворкадаптерсеттингс**](setfailovernetworkadaptersettings-msvm-replicationservice.md) | Настройка IP-параметров сетевого адаптера для применения к виртуальной машине после отработки отказа.<br/>                                                                                                                                                                                  |
| [**StartReplication**](startreplication-msvm-replicationservice.md)                                   | Запускает репликацию виртуальной машины.<br/>                                                                                                                                                                                                                                       |
| [**StartService**](msvm-replicationservice-startservice.md)                                           | запускает службу.<br/>                                                                                                                                                                                                                                                                |
| [**StopService**](msvm-replicationservice-stopservice.md)                                             | останавливает службу.<br/>                                                                                                                                                                                                                                                                 |
| [**тестрепликасистем**](testreplicasystem-msvm-replicationservice.md)                                 | Создает новую реплику виртуальной машины с указанным моментальным снимком для целей тестирования.<br/>                                                                                                                                                                                       |
| [**тестрепликатионконнектион**](testreplicationconnection-msvm-replicationservice.md)                 | Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.<br/>                                                                                                                                                                          |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ репликатионсервице** имеет следующие свойства.

<dl> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* . Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба реплики Hyper-V".

</dd> <dt>

**коммуникатионстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает способность инструментирования взаимодействовать с базовым управляемым элементом. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)
</dt> <dt>

<span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ репликатионсервице".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба репликации".

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дополняет свойство **примаристатус** дополнительными сведениями о состоянии. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)
</dt> <dt>

<span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)
</dt> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)
</dt> <dt>

<span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)
</dt> <dt>

<span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)
</dt> <dt>

<span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**енабледдефаулт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Конфигурация по умолчанию или запуска администратора для включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).



| Значение                                                                        | Значение            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Активировано<br/> |



 

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Включенные и отключенные состояния элемента. Он также может указывать на переходы между этими запрошенными состояниями. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).



| Значение                                                                        | Значение            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>2</dt> </dl> | Активировано<br/> |



 

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущая работоспособность элемента. Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов. Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).



| Значение                                                                        | Значение                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>5</dt> </dl> | Состояние работоспособности — нормальное.<br/> |



 

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата и время создания конфигурации виртуальной машины. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение **null**.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "репликасвк".

</dd> <dt>

**оператингстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** . Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)
</dt> <dt>

<span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)
</dt> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)
</dt> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)
</dt> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)
</dt> <dt>

<span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)
</dt> <dt>

<span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)
</dt> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)
</dt> <dt>

<span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)
</dt> <dt>

<span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)
</dt> <dt>

<span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)
</dt> <dt>

<span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)
</dt> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)
</dt> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)
</dt> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)
</dt> <dt>

<span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив, содержащий текущие состояния объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement). Значением с нулевым индексом будет одно из следующих значений.



| Значение                                                                                                                                                                                                               | Значение                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="OK"></span><span id="ok"></span><dl> <dt>**ОК**</dt> <dt>2</dt> </dl>                                  | Служба репликации работает нормально.<br/>                                                                     |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span><dl> <dt>**Ошибка**</dt> <dt>6</dt> </dl> | Один или несколько прослушивателей сети репликации не работают. Убедитесь, что параметры службы репликации являются допустимыми.<br/> |



 

</dd> <dt>

**осеренабледстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое"). Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (256)
</dt> </dl>

Любые сведения о том, как можно достичь основного владельца службы (например, номер телефона, адрес электронной почты и т. д.). Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (64)
</dt> </dl>

Имя основного владельца службы, если она определена. Первичный владелец — это первоначальный контактный контакт для службы поддержки. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.

</dd> <dt>

**примаристатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Предоставляет сведения о состоянии высокого уровня. Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов. Значение **null** указывает, что это свойство не реализовано. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)
</dt> <dt>

<span id="OK"></span><span id="ok"></span>**ОК** (1)
</dt> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000.. )
</dt> </dl>

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Последнее запрошенное или требуемое состояние элемента. Фактическое состояние элемента представлено параметром **EnabledState**. Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента. Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** . В этом случае используется значение 12 ("неприменимо"). Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).



| Значение                                                                         | Значение                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | Не применяется<br/> |



 

</dd> <dt>

**Запуск**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, запущена ли служба в данный момент. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **true**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **maxlen** (10)
</dt> </dl>

Строковое значение, указывающее, запускается ли служба автоматически системой, операционной системой или запускается только по запросу. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение **null**.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает состояние элемента. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "ОК".

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**системкреатионкласснаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Имя класса создания системы области. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ ComputerSystem".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

NetBIOS-имя системы размещающего компьютера. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).

</dd> <dt>

**тимеофластстатечанже**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Дата или время последнего изменения включенного состояния элемента. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**транситионингтостате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает целевое состояние, в которое переходит экземпляр. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

