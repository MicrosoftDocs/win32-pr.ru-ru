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
# <a name="win32_terminalservicesetting-class"></a><span data-ttu-id="6d432-105">\_Класс Win32 терминалсервицесеттинг</span><span class="sxs-lookup"><span data-stu-id="6d432-105">Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="6d432-106">Класс **WMI \_ Терминалсервицесеттинг для Win32** представляет конфигурацию для сервера узла сеансов сеансов (RD) удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6d432-106">The **Win32\_TerminalServiceSetting** WMI class represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="6d432-107">Параметры включают такие возможности, как режим сервера узла сеансов удаленных рабочих столов, лицензирование, активный рабочий стол, разрешения, удаление временных папок и временные каталоги для сеансов.</span><span class="sxs-lookup"><span data-stu-id="6d432-107">Settings include capabilities such as RD Session Host server mode, licensing, Active Desktop, permissions, deletion of temporary folders, and temporary directories for sessions.</span></span>

<span data-ttu-id="6d432-108">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="6d432-108">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="6d432-109">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="6d432-109">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d432-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d432-110">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="6d432-111">Члены</span><span class="sxs-lookup"><span data-stu-id="6d432-111">Members</span></span>

<span data-ttu-id="6d432-112">Класс **Win32 \_ терминалсервицесеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6d432-112">The **Win32\_TerminalServiceSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="6d432-113">Методы</span><span class="sxs-lookup"><span data-stu-id="6d432-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="6d432-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d432-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6d432-115">Методы</span><span class="sxs-lookup"><span data-stu-id="6d432-115">Methods</span></span>

<span data-ttu-id="6d432-116">Класс **Win32 \_ терминалсервицесеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="6d432-116">The **Win32\_TerminalServiceSetting** class has these methods.</span></span>



| <span data-ttu-id="6d432-117">Метод</span><span class="sxs-lookup"><span data-stu-id="6d432-117">Method</span></span>                                                                                                                | <span data-ttu-id="6d432-118">Описание</span><span class="sxs-lookup"><span data-stu-id="6d432-118">Description</span></span>                                                                                                                                                                    |
|:----------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d432-119">**адддиректконнектлиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-119">**AddDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-adddirectconnectlicenseserver.md)                   | <span data-ttu-id="6d432-120">Настраивает новый сервер лицензирования в Организации.</span><span class="sxs-lookup"><span data-stu-id="6d432-120">Configures a new license server in the enterprise.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="6d432-121">**аддлстоспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-121">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)           | <span data-ttu-id="6d432-122">Добавляет указанный сервер лицензирования в конец списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-122">Adds the given license server to the end of the list of specified license servers.</span></span><br/>                                                                                  |
| [<span data-ttu-id="6d432-123">**канакцесслиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-123">**CanAccessLicenseServer**</span></span>](canaccesslicenseserver-win32-terminalservicesetting.md)                                 | <span data-ttu-id="6d432-124">Определяет, разрешено ли серверу узла сеансов удаленных рабочих столов запрашивать службы удаленных рабочих столов клиентских лицензий (RDS CAL) с сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6d432-124">Determines whether the RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from a Remote Desktop license server.</span></span><br/> |
| [<span data-ttu-id="6d432-125">**ChangeMode**</span><span class="sxs-lookup"><span data-stu-id="6d432-125">**ChangeMode**</span></span>](win32-terminalservicesetting-changemode.md)                                                         | <span data-ttu-id="6d432-126">Задает тип лицензирования сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6d432-126">Sets the licensing type of the Remote Desktop license server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="6d432-127">**креатевинстатион**</span><span class="sxs-lookup"><span data-stu-id="6d432-127">**CreateWinstation**</span></span>](createwinstation-win32-terminalservicesetting.md)                                             | <span data-ttu-id="6d432-128">Создает новый стек прослушивателя на основе уникального сочетания имени прослушивателя и сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="6d432-128">Creates a new listener stack based on the unique combination of listener name and NIC.</span></span><br/>                                                                              |
| [<span data-ttu-id="6d432-129">**делетедиректконнектлиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-129">**DeleteDirectConnectLicenseServer**</span></span>](win32-terminalservicesetting-deletedirectconnectlicenseserver.md)             | <span data-ttu-id="6d432-130">Удаляет указанный сервер лицензирования из Организации.</span><span class="sxs-lookup"><span data-stu-id="6d432-130">Deletes the specified license server from the enterprise.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="6d432-131">**емптиспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)               | <span data-ttu-id="6d432-132">Удаляет все серверы лицензий из списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-132">Removes all license servers from the list of specified license servers.</span></span><br/>                                                                                             |
| [<span data-ttu-id="6d432-133">**финдлиценсесерверс**</span><span class="sxs-lookup"><span data-stu-id="6d432-133">**FindLicenseServers**</span></span>](findlicenseservers-win32-terminalservicesetting.md)                                         | <span data-ttu-id="6d432-134">Перечисляет все серверы лицензий удаленный рабочий стол и метод обнаружения.</span><span class="sxs-lookup"><span data-stu-id="6d432-134">Enumerates all of the Remote Desktop license servers and the method of discovery.</span></span><br/>                                                                                   |
| [<span data-ttu-id="6d432-135">**Поддомен**</span><span class="sxs-lookup"><span data-stu-id="6d432-135">**GetDomain**</span></span>](getdomain-win32-terminalservicesetting.md)                                                           | <span data-ttu-id="6d432-136">Возвращает имя домена, в который входит сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-136">Retrieves the name of the domain that the RD Session Host server is a member of.</span></span><br/>                                                                                    |
| [<span data-ttu-id="6d432-137">**жетграцепериоддайс**</span><span class="sxs-lookup"><span data-stu-id="6d432-137">**GetGracePeriodDays**</span></span>](getgraceperioddays-win32-terminalservicesetting.md)                                         | <span data-ttu-id="6d432-138">Извлекает количество дней, оставшихся в льготном периоде лицензирования удаленных рабочих столов для сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-138">Retrieves the number of days that are remaining in the RD Licensing grace period for an RD Session Host server.</span></span><br/>                                                     |
| [<span data-ttu-id="6d432-139">**жетрегистередлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-139">**GetRegisteredLicenseServerList**</span></span>](getregisteredlicenseserverlist-win32-terminalservicesetting.md)                 | <span data-ttu-id="6d432-140">Возвращает список зарегистрированных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-140">Gets the list of registered license servers.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6d432-141">**жетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-141">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="6d432-142">Извлекает список указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-142">Retrieves the list of specified license servers.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="6d432-143">**жеттсланаидс**</span><span class="sxs-lookup"><span data-stu-id="6d432-143">**GetTSLanaIds**</span></span>](gettslanaids-win32-terminalservicesetting.md)                                                     | <span data-ttu-id="6d432-144">Возвращает идентификаторы и описания сетевых адаптеров службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-144">Gets the IDs and descriptions of Remote Desktop Services network adapters.</span></span><br/>                                                                                          |
| [<span data-ttu-id="6d432-145">**жеттстолсконнективитистатус**</span><span class="sxs-lookup"><span data-stu-id="6d432-145">**GetTStoLSConnectivityStatus**</span></span>](gettstolsconnectivitystatus-win32-terminalservicesetting.md)                       | <span data-ttu-id="6d432-146">Определяет состояние подключения между службы удаленных рабочих столов и сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-146">Determines the connectivity status between Remote Desktop Services and a license server.</span></span><br/>                                                                            |
| [<span data-ttu-id="6d432-147">**жетвинстатиондривернамес**</span><span class="sxs-lookup"><span data-stu-id="6d432-147">**GetWinstationDriverNames**</span></span>](getwinstationdrivernames-win32-terminalservicesetting.md)                             | <span data-ttu-id="6d432-148">Возвращает список имен драйверов Винстатион.</span><span class="sxs-lookup"><span data-stu-id="6d432-148">Retrieves a list of Winstation driver names.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6d432-149">**пинглиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-149">**PingLicenseServer**</span></span>](pinglicenseserver-win32-terminalservicesetting.md)                                           | <span data-ttu-id="6d432-150">Проверяет связь с сервером лицензирования, чтобы определить, является ли он действительным сервером лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-150">Pings the license server to determine whether it is a valid license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="6d432-151">**ремовелсфромспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-151">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md) | <span data-ttu-id="6d432-152">Удаляет указанный сервер лицензирования из списка указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-152">Removes the given license server from the list of specified license servers.</span></span><br/>                                                                                        |
| [<span data-ttu-id="6d432-153">**сеталловтсконнектионс**</span><span class="sxs-lookup"><span data-stu-id="6d432-153">**SetAllowTSConnections**</span></span>](win32-terminalservicesetting-setallowtsconnections.md)                                   | <span data-ttu-id="6d432-154">Задает свойство **алловтсконнектионс** .</span><span class="sxs-lookup"><span data-stu-id="6d432-154">Sets the **AllowTSConnections** property.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="6d432-155">**сетдисаблефорЦиблелогофф**</span><span class="sxs-lookup"><span data-stu-id="6d432-155">**SetDisableForcibleLogoff**</span></span>](win32-terminalservicesetting-setdisableforciblelogoff.md)                             | <span data-ttu-id="6d432-156">Задает свойство **дисаблефорЦиблелогофф** .</span><span class="sxs-lookup"><span data-stu-id="6d432-156">Sets the **DisableForcibleLogoff** property.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="6d432-157">**сетфаллбаккпринтдривертипе**</span><span class="sxs-lookup"><span data-stu-id="6d432-157">**SetFallbackPrintDriverType**</span></span>](win32-terminalservicesetting-setfallbackprintdrivertype.md)                         | <span data-ttu-id="6d432-158">Задает свойство **фаллбаккпринтдривертипе** .</span><span class="sxs-lookup"><span data-stu-id="6d432-158">Sets the **FallbackPrintDriverType** property.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="6d432-159">**сесомедиректори**</span><span class="sxs-lookup"><span data-stu-id="6d432-159">**SetHomeDirectory**</span></span>](win32-terminalservicesetting-sethomedirectory.md)                                             | <span data-ttu-id="6d432-160">Задает свойство **хомедиректори** .</span><span class="sxs-lookup"><span data-stu-id="6d432-160">Sets the **HomeDirectory** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6d432-161">**сетполиципропертинаме**</span><span class="sxs-lookup"><span data-stu-id="6d432-161">**SetPolicyPropertyName**</span></span>](win32-terminalservicesetting-setpolicypropertyname.md)                                   | <span data-ttu-id="6d432-162">Задает одно из следующих свойств: **делететемпфолдерс** или **усетемпфолдерс**.</span><span class="sxs-lookup"><span data-stu-id="6d432-162">Sets one of the following properties: **DeleteTempFolders** or **UseTempFolders**.</span></span><br/>                                                                                  |
| [<span data-ttu-id="6d432-163">**сетпримарилиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-163">**SetPrimaryLicenseServer**</span></span>](setprimarylicenseserver-win32-terminalservicesetting.md)                               | <span data-ttu-id="6d432-164">Задает указанный сервер лицензирования в качестве первой записи в списке указанных серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-164">Sets the given license server as the first entry in the list of specified license servers.</span></span><br/>                                                                          |
| [<span data-ttu-id="6d432-165">**сетпрофилепас**</span><span class="sxs-lookup"><span data-stu-id="6d432-165">**SetProfilePath**</span></span>](win32-terminalservicesetting-setprofilepath.md)                                                 | <span data-ttu-id="6d432-166">Задает свойство **FilePath** .</span><span class="sxs-lookup"><span data-stu-id="6d432-166">Sets the **ProfilePath** property.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="6d432-167">**сетсинглесессион**</span><span class="sxs-lookup"><span data-stu-id="6d432-167">**SetSingleSession**</span></span>](win32-terminalservicesetting-setsinglesession.md)                                             | <span data-ttu-id="6d432-168">Задает свойство **синглесессион** .</span><span class="sxs-lookup"><span data-stu-id="6d432-168">Sets the **SingleSession** property.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="6d432-169">**сетспеЦифиедлиценсесерверлист**</span><span class="sxs-lookup"><span data-stu-id="6d432-169">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)                   | <span data-ttu-id="6d432-170">Обновляет список указанных серверов лицензирования, заменяя все существующие указанные серверы лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-170">Updates the list of specified license servers, replacing any existing specified license servers.</span></span><br/>                                                                    |
| [<span data-ttu-id="6d432-171">**сеттимезонередиректион**</span><span class="sxs-lookup"><span data-stu-id="6d432-171">**SetTimeZoneRedirection**</span></span>](win32-terminalservicesetting-settimezoneredirection.md)                                 | <span data-ttu-id="6d432-172">Задает свойство **тимезонередиректион** .</span><span class="sxs-lookup"><span data-stu-id="6d432-172">Sets the **TimeZoneRedirection** property.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="6d432-173">**упдатедиректконнектлиценсесервер**</span><span class="sxs-lookup"><span data-stu-id="6d432-173">**UpdateDirectConnectLicenseServer**</span></span>](updatedirectconnectlicenseserver-win32-terminalservicesetting.md)             | <span data-ttu-id="6d432-174">Обновляет список серверов лицензирования обнаружения.</span><span class="sxs-lookup"><span data-stu-id="6d432-174">Updates the list of discovery license servers.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="6d432-175">Свойства</span><span class="sxs-lookup"><span data-stu-id="6d432-175">Properties</span></span>

<span data-ttu-id="6d432-176">Класс **Win32 \_ терминалсервицесеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6d432-176">The **Win32\_TerminalServiceSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6d432-177">**активедесктоп**</span><span class="sxs-lookup"><span data-stu-id="6d432-177">**ActiveDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-178">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-178">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-179">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-179">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-180">Указывает, разрешен ли активный рабочий стол в каждом сеансе пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-180">Specifies whether Active Desktop is allowed in each user session.</span></span>

<dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="6d432-181"><span id="TRUE"></span><span id="true"></span>**True** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-181"><span id="TRUE"></span><span id="true"></span>**TRUE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-182">Active Desktop не разрешается в каждом сеансе пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-182">Active Desktop is not allowed in each user session.</span></span>

</dd> <dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="6d432-183"><span id="FALSE"></span><span id="false"></span>**False** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-183"><span id="FALSE"></span><span id="false"></span>**FALSE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-184">Разрешено использовать Active Desktop в каждом пользовательском сеансе.</span><span class="sxs-lookup"><span data-stu-id="6d432-184">Active Desktop is allowed in each user session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-185">**алловтсконнектионс**</span><span class="sxs-lookup"><span data-stu-id="6d432-185">**AllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-186">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-188">Указывает, разрешены ли новые службы удаленных рабочих столов подключения.</span><span class="sxs-lookup"><span data-stu-id="6d432-188">Specifies whether new Remote Desktop Services connections are allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="6d432-189"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-189"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-190">Новые подключения не допускаются.</span><span class="sxs-lookup"><span data-stu-id="6d432-190">New connections are not allowed.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="6d432-191"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-191"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-192">Новые подключения разрешены.</span><span class="sxs-lookup"><span data-stu-id="6d432-192">New connections are allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-193">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="6d432-193">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-195">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-195">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-196">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="6d432-196">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="6d432-197">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="6d432-197">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="6d432-198">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d432-198">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d432-199">**делететемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="6d432-199">**DeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-200">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-202">Указывает, удаляются ли временные каталоги при выходе из программы.</span><span class="sxs-lookup"><span data-stu-id="6d432-202">Specifies whether temporary directories are deleted on exit.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="6d432-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-204">Удаление временных каталогов отключено.</span><span class="sxs-lookup"><span data-stu-id="6d432-204">Deletion of temporary directories is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="6d432-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-206">Удаление временных каталогов включено.</span><span class="sxs-lookup"><span data-stu-id="6d432-206">Deletion of temporary directories is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-207">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6d432-207">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-210">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="6d432-210">Description of the object.</span></span>

<span data-ttu-id="6d432-211">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d432-211">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d432-212">**директконнектлиценсесерверс**</span><span class="sxs-lookup"><span data-stu-id="6d432-212">**DirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-213">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-213">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-215">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6d432-215">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6d432-216">Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-216">This property is not available.</span></span>

<span data-ttu-id="6d432-217">**Windows Server 2008:** Перечисляет список серверов лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-217">**Windows Server 2008:** Enumerates the list of license servers.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-218">**дисаблефорЦиблелогофф**</span><span class="sxs-lookup"><span data-stu-id="6d432-218">**DisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-219">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-219">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-220">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-221">Определяет, можно ли принудительно завершить работу администратора, выполнившего вход в консоль.</span><span class="sxs-lookup"><span data-stu-id="6d432-221">Determines whether an administrator that is logged on to the console can be forcibly logged off.</span></span>

<dt>

<span data-ttu-id="6d432-222">0</span><span class="sxs-lookup"><span data-stu-id="6d432-222">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-223">Администратор может принудительно завершить работу.</span><span class="sxs-lookup"><span data-stu-id="6d432-223">Administrator can be forcibly logged off.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-224">1</span><span class="sxs-lookup"><span data-stu-id="6d432-224">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-225">Невозможно принудительно завершить работу администратора.</span><span class="sxs-lookup"><span data-stu-id="6d432-225">Administrator cannot be forcibly logged off.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-226">**енаблеаутоматикреконнектион**</span><span class="sxs-lookup"><span data-stu-id="6d432-226">**EnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-227">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-227">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-228">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-228">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-229">Указывает, разрешено ли клиентам подключения удаленный рабочий стол автоматическое повторное подключение к сеансам на сервере узла сеансов удаленных рабочих столов, если сетевое подключение временно потеряно.</span><span class="sxs-lookup"><span data-stu-id="6d432-229">Specifies whether to allow Remote Desktop connection clients to automatically reconnect to sessions on an RD Session Host server if the network link is temporarily lost.</span></span>

<dt>

<span data-ttu-id="6d432-230">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-230">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-231">Автоматическое повторное подключение отключено.</span><span class="sxs-lookup"><span data-stu-id="6d432-231">Automatic reconnection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-232">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-232">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-233">Автоматическое повторное подключение включено.</span><span class="sxs-lookup"><span data-stu-id="6d432-233">Automatic reconnection is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="6d432-234">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-234">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-235">**енабледфсс**</span><span class="sxs-lookup"><span data-stu-id="6d432-235">**EnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-236">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-237">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-238">Указывает, включено ли динамическое планирование равномерного предоставления общего доступа (ДФСС).</span><span class="sxs-lookup"><span data-stu-id="6d432-238">Indicates whether dynamic fair-share scheduling (DFSS) is enabled or disabled.</span></span> <span data-ttu-id="6d432-239">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6d432-239">This can be one of the following values.</span></span>

<span data-ttu-id="6d432-240">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6d432-240">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="6d432-241">0</span><span class="sxs-lookup"><span data-stu-id="6d432-241">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-242">ДФСС отключен.</span><span class="sxs-lookup"><span data-stu-id="6d432-242">DFSS is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-243">1</span><span class="sxs-lookup"><span data-stu-id="6d432-243">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-244">ДФСС включен.</span><span class="sxs-lookup"><span data-stu-id="6d432-244">DFSS is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-245">**енабледискфсс**</span><span class="sxs-lookup"><span data-stu-id="6d432-245">**EnableDiskFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-246">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-246">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-247">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-247">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-248">Указывает, включено ли планирование распределения дискового ресурса.</span><span class="sxs-lookup"><span data-stu-id="6d432-248">Specifies if disk fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="6d432-249">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-249">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-250">Планирование распределения дискового ресурса отключено.</span><span class="sxs-lookup"><span data-stu-id="6d432-250">Disk fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-251">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-251">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-252">Планирование распределения дискового ресурса включено.</span><span class="sxs-lookup"><span data-stu-id="6d432-252">Disk fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="6d432-253">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-253">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-254">**енабленетворкфсс**</span><span class="sxs-lookup"><span data-stu-id="6d432-254">**EnableNetworkFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-255">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-256">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-256">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-257">Указывает, включено ли планирование распределения ресурсов по сети.</span><span class="sxs-lookup"><span data-stu-id="6d432-257">Specifies if network fair share scheduling is enabled.</span></span>

<dt>

<span data-ttu-id="6d432-258">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-258">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-259">Планирование распределения сетевых ресурсов отключено.</span><span class="sxs-lookup"><span data-stu-id="6d432-259">Network fair share scheduling is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-260">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-260">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-261">Планирование распределения сетевых ресурсов включено.</span><span class="sxs-lookup"><span data-stu-id="6d432-261">Network fair share scheduling is enabled.</span></span>

</dd> </dl>

<span data-ttu-id="6d432-262">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-262">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-263">**енаблеремотедесктопмси**</span><span class="sxs-lookup"><span data-stu-id="6d432-263">**EnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-264">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-264">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-265">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-265">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-266">Указывает, включен или отключен удаленный рабочий стол MSI.</span><span class="sxs-lookup"><span data-stu-id="6d432-266">Indicates whether the Remote Desktop MSI is enabled or disabled.</span></span>

<dt>

<span data-ttu-id="6d432-267">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-267">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-268">Выключено</span><span class="sxs-lookup"><span data-stu-id="6d432-268">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="6d432-269">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-269">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-270">Активировано</span><span class="sxs-lookup"><span data-stu-id="6d432-270">Enabled</span></span>

</dd> </dl>

<span data-ttu-id="6d432-271">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6d432-271">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-272">**фаллбаккпринтдривертипе**</span><span class="sxs-lookup"><span data-stu-id="6d432-272">**FallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-273">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-274">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-274">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-275">Указывает, к какому драйверу принтера следует выполнить откат.</span><span class="sxs-lookup"><span data-stu-id="6d432-275">Specifies which printer driver to fallback to.</span></span>

<dt>

<span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>

<span data-ttu-id="6d432-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**Нет резервного дирверс = 0** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-276"><span id="No_fallback_dirvers_0"></span><span id="no_fallback_dirvers_0"></span><span id="NO_FALLBACK_DIRVERS_0"></span>**No fallback dirvers=0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-277">Нет резервных драйверов.</span><span class="sxs-lookup"><span data-stu-id="6d432-277">No fallback drivers.</span></span>

</dd> <dt>

<span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>

<span data-ttu-id="6d432-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Наилучшее предположение = 1** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-278"><span id="Best_guess_1"></span><span id="best_guess_1"></span><span id="BEST_GUESS_1"></span>**Best guess=1** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-279">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="6d432-279">Best guess.</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>

<span data-ttu-id="6d432-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Лучшее предположение, если в качестве отката для PCL = 2 (2) не найдено совпадений**</span><span class="sxs-lookup"><span data-stu-id="6d432-280"><span id="Best_guess__if_no_match_is_found_fallback_to_PCL_2"></span><span id="best_guess__if_no_match_is_found_fallback_to_pcl_2"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PCL_2"></span>**Best guess, if no match is found fallback to PCL=2** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-281">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="6d432-281">Best guess.</span></span> <span data-ttu-id="6d432-282">Если совпадений не найдено, откат к Hewlett-Packard языку управления принтера (PCL).</span><span class="sxs-lookup"><span data-stu-id="6d432-282">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>

<span data-ttu-id="6d432-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Лучшее предположение, если для перехода на PS = 3 (3) не найдено совпадений**</span><span class="sxs-lookup"><span data-stu-id="6d432-283"><span id="Best_guess__if_no_match_is_found_fallback_to_PS_3"></span><span id="best_guess__if_no_match_is_found_fallback_to_ps_3"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_FALLBACK_TO_PS_3"></span>**Best guess, if no match is found fallback to PS=3** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-284">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="6d432-284">Best guess.</span></span> <span data-ttu-id="6d432-285">Если совпадений не найдено, возвращается резервный вариант в PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="6d432-285">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>

<span data-ttu-id="6d432-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Наилучшее предположение. Если совпадение не найдено, не показывать драйверы PCL и PS = 4** (4)</span><span class="sxs-lookup"><span data-stu-id="6d432-286"><span id="Best_guess__if_no_match_is_found_show_both_PCL_and_PS_drivers_4"></span><span id="best_guess__if_no_match_is_found_show_both_pcl_and_ps_drivers_4"></span><span id="BEST_GUESS__IF_NO_MATCH_IS_FOUND_SHOW_BOTH_PCL_AND_PS_DRIVERS_4"></span>**Best guess, if no match is found show both PCL and PS drivers=4** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-287">Лучшее предположение.</span><span class="sxs-lookup"><span data-stu-id="6d432-287">Best guess.</span></span> <span data-ttu-id="6d432-288">Если совпадений не найдено, отобразите драйверы PS и PCL.</span><span class="sxs-lookup"><span data-stu-id="6d432-288">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-289">**жеткапабилитиесид**</span><span class="sxs-lookup"><span data-stu-id="6d432-289">**GetCapabilitiesID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-290">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-291">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-292">Идентификатор возможностей для поставщика.</span><span class="sxs-lookup"><span data-stu-id="6d432-292">Capabilities ID for the provider.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-293">**HomeDirectory**</span><span class="sxs-lookup"><span data-stu-id="6d432-293">**HomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-294">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-294">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-296">Корневой каталог для компьютера.</span><span class="sxs-lookup"><span data-stu-id="6d432-296">The root directory for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-297">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6d432-297">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-298">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6d432-298">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-299">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-299">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-300">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="6d432-300">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="6d432-301">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="6d432-301">The date the object was installed.</span></span> <span data-ttu-id="6d432-302">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="6d432-302">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6d432-303">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d432-303">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d432-304">**лиценсингдескриптион**</span><span class="sxs-lookup"><span data-stu-id="6d432-304">**LicensingDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-306">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-307">Краткое описание режима лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-307">A brief description of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-308">**лиценсингнаме**</span><span class="sxs-lookup"><span data-stu-id="6d432-308">**LicensingName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-309">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-309">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-310">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-310">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-311">Имя режима лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-311">The name of the licensing mode.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-312">**лиценсингтипе**</span><span class="sxs-lookup"><span data-stu-id="6d432-312">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-313">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-313">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-314">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-315">Тип лицензирования для указанного режима сервера.</span><span class="sxs-lookup"><span data-stu-id="6d432-315">The licensing type for the specified server mode.</span></span>

<dt>

<span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>

<span data-ttu-id="6d432-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Личный сервер терминалов** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-316"><span id="Personal_Terminal_Server"></span><span id="personal_terminal_server"></span><span id="PERSONAL_TERMINAL_SERVER"></span>**Personal Terminal Server** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-317">Сервер узла сеансов личных удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-317">Personal RD Session Host server.</span></span>

</dd> <dt>

<span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>

<span data-ttu-id="6d432-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Удаленный рабочий стол для администрирования** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-318"><span id="Remote_Desktop_for_Administration"></span><span id="remote_desktop_for_administration"></span><span id="REMOTE_DESKTOP_FOR_ADMINISTRATION"></span>**Remote Desktop for Administration** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-319">Удаленный рабочий стол для администрирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-319">Remote Desktop for Administration.</span></span>

</dd> <dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="6d432-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**На устройство** (2)</span><span class="sxs-lookup"><span data-stu-id="6d432-320"><span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>**Per Device** (2)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-321">На устройство.</span><span class="sxs-lookup"><span data-stu-id="6d432-321">Per Device.</span></span> <span data-ttu-id="6d432-322">Допустимо для серверов приложений.</span><span class="sxs-lookup"><span data-stu-id="6d432-322">Valid for application servers.</span></span>

</dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="6d432-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (3)</span><span class="sxs-lookup"><span data-stu-id="6d432-323"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (3)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-324">На пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-324">Per User.</span></span> <span data-ttu-id="6d432-325">Допустимо для серверов приложений.</span><span class="sxs-lookup"><span data-stu-id="6d432-325">Valid for application servers.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="6d432-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Не настроено** (4)</span><span class="sxs-lookup"><span data-stu-id="6d432-326"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (4)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-327">Не настроено.</span><span class="sxs-lookup"><span data-stu-id="6d432-327">Not Configured.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-328">**лимитедусерсессионс**</span><span class="sxs-lookup"><span data-stu-id="6d432-328">**LimitedUserSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-329">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-329">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-330">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-330">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-331">Указывает, разрешена ли функция ограничивать количество активных и неактивных сеансов, разрешенных на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-331">Indicates whether the feature to limit the number of both active and inactive sessions that are allowed on an RD Session Host server is enabled.</span></span> <span data-ttu-id="6d432-332">Например, может потребоваться настроить **лимитедусерсессионс** для обеспечения соответствия лицензий определенному приложению, установленному на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-332">For example, you may want to set **LimitedUserSessions** to guarantee license compliance for a particular application that is installed on the RD Session Host server.</span></span> <span data-ttu-id="6d432-333">Кроме того, может потребоваться ограничить максимальное количество сеансов на сервере узла сеансов удаленных рабочих столов в ферме с балансировкой нагрузки, чтобы сервер не перезагружался в случае сбоя другого сервера в ферме.</span><span class="sxs-lookup"><span data-stu-id="6d432-333">Or, you may want to limit the maximum number of sessions on an RD Session Host server in a load-balanced farm so that the server will not be overloaded if another server in the farm fails.</span></span>

> [!Note]
>
> <span data-ttu-id="6d432-334">Сеанс, используемый для подключения к серверу в целях администрирования, не влияет на **лимитедусерсессионс**.</span><span class="sxs-lookup"><span data-stu-id="6d432-334">The session that is used to connect to the server for administrative purposes is not affected by **LimitedUserSessions**.</span></span>
>
> <span data-ttu-id="6d432-335">В ферме серверов узла сеансов удаленных рабочих столов, если пользователь превышает ограничение на число сеансов, сеанс будет перенаправлен на другой сервер, RDCB балансировку нагрузки.</span><span class="sxs-lookup"><span data-stu-id="6d432-335">In an RD Session Host server farm, if a user exceeds the session limit, the session will be directed to another server by RD Connection Broker load balancing.</span></span> <span data-ttu-id="6d432-336">Если сервер является изолированным, пользователь не сможет подключиться к серверу.</span><span class="sxs-lookup"><span data-stu-id="6d432-336">If the server is a stand-alone server, the user will not be able to connect.</span></span>
>
> <span data-ttu-id="6d432-337">Из-за сеанса, который используется для подключения к серверу для административных целей, и времени принудительного выполнения количества сеансов во время цикла входа в систему рекомендуется установить значение **лимитедусерсессионс** , которое немного меньше, чем физическое ограничение числа сеансов на сервере.</span><span class="sxs-lookup"><span data-stu-id="6d432-337">Because of the session that is used to connect to the server for administrative purposes, and the timing of the enforcement of the number of sessions during the logon cycle, it is recommended that you set **LimitedUserSessions** to a value that is slightly lower that the physical limit for the number of sessions on a server.</span></span>
>
> <span data-ttu-id="6d432-338">Свойство **лимитедусерсессионс** допустимо только в том случае, если установлена служба роли узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-338">The **LimitedUserSessions** property is only valid if the RD Session Host role service is installed.</span></span>

 

<dt>

<span data-ttu-id="6d432-339">0</span><span class="sxs-lookup"><span data-stu-id="6d432-339">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-340">Эта функция отключена.</span><span class="sxs-lookup"><span data-stu-id="6d432-340">The feature is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-341">1 или более</span><span class="sxs-lookup"><span data-stu-id="6d432-341">1 or greater</span></span>
</dt> <dd>

<span data-ttu-id="6d432-342">Значение 1 или больше представляет максимальное количество сеансов (активных и неактивных), разрешенных на сервере узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-342">A value of one or greater represents the maximum number of sessions (both active and inactive) that are allowed on the RD Session Host server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-343">**Входов**</span><span class="sxs-lookup"><span data-stu-id="6d432-343">**Logons**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-344">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-344">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-345">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-345">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-346">Указывает, разрешены ли новые сеансы.</span><span class="sxs-lookup"><span data-stu-id="6d432-346">Specifies whether new sessions are allowed.</span></span> <span data-ttu-id="6d432-347">Этот параметр не влияет на существующие параметры.</span><span class="sxs-lookup"><span data-stu-id="6d432-347">This setting does not affect existing settings.</span></span>

<dt>

<span data-ttu-id="6d432-348">0</span><span class="sxs-lookup"><span data-stu-id="6d432-348">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-349">Новые сеансы разрешены.</span><span class="sxs-lookup"><span data-stu-id="6d432-349">New sessions are allowed.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-350">1</span><span class="sxs-lookup"><span data-stu-id="6d432-350">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-351">Новые сеансы не разрешены.</span><span class="sxs-lookup"><span data-stu-id="6d432-351">New sessions are not allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-352">**Name**</span><span class="sxs-lookup"><span data-stu-id="6d432-352">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-353">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-354">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-354">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-355">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="6d432-355">The name of the object.</span></span>

<span data-ttu-id="6d432-356">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d432-356">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6d432-357">**нетворкфсскатчаллвеигхт**</span><span class="sxs-lookup"><span data-stu-id="6d432-357">**NetworkFSSCatchAllWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-358">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-358">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-359">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-359">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-360">Указывает весовой коэффициент распределения по сети по умолчанию для перехватывать весь сетевой трафик.</span><span class="sxs-lookup"><span data-stu-id="6d432-360">Specifies the default network fair share weight for catch-all network traffic.</span></span> <span data-ttu-id="6d432-361">Допустимые значения: от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="6d432-361">Valid values are 1 to 9.</span></span>

<span data-ttu-id="6d432-362">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-362">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-363">**нетворкфсслокалсистемвеигхт**</span><span class="sxs-lookup"><span data-stu-id="6d432-363">**NetworkFSSLocalSystemWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-364">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-364">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-365">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-365">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-366">Указывает весовой коэффициент распределения по сети по умолчанию для процессов локальной системы.</span><span class="sxs-lookup"><span data-stu-id="6d432-366">Specifies the default network fair share weight for a local system processes.</span></span> <span data-ttu-id="6d432-367">Допустимые значения: от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="6d432-367">Valid values are 1 to 9.</span></span>

<span data-ttu-id="6d432-368">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-368">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-369">**нетворкфссусерсессионвеигхт**</span><span class="sxs-lookup"><span data-stu-id="6d432-369">**NetworkFSSUserSessionWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-370">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-370">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-371">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-371">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-372">Указывает весовой коэффициент распределения по сети по умолчанию для сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-372">Specifies the default network fair share weight for a user session.</span></span> <span data-ttu-id="6d432-373">Допустимые значения: от 1 до 9.</span><span class="sxs-lookup"><span data-stu-id="6d432-373">Valid values are 1 to 9.</span></span>

<span data-ttu-id="6d432-374">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-374">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-375">**полицисаурцеалловтсконнектионс**</span><span class="sxs-lookup"><span data-stu-id="6d432-375">**PolicySourceAllowTSConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-376">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-376">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-377">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-377">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-378">Указывает, настроено ли свойство **алловтсконнектионс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-378">Indicates whether the **AllowTSConnections** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-379">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-379">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-380">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-380">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-381">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-381">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-382">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-382">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-383">**полицисаурцеконфигуредлиценсесерверс**</span><span class="sxs-lookup"><span data-stu-id="6d432-383">**PolicySourceConfiguredLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-384">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-384">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-385">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-385">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-386">Указывает, настраиваются ли серверы лицензий, возвращаемые методом [**жетспеЦифиедлиценсесерверлист**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) , сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-386">Indicates whether the license servers returned by the [**GetSpecifiedLicenseServerList**](getspecifiedlicenseserverlist-win32-terminalservicesetting.md) method are configured by the server or by group policy.</span></span>

<span data-ttu-id="6d432-387">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-387">**Windows Server 2008:** This property is not available.</span></span>

<dt>

<span data-ttu-id="6d432-388">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-388">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-389">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-389">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-390">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-390">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-391">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-391">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-392">**полицисаурцеделететемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="6d432-392">**PolicySourceDeleteTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-393">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-393">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-395">Указывает, настроено ли свойство **делететемпфолдерс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-395">Indicates whether the **DeleteTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-396">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-396">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-397">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-397">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-398">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-398">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-399">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-399">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-400">**полицисаурцедиректконнектлиценсесерверс**</span><span class="sxs-lookup"><span data-stu-id="6d432-400">**PolicySourceDirectConnectLicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-401">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-401">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-402">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-402">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-403">Квалификаторы: не [ **рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6d432-403">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6d432-404">Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-404">This property is not available.</span></span>

<span data-ttu-id="6d432-405">**Windows Server 2008:** Указывает, настроено ли свойство **директконнектлиценсесерверс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-405">**Windows Server 2008:** Indicates whether the **DirectConnectLicenseServers** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-406">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-406">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-407">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-407">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-408">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-408">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-409">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-409">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-410">**полицисаурцедисаблефорЦиблелогофф**</span><span class="sxs-lookup"><span data-stu-id="6d432-410">**PolicySourceDisableForcibleLogoff**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-411">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-411">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-412">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-413">Данное свойство не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="6d432-413">This property is not supported.</span></span>

<span data-ttu-id="6d432-414">**Windows Server 2008:** Определяет, настроено ли свойство **дисаблефорЦиблелогофф** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-414">**Windows Server 2008:** Determines whether the **DisableForcibleLogoff** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-415">0</span><span class="sxs-lookup"><span data-stu-id="6d432-415">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-416">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-416">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-417">1</span><span class="sxs-lookup"><span data-stu-id="6d432-417">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-418">Групповая политика.</span><span class="sxs-lookup"><span data-stu-id="6d432-418">Group Policy.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-419">**полицисаурцеенаблеаутоматикреконнектион**</span><span class="sxs-lookup"><span data-stu-id="6d432-419">**PolicySourceEnableAutomaticReconnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-420">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-420">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-422">Указывает, настроено ли свойство **енаблеаутоматикреконнектион** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-422">Indicates whether the **EnableAutomaticReconnection** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="6d432-423">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-423">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-424">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-424">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-425">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-425">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-426">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-426">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="6d432-427">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-427">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-428">**полицисаурцеенабледфсс**</span><span class="sxs-lookup"><span data-stu-id="6d432-428">**PolicySourceEnableDFSS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-429">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-429">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-430">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-430">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-431">Указывает, настроено ли свойство **енабледфсс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-431">Indicates whether the **EnableDFSS** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-432">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-432">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-433">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-433">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-434">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-434">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-435">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-435">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="6d432-436">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6d432-436">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-437">**полицисаурцеенаблеремотедесктопмси**</span><span class="sxs-lookup"><span data-stu-id="6d432-437">**PolicySourceEnableRemoteDesktopMSI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-438">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-438">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-439">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-440">Указывает, настроено ли свойство **енаблеремотедесктопмси** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-440">Indicates whether the **EnableRemoteDesktopMSI** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="6d432-441">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-441">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-442">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-442">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-443">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-443">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-444">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-444">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="6d432-445">**Windows Server 2008:** Это свойство недоступно до Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6d432-445">**Windows Server 2008:** This property is unavailable prior to Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-446">**полицисаурцефаллбаккпринтдривертипе**</span><span class="sxs-lookup"><span data-stu-id="6d432-446">**PolicySourceFallbackPrintDriverType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-447">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-447">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-448">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-448">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-449">Указывает, настроено ли свойство **фаллбаккпринтдривертипе** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-449">Indicates whether the **FallbackPrintDriverType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-450">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-450">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-451">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-451">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-452">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-452">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-453">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-453">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-454">**полицисаурцехомедиректори**</span><span class="sxs-lookup"><span data-stu-id="6d432-454">**PolicySourceHomeDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-455">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-455">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-456">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-456">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-457">Указывает, настроено ли свойство **хомедиректори** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-457">Indicates whether the **HomeDirectory** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-458">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-458">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-459">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-459">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-460">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-460">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-461">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-461">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-462">**полицисаурцелиценсингтипе**</span><span class="sxs-lookup"><span data-stu-id="6d432-462">**PolicySourceLicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-463">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-463">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-464">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-464">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-465">Указывает, настроено ли свойство **лиценсингтипе** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-465">Indicates whether the **LicensingType** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-466">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-466">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-467">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-467">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-468">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-468">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-469">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-469">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-470">**полицисаурцепрофилепас**</span><span class="sxs-lookup"><span data-stu-id="6d432-470">**PolicySourceProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-471">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-471">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-472">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-473">Указывает, настроено ли свойство " **FilePath** " сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-473">Indicates whether the **ProfilePath** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-474">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-474">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-475">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-475">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-476">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-476">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-477">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-477">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-478">**полицисаурцередиректсмарткардс**</span><span class="sxs-lookup"><span data-stu-id="6d432-478">**PolicySourceRedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-479">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-479">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-480">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-481">Указывает, настроено ли свойство **редиректсмарткардс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-481">Indicates whether the **RedirectSmartCards** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="6d432-482">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-482">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-483">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-483">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-484">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-484">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-485">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-485">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="6d432-486">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-486">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-487">**полицисаурцесинглесессион**</span><span class="sxs-lookup"><span data-stu-id="6d432-487">**PolicySourceSingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-488">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-488">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-489">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-489">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-490">Указывает, настроено ли свойство **синглесессион** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-490">Indicates whether the property **SingleSession** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-491">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-491">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-492">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-492">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-493">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-493">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-494">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-494">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-495">**полицисаурцетимезонередиректион**</span><span class="sxs-lookup"><span data-stu-id="6d432-495">**PolicySourceTimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-496">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-496">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-497">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-497">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-498">Указывает, настроено ли свойство **тимезонередиректион** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-498">Indicates whether the property **TimeZoneRedirection** is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-499">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-499">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-500">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-500">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-501">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-501">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-502">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-502">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-503">**полицисаурцеусердеасипринтдривер**</span><span class="sxs-lookup"><span data-stu-id="6d432-503">**PolicySourceUseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-504">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-504">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-505">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-505">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-506">Указывает, настроено ли свойство **усердеасипринтдривер** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-506">Indicates whether the **UseRDEasyPrintDriver** property is configured by the server or group policy.</span></span>

<dt>

<span data-ttu-id="6d432-507">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-507">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-508">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-508">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-509">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-509">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-510">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-510">Group policy</span></span>

</dd> </dl>

<span data-ttu-id="6d432-511">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-511">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-512">**полицисаурцеусетемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="6d432-512">**PolicySourceUseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-513">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-513">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-514">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-514">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-515">Указывает, настроено ли свойство **усетемпфолдерс** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="6d432-515">Indicates whether the **UseTempFolders** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="6d432-516">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-516">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-517">Сервер</span><span class="sxs-lookup"><span data-stu-id="6d432-517">Server</span></span>

</dd> <dt>

<span data-ttu-id="6d432-518">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-518">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-519">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="6d432-519">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-520">**поссиблелиценсингтипес**</span><span class="sxs-lookup"><span data-stu-id="6d432-520">**PossibleLicensingTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-521">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-522">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-523">Квалификаторы: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**Битвалуес**](/windows/desktop/WmiSdk/standard-qualifiers) ("личный сервер терминалов", "удаленный рабочий стол для администрирования", "на устройство", "на пользователя", "не настроено")</span><span class="sxs-lookup"><span data-stu-id="6d432-523">Qualifiers: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "4", "5"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Personal Terminal Server", "Remote Desktop for Administration", "Per Device", "Per User", "Not Configured")</span></span>
</dt> </dl>

<span data-ttu-id="6d432-524">Битовая маска, указывающая доступные типы лицензирования.</span><span class="sxs-lookup"><span data-stu-id="6d432-524">A bitmask that specifies the licensing types that are available.</span></span> <span data-ttu-id="6d432-525">Это может быть сочетание одного или нескольких из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="6d432-525">This can be a combination of one or more of the following values.</span></span>

<dt>

<span data-ttu-id="6d432-526">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-526">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-527">Поддерживаются лицензии на сервер узла личных сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-527">Personal RD Session Host server licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-528">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="6d432-528">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-529">Поддерживаются лицензии на удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="6d432-529">Remote Desktop licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-530">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="6d432-530">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-531">Поддерживаются лицензии "на устройство".</span><span class="sxs-lookup"><span data-stu-id="6d432-531">Per device licenses are supported.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-532">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="6d432-532">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-533">Поддерживаются лицензии "на пользователя".</span><span class="sxs-lookup"><span data-stu-id="6d432-533">Per user licenses are supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-534">**Путь к пути**</span><span class="sxs-lookup"><span data-stu-id="6d432-534">**ProfilePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-535">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-536">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-536">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-537">Путь к профилю для компьютера.</span><span class="sxs-lookup"><span data-stu-id="6d432-537">Profile path for the computer.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-538">**редиректсмарткардс**</span><span class="sxs-lookup"><span data-stu-id="6d432-538">**RedirectSmartCards**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-539">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-539">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-540">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-540">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-541">Указывает, разрешено ли перенаправление устройств смарт-карт в удаленном сеансе.</span><span class="sxs-lookup"><span data-stu-id="6d432-541">Specifies if redirection of smart card devices is allowed in a remote session.</span></span>

<dt>

<span data-ttu-id="6d432-542">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="6d432-542">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-543">Перенаправление устройств смарт-карт не разрешено.</span><span class="sxs-lookup"><span data-stu-id="6d432-543">Smart card device redirection is not allowed.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-544">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="6d432-544">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="6d432-545">Перенаправление устройств смарт-карт разрешено.</span><span class="sxs-lookup"><span data-stu-id="6d432-545">Smart card device redirection is allowed.</span></span>

</dd> </dl>

<span data-ttu-id="6d432-546">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-546">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-547">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="6d432-547">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-548">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-548">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-549">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-549">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-550">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6d432-550">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6d432-551">Имя сервера узла сеансов удаленных рабочих столов, свойства которого представляют интерес.</span><span class="sxs-lookup"><span data-stu-id="6d432-551">Name of the RD Session Host server whose properties are of interest.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-552">**сессионброкердраинмоде**</span><span class="sxs-lookup"><span data-stu-id="6d432-552">**SessionBrokerDrainMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-553">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-553">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-554">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-554">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-555">RDCB режим входа пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-555">The RD Connection Broker user logon mode.</span></span>

<dt>

<span data-ttu-id="6d432-556">0</span><span class="sxs-lookup"><span data-stu-id="6d432-556">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-557">Разрешить все подключения.</span><span class="sxs-lookup"><span data-stu-id="6d432-557">Allow all connections.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-558">1</span><span class="sxs-lookup"><span data-stu-id="6d432-558">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-559">Разрешить повторное подключение, но запретить новые входы до перезапуска сервера.</span><span class="sxs-lookup"><span data-stu-id="6d432-559">Allow reconnections, but prevent new logons until the server is restarted.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-560">2</span><span class="sxs-lookup"><span data-stu-id="6d432-560">2</span></span>
</dt> <dd>

<span data-ttu-id="6d432-561">Разрешить повторное подключение, но запретить новые входы в систему.</span><span class="sxs-lookup"><span data-stu-id="6d432-561">Allow reconnections, but prevent new logons.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-562">**синглесессион**</span><span class="sxs-lookup"><span data-stu-id="6d432-562">**SingleSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-563">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-563">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-564">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-564">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-565">Указывает, разрешен ли один или несколько сеансов службы удаленных рабочих столов для каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="6d432-565">Specifies whether one or more Remote Desktop Services sessions are allowed per user.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="6d432-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-566"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-567">Для каждого пользователя разрешено более одного сеанса.</span><span class="sxs-lookup"><span data-stu-id="6d432-567">More than one session is allowed per user.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="6d432-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-568"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-569">Для каждого пользователя допускается только один сеанс.</span><span class="sxs-lookup"><span data-stu-id="6d432-569">Only one session is allowed per user.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-570">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="6d432-570">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-571">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="6d432-571">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-572">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-572">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6d432-573">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="6d432-573">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="6d432-574">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="6d432-574">Current status of the object.</span></span> <span data-ttu-id="6d432-575">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="6d432-575">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="6d432-576">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="6d432-576">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="6d432-577">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="6d432-577">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6d432-578">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="6d432-578">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6d432-579">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="6d432-579">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6d432-580">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6d432-580">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="6d432-581">("ОК")</span><span class="sxs-lookup"><span data-stu-id="6d432-581">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-582">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="6d432-582">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-583">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="6d432-583">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-584">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="6d432-584">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-585">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="6d432-585">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-586">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="6d432-586">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-587">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="6d432-587">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="6d432-588">("Служба")</span><span class="sxs-lookup"><span data-stu-id="6d432-588">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-589">**терминалсервермоде**</span><span class="sxs-lookup"><span data-stu-id="6d432-589">**TerminalServerMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-590">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-590">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-591">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-592">Режим работы сервера узла сеансов удаленных рабочих столов для службы службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-592">The RD Session Host server operating mode of the Remote Desktop Services service.</span></span> <span data-ttu-id="6d432-593">Этот режим управляет применяемыми политиками лицензирования, а также включением функций совместимости приложений.</span><span class="sxs-lookup"><span data-stu-id="6d432-593">This mode controls the licensing policies that are applicable as well as whether application-compatibility features are enabled.</span></span>

<dt>

<span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>

<span data-ttu-id="6d432-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**Выборе** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-594"><span id="AppServer"></span><span id="appserver"></span><span id="APPSERVER"></span>**AppServer** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-595">Сервер работает как сервер приложений.</span><span class="sxs-lookup"><span data-stu-id="6d432-595">The server operates as an application server.</span></span>

</dd> <dt>

<span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>

<span data-ttu-id="6d432-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**Ремотеадмин** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-596"><span id="RemoteAdmin"></span><span id="remoteadmin"></span><span id="REMOTEADMIN"></span>**RemoteAdmin** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-597">Сеанс администрируется удаленно.</span><span class="sxs-lookup"><span data-stu-id="6d432-597">The session is administered remotely.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-598">**тимезонередиректион**</span><span class="sxs-lookup"><span data-stu-id="6d432-598">**TimeZoneRedirection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-599">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-599">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-600">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-600">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-601">Указывает, может ли клиентский компьютер перенаправлять параметры часового пояса в сеанс службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6d432-601">Specifies whether the client computer can redirect its time zone settings to the Remote Desktop Services session.</span></span>

<dt>

<span data-ttu-id="6d432-602">0</span><span class="sxs-lookup"><span data-stu-id="6d432-602">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-603">Перенаправление отключено.</span><span class="sxs-lookup"><span data-stu-id="6d432-603">Redirection is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-604">1</span><span class="sxs-lookup"><span data-stu-id="6d432-604">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-605">Перенаправление включено.</span><span class="sxs-lookup"><span data-stu-id="6d432-605">Redirection is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-606">**усердеасипринтдривер**</span><span class="sxs-lookup"><span data-stu-id="6d432-606">**UseRDEasyPrintDriver**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-607">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-607">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-608">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-608">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-609">Указывает, используется ли первый драйвер принтера компонент Easy Print служб удаленных рабочих столов для установки всех клиентских принтеров.</span><span class="sxs-lookup"><span data-stu-id="6d432-609">Specifies whether the Remote Desktop Easy Print printer driver is used first to install all client printers.</span></span>

<dt>

<span data-ttu-id="6d432-610">0</span><span class="sxs-lookup"><span data-stu-id="6d432-610">0</span></span>
</dt> <dd>

<span data-ttu-id="6d432-611">Сервер узла сеансов удаленных рабочих столов пытается найти подходящий драйвер принтера для установки клиентского принтера.</span><span class="sxs-lookup"><span data-stu-id="6d432-611">The RD Session Host server tries to find a suitable printer driver to install the client printer.</span></span> <span data-ttu-id="6d432-612">Если у сервера узла сеансов удаленных рабочих столов нет драйвера принтера, соответствующего принтеру клиента, сервер пытается использовать драйвер компонент Easy Print служб удаленных рабочих столов для установки клиентского принтера.</span><span class="sxs-lookup"><span data-stu-id="6d432-612">If the RD Session Host server does not have a printer driver that matches the client printer, the server tries to use the Remote Desktop Easy Print driver to install the client printer.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-613">1</span><span class="sxs-lookup"><span data-stu-id="6d432-613">1</span></span>
</dt> <dd>

<span data-ttu-id="6d432-614">Сначала сервер узла сеансов удаленных рабочих столов пытается использовать драйвер принтера компонент Easy Print служб удаленных рабочих столов для установки всех клиентских принтеров.</span><span class="sxs-lookup"><span data-stu-id="6d432-614">The RD Session Host server first tries to use the Remote Desktop Easy Print printer driver to install all client printers.</span></span> <span data-ttu-id="6d432-615">Если по какой-либо причине не удается использовать драйвер принтера компонент Easy Print служб удаленных рабочих столов, используется драйвер принтера на сервере узла сеансов удаленных рабочих столов, который соответствует принтеру клиента.</span><span class="sxs-lookup"><span data-stu-id="6d432-615">If for any reason the Remote Desktop Easy Print printer driver cannot be used, a printer driver on the RD Session Host server that matches the client printer is used.</span></span>

</dd> </dl>

<span data-ttu-id="6d432-616">**Windows server 2008 R2 и Windows server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="6d432-616">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="6d432-617">**усерпермиссион**</span><span class="sxs-lookup"><span data-stu-id="6d432-617">**UserPermission**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-618">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-618">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-619">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="6d432-619">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="6d432-620">Указывает, имеет ли каждый сеанс пользователя строгую или ослабленную безопасность.</span><span class="sxs-lookup"><span data-stu-id="6d432-620">Specifies if each user session has tight or relaxed security.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="6d432-621"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-621"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-622">Обеспечение безопасности является тесной.</span><span class="sxs-lookup"><span data-stu-id="6d432-622">Security is tight.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="6d432-623"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-623"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-624">Безопасность ослаблена.</span><span class="sxs-lookup"><span data-stu-id="6d432-624">Security is relaxed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="6d432-625">**усетемпфолдерс**</span><span class="sxs-lookup"><span data-stu-id="6d432-625">**UseTempFolders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6d432-626">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6d432-626">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6d432-627">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6d432-627">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6d432-628">Указывает, будут ли временные каталоги создаваться и удаляться отдельно для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="6d432-628">Specifies whether temporary directories are created and deleted on a per-session basis.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="6d432-629"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="6d432-629"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-630">Временные каталоги не создаются и не удаляются для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="6d432-630">Temporary directories are not created and deleted for each session.</span></span> <span data-ttu-id="6d432-631">Один из них создается для первого сеанса и никогда не удаляется.</span><span class="sxs-lookup"><span data-stu-id="6d432-631">One is created for the first session and never deleted.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="6d432-632"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="6d432-632"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="6d432-633">Временные каталоги создаются и удаляются для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="6d432-633">Temporary directories are created and deleted for each session.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6d432-634">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d432-634">Remarks</span></span>

<span data-ttu-id="6d432-635">**Win32 \_ Терминалсервицесеттинг** связан с [**Win32 \_ терминалсервице**](win32-terminalservice.md) в качестве свойства **Setting** ассоциации [**Win32 \_ терминалсервицетосеттинг**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="6d432-635">**Win32\_TerminalServiceSetting** is associated to [**Win32\_TerminalService**](win32-terminalservice.md) as the **Setting** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

<span data-ttu-id="6d432-636">[**Win32 \_ Терминалсеттинг**](win32-terminalsetting.md) связывается с [**\_ терминалом Win32**](win32-terminal.md) как свойство **Setting** ассоциации [**Win32 \_ терминалтерминалсеттинг**](win32-terminalterminalsetting.md) .</span><span class="sxs-lookup"><span data-stu-id="6d432-636">[**Win32\_TerminalSetting**](win32-terminalsetting.md) is associated to [**Win32\_Terminal**](win32-terminal.md) as the **Setting** property of the [**Win32\_TerminalTerminalSetting**](win32-terminalterminalsetting.md) association.</span></span>

<span data-ttu-id="6d432-637">Чтобы подключиться к корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d432-637">To connect to the Root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="6d432-638">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="6d432-638">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="6d432-639">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.</span><span class="sxs-lookup"><span data-stu-id="6d432-639">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="6d432-640">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="6d432-640">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="6d432-641">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="6d432-641">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="6d432-642">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="6d432-642">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="6d432-643">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="6d432-643">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="6d432-644">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="6d432-644">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="6d432-645">Требования</span><span class="sxs-lookup"><span data-stu-id="6d432-645">Requirements</span></span>



| <span data-ttu-id="6d432-646">Требование</span><span class="sxs-lookup"><span data-stu-id="6d432-646">Requirement</span></span> | <span data-ttu-id="6d432-647">Значение</span><span class="sxs-lookup"><span data-stu-id="6d432-647">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d432-648">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d432-648">Minimum supported client</span></span><br/> | <span data-ttu-id="6d432-649">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d432-649">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6d432-650">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d432-650">Minimum supported server</span></span><br/> | <span data-ttu-id="6d432-651">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6d432-651">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6d432-652">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d432-652">Namespace</span></span><br/>                | <span data-ttu-id="6d432-653">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6d432-653">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="6d432-654">MOF</span><span class="sxs-lookup"><span data-stu-id="6d432-654">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d432-655"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d432-655"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d432-656">DLL</span><span class="sxs-lookup"><span data-stu-id="6d432-656">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d432-657"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d432-657"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d432-658">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d432-658">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d432-659">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="6d432-659">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="6d432-660">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="6d432-660">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="6d432-661">**\_Терминалсервице Win32**</span><span class="sxs-lookup"><span data-stu-id="6d432-661">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="6d432-662">**\_Терминалсервицетосеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="6d432-662">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dt>

[<span data-ttu-id="6d432-663">**\_Терминалтерминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="6d432-663">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dt>

[<span data-ttu-id="6d432-664">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="6d432-664">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> </dl>

 

