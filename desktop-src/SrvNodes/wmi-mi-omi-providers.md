---
description: Инфраструктура управления Windows (WMI), Инструментарий управления (MI) и открытая инфраструктура управления (OMI) используют файлы формата MOF для описания информации, доступной через соответствующих поставщиков.
ms.assetid: 5ec3c6a2-df23-446d-a4da-b8e207eeb6f6
title: Поставщики WMI, MI и OMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505a0853d9df7d9cf6f2371f6342b77f61f536b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664723"
---
# <a name="wmimiomi-providers"></a><span data-ttu-id="dc885-103">Поставщики WMI, MI и OMI</span><span class="sxs-lookup"><span data-stu-id="dc885-103">WMI/MI/OMI Providers</span></span>

<span data-ttu-id="dc885-104">Инфраструктура управления Windows (WMI), Инструментарий управления (MI) и открытая инфраструктура управления (OMI) используют файлы формата MOF для описания информации, доступной через соответствующих поставщиков.</span><span class="sxs-lookup"><span data-stu-id="dc885-104">Windows Management Infrastructure (WMI), Management Instrumentation (MI) and Open Management Infrastructure (OMI) all use Management Object Format (MOF) files to describe the information made available through their respective providers.</span></span>

<dl> <dt>

<span data-ttu-id="dc885-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-105"><span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-106">Поставщик Active Directory, также известный как поставщик служб каталогов (DS), сопоставляет объекты Active Directory с WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-106">The Active Directory provider, also known as the Directory Services (DS) provider, maps Active Directory objects to WMI.</span></span> <span data-ttu-id="dc885-107">С помощью доступа к пространству имен LDAP в WMI можно ссылаться на объект или сделать его псевдонимом в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dc885-107">By accessing the Lightweight Directory Access Protocol (LDAP) namespace in WMI, you can reference or make an object an alias in the Active Directory.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Инвентаризация приложений](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-108"><span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Application Inventory](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-109">Классы WMI для инвентаризации приложений позволяют обнаруживать установленные приложения Win32 и приложения Магазина Windows в системе Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-109">The WMI classes for Application Inventory enable discovery of the installed Win32 applications and Windows store applications on a Windows system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Прокси приложения](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-110"><span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Application Proxy](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-111">Поставщик WMI прокси приложения позволяет разработчикам получить доступ к службе прокси веб-приложения, чтобы администраторы могли публиковать приложения для внешнего доступа.</span><span class="sxs-lookup"><span data-stu-id="dc885-111">Application Proxy WMI Provider enables developers to access the Web Application Proxy service so administrators can publish applications for external access.</span></span> <span data-ttu-id="dc885-112">Прокси веб-приложения — это обратный прокси для службы федерации Active Directory (AD FS) (AD FS).</span><span class="sxs-lookup"><span data-stu-id="dc885-112">Web Application Proxy is a reverse proxy for Active Directory Federation Services (AD FS).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Шифрование диска BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-113"><span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[BitLocker Drive Encryption (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-114">Обеспечивает настройку и управление для области хранения на жестком диске, представленной экземпляром [**Win32 \_ енкриптаблеволуме**](/windows/desktop/SecProv/win32-encryptablevolume), который можно защитить с помощью шифрования.</span><span class="sxs-lookup"><span data-stu-id="dc885-114">Provides configuration and management for an area of storage on a hard disk drive, represented by an instance of [**Win32\_EncryptableVolume**](/windows/desktop/SecProv/win32-encryptablevolume), that can be protected by using encryption.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-115"><span id="BITS"></span><span id="bits"></span>[ЧИСЛА](/previous-versions/windows/desktop/bitsprov/bits-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-115"><span id="BITS"></span><span id="bits"></span>[BITS](/previous-versions/windows/desktop/bitsprov/bits-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-116">Фоновая интеллектуальная служба передачи (BITS) Compact Server с удаленным управлением BITS позволяет администраторам или контроллерам, прошедшим проверку подлинности, создавать, изменять и администрировать задания передачи BITS удаленно без использования службы службы IIS (IIS).</span><span class="sxs-lookup"><span data-stu-id="dc885-116">The Background Intelligent Transfer Service (BITS) Compact Server with BITS Remote Management allows authenticated administrators or controller applications to create, modify and manage BITS transfer jobs remotely without using the Internet Information Services (IIS) service.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Реквизит](https://msdn.microsoft.com/library/ms941491.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc885-117"><span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[BizTalk](https://msdn.microsoft.com/library/ms941491.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-118">Предоставляет доступ к объектам администрирования BizTalk, представленным классами WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-118">Supplies access to the BizTalk administration objects represented by WMI classes.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[данные конфигурации загрузки](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-119"><span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[Boot Configuration Data](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-120">Поставщик данные конфигурации загрузки (BCD) предоставляет хранилище, которое используется для описания приложений загрузки и параметров приложения загрузки.</span><span class="sxs-lookup"><span data-stu-id="dc885-120">The Boot Configuration Data (BCD) provider provides a store that is used to describe boot applications and boot application settings.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Сборщик событий загрузки](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-121"><span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Boot Event Collector](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-122">Поставщик WMI сборщика событий загрузки предоставляет доступ к сведениям о подключении и конфигурации для функции сбора событий установки и загрузки в Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dc885-122">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, события управления питанием](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span><span class="sxs-lookup"><span data-stu-id="dc885-123"><span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, Power Management Events](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-124">Поставщики CIMWin32 поддерживают классы, реализованные в CimWin32.dll, и состоят из основных классов CIM, реализации этих классов в Win32 и событий управления питанием.</span><span class="sxs-lookup"><span data-stu-id="dc885-124">The CIMWin32 providers support the classes implemented in CimWin32.dll, and consist of the core CIM classes, the Win32 implementation of those classes, and power management events.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-125"><span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-126">Поставщик CIMWin32a расширяет классы, доступные в [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span><span class="sxs-lookup"><span data-stu-id="dc885-126">The CIMWin32a provider extends the classes available in the [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[дкбкосЦим](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span><span class="sxs-lookup"><span data-stu-id="dc885-127"><span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[DcbQosCim](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-128">Поставщик ДкбкосЦим поддерживает классы, описывающие данные параметров качества обслуживания сети, данные параметров управления и данные о параметрах класса трафика.</span><span class="sxs-lookup"><span data-stu-id="dc885-128">The DcbQosCim provider supports classes that describe Network QOS setting data, control setting data, and traffic class setting data.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Распределенная файловая система (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-129"><span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Distributed File System (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-130">Поставщик DFS предоставляет функции для работы с скриптами DFS через WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-130">The DFS provider supplies scriptable DFS functions through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Репликация распределенная файловая система (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span><span class="sxs-lookup"><span data-stu-id="dc885-131"><span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-132">Создает средства для настройки и мониторинга службы [Распределенная файловая система (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) .</span><span class="sxs-lookup"><span data-stu-id="dc885-132">Creates tools for configuring and monitoring the [Distributed File System (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) service.</span></span> <span data-ttu-id="dc885-133">Дополнительные сведения см. в разделе [классы WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dc885-133">For more information, see [DFSR WMI Classes](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[дфснЦимпров](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-134"><span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-135">Поставщик [дфснЦимпров](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) поддерживает классы, реализующие доступ к пространству имен DFS.</span><span class="sxs-lookup"><span data-stu-id="dc885-135">The [Dfsncimprov](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) provider supports classes that implement DFS namespace access.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[дхкпсерверпспровидер](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-136"><span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-137">Поставщик [дхкпсерверпспровидер](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) поддерживает классы, взаимодействующие с DHCP-сервером.</span><span class="sxs-lookup"><span data-stu-id="dc885-137">The [DhcpServerPSProvider](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) provider supports classes that interact with a dynamic host configuration protocol (DHCP) server.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Квота диска](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-138"><span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Disk Quota](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-139">Поставщик дисковых квот Windows позволяет администраторам управлять объемом данных, которые каждый пользователь сохраняет в файловой системе NTFS.</span><span class="sxs-lookup"><span data-stu-id="dc885-139">The Windows Disk Quota provider allows administrators to control the amount of data that each user stores on an NTFS file system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Координатор распределенных транзакций (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-140"><span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Distributed Transaction Coordinator (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-141">Поставщик DTC обеспечивает управление DTC.</span><span class="sxs-lookup"><span data-stu-id="dc885-141">The DTC provider enables management of the DTC.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-142"><span id="DNS"></span><span id="dns"></span>[СЕРВЕРЕ](/windows/desktop/DNS/dns-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-142"><span id="DNS"></span><span id="dns"></span>[DNS](/windows/desktop/DNS/dns-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-143">Позволяет администраторам и программистам настраивать записи ресурсов (RR) системы доменных имен (DNS) и DNS-серверы с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-143">Enables administrators and programmers to configure Domain Name System (DNS) resource records (RRs) and DNS Servers using WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Классы поставщиков днсклиентЦим](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-144"><span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Dnsclientcim Provider Classes](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-145">Поставщик ДнсклиентЦим поддерживает классы, взаимодействующие с клиентом службы доменных имен (DNS).</span><span class="sxs-lookup"><span data-stu-id="dc885-145">The Dnsclientcim provider supports classes that interact with a Domain Name System (DNS) client.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[днсклиентпспровидер](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-146"><span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-147">Поставщик [днсклиентпспровидер](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) поддерживает классы WMI, взаимодействующие с DNS-клиентом.</span><span class="sxs-lookup"><span data-stu-id="dc885-147">The [DnsClientPSProvider](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) provider supports WMI classes that interact with a DNS client.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[днссерверпспровидер](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-148"><span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-149">Поставщик [днссерверпспровидер](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) поддерживает классы WMI, взаимодействующие с DNS-сервером.</span><span class="sxs-lookup"><span data-stu-id="dc885-149">The [DnsServerPSProvider](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) provider supports WMI classes that interact with a DNS server.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Журнал событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-150"><span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-151">Поставщик [журнала событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) предоставляет доступ к данным из службы журнала событий и уведомлению о событиях.</span><span class="sxs-lookup"><span data-stu-id="dc885-151">The [Event Log](/previous-versions/windows/desktop/eventlogprov/event-log-provider) provider supplies access to data from the event log service, and notification of events.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Управление трассировкой событий](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-152"><span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Event Tracing Management](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-153">Поставщик управления трассировкой событий предоставляет доступ к средствам трассировки событий для конфигурации сеансов авторегистратора ETW и событиям трассировки.</span><span class="sxs-lookup"><span data-stu-id="dc885-153">The Event Tracing Management provider provides access to Event Tracing for Windows (ETW) autologger session configurations and trace events.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Обновление Cluster-Aware отработки отказа](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-154"><span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Failover Cluster-Aware Updating](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-155">Поставщик отработки отказа Cluster-Aware обновления (CAU) поддерживает координацию и управление для CAU.</span><span class="sxs-lookup"><span data-stu-id="dc885-155">The Failover Cluster-Aware Updating (CAU) provider supports coordination with and management of CAU.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Отказоустойчивая кластеризация Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-156"><span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Failover Clustering Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-157">Поставщик отказоустойчивой кластеризации Hyper-V обеспечивает управление и создание отчетов Hyper-V в среде кластеризации.</span><span class="sxs-lookup"><span data-stu-id="dc885-157">The Failover Clustering Hyper-V provider provides management and reporting of Hyper-V in a clustering environment.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Качество обслуживания хранилища отказоустойчивой кластеризации](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-158"><span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Failover Clustering Storage QoS](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-159">Поставщик качества обслуживания хранилища отказоустойчивой кластеризации обеспечивает управление и создание отчетов по политикам качества обслуживания для кластерного хранилища.</span><span class="sxs-lookup"><span data-stu-id="dc885-159">The Failover Clustering Storage Quality of Service (QoS) provider provides management and reporting of the clustering storage QoS policies.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Поставщик отказоустойчивого кластера v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-160"><span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Failover Cluster V1 Provider](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-161">Поставщик отказоустойчивого кластера версии 1 обеспечивает Управление отказоустойчивым кластером.</span><span class="sxs-lookup"><span data-stu-id="dc885-161">The Failover Cluster V1 provider provides management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Расширения отказоустойчивого кластера версии 1](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-162"><span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Failover Cluster V1 Extensions](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-163">Поставщик расширений отказоустойчивого кластера обеспечивает дополнительное Управление отказоустойчивым кластером.</span><span class="sxs-lookup"><span data-stu-id="dc885-163">The Failover Cluster Extensions provider provides additional management of a failover cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Монитор работоспособности шлюза](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-164"><span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Gateway Health Monitor](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-165">Поставщик монитора работоспособности шлюза управляет событиями и данными мониторинга работоспособности шлюза.</span><span class="sxs-lookup"><span data-stu-id="dc885-165">The Gateway Health Monitor provider manages gateway health monitoring events and information.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[групповая политика API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span><span class="sxs-lookup"><span data-stu-id="dc885-166"><span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[Group Policy API](/previous-versions/windows/desktop/Policy/group-policy-start-page)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-167">Поставщик групповая политика обеспечивает администрирование на основе политик с помощью служб каталогов Microsoft Active Directory (AD).</span><span class="sxs-lookup"><span data-stu-id="dc885-167">The Group Policy provider enables policy-based administration using Microsoft Active Directory (AD) directory services.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Служба защиты узла](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-168"><span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Host Guardian Service](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-169">Поставщик службы защиты узла обеспечивает управление службой защиты узла для экранированных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="dc885-169">The Host Guardian Service provider provides management of the Host Guardian Service for shielded VMs.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-170"><span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-171">Поставщик Hyper-V позволяет управлять и извлекать сведения о виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="dc885-171">The Hyper-V provider allows you to manage and retrieve information about virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-172"><span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-173">Поставщик Hyper-V (v2) расширяет возможности поставщика [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .</span><span class="sxs-lookup"><span data-stu-id="dc885-173">The Hyper-V (V2) provider extends the [Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) provider.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Службы IIS (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="dc885-174"><span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Internet Information Services (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))</span></span>
</dt> <dd>

<span data-ttu-id="dc885-175">Предоставляет интерфейсы программирования, которые можно использовать для запроса и настройки метабазы IIS.</span><span class="sxs-lookup"><span data-stu-id="dc885-175">Exposes programming interfaces that can be used to query and configure the IIS metabase.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Сервер управления IP-адресами (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-176"><span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Internet Protocol Address Management (IPAM) Server](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-177">Поставщик IPAM-сервера позволяет разработчикам управлять IPAM с помощью WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-177">The IPAM Server Provider enables developers to manage IPAM through WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-178"><span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-179">Предустановленный поставщик IP-маршрутов предоставляет сведения о маршрутизации сети IPV4, включая (но не ограничиваясь) сведения, доступные с помощью команды **route print** .</span><span class="sxs-lookup"><span data-stu-id="dc885-179">The preinstalled IP Route provider supplies IPV4 network routing information, including (but not limited to) the information available through the **route print** command.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Интеллектуальный интерфейс управления платформой (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-180"><span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Intelligent Platform Management Interface (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-181">Предоставляет данные IPMI от операций контроллера управления основной платой (BMC).</span><span class="sxs-lookup"><span data-stu-id="dc885-181">Supplies IPMI data from Baseboard Management Controller (BMC) operations.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Сервер цели iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-182"><span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[iSCSI Target Server](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-183">Поставщик сервера цели iSCSI поддерживает интерфейс WMI для управления сервером Microsoft iSCSI Target Server, например создание виртуальных дисков и их представление клиенту.</span><span class="sxs-lookup"><span data-stu-id="dc885-183">The iSCSI Target Server provider supports a WMI interface for managing the Microsoft iSCSI Target Server, such as creating virtual disks, and for presenting them to the client.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Объект задания](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-184"><span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Job Object](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-185">Поставщик объектов задания поддерживает доступ к данным об именованных объектах заданий ядра.</span><span class="sxs-lookup"><span data-stu-id="dc885-185">The Job Object provider supports access to data about named kernel job objects.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Трассировка ядра](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-186"><span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Kernel Trace](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-187">Предварительно установленный поставщик событий трассировки ядра позволяет просматривать события трассировки ядра при создании процесса, завершении процесса, создании потока, завершении потока и загрузке модуля.</span><span class="sxs-lookup"><span data-stu-id="dc885-187">The preinstalled Kernel Trace event provider allows you to see kernel trace events on Process creation, Process termination, Thread creation, Thread termination and module load.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span><span class="sxs-lookup"><span data-stu-id="dc885-188"><span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))</span></span>
</dt> <dd>

<span data-ttu-id="dc885-189">Предоставляет классы для создания, регистрации, настройки и управления приложениями пользовательского протокола SIP с помощью [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span><span class="sxs-lookup"><span data-stu-id="dc885-189">Provides classes that create, register, configure, manage custom Session Initiation Protocol (SIP) applications with the [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Реестр средств управления](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-190"><span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Management Tools Registry](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-191">Поставщик реестра средств управления предоставляет удаленный доступ к реестру.</span><span class="sxs-lookup"><span data-stu-id="dc885-191">The Management Tools Registry provider provides remote access to the registry.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Диспетчер задач средств управления](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-192"><span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Management Tools Task Manager](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-193">Поставщик диспетчера задач средств управления предоставляет доступ к данным диспетчера задач и управление ими.</span><span class="sxs-lookup"><span data-stu-id="dc885-193">The Management Tools Task Manager provider provides access and management of the Task Manager data.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Приложение MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-194"><span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[MDM Application](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-195">Поставщик приложений управления мобильными устройствами (MDM) управляет приложениями на устройствах, подписанных на службу MDM.</span><span class="sxs-lookup"><span data-stu-id="dc885-195">The Mobile Device Management (MDM) application provider manages applications on devices that are subscribed to the MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Мост MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-196"><span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[MDM Bridge](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-197">Поставщик моста MDM позволяет управлять сетевым мостом с помощью MDM.</span><span class="sxs-lookup"><span data-stu-id="dc885-197">The MDM Bridge provider enables MDM management of a network bridge.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Параметры MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-198"><span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[MDM Settings](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-199">Поставщик параметров MDM позволяет управлять параметрами на устройствах, зарегистрированных в службе MDM.</span><span class="sxs-lookup"><span data-stu-id="dc885-199">The MDM Settings Provider enables management of settings on devices enrolled with a MDM service.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ пксвдевице](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-200"><span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-201">Поставщик [MSFT \_ пксвдевице](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) предоставляет класс, определяющий класс представления для физической компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="dc885-201">The [MSFT\_PCSVDevice](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) provider exposes a class that defines a view class for a physical computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[мснетимплатформ](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-202"><span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-203">В разделе Поставщик [мснетимплатформ](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) содержатся справочные сведения о классах поставщиков мснетимплатформ, реализованных в NdisIMPlatCim.dll.</span><span class="sxs-lookup"><span data-stu-id="dc885-203">The [MsNetImPlatform](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) provider section provides reference information for MsNetImPlatform provider classes implemented in NdisIMPlatCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[нетадаптерЦим](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-204"><span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-205">Поставщик [нетадаптерЦим](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) поддерживает классы, обращающиеся к сетевым адаптерам.</span><span class="sxs-lookup"><span data-stu-id="dc885-205">The [NetAdapterCim](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) provider supports classes that access network adapters.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[нетдаЦим](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-206"><span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-207">В этом разделе содержатся справочные сведения о классах поставщиков [нетдаЦим](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .</span><span class="sxs-lookup"><span data-stu-id="dc885-207">This section provides reference information for [NetDaCim](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) Provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[нетнкЦим](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span><span class="sxs-lookup"><span data-stu-id="dc885-208"><span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-209">Содержит справочную информацию о классах поставщика [нетнкЦим](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .</span><span class="sxs-lookup"><span data-stu-id="dc885-209">Provides reference information for [NetNcCim](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) provider classes.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[нетпирдист](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span><span class="sxs-lookup"><span data-stu-id="dc885-210"><span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-211">Поставщик [нетпирдист](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) поддерживает классы, взаимодействующие с инфраструктурой кэша филиала.</span><span class="sxs-lookup"><span data-stu-id="dc885-211">The [NetPeerDist](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) provider supports classes that interact with the Branch Cache infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[неткосЦим](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-212"><span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-213">Поставщик [неткосЦим](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) предоставляет данные для данных о параметрах качества обслуживания сети (QoS) и качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="dc885-213">The [NetQosCim](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) provider supplies data for network quality of service (QoS) and QoS setting data.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[нетсвитчтеам](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-214"><span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[NetSwitchTeam](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-215">В этом разделе содержатся справочные сведения о классах поставщиков Нетсвитчтеам, объявленных в Нетсвитчтеам. mof и реализованных в NetSwitchTeamCim.dll.</span><span class="sxs-lookup"><span data-stu-id="dc885-215">This section provides reference information for NetSwitchTeam provider classes declared in NetSwitchTeam.mof and implemented in NetSwitchTeamCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[нетткпип](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-216"><span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[NetTCPIP](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-217">Поставщик Нетткпип поддерживает классы, взаимодействующие с подключениями TCPIP.</span><span class="sxs-lookup"><span data-stu-id="dc885-217">The NetTCPIP provider supports classes that interact with TCPIP connections.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[нетттЦим](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-218"><span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[NetTtCim](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-219">В этом разделе содержатся справочные сведения о классах поставщиков НетттЦим, определенных в НетттЦим. mof и реализованных в NetTtCim.dll.</span><span class="sxs-lookup"><span data-stu-id="dc885-219">This section provides reference information for NetTtCim provider classes defined in NetTtCim.mof and implemented in NetTtCim.dll.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[нетвнв](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-220"><span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[NetWNV](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-221">Поставщик Нетвнв поддерживает классы, взаимодействующие с технологиями виртуализации сети.</span><span class="sxs-lookup"><span data-stu-id="dc885-221">The NetWNV provider supports classes that interact with net virtualization technologies.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Защита доступа к сети](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-222"><span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Network Access Protection](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-223">Поставщик защиты доступа к сети предоставляет платформу для защищенного доступа к частным сетям.</span><span class="sxs-lookup"><span data-stu-id="dc885-223">The Network Access Protection provider exposes a platform for protected access to private networks.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Балансировка сетевой нагрузки](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-224"><span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Network Load Balancing](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-225">Поставщик балансировки сетевой нагрузки (NLB) обеспечивает управление кластером NLB.</span><span class="sxs-lookup"><span data-stu-id="dc885-225">The Network Load Balancing (NLB) Provider enables management of a NLB cluster.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Сервер Нетворкконтроллер](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-226"><span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[NetworkController Server](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-227">Поставщик обеспечивает управление сервером сетевого контроллера.</span><span class="sxs-lookup"><span data-stu-id="dc885-227">The provider enables management of a network controller server.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-228"><span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-229">Поставщик NFS позволяет создавать средства и сценарии для настройки и мониторинга сетевой файловой системы Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-229">The provider for NFS allows you to create tools and scripts for configuring and monitoring the Windows Network File System.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Проверок](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-230"><span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Ping](/previous-versions/windows/desktop/wmipicmp/ping-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-231">Поставщик проверки связи предоставляет доступ к сведениям о состоянии, предоставленным стандартной командой ping.</span><span class="sxs-lookup"><span data-stu-id="dc885-231">The Ping provider supplies access to the status information provided by the standard ping command.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Политик](/previous-versions/windows/desktop/policmanprov/policy-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-232"><span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Policy](/previous-versions/windows/desktop/policmanprov/policy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-233">Предоставляет расширения для групповой политики и позволяет выполнять уточнения в приложении политики.</span><span class="sxs-lookup"><span data-stu-id="dc885-233">Provides extensions to group policy, and permits refinements in the application of policy.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Индикатор питания](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span><span class="sxs-lookup"><span data-stu-id="dc885-234"><span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Power Meter](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-235">Поставщик счетчиков питания поддерживает интерфейс измерения питания и бюджетирования (ПМБ).</span><span class="sxs-lookup"><span data-stu-id="dc885-235">The Power Meter provider supports the Power Metering and Budgeting (PMB) interface.</span></span> <span data-ttu-id="dc885-236">Эти классы являются основным интерфейсом для запроса информации о Power измерителя из базовых показателей питания в системе.</span><span class="sxs-lookup"><span data-stu-id="dc885-236">These classes are the primary interface for the query of Power Meter Interface (PMI) information from underlying power meters on the system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Политика питания](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span><span class="sxs-lookup"><span data-stu-id="dc885-237"><span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Power Policy](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-238">Поставщик политики управления питанием предоставляет классы, позволяющие удаленно управлять всей инфраструктурой политики управления питанием.</span><span class="sxs-lookup"><span data-stu-id="dc885-238">The Power Policy provider provides classes the ability to remotely manage all the power policy infrastructure.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[рамгмтпспровидер](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span><span class="sxs-lookup"><span data-stu-id="dc885-239"><span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-240">Поставщик [рамгмтпспровидер](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) предоставляет классы для управления удаленным доступом.</span><span class="sxs-lookup"><span data-stu-id="dc885-240">The [RAMgmtPSProvider](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) provider provides classes to manage Remote Access.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[расерверпспровидер](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span><span class="sxs-lookup"><span data-stu-id="dc885-241"><span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-242">Поставщик [расерверпспровидер](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) предоставляет классы для управления сервером удаленного доступа.</span><span class="sxs-lookup"><span data-stu-id="dc885-242">The [RAServerPSProvider](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) provider provides classes to manage the Remote Access Server.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[релиабилитиметрикспровидер](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-243"><span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-244">Поставщик [релиабилитиметрикспровидер](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) предоставляет метрики надежности систем и журнала событий Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-244">The [ReliabilityMetricsProvider](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) provider exposes system and Windows Event Log reliability metrics.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[службы удаленных рабочих столов](/windows/desktop/TermServ/terminal-services-wmi-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-245"><span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[Remote Desktop Services](/windows/desktop/TermServ/terminal-services-wmi-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-246">Обеспечивает единообразное администрирование сервера в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="dc885-246">Enables consistent server administration in a Remote Desktop Services environment.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span><span class="sxs-lookup"><span data-stu-id="dc885-247"><span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-248">Определяет классы, позволяющие создавать скрипты и код для изменения параметров сервера отчетов и диспетчер отчетов.</span><span class="sxs-lookup"><span data-stu-id="dc885-248">Defines classes that allow you to write scripts and code to modify the settings of the report server and the Report Manager.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Результирующий набор политик (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span><span class="sxs-lookup"><span data-stu-id="dc885-249"><span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Resultant Set of Policy (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-250">Предоставляет методы для планирования и отладки параметров политики в ситуации "что если".</span><span class="sxs-lookup"><span data-stu-id="dc885-250">Supplies methods to plan and debug policy settings in a what-if situation.</span></span> <span data-ttu-id="dc885-251">Эти методы позволяют администраторам легко определить сочетание параметров политики, применяемых к пользователю или компьютеру, или к нему.</span><span class="sxs-lookup"><span data-stu-id="dc885-251">These methods allow administrators to determine easily the combination of policy settings that apply to, or will apply to, a user or computer.</span></span> <span data-ttu-id="dc885-252">Это называется результирующим набором политик (RSoP).</span><span class="sxs-lookup"><span data-stu-id="dc885-252">This is known as the Resultant Set of Policy (RSoP).</span></span> <span data-ttu-id="dc885-253">Дополнительные сведения см. [в разделе о поставщике методов WMI RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) и [классах WMI RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dc885-253">For more information, see [About the RSoP WMI Method Provider](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) and [RSoP WMI Classes](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Бюллетеня](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-254"><span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Security](/previous-versions/windows/desktop/secrcw32prov/security-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-255">Извлекает или изменяет параметры безопасности, управляющие владением, аудитом и правами доступа к файлам, каталогам и общим ресурсам.</span><span class="sxs-lookup"><span data-stu-id="dc885-255">Retrieves or changes security settings that control ownership, auditing, and access rights to files, directories, and shares.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span><span class="sxs-lookup"><span data-stu-id="dc885-256"><span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-257">[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) предоставляет функциональные возможности развертывания.</span><span class="sxs-lookup"><span data-stu-id="dc885-257">The [ServerManager.DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) exposes deployment functionality.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Сессии](/previous-versions/windows/desktop/wmipsess/session-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-258"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Session](/previous-versions/windows/desktop/wmipsess/session-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-259">Управляет сетевыми сеансами и подключениями.</span><span class="sxs-lookup"><span data-stu-id="dc885-259">Manages network sessions and connections.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Теневое копирование](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-260"><span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Shadow Copy](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-261">Предоставляет функции управления для теневых копий компонента общих папок.</span><span class="sxs-lookup"><span data-stu-id="dc885-261">Supplies management functions for the Shadow Copies of the Shared Folders feature.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Подготовка экранированной виртуальной машины](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-262"><span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Shielded VM Provisioning](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-263">Поставщик подготовки экранированной виртуальной машины позволяет контроллеру структуры запускать безопасную подготовку экранированной виртуальной машины на узле Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="dc885-263">The Shielded VM Provisioning provider enables a fabric controller to start the secure provisioning of a shielded VM on a Hyper-V host.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Служба подготовки экранированной виртуальной машины](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-264"><span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Shielded VM Provisioning Service](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-265">Поставщик позволяет подготовить экранированную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="dc885-265">The provider enables provisioning of a shielded virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Управление SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-266"><span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[SMB Management](/previous-versions/windows/desktop/smb/smb-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-267">API управления SMB предоставляет классы и методы для управления общими ресурсами и предоставления общего доступа.</span><span class="sxs-lookup"><span data-stu-id="dc885-267">The SMB Management API provides classes and methods to manage shares and share access.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-268"><span id="SNMP"></span><span id="snmp"></span>[СООБЩА](/windows/desktop/WmiSdk/snmp-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-268"><span id="SNMP"></span><span id="snmp"></span>[SNMP](/windows/desktop/WmiSdk/snmp-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-269">Сопоставляет объекты протокола SNMP, определенные в объектах схемы базы данных MIB, с классами.</span><span class="sxs-lookup"><span data-stu-id="dc885-269">Maps Simple Network Management Protocol (SNMP) objects that are defined in Management Information Base (MIB) schema objects to classes.</span></span> <span data-ttu-id="dc885-270">Дополнительные сведения см. [в разделе Настройка среды SNMP WMI](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span><span class="sxs-lookup"><span data-stu-id="dc885-270">For more information, see [Setting up the WMI SNMP Environment](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Ведение журнала инвентаризации программного обеспечения](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-271"><span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Software Inventory Logging](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-272">Поставщик ведения журнала инвентаризации программного обеспечения собирает данные лицензирования о программном обеспечении, установленном на сервере Windows Server, и предоставляет удаленный доступ к данным, чтобы их можно было легко объединить с помощью центра обработки данных.</span><span class="sxs-lookup"><span data-stu-id="dc885-272">The Software Inventory Logging provider collects licensing data about software installed on a Windows Server, and provides remote access to the data so it can be aggregated easily by a datacenter.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Лицензирование программного обеспечения для Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span><span class="sxs-lookup"><span data-stu-id="dc885-273"><span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Software Licensing for Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-274">[Классы лицензирования программного обеспечения](/previous-versions/windows/desktop/sppwmi/software-license-provider-) , используемые для Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dc885-274">[Software Licensing Classes](/previous-versions/windows/desktop/sppwmi/software-license-provider-) used for Windows Vista.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Лицензия на программное обеспечение](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span><span class="sxs-lookup"><span data-stu-id="dc885-275"><span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Software License](/previous-versions/windows/desktop/sppwmi/software-license-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-276">Поставщик лицензирования программного обеспечения извлекает данные лицензирования программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="dc885-276">The Software Licensing provider retrieves software licensing data.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Том хранилища](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-277"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Storage Volume](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-278">Поставщик томов хранилища предоставляет функции управления томами.</span><span class="sxs-lookup"><span data-stu-id="dc885-278">The Storage Volume provider supplies volume management functions.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Реплика хранилища](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-279"><span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Storage Replica](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-280">Поставщик обеспечивает управление репликой хранилища.</span><span class="sxs-lookup"><span data-stu-id="dc885-280">The provider enables management of a storage replica.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Системный реестр](/previous-versions/windows/desktop/regprov/system-registry-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-281"><span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[System Registry](/previous-versions/windows/desktop/regprov/system-registry-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-282">Поставщик системного реестра позволяет приложениям управления извлекать и изменять данные в системном реестре, а также получать уведомления при внесении изменений.</span><span class="sxs-lookup"><span data-stu-id="dc885-282">The System Registry provider enables management applications to retrieve and modify data in the system registry, and receive notifications when changes occur.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Восстановление системы](/windows/desktop/sr/system-restore-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-283"><span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[System Restore](/windows/desktop/sr/system-restore-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-284">Предоставляет классы, которые настраивают и используют функцию восстановления системы.</span><span class="sxs-lookup"><span data-stu-id="dc885-284">Supplies classes that configure and use System Restore functionality.</span></span> <span data-ttu-id="dc885-285">Дополнительные сведения см. в разделе [Настройка восстановления системы](/windows/desktop/sr/configuring-system-restore) и [классы WMI для восстановления системы](/windows/desktop/sr/system-restore-wmi-classes).</span><span class="sxs-lookup"><span data-stu-id="dc885-285">For more information, see [Configuring System Restore](/windows/desktop/sr/configuring-system-restore) and the [System Restore WMI Classes](/windows/desktop/sr/system-restore-wmi-classes).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[доверенный платформенный модуль (TPM)](/windows/desktop/SecProv/trusted-platform-module-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-286"><span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[Trusted Platform Module](/windows/desktop/SecProv/trusted-platform-module-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-287">Предоставляет доступ к данным об устройстве безопасности, представленном экземпляром [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm), который является корнем отношения доверия для системы компьютеров с доверенной платформой Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-287">Provides access to data about a security device, represented by an instance of [**Win32\_TPM**](/windows/desktop/SecProv/win32-tpm), that is the root of trust for a Microsoft Windows trusted platform computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Средство TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-288"><span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-289">Поставщик [средство TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) — это поставщик экземпляров, который создает классы со сведениями о доверительных отношениях между доменами.</span><span class="sxs-lookup"><span data-stu-id="dc885-289">The [Trustmon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) provider is an instance provider that creates classes with information about the trust relationships between domains.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Ведение журнала доступа пользователей](/previous-versions/windows/desktop/ual/user-access-logging)</span><span class="sxs-lookup"><span data-stu-id="dc885-290"><span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[User Access Logging](/previous-versions/windows/desktop/ual/user-access-logging)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-291">Ведение журнала доступа пользователей (UAL) — это общая платформа для ролей Windows Server, сообщающая о соответствующих метриках потребления.</span><span class="sxs-lookup"><span data-stu-id="dc885-291">User Access Logging (UAL) is a common framework for Windows Server roles to report their respective consumption metrics.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[усерпрофилепровидер](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-292"><span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-293">Поставщик [усерпрофилепровидер](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) предоставляет классы, предоставляющие сведения о профиле пользователя в системе Windows, а также о состоянии работоспособности перенаправленной папки пользователя.</span><span class="sxs-lookup"><span data-stu-id="dc885-293">The [UserProfileProvider](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) provider exposes classes that provide information about a user profile on a Windows system, as well as the health status of a redirected user folder.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Управление пользовательской областью](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-294"><span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[User State Management](/previous-versions/windows/desktop/usm/user-state-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-295">Поставщик управления пользовательской среды предоставляет API управления и отчетов для корпоративных сценариев.</span><span class="sxs-lookup"><span data-stu-id="dc885-295">The User State Management provider exposes a management and reporting API for enterprise scenarios.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[Режиме](/windows/desktop/WmiSdk/view-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-296"><span id="View"></span><span id="view"></span><span id="VIEW"></span>[View](/windows/desktop/WmiSdk/view-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-297">Создает новые экземпляры и методы на основе экземпляров других классов.</span><span class="sxs-lookup"><span data-stu-id="dc885-297">Creates new instances and methods based on instances of other classes.</span></span> <span data-ttu-id="dc885-298">На 64-разрядных платформах доступны две версии поставщика представления.</span><span class="sxs-lookup"><span data-stu-id="dc885-298">Two versions of the View provider are available on 64-bit platforms.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[впнклиентпспровидер](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span><span class="sxs-lookup"><span data-stu-id="dc885-299"><span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-300">Поставщик [впнклиентпспровидер](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) предоставляет платформу для автоматизации подключения к клиенту виртуальной частной сети.</span><span class="sxs-lookup"><span data-stu-id="dc885-300">The [VPNClientPSProvider](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) provider exposes a platform for automating connectivity to a virtual private network client.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-301"><span id="WDM"></span><span id="wdm"></span>[ПОТОКА](/windows/desktop/WmiCoreProv/wdm-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-301"><span id="WDM"></span><span id="wdm"></span>[WDM](/windows/desktop/WmiCoreProv/wdm-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-302">Предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют WDM (WDM).</span><span class="sxs-lookup"><span data-stu-id="dc885-302">Provides access to the classes, instances, methods, and events of hardware drivers that conform to the Windows Driver Model (WDM).</span></span>

</dd> <dt>

<span data-ttu-id="dc885-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[вфасЦим](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-303"><span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-304">Поставщик [вфасЦим](/previous-versions/windows/desktop/wfascimprov/network-security-classes) предоставляет функции сетевой безопасности и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="dc885-304">The [WFasCim](/previous-versions/windows/desktop/wfascimprov/network-security-classes) provider exposes network security and filtering features.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[вхклпровидер](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-305"><span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-306">Поставщик [вхклпровидер](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) предоставляет сведения о цифровых подписях для драйверов.</span><span class="sxs-lookup"><span data-stu-id="dc885-306">The [WhqlProvider](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) provider exposes digital signature information about drivers.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-307"><span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-308">Поставщик [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) отображает текущие, локальные и временные метки времени на основе времени в формате UTC в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="dc885-308">The [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) provider exposes the current, local, and UTC-based timestamps on a computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Компоненты доступа к данным Windows (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-309"><span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Windows Data Access Components (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-310">Предоставляет управление WDAC.</span><span class="sxs-lookup"><span data-stu-id="dc885-310">Provides management of WDAC.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Защитник Windows](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-311"><span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Windows Defender](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-312">Поставщик защитника Windows предоставляет функции безопасности защитника Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-312">The Windows Defender provider exposes Windows Defender security features.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[установщик Windows](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-313"><span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[Windows Installer](/previous-versions/windows/desktop/msiprov/windows-installer-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-314">Поставщик установщик Windows, также известный как поставщик MSI, позволяет приложениям получать доступ к информации, собранной из приложений, совместимых с установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="dc885-314">The Windows Installer provider, also known as the MSI provider allows applications to access information collected from Windows Installer compliant applications.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Активация продуктов Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-315"><span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Windows Product Activation](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-316">Поставщик активации Windows (WPA) — это технология борьбы с пиратством, предназначенная для уменьшения случайного копирования программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="dc885-316">The Windows Product Activation (WPA) provider is an anti-piracy technology aimed at reducing the casual copying of software.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[диспетчер сервера Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-317"><span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[Windows Server Manager](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-318">Поставщик обеспечивает доступ к конфигурации, управляемой приложением диспетчер сервера, и управление ею.</span><span class="sxs-lookup"><span data-stu-id="dc885-318">The provider enables access to and management of the configuration controlled by the Server Manager application.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Управление хранилищем Windows Server (Мсфтстргман)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-319"><span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Windows Server Storage Management (MsftStrgMan)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-320">Поставщик Мсфтстргман обеспечивает управление системами хранения данных в продуктах Windows Server.</span><span class="sxs-lookup"><span data-stu-id="dc885-320">The MsftStrgMan provider provides management for storage systems on Windows Server products.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Управление хранилищем Windows (Стргмгмт)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-321"><span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Windows Storage Management (StrgMgmt)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-322">Поставщик Стргмгмт можно использовать для управления широким спектром конфигураций хранилища, от планшетов до внешних массивов хранения данных на серверах.</span><span class="sxs-lookup"><span data-stu-id="dc885-322">The StrgMgmt provider can be used to manage a wide range of storage configurations, from tablets to external storage arrays on servers.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Средство оценки системы Windows](/windows/desktop/WinSAT/winsat-mof-classes)</span><span class="sxs-lookup"><span data-stu-id="dc885-323"><span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Windows System Assessment Tool](/windows/desktop/WinSAT/winsat-mof-classes)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-324">Средство Windows System оценке (WinSAT) предоставляет ряд классов, оценивающих характеристики и возможности производительности компьютера.</span><span class="sxs-lookup"><span data-stu-id="dc885-324">The Windows System Assessment Tool (WinSAT) exposes a number of classes that assesses the performance characteristics and capabilities of a computer.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Ядро WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span><span class="sxs-lookup"><span data-stu-id="dc885-325"><span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[WMI Core](/windows/desktop/WmiCoreProv/wmi-core-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-326">Поставщик ядра WMI определяет классы, составляющие основные функциональные возможности WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-326">The WMI Core provider defines classes that compose the core functionality of WMI.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[MSFT \_ провидерсубсистем](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span><span class="sxs-lookup"><span data-stu-id="dc885-327"><span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-328">Поставщик [MSFT \_ провидерсубсистем](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) поддерживает поставщиков.</span><span class="sxs-lookup"><span data-stu-id="dc885-328">The [Msft\_ProviderSubSystem](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) provider supports providers.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Производительность \_ Win32](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dc885-329"><span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Win32\_Perf](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-330">Абстрактный класс [**\_ производительности Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) является базовым классом для классов счетчиков производительности [**Win32 \_ перфравдата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) и [**Win32 \_ перфформаттеддата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span><span class="sxs-lookup"><span data-stu-id="dc885-330">The [**Win32\_Perf**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) abstract class is the base class for the performance counter classes [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) and [**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov).</span></span> <span data-ttu-id="dc885-331">Он определяет требуемые свойства timestamp и Frequency, используемые в алгоритмах CounterType для классов счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="dc885-331">It defines the required timestamp and frequency properties used in the CounterType algorithms for the performance counter classes.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_Перфформаттеддата Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dc885-332"><span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**Win32\_PerfFormattedData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-333">Абстрактный базовый класс для предварительно установленных и вычисляемых классов данных.</span><span class="sxs-lookup"><span data-stu-id="dc885-333">An abstract base class for the pre-installed, calculated data classes.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_Перфравдата Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span><span class="sxs-lookup"><span data-stu-id="dc885-334"><span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-335">Класс счетчика производительности [**Win32 \_ перфравдата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) является абстрактным базовым классом для всех конкретных классов необработанных счетчиков производительности.</span><span class="sxs-lookup"><span data-stu-id="dc885-335">The performance counter class [**Win32\_PerfRawData**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) is the abstract base class for all concrete raw performance counter classes.</span></span> <span data-ttu-id="dc885-336">Для отображения в системном мониторе классы счетчиков производительности должны быть добавлены в \\ пространство имен root CIMv2 и быть производными от **Win32 \_ перфравдата**.</span><span class="sxs-lookup"><span data-stu-id="dc885-336">To appear in System Monitor, performance counter classes must be added to the "Root\\CIMv2" namespace and derived from **Win32\_PerfRawData**.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[вмиперфкласс](/windows/desktop/WmiSdk/wmiperfclass-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-337"><span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[WMIPerfClass](/windows/desktop/WmiSdk/wmiperfclass-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-338">Создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI.</span><span class="sxs-lookup"><span data-stu-id="dc885-338">Creates the WMI [Performance Counter Classes](/windows/desktop/CIMWin32Prov/performance-counter-classes).</span></span> <span data-ttu-id="dc885-339">Данные в эти классы производительности динамически передаются поставщиком Вмиперфинст.</span><span class="sxs-lookup"><span data-stu-id="dc885-339">Data is dynamically supplied to these performance classes by the WMIPerfInst provider.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[вмиперфинст](/windows/desktop/WmiSdk/wmiperfinst-provider)</span><span class="sxs-lookup"><span data-stu-id="dc885-340"><span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[WmiPerfInst](/windows/desktop/WmiSdk/wmiperfinst-provider)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-341">Динамически предоставляет необработанные и отформатированные данные счетчиков производительности из определений [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) .</span><span class="sxs-lookup"><span data-stu-id="dc885-341">Supplies raw and formatted performance counter data dynamically from [Performance Counter Class](/windows/desktop/CIMWin32Prov/performance-counter-classes) definitions.</span></span>

</dd> <dt>

<span data-ttu-id="dc885-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Рабочие папки](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span><span class="sxs-lookup"><span data-stu-id="dc885-342"><span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Work Folders](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)</span></span>
</dt> <dd>

<span data-ttu-id="dc885-343">Рабочие папки используются для синхронизации файлов с несколькими компьютерами и мобильными устройствами.</span><span class="sxs-lookup"><span data-stu-id="dc885-343">Work Folders is used to synchronize files with multiple PCs and mobile devices.</span></span>

</dd> </dl>

 

 
