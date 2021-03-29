---
description: Представляет компьютерную систему под Windows.
ms.assetid: fdb9fe36-1b8a-4dfa-a1cd-55065017ba2a
ms.tgt_platform: multiple
title: Класс Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem
- Win32_ComputerSystem.SetPowerState
- Win32_ComputerSystem.AdminPasswordStatus
- Win32_ComputerSystem.AutomaticManagedPagefile
- Win32_ComputerSystem.AutomaticResetBootOption
- Win32_ComputerSystem.AutomaticResetCapability
- Win32_ComputerSystem.BootOptionOnLimit
- Win32_ComputerSystem.BootOptionOnWatchDog
- Win32_ComputerSystem.BootROMSupported
- Win32_ComputerSystem.BootupState
- Win32_ComputerSystem.BootStatus
- Win32_ComputerSystem.Caption
- Win32_ComputerSystem.ChassisBootupState
- Win32_ComputerSystem.ChassisSKUNumber
- Win32_ComputerSystem.CreationClassName
- Win32_ComputerSystem.CurrentTimeZone
- Win32_ComputerSystem.DaylightInEffect
- Win32_ComputerSystem.Description
- Win32_ComputerSystem.DNSHostName
- Win32_ComputerSystem.Domain
- Win32_ComputerSystem.DomainRole
- Win32_ComputerSystem.EnableDaylightSavingsTime
- Win32_ComputerSystem.FrontPanelResetStatus
- Win32_ComputerSystem.HypervisorPresent
- Win32_ComputerSystem.InfraredSupported
- Win32_ComputerSystem.InitialLoadInfo
- Win32_ComputerSystem.InstallDate
- Win32_ComputerSystem.KeyboardPasswordStatus
- Win32_ComputerSystem.LastLoadInfo
- Win32_ComputerSystem.Manufacturer
- Win32_ComputerSystem.Model
- Win32_ComputerSystem.Name
- Win32_ComputerSystem.NameFormat
- Win32_ComputerSystem.NetworkServerModeEnabled
- Win32_ComputerSystem.NumberOfLogicalProcessors
- Win32_ComputerSystem.NumberOfProcessors
- Win32_ComputerSystem.OEMLogoBitmap
- Win32_ComputerSystem.OEMStringArray
- Win32_ComputerSystem.PartOfDomain
- Win32_ComputerSystem.PauseAfterReset
- Win32_ComputerSystem.PCSystemType
- Win32_ComputerSystem.PCSystemTypeEx
- Win32_ComputerSystem.PowerManagementCapabilities
- Win32_ComputerSystem.PowerManagementSupported
- Win32_ComputerSystem.PowerOnPasswordStatus
- Win32_ComputerSystem.PowerState
- Win32_ComputerSystem.PowerSupplyState
- Win32_ComputerSystem.PrimaryOwnerContact
- Win32_ComputerSystem.PrimaryOwnerName
- Win32_ComputerSystem.ResetCapability
- Win32_ComputerSystem.ResetCount
- Win32_ComputerSystem.ResetLimit
- Win32_ComputerSystem.Roles
- Win32_ComputerSystem.Status
- Win32_ComputerSystem.SupportContactDescription
- Win32_ComputerSystem.SystemFamily
- Win32_ComputerSystem.SystemSKUNumber
- Win32_ComputerSystem.SystemStartupDelay
- Win32_ComputerSystem.SystemStartupOptions
- Win32_ComputerSystem.SystemStartupSetting
- Win32_ComputerSystem.SystemType
- Win32_ComputerSystem.ThermalState
- Win32_ComputerSystem.TotalPhysicalMemory
- Win32_ComputerSystem.UserName
- Win32_ComputerSystem.WakeUpType
- Win32_ComputerSystem.Workgroup
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e5282c854bfdb1ce4b80f61a202ebecac990576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141167"
---
# <a name="win32_computersystem-class"></a>\_Класс Win32 ComputerSystem

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ ComputerSystem** представляет компьютер, работающий под Windows.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4B0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystem : CIM_UnitaryComputerSystem
{
  uint16   AdminPasswordStatus;
  boolean  AutomaticManagedPagefile;
  boolean  AutomaticResetBootOption;
  boolean  AutomaticResetCapability;
  uint16   BootOptionOnLimit;
  uint16   BootOptionOnWatchDog;
  boolean  BootROMSupported;
  string   BootupState;
  uint16   BootStatus[];
  string   Caption;
  uint16   ChassisBootupState;
  string   ChassisSKUNumber;
  string   CreationClassName;
  sint16   CurrentTimeZone;
  boolean  DaylightInEffect;
  string   Description;
  string   DNSHostName;
  string   Domain;
  uint16   DomainRole;
  boolean  EnableDaylightSavingsTime;
  uint16   FrontPanelResetStatus;
  boolean  HypervisorPresent;
  boolean  InfraredSupported;
  string   InitialLoadInfo[];
  datetime InstallDate;
  uint16   KeyboardPasswordStatus;
  string   LastLoadInfo;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   NameFormat;
  boolean  NetworkServerModeEnabled;
  uint32   NumberOfLogicalProcessors;
  uint32   NumberOfProcessors;
  uint8    OEMLogoBitmap[];
  string   OEMStringArray[];
  boolean  PartOfDomain;
  sint64   PauseAfterReset;
  uint16   PCSystemType;
  uint16   PCSystemTypeEx;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PowerOnPasswordStatus;
  uint16   PowerState;
  uint16   PowerSupplyState;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  uint16   ResetCapability;
  sint16   ResetCount;
  sint16   ResetLimit;
  string   Roles[];
  string   Status;
  string   SupportContactDescription[];
  string   SystemFamily;
  string   SystemSKUNumber;
  uint16   SystemStartupDelay;
  string   SystemStartupOptions[];
  uint8    SystemStartupSetting;
  string   SystemType;
  uint16   ThermalState;
  uint64   TotalPhysicalMemory;
  string   UserName;
  uint16   WakeUpType;
  string   Workgroup;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ ComputerSystem** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ ComputerSystem** содержит следующие методы.



| Метод                                                                                          | Описание                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жоиндомаинорворкграуп**](joindomainorworkgroup-method-in-class-win32-computersystem.md)     | Добавляет компьютерную систему в домен или рабочую группу.<br/>                                                                                                                                                                                   |
| [**Имени**](rename-method-in-class-win32-computersystem.md)                                   | Переименовывает локальный компьютер.<br/>                                                                                                                                                                                                          |
| **SetPowerState**                                                                               | Не реализован. Дополнительные сведения о том, как реализовать этот метод, см. в описании метода [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) в [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).<br/> |
| [**унжоиндомаинорворкграуп**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md) | Удаляет компьютерную систему из домена или рабочей группы.<br/>                                                                                                                                                                              |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ ComputerSystem** имеет следующие свойства.

<dl> <dt>

**админпассвордстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| админпассвордстатус")
</dt> </dl>

Параметры безопасности оборудования системы для состояния пароля администратора.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**аутоматикманажедпажефиле**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Если **значение — true**, система управляет файлом подкачки.

</dd> <dt>

**аутоматикресетбутоптион**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ \_ \\ \\ System \\ \\ CurrentControlSet \\ \\ Control \\ \\ крашконтрол \| rereboot")
</dt> </dl>

Если задано **значение true**, то включен режим автоматической перезагрузки.

</dd> <dt>

**аутоматикресеткапабилити**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Если задано **значение true**, автоматический сброс включен.

</dd> <dt>

**бутоптиононлимит**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| возможности \| загрузки при ограничении")
</dt> </dl>

Параметр загрузки имеет значение ON. Определяет системное действие при достижении значения **ресетлимит** .

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Зарезервировано** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Операционная система** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Системные служебные программы** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

Не **перезагружать** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**бутоптиононватчдог**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| возможностей \| загрузки")
</dt> </dl>

Тип действия перезагрузки после истечения времени таймера наблюдения.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Зарезервировано** (0)


</dt> <dd></dd> <dt>

<span id="Operating_system"></span><span id="operating_system"></span><span id="OPERATING_SYSTEM"></span>

**Операционная система** (1)


</dt> <dd></dd> <dt>

<span id="System_utilities"></span><span id="system_utilities"></span><span id="SYSTEM_UTILITIES"></span>

**Системные служебные программы** (2)


</dt> <dd></dd> <dt>

<span id="Do_not_reboot"></span><span id="do_not_reboot"></span><span id="DO_NOT_REBOOT"></span>

Не **перезагружать** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**бутромсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Если **значение — true**, указывает, поддерживается ли загрузочное ПЗУ.

</dd> <dt>

**бутстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 32. \| состояние загрузки системной информации \| ")
</dt> </dl>

Состояние и дополнительные поля данных, которые указывают состояние загрузки.

Это значение берется из элемента **состояние загрузки** в структуре **сведений о загрузке системы** в сведениях SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.

</dd> <dt>

**бутупстате**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетсистемметрикс**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) \| SM \_ клеанбут")
</dt> </dl>

Система запущена. Безошибочная Загрузка обходит файлы запуска пользователей, также называемые SafeBoot.

В следующем списке содержатся необходимые значения:

<dl> <dd>"Обычная загрузка"</dd> <dd>"Неудачно безопасный запуск"</dd> <dd>"Безопасный режим с сетевой загрузкой"</dd> </dl>

<dt>

<span id="Normal_boot"></span><span id="normal_boot"></span><span id="NORMAL_BOOT"></span>

**Обычная загрузка** ("Обычная загрузка")


</dt> <dd></dd> <dt>

<span id="Fail-safe_boot"></span><span id="fail-safe_boot"></span><span id="FAIL-SAFE_BOOT"></span>

**Отказоустойчивая загрузка** ("неудачно безопасный запуск")


</dt> <dd></dd> <dt>

<span id="Fail-safe_with_network_boot"></span><span id="fail-safe_with_network_boot"></span><span id="FAIL-SAFE_WITH_NETWORK_BOOT"></span>

**Отказоустойчивость с сетевой загрузкой** ("отказоустойчивость с сетевой загрузкой")


</dt> <dd></dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Краткое описание объекта — однострочная строка.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**чассисбутупстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3, \| загрузочное состояние")
</dt> </dl>

Загрузка состояния корпуса.

Это значение берется из элемента **состояние загрузки** в структуре **корпуса или шасси** в сведениях SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Безопасность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Критическая** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Без возможности восстановления** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**чассисскунумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| - \| номера SKU корпуса")
</dt> </dl>

Номер SKU шасси или корпуса в виде строки.

Это значение берется из **номера SKU** в структуре **System корпуса или корпуса** в информации SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Имя первого конкретного класса в цепочке наследования экземпляра. Это свойство можно использовать с другими свойствами класса для обнаружения всех экземпляров класса и его подклассов.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**курренттимезоне**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| времени структуры времени \| [**часового \_ пояса \_**](/windows/desktop/api/timezoneapi/ns-timezoneapi-time_zone_information) \| "), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("минуты")
</dt> </dl>

Время, в течение которого единая система компьютера смещается со времени в формате UTC.

</dd> <dt>

**дайлигхтинеффект**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| функции времени Win32API \| [**жеттимезонеинформатион**](/windows/desktop/api/timezoneapi/nf-timezoneapi-gettimezoneinformation)")
</dt> </dl>

Если задано **значение true**, режим летнего сбережения включен.

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

**Атрибуты**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| предполагался сбой getcomputernameex \| компутернамедншостнаме")
</dt> </dl>

Имя локального компьютера в соответствии с именем сервера доменных имен (DNS).

</dd> <dt>

**Доменная**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**вкста \_ info \_ 100**](/windows/desktop/api/lmwksta/ns-lmwksta-wksta_info_100) \| wki100 \_ ланграуп")
</dt> </dl>

Имя домена, к которому принадлежит компьютер.

> [!Note]  
> Если компьютер не входит в домен, возвращается имя рабочей группы.

 

</dd> <dt>

**DomainRole**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Directory Service (DS) Structures \| [**дсроле \_ основной \_ домен \_ сведения \_ Basic**](/windows/desktop/api/dsrole/ns-dsrole-dsrole_primary_domain_info_basic) \| [**дсроле \_ Machine \_ Role**](/windows/desktop/api/dsrole/ne-dsrole-dsrole_machine_role) \| мачинероле")
</dt> </dl>

Роль компьютера в назначенной Рабочей группе домена. Доменная Рабочая группа — это коллекция компьютеров в одной сети. Например, свойство **DomainRole** может показывать, что компьютер является членом рабочей станции.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

<dt>

<span id="Standalone_Workstation"></span><span id="standalone_workstation"></span><span id="STANDALONE_WORKSTATION"></span>

**Автономная рабочая станция** (0)


</dt> <dd></dd> <dt>

<span id="Member_Workstation"></span><span id="member_workstation"></span><span id="MEMBER_WORKSTATION"></span>

**Рядовая Рабочая станция** (1)


</dt> <dd></dd> <dt>

<span id="Standalone_Server"></span><span id="standalone_server"></span><span id="STANDALONE_SERVER"></span>

**Изолированный сервер** (2)


</dt> <dd></dd> <dt>

<span id="Member_Server"></span><span id="member_server"></span><span id="MEMBER_SERVER"></span>

**Рядовой сервер** (3)


</dt> <dd></dd> <dt>

<span id="Backup_Domain_Controller"></span><span id="backup_domain_controller"></span><span id="BACKUP_DOMAIN_CONTROLLER"></span>

**Резервный контроллер домена** (4)


</dt> <dd></dd> <dt>

<span id="Primary_Domain_Controller"></span><span id="primary_domain_controller"></span><span id="PRIMARY_DOMAIN_CONTROLLER"></span>

**Основной контроллер домена** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**енабледайлигхтсавингстиме**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Включает летнее время (DST) на компьютере. Значение **true** указывает, что системное время меняется на час вперед или назад при начале или ОКОНЧАНИи летнего времени. Значение **false** указывает, что системное время не меняется на час впереди или после окончания летнего времени. Значение **null** указывает, что состояние DST неизвестно в системе.

</dd> <dt>

**фронтпанелресетстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| фронтпанелресетстатус")
</dt> </dl>

В следующей таблице перечислены параметры безопасности оборудования для кнопки Сброс на компьютере.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**хипервисорпресент**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Если задано **значение true**, низкоуровневая оболочка.

**Windows server 2008 R2, Windows 7, Windows Server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 8 и Windows Server 2012.

</dd> <dt>

**инфраредсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**Значение true** показывает, что инфракрасный порт (IR) существует в компьютерной системе.

</dd> <dt>

**инитиаллоадинфо**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Данные, необходимые для поиска устройства начальной загрузки или службы загрузки для запроса запуска операционной системы.

Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

**Windows Server 2008 R2:** Это свойство доступно, но пусто.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")
</dt> </dl>

Объект установлен. Для объекта не требуется значение, указывающее, что он установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**кэйбоардпассвордстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| кэйбоардпассвордстатус")
</dt> </dl>

Параметры безопасности оборудования системы для состояния пароля клавиатуры.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ластлоадинфо**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Элемент массива свойства **инитиаллоадинфо** , содержащего данные для запуска загруженной операционной системы.

Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

</dd> <dt>

**Производителя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| поставщик сведений о системе SMBIOS Type 1 \| )"
</dt> </dl>

Имя изготовителя компьютера.

Пример: Adventure Works

</dd> <dt>

**Модель**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| системная информация \| Название продукта")
</dt> </dl>

Название продукта, которое изготовитель передает компьютеру. Это свойство должно иметь значение.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ключ экземпляра [**\_ системы CIM**](cim-system.md) в корпоративной среде.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**намеформат**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение **имени** системы компьютера, создаваемое автоматически. Объект [**CIM \_ ComputerSystem**](cim-computersystem.md) и его производные являются объектами верхнего уровня модель CIM (CIM). Они предоставляют область для нескольких компонентов. Требуются [**уникальные \_ системные ключи CIM**](cim-system.md) , но можно определить эвристику для создания имени **CIM \_ ComputerSystem** , создающего то же имя, и оно не зависит от протокола обнаружения. Это предотвращает проблемы с инвентаризацией и управлением, когда один и тот же ресурс или сущность обнаруживается несколько раз, но не может быть разрешена в один объект. Рекомендуется использовать эвристический подход, но это не обязательно.

Эвристический алгоритм описан в спецификации общей модели CIM V2 и предполагает, что для определения и назначения имени используются документированные правила. Список значений **намеформат** определяет порядок назначения имени системы компьютера. Несколько правил сопоставляются с одним и тем же значением.

Значение [**\_ имени системы CIM**](cim-computersystem.md) , которое вычисляется с помощью эвристики, является ключевым значением в системе. Однако используйте псевдонимы, чтобы назначить другое имя для **CIM \_ ComputerSystem**, которое может быть более уникальным для вашей компании.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

В эти значения входят:

<dt>

<span id="IP"></span><span id="ip"></span>

**IP-адрес** ("IP")


</dt> <dd></dd> <dt>

<span id="Dial"></span><span id="dial"></span><span id="DIAL"></span>

**Набрать номер** ("набрать")


</dt> <dd></dd> <dt>

<span id="HID"></span><span id="hid"></span>

**HID** (HID)


</dt> <dd></dd> <dt>

<span id="NWA"></span><span id="nwa"></span>

**НВА** ("НВА")


</dt> <dd></dd> <dt>

<span id="HWA"></span><span id="hwa"></span>

**Хва** ("Хва")


</dt> <dd></dd> <dt>

<span id="X25"></span><span id="x25"></span>

**X25** ("x25")


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** (ISDN)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** ("IPX")


</dt> <dd></dd> <dt>

<span id="DCC"></span><span id="dcc"></span>

**ДКК** ("ДКК")


</dt> <dd></dd> <dt>

<span id="ICD"></span><span id="icd"></span>

**ICD** ("ICD")


</dt> <dd></dd> <dt>

<span id="E.164"></span><span id="e.164"></span>

**E. 164** ("E. 164")


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** ("SNA")


</dt> <dd></dd> <dt>

<span id="OID_OSI"></span><span id="oid_osi"></span>

**OID/OSI** ("OID/OSI")


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** ("другое")


</dt> <dd></dd> </dl>

</dd> <dt>

**нетворксервермодинаблед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Network Management Structures \| [**Server \_ info \_ 101**](/windows/desktop/api/lmserver/ns-lmserver-server_info_101) \| sv101 \_ Type \| ОКП \_ Type \_ Server")
</dt> </dl>

**Значение true** показывает, что режим сетевого сервера включен.

</dd> <dt>

**нумберофлогикалпроцессорс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Число логических процессоров, доступных на компьютере.

Можно использовать **нумберофлогикалпроцессорс** и **NumberOfProcessors** , чтобы определить, является ли компьютер технологией Hyper-Threading. Дополнительные сведения см. в подразделе "Примечания".

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| двнумберофпроцессорс")
</dt> </dl>

Число физических процессоров, доступных в данный момент в системе. Это число включенных в систему процессоров, которые не включают отключенные процессоры. Если компьютерная система содержит два физических процессора, каждый из которых содержит два логических процессора, значение **NumberOfProcessors** равно 2, а **нумберофлогикалпроцессорс** — 4. Процессоры могут быть многоядерными, или же они могут быть процессорами технологии Hyper. Дополнительные сведения см. в подразделе "Примечания".

</dd> <dt>

**оемлогобитмап**
</dt> <dd> <dl> <dt>

Тип данных: массив **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Список данных для точечного рисунка, создаваемого изготовителем оборудования (OEM).

</dd> <dt>

**оемстрингаррай**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 11: \| строки OEM")
</dt> </dl>

Список произвольных строк, определяемых изготовителем оборудования. Например, изготовитель оборудования определяет номера частей для справочных документов по системе, контактные данные производителя и т. д.

</dd> <dt>

**партофдомаин**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

**Значение true** показывает, что компьютер является частью домена. Если значение равно **null**, компьютер не находится в домене или состояние неизвестно. Если удалить компьютер из домена, значение будет **равно false**.

</dd> <dt>

**паусеафтерресет**
</dt> <dd> <dl> <dt>

Тип данных: **sint64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| timeout"), [**единиц**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунд")
</dt> </dl>

Временная задержка перед инициацией перезагрузки в миллисекундах. Он используется после системного цикла питания, локального или удаленного сброса системы и автоматического сброса системы. Значение 1 (минус единица) указывает на то, что значение приостановки неизвестно.

**Windows Vista:** Это свойство может возвращать неизвестное число.

</dd> <dt>

**пксистемтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Тип используемого компьютера, например портативный компьютер, Настольный компьютер или планшетный компьютер.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>Не **указано** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Рабочий стол** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>**Мобильные устройства** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>**Рабочая станция** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>**Корпоративный сервер** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>**Сервер локальной** сети (5)


</dt> <dd>

Небольшой офисный и домашний офисный сервер

</dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>**Устройство PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>**Сервер производительности** (7)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**пксистемтипикс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Тип используемого компьютера, например портативный компьютер, Настольный компьютер или планшетный компьютер.

**Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 8.1 и Windows Server 2012 R2.

<dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

Не **указано** (0)


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

**Рабочий стол** (1)


</dt> <dd></dd> <dt>

<span id="Mobile"></span><span id="mobile"></span><span id="MOBILE"></span>

**Мобильные устройства** (2)


</dt> <dd></dd> <dt>

<span id="Workstation"></span><span id="workstation"></span><span id="WORKSTATION"></span>

**Рабочая станция** (3)


</dt> <dd></dd> <dt>

<span id="Enterprise_Server"></span><span id="enterprise_server"></span><span id="ENTERPRISE_SERVER"></span>

**Корпоративный сервер** (4)


</dt> <dd></dd> <dt>

<span id="SOHO_Server"></span><span id="soho_server"></span><span id="SOHO_SERVER"></span>

**Сервер локальной** сети (5)


</dt> <dd></dd> <dt>

<span id="Appliance_PC"></span><span id="appliance_pc"></span><span id="APPLIANCE_PC"></span>

**Устройство PC** (6)


</dt> <dd></dd> <dt>

<span id="Performance_Server"></span><span id="performance_server"></span><span id="PERFORMANCE_SERVER"></span>

**Сервер производительности** (7)


</dt> <dd></dd> <dt>

<span id="Slate"></span><span id="slate"></span><span id="SLATE"></span>

**Содержание** (8)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Максимум** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**поверманажементкапабилитиес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")
</dt> </dl>

Массив конкретных возможностей логического устройства, связанных с питанием.

Это свойство наследуется **от \_ CIM**-унаследованной модели.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Не поддерживается** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (3)


</dt> <dd>

Функции управления питанием в настоящее время включены, но точный набор функций неизвестен или информация недоступна.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Режимы энергосбережения** записываются автоматически (4)


</dt> <dd>

Устройство может изменить свое состояние электропитания на основе использования или других критериев.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Настраиваемое состояние питания** (5)


</dt> <dd>

Поддерживается метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Этот метод находится в родительском классе **класса \_ CIM** и может быть реализован. Дополнительные сведения см. в разделе [Конструирование классов MOF-файл (MOF)](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Поддержка циклов электропитания** (6)


</dt> <dd>

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (Power Cycle).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Поддерживается время включения** (7)


</dt> <dd>

Поддержка по времени Power-On

Метод [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) может быть вызван с параметром *PowerState* , установленным в значение 5 (цикл электропитания) и *временем* , равным определенной дате и времени (или интервалу) для включения питания.

</dd> </dl>

</dd> <dt>

**поверманажементсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Если **true**, устройство может управляться с помощью управления питанием, например, устройство может быть переведено в режим приостановки и т. д. Это свойство не указывает, что функции управления питанием включены в настоящее время, но это означает, что логическое устройство поддерживает управление питанием.

Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

</dd> <dt>

**поверонпассвордстатус**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 24 \| Параметры безопасности оборудования \| поверонпассвордстатус")
</dt> </dl>

Параметры безопасности оборудования системы для Power-On состояние пароля.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (0)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (1)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Не реализовано** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Установлен**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Текущее состояние электропитания компьютера и связанной с ним операционной системы. Состояния энергосбережения имеют следующие значения: значение 4 (неизвестно) указывает, что система находится в режиме энергосбережения, но ее точное состояние в этом режиме неизвестно. 2 (режим низкого энергопотребления) указывает, что система находится в состоянии энергосбережения, но по-прежнему работает и может привести к снижению производительности. 3 (в режиме ожидания) указывает, что система не работает, но ее можно быстро включить в полную мощность. и 7 (предупреждение) означает, что компьютерная система находится в состоянии предупреждения и режиме энергосбережения.

Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Энергосбережение **— неизвестно** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Энергосбережение **— предупреждение** (7)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>

<span id="Power_Save_-_Hibernate"></span><span id="power_save_-_hibernate"></span><span id="POWER_SAVE_-_HIBERNATE"></span>Энергосбережение **— режим гибернации** (8)


</dt> <dd>

Power Save Гибернация.

</dd> <dt>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>

<span id="Power_Save_-_Soft_Off"></span><span id="power_save_-_soft_off"></span><span id="POWER_SAVE_-_SOFT_OFF"></span>Энергосбережение **— мягкое отключение** (9)


</dt> <dd>

Энергосбережение с мягким отключением.

</dd> </dl>

</dd> <dt>

**поверсупплистате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| системного корпуса или \| состояние источника питания корпуса")
</dt> </dl>

Состояние источника питания или поставляется при последней загрузке.

Это значение берется из элемента **состояния источника питания** в структуре **корпуса или шасси** в сведениях SMBIOS.

В следующем списке указаны значения для этого свойства.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>**Безопасность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Критическая** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>**Без возможности восстановления** (6)


</dt> <dd>

Произошла неустранимая

</dd> </dl>

</dd> <dt>

**примарйовнерконтакт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Контактные данные для владельца первичной системы, например номер телефона, адрес электронной почты и т. д.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**примарйовнернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Имя основного владельца системы.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**ресеткапабилити**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")
</dt> </dl>

Если параметр включен, то значение равно 4, а единая система компьютера может быть сброшена с помощью кнопок включения и выключения. Если параметр отключен, значение равно 3, а сброс не разрешен.

Это свойство наследуется от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>**Не реализовано** (5)


</dt> <dd>

Произошла неустранимая

</dd> </dl>

</dd> <dt>

**ресеткаунт**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| Счетчик сброса системных сбросов \| ")
</dt> </dl>

Число автоматических сбросов с момента последнего сброса. Значение 1 (минус единица) указывает на то, что счетчик неизвестен.

</dd> <dt>

**ресетлимит**
</dt> <dd> <dl> <dt>

Тип данных: **sint16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 23 \| \| Превышено ограничение на сброс системы")
</dt> </dl>

Число последовательных попыток сброса системы. Значение 1 (минус единица) указывает на то, что ограничение неизвестно.

</dd> <dt>

**Роли**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Список, указывающий роли системы в среде информационных технологий.

Это свойство наследуется [**от \_ системы CIM**](cim-system.md).

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")
</dt> </dl>

Текущее состояние объекта.

Для Win32_ComputerSystem состояние всегда равно «ОК».

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dl>

</dd> <dt>

**суппортконтактдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| [](/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring) \| сведения о поддержке Win32API жетприватепрофилестринг")
</dt> </dl>

Список контактных данных службы поддержки для операционной системы Windows.

</dd> <dt>

**системфамили**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| семейство системных сведений SMBIOS Type 1 \| ")
</dt> </dl>

Семейство, к которому принадлежит определенный компьютер. Семейство относится к набору компьютеров, которые похожи, но не идентичны с точки зрения оборудования или программного обеспечения.

Это значение берется из члена **семьи** структуры **сведений о системе** в сведениях SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.

</dd> <dt>

**системскунумбер**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 1 \| системы, \| номер SKU")
</dt> </dl>

Определяет конфигурацию конкретного компьютера для продажи. Иногда он также называется ИДЕНТИФИКАТОРом продукта или номером заказа на покупку.

Это значение берется из **номера SKU** в структуре **сведений о системе** в сведениях SMBIOS.

**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows server 2008 и Windows Vista:** Это свойство не поддерживается до Windows 10 и Windows Server 2016.

</dd> <dt>

**системстартупделай**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**устаревшие**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетприватепрофилеинт**](/windows/desktop/api/winbase/nf-winbase-getprivateprofileint) \| \| время ожидания загрузки"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("секунды")
</dt> </dl>

**Системстартупделай** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы. Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .

</dd> <dt>

**системстартупоптионс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| [**жетприватепрофилесектион**](/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection) \| операционные системы")
</dt> </dl>

**Системстартупоптионс** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы. Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .

</dd> <dt>

**системстартупсеттинг**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**привилегии**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Сесистеменвиронментпривилеже"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

**Системстартупсеттинг** больше не доступен для использования, так как Boot.ini не используется для настройки запуска системы. Вместо этого используйте [классы BCD](/previous-versions/windows/desktop/bcd/bcd-classes) , предоставляемые поставщиком WMI данные конфигурации загрузки (BCD) или команду **BCDEdit** .

</dd> <dt>

**SystemType**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information Structures \| [**System \_ info**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) \| впроцессорарчитектуре")
</dt> </dl>

Система на компьютере под управлением Windows. Это свойство должно иметь значение.

В следующем списке указаны некоторые из возможных значений этого свойства.

<dl> <dd>"компьютер на базе x64"</dd> <dd>"Компьютер на базе x86"</dd> <dd>"ПК на основе MIPS"</dd> <dd>"ПК на базе Alpha"</dd> <dd>"Power PC"</dd> <dd>«КОМПЬЮТЕР SH-x»</dd> <dd>"Стронгарм ПК"</dd> <dd>"64-разрядный Intel PC"</dd> <dd>"64-разрядный ПК Alpha"</dd> <dd>Неизвестный</dd> <dd>"X86-Nec98 PC"</dd> </dl>

<dt>

<span id="X86-based_PC"></span><span id="x86-based_pc"></span><span id="X86-BASED_PC"></span>

**Компьютер на базе x86** ("ПК на базе x86")


</dt> <dd></dd> <dt>

<span id="MIPS-based_PC"></span><span id="mips-based_pc"></span><span id="MIPS-BASED_PC"></span>

**Компьютер на основе MIPS** ("ПК на основе MIPS")


</dt> <dd></dd> <dt>

<span id="Alpha-based_PC"></span><span id="alpha-based_pc"></span><span id="ALPHA-BASED_PC"></span>

**ПК на базе Alpha** ("ПК на основе Alpha")


</dt> <dd></dd> <dt>

<span id="Power_PC"></span><span id="power_pc"></span><span id="POWER_PC"></span>

**Power PC** ("Power PC")


</dt> <dd></dd> <dt>

<span id="SH-x_PC"></span><span id="sh-x_pc"></span><span id="SH-X_PC"></span>

**Компьютер SH-x** («компьютер SH-x»)


</dt> <dd></dd> <dt>

<span id="StrongARM_PC"></span><span id="strongarm_pc"></span><span id="STRONGARM_PC"></span>

**СТРОНГАРМ ПК** ("стронгарм PC")


</dt> <dd></dd> <dt>

<span id="64-bit_Intel_PC"></span><span id="64-bit_intel_pc"></span><span id="64-BIT_INTEL_PC"></span>

**64-разрядный компьютер Intel** ("64-разрядный Intel PC")


</dt> <dd></dd> <dt>

<span id="x64-based_PC"></span><span id="x64-based_pc"></span><span id="X64-BASED_PC"></span>

**компьютер на базе x64** ("ПК на базе x64")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** ("неизвестно")


</dt> <dd></dd> <dt>

<span id="X86-Nec98_PC"></span><span id="x86-nec98_pc"></span><span id="X86-NEC98_PC"></span>

**X86-NEC98 PC** ("x86-Nec98 PC")


</dt> <dd></dd> </dl>

</dd> <dt>

**сермалстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| тип SMBIOS 3 \| системного корпуса или \| термальное состояние корпуса")
</dt> </dl>

Состояние температуры системы при последней загрузке.

Это значение берется из элемента " **состояние тепловой температуры** " в структуре **корпуса или** в данных SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="Safe"></span><span id="safe"></span><span id="SAFE"></span>

**Безопасность** (3)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Предупреждение** (4)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Критическая** (5)


</dt> <dd></dd> <dt>

<span id="Non-recoverable"></span><span id="non-recoverable"></span><span id="NON-RECOVERABLE"></span>

**Без возможности восстановления** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**TotalPhysicalMemory**
</dt> <dd> <dl> <dt>

Тип данных: **UInt64**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| структуры управления памятью \| [**MEMORYSTATUS**](/windows/desktop/api/winbase/ns-winbase-memorystatus) \| двтоталфис"), [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("байт")
</dt> </dl>

Общий размер физической памяти. Имейте в виду, что в некоторых обстоятельствах это свойство может не возвращать точное значение физической памяти. Например, неточна, если BIOS использует часть физической памяти. Чтобы получить точное значение, используйте вместо этого свойство **Capacity** в [**Win32 \_ фисикалмемори**](win32-physicalmemory.md) .

Пример: 67108864

Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| System Information functions- \| [**username**](/windows/desktop/api/winbase/nf-winbase-getusernamea)")
</dt> </dl>

Имя пользователя, выполнившего вход в систему. Это свойство должно иметь значение. В сеансе служб терминалов **username** возвращает имя пользователя, вошедшего в консоль, а не пользователя, вошедшего в систему во время сеанса службы терминалов.

Пример: жеффсмис

</dd> <dt>

**вакеуптипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("тип SMBIOS \| 1 \| системная информация о \| типе пробуждения")
</dt> </dl>

Событие, которое приводит к включению системы.

Это значение берется из члена **типа пробуждения** в структуре **сведений о системе** в сведениях SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Зарезервировано** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (2)


</dt> <dd></dd> <dt>

<span id="APM_Timer"></span><span id="apm_timer"></span><span id="APM_TIMER"></span>

**Таймер APM** (3)


</dt> <dd></dd> <dt>

<span id="Modem_Ring"></span><span id="modem_ring"></span><span id="MODEM_RING"></span>

**Кольцо модема** (4)


</dt> <dd></dd> <dt>

<span id="LAN_Remote"></span><span id="lan_remote"></span><span id="LAN_REMOTE"></span>

**Удаленная локальная сеть** (5)


</dt> <dd></dd> <dt>

<span id="Power_Switch"></span><span id="power_switch"></span><span id="POWER_SWITCH"></span>

**Выключатель питания** (6)


</dt> <dd></dd> <dt>

<span id="PCI_PME_"></span><span id="pci_pme_"></span>

**PCI PME \#** 7


</dt> <dd></dd> <dt>

<span id="AC_Power_Restored"></span><span id="ac_power_restored"></span><span id="AC_POWER_RESTORED"></span>

**Питание от сети восстановлено** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Группе**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("")
</dt> </dl>

Имя рабочей группы для этого компьютера. Если свойство **партофдомаин** имеет значение **false**, то возвращается имя рабочей группы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы определить общее число экземпляров процессора, связанных с объектом системы компьютера, используйте класс сопоставления [**Win32 \_ компутерсистемпроцессор**](win32-computersystemprocessor.md) .

Экземпляр **Win32 \_ ComputerSystem** с несколькими физическими процессорами связан с несколькими экземплярами [**\_ процессора Win32**](win32-processor.md) . Если значение **нумберофлогикалпроцессорс** больше, чем значение **NumberOfProcessors** , то компьютерная система является либо многоядерной системой, либо для нее включен один или несколько процессоров. Дополнительные сведения см. в разделе **нумберофлогикалпроцессорс** and **нумберофкорес** Properties and remarks статьи **Win32 \_ Processor**.

Класс **Win32 \_ ComputerSystem** является производным от [**CIM \_ унитарикомпутерсистем**](cim-unitarycomputersystem.md).

## <a name="examples"></a>Примеры

Следующий [пример кода](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Display-computers-status-c8ff289d) в центре сценариев использует **Win32 \_ ComputerSystem** для получения информации из нескольких компьютерных систем и отображает их в графическом интерфейсе пользователя.

Пример сценария, который получает данные об операционной системе и процессоре из **Win32 \_ ComputerSystem**, [**\_ процессора Win32**](win32-processor.md)и Win32 Operating, [**можно \_**](win32-operatingsystem.md) найти в примерах, посвященных [**\_ процессору Win32**](win32-processor.md) .

Следующий пример сценария VBScript описывает, как получить доменное имя локального компьютера из экземпляров **Win32 \_ ComputerSystem**.


```VB
Set SystemSet = GetObject("winmgmts:").InstancesOf ("Win32_ComputerSystem")

for each System in SystemSet
 WScript.Echo System.Domain
next
```



В следующем образце Perl показано, как получить имя локального компьютера из экземпляров **Win32 \_ ComputerSystem**.


```
use strict;
use Win32::OLE;

my ($SystemSet, $System);  
eval {$SystemSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("Win32_ComputerSystem") };
  
unless($@)
{
 foreach $System (in $SystemSet)
 {
  print "\n", $System->{Domain}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



В следующем образце Perl описывается получение доменного имени DNS локального компьютера из экземпляров **Win32 \_ ComputerSystem**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($NICSet, $NIC);  
eval {$NICSet = Win32::OLE->GetObject("winmgmts:!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled=true"); };
if (!$@ && defined $NICSet)
{
 foreach $NIC (in $NICSet)
 {
  if(defined $NIC->{DNSDomain})
  {
   print "\n", $NIC->{DNSDomain}, "\n";
  }
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
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

[**\_УНИТАРИКОМПУТЕРСИСТЕМ CIM**](cim-unitarycomputersystem.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[Задачи WMI: учетные записи и домены](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Задачи WMI: оборудование компьютера](/windows/desktop/WmiSdk/wmi-tasks--computer-hardware)
</dt> <dt>

[Задачи WMI: управление рабочим столом](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

