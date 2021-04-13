---
title: Класс Win32_TerminalServiceSetting
description: Представляет конфигурацию для сервера узла сеансов удаленный рабочий стол сеансов (удаленных рабочих столов).
ms.assetid: 4cd047db-921f-4ccb-946b-d2c7b8d6beea
ms.tgt_platform: multiple
keywords:
- Класс Win32_TerminalServiceSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TerminalServiceSetting, описание
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting.Caption
- Win32_TerminalServiceSetting.Description
- Win32_TerminalServiceSetting.InstallDate
- Win32_TerminalServiceSetting.Name
- Win32_TerminalServiceSetting.Status
- Win32_TerminalServiceSetting.ServerName
- Win32_TerminalServiceSetting.TerminalServerMode
- Win32_TerminalServiceSetting.GetCapabilitiesID
- Win32_TerminalServiceSetting.LicensingType
- Win32_TerminalServiceSetting.PolicySourceLicensingType
- Win32_TerminalServiceSetting.PossibleLicensingTypes
- Win32_TerminalServiceSetting.LicensingName
- Win32_TerminalServiceSetting.LicensingDescription
- Win32_TerminalServiceSetting.ActiveDesktop
- Win32_TerminalServiceSetting.UserPermission
- Win32_TerminalServiceSetting.DeleteTempFolders
- Win32_TerminalServiceSetting.PolicySourceDeleteTempFolders
- Win32_TerminalServiceSetting.UseTempFolders
- Win32_TerminalServiceSetting.PolicySourceUseTempFolders
- Win32_TerminalServiceSetting.AllowTSConnections
- Win32_TerminalServiceSetting.PolicySourceAllowTSConnections
- Win32_TerminalServiceSetting.SingleSession
- Win32_TerminalServiceSetting.PolicySourceSingleSession
- Win32_TerminalServiceSetting.ProfilePath
- Win32_TerminalServiceSetting.PolicySourceProfilePath
- Win32_TerminalServiceSetting.HomeDirectory
- Win32_TerminalServiceSetting.PolicySourceHomeDirectory
- Win32_TerminalServiceSetting.TimeZoneRedirection
- Win32_TerminalServiceSetting.PolicySourceTimeZoneRedirection
- Win32_TerminalServiceSetting.Logons
- Win32_TerminalServiceSetting.DirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceDirectConnectLicenseServers
- Win32_TerminalServiceSetting.PolicySourceConfiguredLicenseServers
- Win32_TerminalServiceSetting.DisableForcibleLogoff
- Win32_TerminalServiceSetting.PolicySourceDisableForcibleLogoff
- Win32_TerminalServiceSetting.FallbackPrintDriverType
- Win32_TerminalServiceSetting.PolicySourceFallbackPrintDriverType
- Win32_TerminalServiceSetting.SessionBrokerDrainMode
- Win32_TerminalServiceSetting.LimitedUserSessions
- Win32_TerminalServiceSetting.EnableDFSS
- Win32_TerminalServiceSetting.PolicySourceEnableDFSS
- Win32_TerminalServiceSetting.EnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.PolicySourceEnableRemoteDesktopMSI
- Win32_TerminalServiceSetting.EnableAutomaticReconnection
- Win32_TerminalServiceSetting.PolicySourceEnableAutomaticReconnection
- Win32_TerminalServiceSetting.UseRDEasyPrintDriver
- Win32_TerminalServiceSetting.PolicySourceUseRDEasyPrintDriver
- Win32_TerminalServiceSetting.RedirectSmartCards
- Win32_TerminalServiceSetting.PolicySourceRedirectSmartCards
- Win32_TerminalServiceSetting.EnableDiskFSS
- Win32_TerminalServiceSetting.EnableNetworkFSS
- Win32_TerminalServiceSetting.NetworkFSSUserSessionWeight
- Win32_TerminalServiceSetting.NetworkFSSLocalSystemWeight
- Win32_TerminalServiceSetting.NetworkFSSCatchAllWeight
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc03f02028a331a3688152a1ce8c57ada7269d07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341115"
---
# <a name="win32_terminalservicesetting-class"></a>\_Класс Win32 терминалсервицесеттинг

Класс **WMI \_ Терминалсервицесеттинг для Win32** представляет конфигурацию для сервера узла сеансов сеансов (RD) удаленный рабочий стол. Параметры включают такие возможности, как режим сервера узла сеансов удаленных рабочих столов, лицензирование, активный рабочий стол, разрешения, удаление временных папок и временные каталоги для сеансов.

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICESETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalServiceSetting : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   ServerName;
  uint32   TerminalServerMode;
  uint32   GetCapabilitiesID;
  uint32   LicensingType;
  uint32   PolicySourceLicensingType;
  uint32   PossibleLicensingTypes;
  string   LicensingName;
  string   LicensingDescription;
  uint32   ActiveDesktop;
  uint32   UserPermission;
  uint32   DeleteTempFolders;
  uint32   PolicySourceDeleteTempFolders;
  uint32   UseTempFolders;
  uint32   PolicySourceUseTempFolders;
  uint32   AllowTSConnections;
  uint32   PolicySourceAllowTSConnections;
  uint32   SingleSession;
  uint32   PolicySourceSingleSession;
  string   ProfilePath;
  uint32   PolicySourceProfilePath;
  string   HomeDirectory;
  uint32   PolicySourceHomeDirectory;
  uint32   TimeZoneRedirection;
  uint32   PolicySourceTimeZoneRedirection;
  string   Logons;
  string   DirectConnectLicenseServers;
  uint32   PolicySourceDirectConnectLicenseServers;
  uint32   PolicySourceConfiguredLicenseServers;
  uint32   DisableForcibleLogoff;
  uint32   PolicySourceDisableForcibleLogoff;
  uint32   FallbackPrintDriverType;
  uint32   PolicySourceFallbackPrintDriverType;
  uint32   SessionBrokerDrainMode;
  uint32   LimitedUserSessions;
  uint32   EnableDFSS;
  uint32   PolicySourceEnableDFSS;
  uint32   EnableRemoteDesktopMSI;
  uint32   PolicySourceEnableRemoteDesktopMSI;
  uint32   EnableAutomaticReconnection;
  uint32   PolicySourceEnableAutomaticReconnection;
  uint32   UseRDEasyPrintDriver;
  uint32   PolicySourceUseRDEasyPrintDriver;
  uint32   RedirectSmartCards;
  uint32   PolicySourceRedirectSmartCards;
  uint32   EnableDiskFSS;
  uint32   EnableNetworkFSS;
  uint32   NetworkFSSUserSessionWeight;
  uint32   NetworkFSSLocalSystemWeight;
  uint32   NetworkFSSCatchAllWeight;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ терминалсервицесеттинг** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ терминалсервицесеттинг** содержит следующие методы.



| Метод                                                                                                                | Описание                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**адддиректконнектлиценсесервер**](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | Настраивает новый сервер лицензирования в Организации.<br/>                                                                                                                  |
| [**аддлстоспеЦифиедлиценсесерверлист**](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | Добавляет указанный сервер лицензирования в конец списка указанных серверов лицензирования.<br/>                                                                                  |
| [**канакцесслиценсесервер**](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | Определяет, разрешено ли серверу узла сеансов удаленных рабочих столов запрашивать службы удаленных рабочих столов клиентских лицензий (RDS CAL) с сервера лицензирования удаленный рабочий стол.<br/> |
| [**ChangeMode**](win32-terminalservicesetting-changemode.md)                                                         | Задает тип лицензирования сервера лицензирования удаленный рабочий стол.<br/>                                                                                                       |
| [**креатевинстатион**](createwinstation-win32-terminalservicesetting.md)                                             | Создает новый стек прослушивателя на основе уникального сочетания имени прослушивателя и сетевого адаптера.<br/>                                                                              |
| [**делетедиректконнектлиценсесервер**](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | Удаляет указанный сервер лицензирования из Организации.<br/>                                                                                                           |
| [**емптиспеЦифиедлиценсесерверлист**](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | Удаляет все серверы лицензий из списка указанных серверов лицензирования.<br/>                                                                                             |
| [**финдлиценсесерверс**](findlicenseservers-win32-terminalservicesetting.md)                                         | Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.<br/>                                                                                   |
| [**Поддомен**](getdomain-win32-terminalservicesetting.md)                                                           | Возвращает имя домена, в который входит сервер узла сеансов удаленных рабочих столов.<br/>                                                                                    |
| [**жетграцепериоддайс**](getgraceperioddays-win32-terminalservicesetting.md)                                         | Извлекает количество дней, оставшихся в льготном периоде лицензирования удаленных рабочих столов для сервера узла сеансов удаленных рабочих столов.<br/>                                                     |
| [**жетрегистередлиценсесерверлист**](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | Возвращает список зарегистрированных серверов лицензирования.<br/>                                                                                                                        |
| [**жетспеЦифиедлиценсесерверлист**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Извлекает список указанных серверов лицензирования.<br/>                                                                                                                    |
| [**жеттсланаидс**](gettslanaids-win32-terminalservicesetting.md)                                                     | Возвращает идентификаторы и описания сетевых адаптеров службы удаленных рабочих столов.<br/>                                                                                          |
| [**жеттстолсконнективитистатус**](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.<br/>                                                                            |
| [**жетвинстатиондривернамес**](getwinstationdrivernames-win32-terminalservicesetting.md)                             | Возвращает список имен драйверов Винстатион.<br/>                                                                                                                        |
| [**пинглиценсесервер**](pinglicenseserver-win32-terminalservicesetting.md)                                           | Проверяет связь с сервером лицензирования, чтобы определить, является ли он действительным сервером лицензирования.<br/>                                                                                         |
| [**ремовелсфромспеЦифиедлиценсесерверлист**](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.<br/>                                                                                        |
| [**сеталловтсконнектионс**](win32-terminalservicesetting-setallowtsconnections.md)                                   | Задает свойство **алловтсконнектионс** .<br/>                                                                                                                           |
| [**сетдисаблефорЦиблелогофф**](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | Задает свойство **дисаблефорЦиблелогофф** .<br/>                                                                                                                        |
| [**сетфаллбаккпринтдривертипе**](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | Задает свойство **фаллбаккпринтдривертипе** .<br/>                                                                                                                      |
| [**сесомедиректори**](win32-terminalservicesetting-sethomedirectory.md)                                             | Задает свойство **хомедиректори** .<br/>                                                                                                                                |
| [**сетполиципропертинаме**](win32-terminalservicesetting-setpolicypropertyname.md)                                   | Задает одно из следующих свойств: **делететемпфолдерс** или **усетемпфолдерс**.<br/>                                                                                  |
| [**сетпримарилиценсесервер**](setprimarylicenseserver-win32-terminalservicesetting.md)                               | Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.<br/>                                                                          |
| [**сетпрофилепас**](win32-terminalservicesetting-setprofilepath.md)                                                 | Задает свойство **FilePath** .<br/>                                                                                                                                  |
| [**сетсинглесессион**](win32-terminalservicesetting-setsinglesession.md)                                             | Задает свойство **синглесессион** .<br/>                                                                                                                                |
| [**сетспеЦифиедлиценсесерверлист**](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.<br/>                                                                    |
| [**сеттимезонередиректион**](win32-terminalservicesetting-settimezoneredirection.md)                                 | Задает свойство **тимезонередиректион** .<br/>                                                                                                                          |
| [**упдатедиректконнектлиценсесервер**](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | Обновляет список серверов лицензирования обнаружения.<br/>                                                                                                                      |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ терминалсервицесеттинг** имеет следующие свойства.

<dl> <dt>

**активедесктоп**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешен ли активный рабочий стол в каждом сеансе пользователя.

<dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (0)


</dt> <dd>

Active Desktop не разрешается в каждом сеансе пользователя.

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (1)


</dt> <dd>

Разрешено использовать Active Desktop в каждом пользовательском сеансе.

</dd> </dl>

</dd> <dt>

**алловтсконнектионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешены ли новые службы удаленных рабочих столов подключения.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Новые подключения не допускаются.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Новые подключения разрешены.

</dd> </dl>

</dd> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое описание (однострочная строка) объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**делететемпфолдерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, удаляются ли временные каталоги при выходе из программы.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Удаление временных каталогов отключено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Удаление временных каталогов включено.

</dd> </dl>

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**директконнектлиценсесерверс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Это свойство недоступно.

**Windows Server 2008:** Перечисляет список серверов лицензирования.

</dd> <dt>

**дисаблефорЦиблелогофф**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет, можно ли принудительно завершить работу администратора, выполнившего вход в консоль.

<dt>

0
</dt> <dd>

Администратор может принудительно завершить работу.

</dd> <dt>

1
</dt> <dd>

Невозможно принудительно завершить работу администратора.

</dd> </dl>

</dd> <dt>

**енаблеаутоматикреконнектион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешено ли клиентам подключения удаленный рабочий стол автоматическое повторное подключение к сеансам на сервере узла сеансов удаленных рабочих столов, если сетевое подключение временно потеряно.

<dt>

0 (0x0)
</dt> <dd>

Автоматическое повторное подключение отключено.

</dd> <dt>

1 (0x1)
</dt> <dd>

Автоматическое повторное подключение включено.

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**енабледфсс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включено ли динамическое планирование равномерного предоставления общего доступа (ДФСС). Это может быть одно из следующих значений.

**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.

<dt>

0
</dt> <dd>

ДФСС отключен.

</dd> <dt>

1
</dt> <dd>

ДФСС включен.

</dd> </dl>

</dd> <dt>

**енабледискфсс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включено ли планирование распределения дискового ресурса.

<dt>

0 (0x0)
</dt> <dd>

Планирование распределения дискового ресурса отключено.

</dd> <dt>

1 (0x1)
</dt> <dd>

Планирование распределения дискового ресурса включено.

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**енабленетворкфсс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включено ли планирование распределения ресурсов по сети.

<dt>

0 (0x0)
</dt> <dd>

Планирование распределения сетевых ресурсов отключено.

</dd> <dt>

1 (0x1)
</dt> <dd>

Планирование распределения сетевых ресурсов включено.

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**енаблеремотедесктопмси**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, включен или отключен удаленный рабочий стол MSI.

<dt>

0 (0x0)
</dt> <dd>

Выключено

</dd> <dt>

1 (0x1)
</dt> <dd>

Активировано

</dd> </dl>

**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**фаллбаккпринтдривертипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, к какому драйверу принтера следует выполнить откат.

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Нет резервного дирверс = 0** (0)


</dt> <dd>

Нет резервных драйверов.

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Наилучшее предположение = 1** (1)


</dt> <dd>

Лучшее предположение.

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Лучшее предположение, если в качестве отката для PCL = 2 (2) не найдено совпадений**


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, откат к Hewlett-Packard языку управления принтера (PCL).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Лучшее предположение, если для перехода на PS = 3 (3) не найдено совпадений**


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, возвращается резервный вариант в PostScript (PS).

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Наилучшее предположение. Если совпадение не найдено, не показывать драйверы PCL и PS = 4** (4)


</dt> <dd>

Лучшее предположение. Если совпадений не найдено, отобразите драйверы PS и PCL.

</dd> </dl>

</dd> <dt>

**жеткапабилитиесид**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификатор возможностей для поставщика.

</dd> <dt>

**HomeDirectory**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Корневой каталог для компьютера.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF
</dt> </dl>

Дата установки объекта. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**лиценсингдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание режима лицензирования.

</dd> <dt>

**лиценсингнаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя режима лицензирования.

</dd> <dt>

**лиценсингтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Тип лицензирования для указанного режима сервера.

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Личный сервер терминалов** (0)


</dt> <dd>

Сервер узла сеансов личных удаленных рабочих столов.

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Удаленный рабочий стол для администрирования** (1)


</dt> <dd>

Удаленный рабочий стол для администрирования.

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**На устройство** (2)


</dt> <dd>

На устройство. Допустимо для серверов приложений.

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (3)


</dt> <dd>

На пользователя. Допустимо для серверов приложений.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (4)


</dt> <dd>

Не настроено.

</dd> </dl>

</dd> <dt>

**лимитедусерсессионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешена ли функция ограничивать количество активных и неактивных сеансов, разрешенных на сервере узла сеансов удаленных рабочих столов. Например, может потребоваться настроить **лимитедусерсессионс** для обеспечения соответствия лицензий определенному приложению, установленному на сервере узла сеансов удаленных рабочих столов. Кроме того, может потребоваться ограничить максимальное количество сеансов на сервере узла сеансов удаленных рабочих столов в ферме с балансировкой нагрузки, чтобы сервер не перезагружался в случае сбоя другого сервера в ферме.

> [!Note]
>
> Сеанс, используемый для подключения к серверу в целях администрирования, не влияет на **лимитедусерсессионс**.
>
> В ферме серверов узла сеансов удаленных рабочих столов, если пользователь превышает ограничение на число сеансов, сеанс будет перенаправлен на другой сервер, RDCB балансировку нагрузки. Если сервер является изолированным, пользователь не сможет подключиться к серверу.
>
> Из-за сеанса, который используется для подключения к серверу для административных целей, и времени принудительного выполнения количества сеансов во время цикла входа в систему рекомендуется установить значение **лимитедусерсессионс** , которое немного меньше, чем физическое ограничение числа сеансов на сервере.
>
> Свойство **лимитедусерсессионс** допустимо только в том случае, если установлена служба роли узла сеансов удаленных рабочих столов.

 

<dt>

0
</dt> <dd>

Эта функция отключена.

</dd> <dt>

1 или более
</dt> <dd>

Значение 1 или больше представляет максимальное количество сеансов (активных и неактивных), разрешенных на сервере узла сеансов удаленных рабочих столов.

</dd> </dl>

</dd> <dt>

**Входов**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешены ли новые сеансы. Этот параметр не влияет на существующие параметры.

<dt>

0
</dt> <dd>

Новые сеансы разрешены.

</dd> <dt>

1
</dt> <dd>

Новые сеансы не разрешены.

</dd> </dl>

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**нетворкфсскатчаллвеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает весовой коэффициент распределения по сети по умолчанию для перехватывать весь сетевой трафик. Допустимые значения: от 1 до 9.

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**нетворкфсслокалсистемвеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает весовой коэффициент распределения по сети по умолчанию для процессов локальной системы. Допустимые значения: от 1 до 9.

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**нетворкфссусерсессионвеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает весовой коэффициент распределения по сети по умолчанию для сеанса пользователя. Допустимые значения: от 1 до 9.

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**полицисаурцеалловтсконнектионс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **алловтсконнектионс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеконфигуредлиценсесерверс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настраиваются ли серверы лицензий, возвращаемые методом [**жетспеЦифиедлиценсесерверлист**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) , сервером или групповой политикой.

**Windows Server 2008:** Это свойство недоступно.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеделететемпфолдерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **делететемпфолдерс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцедиректконнектлиценсесерверс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Это свойство недоступно.

**Windows Server 2008:** Указывает, настроено ли свойство **директконнектлиценсесерверс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцедисаблефорЦиблелогофф**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Данное свойство не поддерживается.

**Windows Server 2008:** Определяет, настроено ли свойство **дисаблефорЦиблелогофф** сервером или групповой политикой.

<dt>

0
</dt> <dd>

Сервер

</dd> <dt>

1
</dt> <dd>

Групповая политика.

</dd> </dl>

</dd> <dt>

**полицисаурцеенаблеаутоматикреконнектион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **енаблеаутоматикреконнектион** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**полицисаурцеенабледфсс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **енабледфсс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**полицисаурцеенаблеремотедесктопмси**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **енаблеремотедесктопмси** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.

</dd> <dt>

**полицисаурцефаллбаккпринтдривертипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **фаллбаккпринтдривертипе** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцехомедиректори**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **хомедиректори** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцелиценсингтипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **лиценсингтипе** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцепрофилепас**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство " **FilePath** " сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцередиректсмарткардс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **редиректсмарткардс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**полицисаурцесинглесессион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **синглесессион** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцетимезонередиректион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **тимезонередиректион** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцеусердеасипринтдривер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **усердеасипринтдривер** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**полицисаурцеусетемпфолдерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **усетемпфолдерс** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**поссиблелиценсингтипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**Битвалуес**](/windows/desktop/WmiSdk/standard-qualifiers) ("личный сервер терминалов", "удаленный рабочий стол для администрирования", "на устройство", "на пользователя", "не настроено")
</dt> </dl>

Битовая маска, указывающая доступные типы лицензирования. Это может быть сочетание одного или нескольких из следующих значений.

<dt>

1 (0x1)
</dt> <dd>

Поддерживаются лицензии на сервер узла личных сеансов удаленных рабочих столов.

</dd> <dt>

2 (0x2)
</dt> <dd>

Поддерживаются лицензии на удаленный рабочий стол.

</dd> <dt>

4 (0x4)
</dt> <dd>

Поддерживаются лицензии "на устройство".

</dd> <dt>

8 (0x8)
</dt> <dd>

Поддерживаются лицензии "на пользователя".

</dd> </dl>

</dd> <dt>

**Путь к пути**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к профилю для компьютера.

</dd> <dt>

**редиректсмарткардс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, разрешено ли перенаправление устройств смарт-карт в удаленном сеансе.

<dt>

0 (0x0)
</dt> <dd>

Перенаправление устройств смарт-карт не разрешено.

</dd> <dt>

1 (0x1)
</dt> <dd>

Перенаправление устройств смарт-карт разрешено.

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**ServerName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Имя сервера узла сеансов удаленных рабочих столов, свойства которого представляют интерес.

</dd> <dt>

**сессионброкердраинмоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

RDCB режим входа пользователя.

<dt>

0
</dt> <dd>

Разрешить все подключения.

</dd> <dt>

1
</dt> <dd>

Разрешить повторное подключение, но запретить новые входы до перезапуска сервера.

</dd> <dt>

2
</dt> <dd>

Разрешить повторное подключение, но запретить новые входы в систему.

</dd> </dl>

</dd> <dt>

**синглесессион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешен ли один или несколько сеансов службы удаленных рабочих столов для каждого пользователя.

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)


</dt> <dd>

Для каждого пользователя разрешено более одного сеанса.

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)


</dt> <dd>

Для каждого пользователя допускается только один сеанс.

</dd> </dl>

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

<dt>



 ("ОК")


</dt> <dd></dd> <dt>



 ("Ошибка")


</dt> <dd></dd> <dt>



 ("Пониженное состояние")


</dt> <dd></dd> <dt>



 ("Неизвестно")


</dt> <dd></dd> <dt>



 ("Пред Fail")


</dt> <dd></dd> <dt>



 ("Запуск")


</dt> <dd></dd> <dt>



 ("Остановка")


</dt> <dd></dd> <dt>



 ("Служба")


</dt> <dd></dd> </dl>

</dd> <dt>

**терминалсервермоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Режим работы сервера узла сеансов удаленных рабочих столов для службы службы удаленных рабочих столов. Этот режим управляет применяемыми политиками лицензирования, а также включением функций совместимости приложений.

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**Выборе** (1)


</dt> <dd>

Сервер работает как сервер приложений.

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**Ремотеадмин** (0)


</dt> <dd>

Сеанс администрируется удаленно.

</dd> </dl>

</dd> <dt>

**тимезонередиректион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, может ли клиентский компьютер перенаправлять параметры часового пояса в сеанс службы удаленных рабочих столов.

<dt>

0
</dt> <dd>

Перенаправление отключено.

</dd> <dt>

1
</dt> <dd>

Перенаправление включено.

</dd> </dl>

</dd> <dt>

**усердеасипринтдривер**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, используется ли первый драйвер принтера компонент Easy Print служб удаленных рабочих столов для установки всех клиентских принтеров.

<dt>

0
</dt> <dd>

Сервер узла сеансов удаленных рабочих столов пытается найти подходящий драйвер принтера для установки клиентского принтера. Если у сервера узла сеансов удаленных рабочих столов нет драйвера принтера, соответствующего принтеру клиента, сервер пытается использовать драйвер компонент Easy Print служб удаленных рабочих столов для установки клиентского принтера.

</dd> <dt>

1
</dt> <dd>

Сначала сервер узла сеансов удаленных рабочих столов пытается использовать драйвер принтера компонент Easy Print служб удаленных рабочих столов для установки всех клиентских принтеров. Если по какой-либо причине не удается использовать драйвер принтера компонент Easy Print служб удаленных рабочих столов, используется драйвер принтера на сервере узла сеансов удаленных рабочих столов, который соответствует принтеру клиента.

</dd> </dl>

**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.

</dd> <dt>

**усерпермиссион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Указывает, имеет ли каждый сеанс пользователя строгую или ослабленную безопасность.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Обеспечение безопасности является тесной.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Безопасность ослаблена.

</dd> </dl>

</dd> <dt>

**усетемпфолдерс**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, будут ли временные каталоги создаваться и удаляться отдельно для каждого сеанса.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Временные каталоги не создаются и не удаляются для каждого сеанса. Один из них создается для первого сеанса и никогда не удаляется.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Временные каталоги создаются и удаляются для каждого сеанса.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

**Win32 \_ Терминалсервицесеттинг** связан с [**Win32 \_ терминалсервице**](win32-terminalservice.md) в качестве свойства **Setting** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .

[**Win32 \_ Терминалсеттинг**](win32-terminalsetting.md) связывается с [**\_ терминалом Win32**](win32-terminal.md) как свойство **Setting** ассоциации [**Win32 \_ терминалтерминалсеттинг**](win32-terminalterminalsetting.md) .

Чтобы подключиться к корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.

В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[**\_Терминал Win32**](win32-terminal.md)
</dt> <dt>

[**\_Терминалсервице Win32**](win32-terminalservice.md)
</dt> <dt>

[**\_Терминалсервицетосеттинг Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_Терминалтерминалсеттинг Win32**](win32-terminalterminalsetting.md)
</dt> <dt>

[**\_Параметр CIM**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

