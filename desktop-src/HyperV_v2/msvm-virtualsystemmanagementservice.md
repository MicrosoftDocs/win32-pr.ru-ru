---
description: Представляет службу виртуализации, имеющуюся в одной системе узла.
ms.assetid: 7f4bd9e0-b034-4882-ad01-f7df740939ae
title: Класс Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService
- Msvm_VirtualSystemManagementService.InstanceID
- Msvm_VirtualSystemManagementService.Caption
- Msvm_VirtualSystemManagementService.Description
- Msvm_VirtualSystemManagementService.ElementName
- Msvm_VirtualSystemManagementService.InstallDate
- Msvm_VirtualSystemManagementService.Name
- Msvm_VirtualSystemManagementService.OperationalStatus
- Msvm_VirtualSystemManagementService.StatusDescriptions
- Msvm_VirtualSystemManagementService.Status
- Msvm_VirtualSystemManagementService.HealthState
- Msvm_VirtualSystemManagementService.CommunicationStatus
- Msvm_VirtualSystemManagementService.DetailedStatus
- Msvm_VirtualSystemManagementService.OperatingStatus
- Msvm_VirtualSystemManagementService.PrimaryStatus
- Msvm_VirtualSystemManagementService.EnabledState
- Msvm_VirtualSystemManagementService.OtherEnabledState
- Msvm_VirtualSystemManagementService.RequestedState
- Msvm_VirtualSystemManagementService.EnabledDefault
- Msvm_VirtualSystemManagementService.TimeOfLastStateChange
- Msvm_VirtualSystemManagementService.AvailableRequestedStates
- Msvm_VirtualSystemManagementService.TransitioningToState
- Msvm_VirtualSystemManagementService.SystemCreationClassName
- Msvm_VirtualSystemManagementService.SystemName
- Msvm_VirtualSystemManagementService.CreationClassName
- Msvm_VirtualSystemManagementService.PrimaryOwnerName
- Msvm_VirtualSystemManagementService.PrimaryOwnerContact
- Msvm_VirtualSystemManagementService.StartMode
- Msvm_VirtualSystemManagementService.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0dab3dc9b530ca565e78ecc1f5a6e50a26bc3f630f5c60491b01c253e09aa97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147997"
---
# <a name="msvm_virtualsystemmanagementservice-class"></a>\_Класс мсвм виртуалсистемманажементсервице

Представляет службу виртуализации, имеющуюся в одной системе узла. **Мсвм \_ Виртуалсистемманажементсервице** используется для управления определением, изменением и удалением виртуальных машин. Он также содержит методы для выполнения операций на виртуальных машинах, таких как клонирование, значит, импорт или экспорт виртуальных машин. Чтобы получить сведения о виртуальной машине, используйте [**мсвм \_ ComputerSystem**](msvm-computersystem.md).

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemManagementService : CIM_VirtualSystemManagementService
{
  string   InstanceID;
  string   Caption = "Virtual System Management Service";
  string   Description = "Service for creating, manipulating, and managing virtual machines";
  string   ElementName = "Hyper-V Virtual System Management Service";
  datetime InstallDate;
  string   Name = "vmms";
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
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
  string   CreationClassName = "Msvm_VirtualSystemManagementService";
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   StartMode;
  boolean  Started = True;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемманажементсервице** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **мсвм \_ виртуалсистемманажементсервице** содержит следующие методы.



| Метод                                                                                                                 | Описание                                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддбутсаурцесеттингс**](msvm-virtualsystemmanagementservice-addbootsourcesettings.md)                             | Добавляет исходные загрузочные источники в конфигурацию виртуальной системы при их применении к конфигурации виртуальной системы "состояние".<br/>                                                                                                                             |
| [**аддфеатуресеттингс**](addfeaturesettings-msvm-virtualsystemmanagementservice.md)                                   | Добавляет параметры Ethernet-компонентов в конфигурацию подключения Ethernet виртуальной машины.<br/>                                                                                                                                           |
| [**аддфибречаннелчап**](addfibrechannelchap-msvm-virtualsystemmanagementservice.md)                                 | Добавляет параметры DH-CHAP в виртуальный порт Fibre Channel виртуальной машины.<br/>                                                                                                                                                         |
| [**аддгуестсервицесеттингс**](msvm-virtualsystemmanagementservice-addguestservicesettings.md)                         | Добавляет параметры гостевой службы в конфигурацию виртуальной системы.<br/> При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.<br/>              |
| [**аддквпитемс**](addkvpitems-msvm-virtualsystemmanagementservice.md)                                                 | Добавляет пары "ключ-значение" в виртуальную машину.<br/>                                                                                                                                                                                              |
| [**аддресаурцесеттингс**](addresourcesettings-msvm-virtualsystemmanagementservice.md)                                 | Добавляет ресурсы в конфигурацию виртуальной машины.<br/>                                                                                                                                                                                      |
| [**аддсистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-addsystemcomponentsettings.md)                   | Добавляет универсальные параметры в конфигурацию виртуальной системы.<br/>                                                                                                                                                                                |
| [**дефинепланнедсистем**](msvm-virtualsystemmanagementservice-defineplannedsystem.md)                                 | Определяет запланированную виртуальную систему.<br/> Входные данные, которые указаны не полностью, могут быть заполнены значениями по умолчанию.<br/>                                                                                                              |
| [**дефинесистем**](definesystem-msvm-virtualsystemmanagementservice.md)                                               | Создает новое определение виртуальной машины.<br/>                                                                                                                                                                                               |
| [**дестройсистем**](destroysystem-msvm-virtualsystemmanagementservice.md)                                             | Удаляет существующее определение виртуальной машины.<br/>                                                                                                                                                                                         |
| [**диагносенетворкконнектион**](msvm-virtualsystemmanagementservice-diagnosenetworkconnection.md)                     | диагностика сетевого подключения виртуальной машины в среде Windows виртуализации сети.<br/>                                                                                                                                             |
| [**експортсистемдефинитион**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Экспортирует виртуальную машину или моментальный снимок виртуальной машины в файл.<br/>                                                                                                                                                               |
| [**FormatError**](formaterror-msvm-virtualsystemmanagementservice.md)                                                 | Возвращает отформатированную строку сообщения об ошибке для указанного массива внедренных экземпляров [**\_ ошибок мсвм**](msvm-error.md) .<br/>                                                                                                               |
| [**женератеввпн**](generatewwpn-msvm-virtualsystemmanagementservice.md)                                               | Формирует набор WWN-имен портов (Ввпнс).<br/>                                                                                                                                                                                       |
| [**жеткуррентввпнфромженератор**](getcurrentwwpnfromgenerator-msvm-virtualsystemmanagementservice.md)                 | Предоставляет возможность предварительного просмотра текущего WWN-имени порта (WWPN) без зарезервированного WWPN.<br/>                                                                                                                                |
| [**жетдефинитионфилесуммаринформатион**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) | Возвращает сводные данные о виртуальной машине для указанных файлов определения виртуальной машины.<br/>                                                                                                                                         |
| [**жетсизеофсистемфилес**](getsizeofsystemfiles-msvm-virtualsystemmanagementservice.md)                               | Получает общий размер системных файлов виртуальной машины.<br/>                                                                                                                                                                        |
| [**жетсуммаринформатион**](getsummaryinformation-msvm-virtualsystemmanagementservice.md)                             | Возвращает сводные данные о виртуальной машине.<br/>                                                                                                                                                                                            |
| [**жетвиртуалсистемсумбнаилимаже**](getvirtualsystemthumbnailimage-msvm-virtualsystemmanagementservice.md)           | Извлекает эскиз имеющейся виртуальной машины.<br/>                                                                                                                                                                             |
| [**импортснапшотдефинитионс**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md)                     | Ищет в указанной папке файлы определения моментальных снимков, связанные с указанной запланированной системой компьютера, и создает новый моментальный снимок в запланированной компьютерной системе для каждого связанного файла определения в этом расположении.<br/> |
| [**импортсистемдефинитион**](importsystemdefinition-msvm-virtualsystemmanagementservice.md)                           | Создает новую запланированную компьютерную систему на основе указанного определения виртуальной машины.<br/>                                                                                                                                                |
| [**модифидискмержесеттингс**](modifydiskmergesettings-msvm-virtualsystemmanagementservice.md)                         | Изменяет данные параметров слияния диска.<br/>                                                                                                                                                                                                   |
| [**модифифеатуресеттингс**](modifyfeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Изменяет текущие настройки компонентов подключения Ethernet виртуальной машины.<br/>                                                                                                                                                         |
| [**модифигуестсервицесеттингс**](msvm-virtualsystemmanagementservice-modifyguestservicesettings.md)                   | Изменяет параметры гостевой службы.<br/> При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.<br/>                                            |
| [**модификвпитемс**](modifykvpitems-msvm-virtualsystemmanagementservice.md)                                           | Изменяет существующие пары "ключ-значение" на виртуальной машине.<br/>                                                                                                                                                                                 |
| [**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Изменяет параметры виртуального ресурса.<br/>                                                                                                                                                                                                     |
| [**модифисервицесеттингс**](modifyservicesettings-msvm-virtualsystemmanagementservice.md)                             | Изменяет данные настройки службы.<br/>                                                                                                                                                                                                    |
| [**модифисистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)             | Изменяет общие параметры системных компонентов.<br/>                                                                                                                                                                                             |
| [**модифисистемсеттингс**](modifysystemsettings-msvm-virtualsystemmanagementservice.md)                               | Изменяет параметры виртуальной машины.<br/>                                                                                                                                                                                                      |
| [**реализепланнедсистем**](realizeplannedsystem-msvm-virtualsystemmanagementservice.md)                               | Проверяет конфигурацию запланированной виртуальной машины и преобразует ее в реализованную виртуальную машину.<br/>                                                                                                                                 |
| [**ремовебутсаурцесеттингс**](msvm-virtualsystemmanagementservice-removebootsourcesettings.md)                       | Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.<br/> При применении к частям "текущей" конфигурации виртуальной системы, так как ресурсы активной виртуальной системы могут быть удалены.<br/>            |
| [**ремовефеатуресеттингс**](removefeaturesettings-msvm-virtualsystemmanagementservice.md)                             | Удаляет параметры компонентов из Ethernet-подключения виртуальной машины.<br/>                                                                                                                                                                    |
| [**ремовефибречаннелчап**](removefibrechannelchap-msvm-virtualsystemmanagementservice.md)                           | Удаление параметров DH-CHAP из искусственного Fibre Channel порта на виртуальной машине.<br/>                                                                                                                                                    |
| [**ремовегуестсервицесеттингс**](msvm-virtualsystemmanagementservice-removeguestservicesettings.md)                   | Удаляет параметры гостевой службы из конфигурации виртуальной системы.<br/> При применении к частям "текущей" конфигурации виртуальной системы в качестве побочного действия гостевые службы активной виртуальной системы могут быть изменены.<br/>         |
| [**ремовеквпитемс**](removekvpitems-msvm-virtualsystemmanagementservice.md)                                           | Удаляет существующие пары "ключ-значение" из виртуальной машины.<br/>                                                                                                                                                                                |
| [**ремовересаурцесеттингс**](removeresourcesettings-msvm-virtualsystemmanagementservice.md)                           | Удаляет параметры виртуального ресурса из конфигурации виртуальной машины.<br/>                                                                                                                                                                 |
| [**ремовесистемкомпонентсеттингс**](msvm-virtualsystemmanagementservice-removesystemcomponentsettings.md)             | Удаляет параметры универсального компонента из конфигурации виртуальной системы.<br/>                                                                                                                                                                 |
| [**Равен**](msvm-virtualsystemmanagementservice-requeststatechange.md)                                   | Этот метод не поддерживается.<br/>                                                                                                                                                                                                           |
| [**сетгуестнетворкадаптерконфигуратион**](setguestnetworkadapterconfiguration-msvm-virtualsystemmanagementservice.md) | Настраивает сетевые адаптеры в гостевой операционной системе.<br/>                                                                                                                                                                      |
| [**сетинитиалмачинеконфигуратиондата**](msvm-virtualsystemmanagementservice-setinitialmachineconfigurationdata.md)   | Задает исходные данные конфигурации ВИРТУАЛЬНОЙ машины.<br/>                                                                                                                                                                                         |
| [**StartService**](msvm-virtualsystemmanagementservice-startservice.md)                                               | Этот метод не поддерживается.<br/>                                                                                                                                                                                                           |
| [**StopService**](msvm-virtualsystemmanagementservice-stopservice.md)                                                 | Этот метод не поддерживается.<br/>                                                                                                                                                                                                           |
| [**тестнетворкконнектион**](msvm-virtualsystemmanagementservice-testnetworkconnection.md)                             | проверяет сетевое подключение виртуальной машины в среде Windows виртуализации сети.<br/>                                                                                                                                                 |
| [**упградесистемверсион**](msvm-virtualsystemmanagementservice-upgradesystemversion.md)                               | Обновляет виртуальную систему.<br/> При применении к параметрам системы "Текущая" Конфигурация виртуальной системы<br/>                                                                                                                 |
| [**валидатепланнедсистем**](validateplannedsystem-msvm-virtualsystemmanagementservice.md)                             | Проверяет указанную запланированную систему.<br/>                                                                                                                                                                                                 |



 

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемманажементсервице** имеет следующие свойства.

<dl> <dt>

**аваилаблерекуестедстатес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** . Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".

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

Имя класса или подкласса, используемого при создании экземпляра. Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service)и всегда имеет значение "мсвм \_ виртуалсистемманажементсервице".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "служба для создания виртуальных машин и управления ими".

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

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Служба управления виртуальными системами Hyper-V".

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

Включенные и отключенные состояния элемента. Это свойство также может указывать переходы между этими запрошенными состояниями. Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение 2 (включено).



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

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **Key**, **maxlen** (256)
</dt> </dl>

Метка, по которой известен объект. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение "VMMS".

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

Текущее состояние объекта. Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).

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
| <dl> <dt>12</dt> </dl> | Неприменимо.<br/> |



 

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

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.

</dd> <dt>

**статусдескриптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Строки, описывающие различные значения массива **OperationalStatus** . Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "служба работает нормально".

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

## <a name="remarks"></a>Remarks

Доступ к классу **\_ виртуалсистемманажементсервице мсвм** может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**](cim-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**](/previous-versions//cc136952(v=vs.85))
</dt> <dt>

[**Мсвм \_ виртуалсистемманажементсервице (v1)**](/previous-versions/windows/desktop/legacy/cc136940(v=vs.85))
</dt> <dt>

[Классы управления виртуальной системой](virtual-system-management-classes.md)
</dt> </dl>

 

