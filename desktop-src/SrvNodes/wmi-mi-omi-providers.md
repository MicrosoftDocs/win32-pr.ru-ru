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
# <a name="wmimiomi-providers"></a>Поставщики WMI, MI и OMI

Инфраструктура управления Windows (WMI), Инструментарий управления (MI) и открытая инфраструктура управления (OMI) используют файлы формата MOF для описания информации, доступной через соответствующих поставщиков.

<dl> <dt>

<span id="Active_Directory"></span><span id="active_directory"></span><span id="ACTIVE_DIRECTORY"></span>[Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider)
</dt> <dd>

Поставщик Active Directory, также известный как поставщик служб каталогов (DS), сопоставляет объекты Active Directory с WMI. С помощью доступа к пространству имен LDAP в WMI можно ссылаться на объект или сделать его псевдонимом в Active Directory.

</dd> <dt>

<span id="Application_Inventory"></span><span id="application_inventory"></span><span id="APPLICATION_INVENTORY"></span>[Инвентаризация приложений](/previous-versions/windows/desktop/appdevinvprov/applicationanddeviceinventory-portal)
</dt> <dd>

Классы WMI для инвентаризации приложений позволяют обнаруживать установленные приложения Win32 и приложения Магазина Windows в системе Windows.

</dd> <dt>

<span id="Application_Proxy"></span><span id="application_proxy"></span><span id="APPLICATION_PROXY"></span>[Прокси приложения](/previous-versions/windows/desktop/appproxypsprov/application-proxy-wmi-provider-portal)
</dt> <dd>

Поставщик WMI прокси приложения позволяет разработчикам получить доступ к службе прокси веб-приложения, чтобы администраторы могли публиковать приложения для внешнего доступа. Прокси веб-приложения — это обратный прокси для службы федерации Active Directory (AD FS) (AD FS).

</dd> <dt>

<span id="BitLocker_Drive_Encryption__BDE_"></span><span id="bitlocker_drive_encryption__bde_"></span><span id="BITLOCKER_DRIVE_ENCRYPTION__BDE_"></span>[Шифрование диска BitLocker (BDE)](/windows/desktop/SecProv/bitlocker-drive-encryption-provider)
</dt> <dd>

Обеспечивает настройку и управление для области хранения на жестком диске, представленной экземпляром [**Win32 \_ енкриптаблеволуме**](/windows/desktop/SecProv/win32-encryptablevolume), который можно защитить с помощью шифрования.

</dd> <dt>

<span id="BITS"></span><span id="bits"></span>[ЧИСЛА](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dd>

Фоновая интеллектуальная служба передачи (BITS) Compact Server с удаленным управлением BITS позволяет администраторам или контроллерам, прошедшим проверку подлинности, создавать, изменять и администрировать задания передачи BITS удаленно без использования службы службы IIS (IIS).

</dd> <dt>

<span id="BizTalk"></span><span id="biztalk"></span><span id="BIZTALK"></span>[Реквизит](https://msdn.microsoft.com/library/ms941491.aspx)
</dt> <dd>

Предоставляет доступ к объектам администрирования BizTalk, представленным классами WMI.

</dd> <dt>

<span id="Boot_Configuration_Data"></span><span id="boot_configuration_data"></span><span id="BOOT_CONFIGURATION_DATA"></span>[данные конфигурации загрузки](/previous-versions/windows/desktop/bcd/boot-configuration-data-portal)
</dt> <dd>

Поставщик данные конфигурации загрузки (BCD) предоставляет хранилище, которое используется для описания приложений загрузки и параметров приложения загрузки.

</dd> <dt>

<span id="Boot_Event_Collector"></span><span id="boot_event_collector"></span><span id="BOOT_EVENT_COLLECTOR"></span>[Сборщик событий загрузки](/windows/desktop/BEvtColProv/boot-event-collector-wmi-provider-portal)
</dt> <dd>

Поставщик WMI сборщика событий загрузки предоставляет доступ к сведениям о подключении и конфигурации для функции сбора событий установки и загрузки в Windows Server.

</dd> <dt>

<span id="CIMWin32__Win32__Power_Management_Events"></span><span id="cimwin32__win32__power_management_events"></span><span id="CIMWIN32__WIN32__POWER_MANAGEMENT_EVENTS"></span>[CIMWin32, Win32, события управления питанием](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers)
</dt> <dd>

Поставщики CIMWin32 поддерживают классы, реализованные в CimWin32.dll, и состоят из основных классов CIM, реализации этих классов в Win32 и событий управления питанием.

</dd> <dt>

<span id="CIMWin32a"></span><span id="cimwin32a"></span><span id="CIMWIN32A"></span>[CIMWin32a](/previous-versions/windows/desktop/cimwin32a/cimwin32a-provider-classes)
</dt> <dd>

Поставщик CIMWin32a расширяет классы, доступные в [CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers).

</dd> <dt>

<span id="DcbQosCim"></span><span id="dcbqoscim"></span><span id="DCBQOSCIM"></span>[дкбкосЦим](/previous-versions/windows/desktop/dcbwmiprov/dcb-qos)
</dt> <dd>

Поставщик ДкбкосЦим поддерживает классы, описывающие данные параметров качества обслуживания сети, данные параметров управления и данные о параметрах класса трафика.

</dd> <dt>

<span id="Distributed_File_System__DFS_"></span><span id="distributed_file_system__dfs_"></span><span id="DISTRIBUTED_FILE_SYSTEM__DFS_"></span>[Распределенная файловая система (DFS)](/previous-versions/windows/desktop/wmipdfs/dfs-provider)
</dt> <dd>

Поставщик DFS предоставляет функции для работы с скриптами DFS через WMI.

</dd> <dt>

<span id="Distributed_File_System_Replication__DFSR_"></span><span id="distributed_file_system_replication__dfsr_"></span><span id="DISTRIBUTED_FILE_SYSTEM_REPLICATION__DFSR_"></span>[Репликация распределенная файловая система (DFSR)](/previous-versions/windows/desktop/dfsr/distributed-file-system-replication--dfsr-)
</dt> <dd>

Создает средства для настройки и мониторинга службы [Распределенная файловая система (DFS)](/previous-versions/windows/desktop/dfs/distributed-file-system) . Дополнительные сведения см. в разделе [классы WMI DFSR](/previous-versions/windows/desktop/dfsr/dfsr-wmi-classes).

</dd> <dt>

<span id="Dfsncimprov"></span><span id="dfsncimprov"></span><span id="DFSNCIMPROV"></span>[дфснЦимпров](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes)
</dt> <dd>

Поставщик [дфснЦимпров](/previous-versions/windows/desktop/dfsncimprov/dfs-namespace-classes) поддерживает классы, реализующие доступ к пространству имен DFS.

</dd> <dt>

<span id="DhcpServerPSProvider"></span><span id="dhcpserverpsprovider"></span><span id="DHCPSERVERPSPROVIDER"></span>[дхкпсерверпспровидер](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes)
</dt> <dd>

Поставщик [дхкпсерверпспровидер](/previous-versions/windows/desktop/dhcpserverpsprov/dhcp-classes) поддерживает классы, взаимодействующие с DHCP-сервером.

</dd> <dt>

<span id="Disk_Quota"></span><span id="disk_quota"></span><span id="DISK_QUOTA"></span>[Квота диска](/previous-versions/windows/desktop/wmipdskq/disk-quota-provider)
</dt> <dd>

Поставщик дисковых квот Windows позволяет администраторам управлять объемом данных, которые каждый пользователь сохраняет в файловой системе NTFS.

</dd> <dt>

<span id="Distributed_Transaction_Coordinator__DTC_"></span><span id="distributed_transaction_coordinator__dtc_"></span><span id="DISTRIBUTED_TRANSACTION_COORDINATOR__DTC_"></span>[Координатор распределенных транзакций (DTC)](/previous-versions/windows/desktop/msdtcwmi/distributed-transaction-coordinator-wmi-provider-portal)
</dt> <dd>

Поставщик DTC обеспечивает управление DTC.

</dd> <dt>

<span id="DNS"></span><span id="dns"></span>[СЕРВЕРЕ](/windows/desktop/DNS/dns-wmi-provider)
</dt> <dd>

Позволяет администраторам и программистам настраивать записи ресурсов (RR) системы доменных имен (DNS) и DNS-серверы с помощью WMI.

</dd> <dt>

<span id="Dnsclientcim_Provider_Classes"></span><span id="dnsclientcim_provider_classes"></span><span id="DNSCLIENTCIM_PROVIDER_CLASSES"></span>[Классы поставщиков днсклиентЦим](/previous-versions/windows/desktop/dnsclientcimprov/dns-client-classes)
</dt> <dd>

Поставщик ДнсклиентЦим поддерживает классы, взаимодействующие с клиентом службы доменных имен (DNS).

</dd> <dt>

<span id="DnsClientPSProvider"></span><span id="dnsclientpsprovider"></span><span id="DNSCLIENTPSPROVIDER"></span>[днсклиентпспровидер](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes)
</dt> <dd>

Поставщик [днсклиентпспровидер](/previous-versions/windows/desktop/dnsclientpsprov/dns-nrpt-classes) поддерживает классы WMI, взаимодействующие с DNS-клиентом.

</dd> <dt>

<span id="DnsServerPSProvider"></span><span id="dnsserverpsprovider"></span><span id="DNSSERVERPSPROVIDER"></span>[днссерверпспровидер](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes)
</dt> <dd>

Поставщик [днссерверпспровидер](/previous-versions/windows/desktop/dnsserverpsprov/dns-server-classes) поддерживает классы WMI, взаимодействующие с DNS-сервером.

</dd> <dt>

<span id="Event_Log"></span><span id="event_log"></span><span id="EVENT_LOG"></span>[Журнал событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider)
</dt> <dd>

Поставщик [журнала событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) предоставляет доступ к данным из службы журнала событий и уведомлению о событиях.

</dd> <dt>

<span id="Event_Tracing_Management"></span><span id="event_tracing_management"></span><span id="EVENT_TRACING_MANAGEMENT"></span>[Управление трассировкой событий](/previous-versions/windows/desktop/etwmgmt/event-tracing-management-wmi-provider-portal)
</dt> <dd>

Поставщик управления трассировкой событий предоставляет доступ к средствам трассировки событий для конфигурации сеансов авторегистратора ETW и событиям трассировки.

</dd> <dt>

<span id="Failover_Cluster-Aware_Updating"></span><span id="failover_cluster-aware_updating"></span><span id="FAILOVER_CLUSTER-AWARE_UPDATING"></span>[Обновление Cluster-Aware отработки отказа](/previous-versions/windows/desktop/cauwmiv2/failover-cluster-aware-patching-mi-provider-portal)
</dt> <dd>

Поставщик отработки отказа Cluster-Aware обновления (CAU) поддерживает координацию и управление для CAU.

</dd> <dt>

<span id="Failover_Clustering_Hyper-V"></span><span id="failover_clustering_hyper-v"></span><span id="FAILOVER_CLUSTERING_HYPER-V"></span>[Отказоустойчивая кластеризация Hyper-V](/previous-versions/windows/desktop/clushyperv/failover-clustering-hyper-v-wmi-provider-portal)
</dt> <dd>

Поставщик отказоустойчивой кластеризации Hyper-V обеспечивает управление и создание отчетов Hyper-V в среде кластеризации.

</dd> <dt>

<span id="Failover_Clustering_Storage_QoS"></span><span id="failover_clustering_storage_qos"></span><span id="FAILOVER_CLUSTERING_STORAGE_QOS"></span>[Качество обслуживания хранилища отказоустойчивой кластеризации](/previous-versions/windows/desktop/clusstorageqosprov/failover-clustering-storage-qos-mi-provider-portal)
</dt> <dd>

Поставщик качества обслуживания хранилища отказоустойчивой кластеризации обеспечивает управление и создание отчетов по политикам качества обслуживания для кластерного хранилища.

</dd> <dt>

<span id="Failover_Cluster_V1_Provider"></span><span id="failover_cluster_v1_provider"></span><span id="FAILOVER_CLUSTER_V1_PROVIDER"></span>[Поставщик отказоустойчивого кластера v1](/previous-versions/windows/desktop/cluswmi/failover-cluster-wmi-provider-portal)
</dt> <dd>

Поставщик отказоустойчивого кластера версии 1 обеспечивает Управление отказоустойчивым кластером.

</dd> <dt>

<span id="Failover_Cluster_V1_Extensions"></span><span id="failover_cluster_v1_extensions"></span><span id="FAILOVER_CLUSTER_V1_EXTENSIONS"></span>[Расширения отказоустойчивого кластера версии 1](/previous-versions/windows/desktop/cluswmiext/failover-cluster-wmi-provider-extensions-portal)
</dt> <dd>

Поставщик расширений отказоустойчивого кластера обеспечивает дополнительное Управление отказоустойчивым кластером.

</dd> <dt>

<span id="Gateway_Health_Monitor"></span><span id="gateway_health_monitor"></span><span id="GATEWAY_HEALTH_MONITOR"></span>[Монитор работоспособности шлюза](/previous-versions/windows/desktop/gatewayhealthmonprov/gateway-health-monitor-wmi-provider-portal)
</dt> <dd>

Поставщик монитора работоспособности шлюза управляет событиями и данными мониторинга работоспособности шлюза.

</dd> <dt>

<span id="Group_Policy_API"></span><span id="group_policy_api"></span><span id="GROUP_POLICY_API"></span>[групповая политика API](/previous-versions/windows/desktop/Policy/group-policy-start-page)
</dt> <dd>

Поставщик групповая политика обеспечивает администрирование на основе политик с помощью служб каталогов Microsoft Active Directory (AD).

</dd> <dt>

<span id="Host_Guardian_Service"></span><span id="host_guardian_service"></span><span id="HOST_GUARDIAN_SERVICE"></span>[Служба защиты узла](/previous-versions/windows/desktop/hgsclientwmi/hoster-guardian-service-wmi-provider-portal)
</dt> <dd>

Поставщик службы защиты узла обеспечивает управление службой защиты узла для экранированных виртуальных машин.

</dd> <dt>

<span id="Hyper-V"></span><span id="hyper-v"></span><span id="HYPER-V"></span>[Hyper-V](/previous-versions/windows/desktop/virtual/windows-virtualization-portal)
</dt> <dd>

Поставщик Hyper-V позволяет управлять и извлекать сведения о виртуальных машинах.

</dd> <dt>

<span id="Hyper-V__V2_"></span><span id="hyper-v__v2_"></span><span id="HYPER-V__V2_"></span>[Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal)
</dt> <dd>

Поставщик Hyper-V (v2) расширяет возможности поставщика [Hyper-v](/previous-versions/windows/desktop/virtual/windows-virtualization-portal) .

</dd> <dt>

<span id="Internet_Information_Services__IIS_"></span><span id="internet_information_services__iis_"></span><span id="INTERNET_INFORMATION_SERVICES__IIS_"></span>[Службы IIS (IIS)](/previous-versions/iis/6.0-sdk/ms525309(v=vs.90))
</dt> <dd>

Предоставляет интерфейсы программирования, которые можно использовать для запроса и настройки метабазы IIS.

</dd> <dt>

<span id="Internet_Protocol_Address_Management__IPAM__Server"></span><span id="internet_protocol_address_management__ipam__server"></span><span id="INTERNET_PROTOCOL_ADDRESS_MANAGEMENT__IPAM__SERVER"></span>[Сервер управления IP-адресами (IPAM)](/previous-versions/windows/desktop/ipamserverpsprov/internet-protocol-address-management-server-wmi-provider-portal)
</dt> <dd>

Поставщик IPAM-сервера позволяет разработчикам управлять IPAM с помощью WMI.

</dd> <dt>

<span id="IP_Route_Provider"></span><span id="ip_route_provider"></span><span id="IP_ROUTE_PROVIDER"></span>[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider)
</dt> <dd>

Предустановленный поставщик IP-маршрутов предоставляет сведения о маршрутизации сети IPV4, включая (но не ограничиваясь) сведения, доступные с помощью команды **route print** .

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface__IPMI_"></span><span id="intelligent_platform_management_interface__ipmi_"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE__IPMI_"></span>[Интеллектуальный интерфейс управления платформой (IPMI)](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)
</dt> <dd>

Предоставляет данные IPMI от операций контроллера управления основной платой (BMC).

</dd> <dt>

<span id="iSCSI_Target_Server"></span><span id="iscsi_target_server"></span><span id="ISCSI_TARGET_SERVER"></span>[Сервер цели iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)
</dt> <dd>

Поставщик сервера цели iSCSI поддерживает интерфейс WMI для управления сервером Microsoft iSCSI Target Server, например создание виртуальных дисков и их представление клиенту.

</dd> <dt>

<span id="Job_Object"></span><span id="job_object"></span><span id="JOB_OBJECT"></span>[Объект задания](/previous-versions/windows/desktop/wmipjobobjprov/job-object-provider)
</dt> <dd>

Поставщик объектов задания поддерживает доступ к данным об именованных объектах заданий ядра.

</dd> <dt>

<span id="Kernel_Trace"></span><span id="kernel_trace"></span><span id="KERNEL_TRACE"></span>[Трассировка ядра](/previous-versions/windows/desktop/krnlprov/kernel-trace-provider)
</dt> <dd>

Предварительно установленный поставщик событий трассировки ядра позволяет просматривать события трассировки ядра при создании процесса, завершении процесса, создании потока, завершении потока и загрузке модуля.

</dd> <dt>

<span id="Live_Communications_Server_2003"></span><span id="live_communications_server_2003"></span><span id="LIVE_COMMUNICATIONS_SERVER_2003"></span>[Live Communications Server 2003](/previous-versions/office/developer/office-2003/cc165126(v=office.11))
</dt> <dd>

Предоставляет классы для создания, регистрации, настройки и управления приложениями пользовательского протокола SIP с помощью [Live Communications Server 2003](/previous-versions/office/aa194012(v=office.11)).

</dd> <dt>

<span id="Management_Tools_Registry"></span><span id="management_tools_registry"></span><span id="MANAGEMENT_TOOLS_REGISTRY"></span>[Реестр средств управления](/previous-versions/windows/desktop/mtregprov/managementtools-registry-wmi-provider-portal)
</dt> <dd>

Поставщик реестра средств управления предоставляет удаленный доступ к реестру.

</dd> <dt>

<span id="Management_Tools_Task_Manager"></span><span id="management_tools_task_manager"></span><span id="MANAGEMENT_TOOLS_TASK_MANAGER"></span>[Диспетчер задач средств управления](/previous-versions/windows/desktop/mttmprov/management-tools-task-manager-wmi-provider-portal)
</dt> <dd>

Поставщик диспетчера задач средств управления предоставляет доступ к данным диспетчера задач и управление ими.

</dd> <dt>

<span id="MDM_Application"></span><span id="mdm_application"></span><span id="MDM_APPLICATION"></span>[Приложение MDM](/previous-versions/windows/desktop/mdmappprov/mobile-device-management-application-provider-portal)
</dt> <dd>

Поставщик приложений управления мобильными устройствами (MDM) управляет приложениями на устройствах, подписанных на службу MDM.

</dd> <dt>

<span id="MDM_Bridge"></span><span id="mdm_bridge"></span><span id="MDM_BRIDGE"></span>[Мост MDM](/windows/desktop/DMWmiBridgeProv/mdm-bridge-wmi-provider-portal)
</dt> <dd>

Поставщик моста MDM позволяет управлять сетевым мостом с помощью MDM.

</dd> <dt>

<span id="MDM_Settings"></span><span id="mdm_settings"></span><span id="MDM_SETTINGS"></span>[Параметры MDM](/previous-versions/windows/desktop/mdmsettingsprov/mobile-device-management-settings-provider-portal)
</dt> <dd>

Поставщик параметров MDM позволяет управлять параметрами на устройствах, зарегистрированных в службе MDM.

</dd> <dt>

<span id="MSFT_PCSVDevice"></span><span id="msft_pcsvdevice"></span><span id="MSFT_PCSVDEVICE"></span>[MSFT \_ пксвдевице](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes)
</dt> <dd>

Поставщик [MSFT \_ пксвдевице](/previous-versions/windows/desktop/pcsvdeviceprov/device-management-classes) предоставляет класс, определяющий класс представления для физической компьютерной системы.

</dd> <dt>

<span id="MsNetImPlatform"></span><span id="msnetimplatform"></span><span id="MSNETIMPLATFORM"></span>[мснетимплатформ](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes)
</dt> <dd>

В разделе Поставщик [мснетимплатформ](/previous-versions/windows/desktop/ndisimplatcimprov/lbfo-classes) содержатся справочные сведения о классах поставщиков мснетимплатформ, реализованных в NdisIMPlatCim.dll.

</dd> <dt>

<span id="NetAdapterCim"></span><span id="netadaptercim"></span><span id="NETADAPTERCIM"></span>[нетадаптерЦим](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes)
</dt> <dd>

Поставщик [нетадаптерЦим](/previous-versions/windows/desktop/netadaptercimprov/network-adapter-classes) поддерживает классы, обращающиеся к сетевым адаптерам.

</dd> <dt>

<span id="NetDaCim"></span><span id="netdacim"></span><span id="NETDACIM"></span>[нетдаЦим](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes)
</dt> <dd>

В этом разделе содержатся справочные сведения о классах поставщиков [нетдаЦим](/previous-versions/windows/desktop/netdacimprov/direct-access-client-components-classes) .

</dd> <dt>

<span id="NetNcCim"></span><span id="netnccim"></span><span id="NETNCCIM"></span>[нетнкЦим](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status)
</dt> <dd>

Содержит справочную информацию о классах поставщика [нетнкЦим](/previous-versions/windows/desktop/netnccimprov/network-connectivity-status) .

</dd> <dt>

<span id="NetPeerDist"></span><span id="netpeerdist"></span><span id="NETPEERDIST"></span>[нетпирдист](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache)
</dt> <dd>

Поставщик [нетпирдист](/previous-versions/windows/desktop/netpeerdistcimprov/branch-cache) поддерживает классы, взаимодействующие с инфраструктурой кэша филиала.

</dd> <dt>

<span id="NetQosCim"></span><span id="netqoscim"></span><span id="NETQOSCIM"></span>[неткосЦим](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes)
</dt> <dd>

Поставщик [неткосЦим](/previous-versions/windows/desktop/qoswmiprov/net-qos-classes) предоставляет данные для данных о параметрах качества обслуживания сети (QoS) и качества обслуживания.

</dd> <dt>

<span id="NetSwitchTeam"></span><span id="netswitchteam"></span><span id="NETSWITCHTEAM"></span>[нетсвитчтеам](/previous-versions/windows/desktop/netswitchteamprov/network-switch-team-classes)
</dt> <dd>

В этом разделе содержатся справочные сведения о классах поставщиков Нетсвитчтеам, объявленных в Нетсвитчтеам. mof и реализованных в NetSwitchTeamCim.dll.

</dd> <dt>

<span id="NetTCPIP"></span><span id="nettcpip"></span><span id="NETTCPIP"></span>[нетткпип](/previous-versions/windows/desktop/nettcpipprov/net-tcpip-classes)
</dt> <dd>

Поставщик Нетткпип поддерживает классы, взаимодействующие с подключениями TCPIP.

</dd> <dt>

<span id="NetTtCim"></span><span id="netttcim"></span><span id="NETTTCIM"></span>[нетттЦим](/previous-versions/windows/desktop/netttcimprov/network-transition-classes)
</dt> <dd>

В этом разделе содержатся справочные сведения о классах поставщиков НетттЦим, определенных в НетттЦим. mof и реализованных в NetTtCim.dll.

</dd> <dt>

<span id="NetWNV"></span><span id="netwnv"></span><span id="NETWNV"></span>[нетвнв](/previous-versions/windows/desktop/netwnvprov/net-virtualization-classes)
</dt> <dd>

Поставщик Нетвнв поддерживает классы, взаимодействующие с технологиями виртуализации сети.

</dd> <dt>

<span id="Network_Access_Protection"></span><span id="network_access_protection"></span><span id="NETWORK_ACCESS_PROTECTION"></span>[Защита доступа к сети](/previous-versions/windows/desktop/napprov/network-access-protection-wmi-provider-portal)
</dt> <dd>

Поставщик защиты доступа к сети предоставляет платформу для защищенного доступа к частным сетям.

</dd> <dt>

<span id="Network_Load_Balancing"></span><span id="network_load_balancing"></span><span id="NETWORK_LOAD_BALANCING"></span>[Балансировка сетевой нагрузки](/previous-versions/windows/desktop/wlbsprov/network-load-balancing-provider-portal)
</dt> <dd>

Поставщик балансировки сетевой нагрузки (NLB) обеспечивает управление кластером NLB.

</dd> <dt>

<span id="NetworkController_Server"></span><span id="networkcontroller_server"></span><span id="NETWORKCONTROLLER_SERVER"></span>[Сервер Нетворкконтроллер](/previous-versions/windows/desktop/ncserverpsprov/networkcontroller-server-wmi-provider-portal)
</dt> <dd>

Поставщик обеспечивает управление сервером сетевого контроллера.

</dd> <dt>

<span id="NFS"></span><span id="nfs"></span>[NFS](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)
</dt> <dd>

Поставщик NFS позволяет создавать средства и сценарии для настройки и мониторинга сетевой файловой системы Windows.

</dd> <dt>

<span id="Ping"></span><span id="ping"></span><span id="PING"></span>[Проверок](/previous-versions/windows/desktop/wmipicmp/ping-provider)
</dt> <dd>

Поставщик проверки связи предоставляет доступ к сведениям о состоянии, предоставленным стандартной командой ping.

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>[Политик](/previous-versions/windows/desktop/policmanprov/policy-provider)
</dt> <dd>

Предоставляет расширения для групповой политики и позволяет выполнять уточнения в приложении политики.

</dd> <dt>

<span id="Power_Meter"></span><span id="power_meter"></span><span id="POWER_METER"></span>[Индикатор питания](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-)
</dt> <dd>

Поставщик счетчиков питания поддерживает интерфейс измерения питания и бюджетирования (ПМБ). Эти классы являются основным интерфейсом для запроса информации о Power измерителя из базовых показателей питания в системе.

</dd> <dt>

<span id="Power_Policy"></span><span id="power_policy"></span><span id="POWER_POLICY"></span>[Политика питания](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-)
</dt> <dd>

Поставщик политики управления питанием предоставляет классы, позволяющие удаленно управлять всей инфраструктурой политики управления питанием.

</dd> <dt>

<span id="RAMgmtPSProvider"></span><span id="ramgmtpsprovider"></span><span id="RAMGMTPSPROVIDER"></span>[рамгмтпспровидер](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management)
</dt> <dd>

Поставщик [рамгмтпспровидер](/previous-versions/windows/desktop/ramgmtpsprov/remote-access-management) предоставляет классы для управления удаленным доступом.

</dd> <dt>

<span id="RAServerPSProvider"></span><span id="raserverpsprovider"></span><span id="RASERVERPSPROVIDER"></span>[расерверпспровидер](/previous-versions/windows/desktop/raserverpsprov/remote-access-server)
</dt> <dd>

Поставщик [расерверпспровидер](/previous-versions/windows/desktop/raserverpsprov/remote-access-server) предоставляет классы для управления сервером удаленного доступа.

</dd> <dt>

<span id="ReliabilityMetricsProvider"></span><span id="reliabilitymetricsprovider"></span><span id="RELIABILITYMETRICSPROVIDER"></span>[релиабилитиметрикспровидер](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes)
</dt> <dd>

Поставщик [релиабилитиметрикспровидер](/previous-versions/windows/desktop/racwmiprov/reliabilitymetricsprovider-provider-classes) предоставляет метрики надежности систем и журнала событий Windows.

</dd> <dt>

<span id="Remote_Desktop_Services"></span><span id="remote_desktop_services"></span><span id="REMOTE_DESKTOP_SERVICES"></span>[службы удаленных рабочих столов](/windows/desktop/TermServ/terminal-services-wmi-provider)
</dt> <dd>

Обеспечивает единообразное администрирование сервера в среде службы удаленных рабочих столов.

</dd> <dt>

<span id="Reporting_Services"></span><span id="reporting_services"></span><span id="REPORTING_SERVICES"></span>[Reporting Services](https://msdn.microsoft.com/library/Aa226200.aspx)
</dt> <dd>

Определяет классы, позволяющие создавать скрипты и код для изменения параметров сервера отчетов и диспетчер отчетов.

</dd> <dt>

<span id="Resultant_Set_of_Policy__RSoP_"></span><span id="resultant_set_of_policy__rsop_"></span><span id="RESULTANT_SET_OF_POLICY__RSOP_"></span>[Результирующий набор политик (RSoP)](/previous-versions/windows/desktop/Policy/reporting-group-policy)
</dt> <dd>

Предоставляет методы для планирования и отладки параметров политики в ситуации "что если". Эти методы позволяют администраторам легко определить сочетание параметров политики, применяемых к пользователю или компьютеру, или к нему. Это называется результирующим набором политик (RSoP). Дополнительные сведения см. [в разделе о поставщике методов WMI RSoP](/previous-versions/windows/desktop/Policy/about-the-rsop-wmi-method-provider) и [классах WMI RSoP](/previous-versions/windows/desktop/Policy/rsop-wmi-classes).

</dd> <dt>

<span id="Security"></span><span id="security"></span><span id="SECURITY"></span>[Бюллетеня](/previous-versions/windows/desktop/secrcw32prov/security-provider)
</dt> <dd>

Извлекает или изменяет параметры безопасности, управляющие владением, аудитом и правами доступа к файлам, каталогам и общим ресурсам.

</dd> <dt>

<span id="ServerManager.DeploymentProvider"></span><span id="servermanager.deploymentprovider"></span><span id="SERVERMANAGER.DEPLOYMENTPROVIDER"></span>[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment)
</dt> <dd>

[ServerManager. DeploymentProvider](/previous-versions/windows/desktop/srvmgrdeployprov/server-manager-deployment) предоставляет функциональные возможности развертывания.

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[Сессии](/previous-versions/windows/desktop/wmipsess/session-provider)
</dt> <dd>

Управляет сетевыми сеансами и подключениями.

</dd> <dt>

<span id="Shadow_Copy"></span><span id="shadow_copy"></span><span id="SHADOW_COPY"></span>[Теневое копирование](/previous-versions/windows/desktop/vsswmi/shadow-copy-provider)
</dt> <dd>

Предоставляет функции управления для теневых копий компонента общих папок.

</dd> <dt>

<span id="Shielded_VM_Provisioning"></span><span id="shielded_vm_provisioning"></span><span id="SHIELDED_VM_PROVISIONING"></span>[Подготовка экранированной виртуальной машины](/previous-versions/windows/desktop/mspsprov/shielded-vm-provisioning-wmi-provider-portal)
</dt> <dd>

Поставщик подготовки экранированной виртуальной машины позволяет контроллеру структуры запускать безопасную подготовку экранированной виртуальной машины на узле Hyper-V.

</dd> <dt>

<span id="Shielded_VM_Provisioning_Service"></span><span id="shielded_vm_provisioning_service"></span><span id="SHIELDED_VM_PROVISIONING_SERVICE"></span>[Служба подготовки экранированной виртуальной машины](/previous-versions/windows/desktop/mspsserviceprov/shielded-vm-provisioning-service-wmi-provider-portal)
</dt> <dd>

Поставщик позволяет подготовить экранированную виртуальную машину.

</dd> <dt>

<span id="SMB_Management"></span><span id="smb_management"></span><span id="SMB_MANAGEMENT"></span>[Управление SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)
</dt> <dd>

API управления SMB предоставляет классы и методы для управления общими ресурсами и предоставления общего доступа.

</dd> <dt>

<span id="SNMP"></span><span id="snmp"></span>[СООБЩА](/windows/desktop/WmiSdk/snmp-provider)
</dt> <dd>

Сопоставляет объекты протокола SNMP, определенные в объектах схемы базы данных MIB, с классами. Дополнительные сведения см. [в разделе Настройка среды SNMP WMI](/windows/desktop/WmiSdk/setting-up-the-wmi-snmp-environment).

</dd> <dt>

<span id="Software_Inventory_Logging"></span><span id="software_inventory_logging"></span><span id="SOFTWARE_INVENTORY_LOGGING"></span>[Ведение журнала инвентаризации программного обеспечения](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)
</dt> <dd>

Поставщик ведения журнала инвентаризации программного обеспечения собирает данные лицензирования о программном обеспечении, установленном на сервере Windows Server, и предоставляет удаленный доступ к данным, чтобы их можно было легко объединить с помощью центра обработки данных.

</dd> <dt>

<span id="Software_Licensing_for_"></span><span id="software_licensing_for_"></span><span id="SOFTWARE_LICENSING_FOR_"></span>[Лицензирование программного обеспечения для Windows Vista](/previous-versions/windows/desktop/slwmiprov/software-licensing-classes-for-windows-vista)
</dt> <dd>

[Классы лицензирования программного обеспечения](/previous-versions/windows/desktop/sppwmi/software-license-provider-) , используемые для Windows Vista.

</dd> <dt>

<span id="Software_License"></span><span id="software_license"></span><span id="SOFTWARE_LICENSE"></span>[Лицензия на программное обеспечение](/previous-versions/windows/desktop/sppwmi/software-license-provider-)
</dt> <dd>

Поставщик лицензирования программного обеспечения извлекает данные лицензирования программного обеспечения.

</dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>[Том хранилища](/previous-versions/windows/desktop/vdswmi/storage-volume-provider)
</dt> <dd>

Поставщик томов хранилища предоставляет функции управления томами.

</dd> <dt>

<span id="Storage_Replica"></span><span id="storage_replica"></span><span id="STORAGE_REPLICA"></span>[Реплика хранилища](/previous-versions/windows/desktop/wvrcimprov/storage-replica-mi-provider-portal)
</dt> <dd>

Поставщик обеспечивает управление репликой хранилища.

</dd> <dt>

<span id="System_Registry"></span><span id="system_registry"></span><span id="SYSTEM_REGISTRY"></span>[Системный реестр](/previous-versions/windows/desktop/regprov/system-registry-provider)
</dt> <dd>

Поставщик системного реестра позволяет приложениям управления извлекать и изменять данные в системном реестре, а также получать уведомления при внесении изменений.

</dd> <dt>

<span id="System_Restore"></span><span id="system_restore"></span><span id="SYSTEM_RESTORE"></span>[Восстановление системы](/windows/desktop/sr/system-restore-portal)
</dt> <dd>

Предоставляет классы, которые настраивают и используют функцию восстановления системы. Дополнительные сведения см. в разделе [Настройка восстановления системы](/windows/desktop/sr/configuring-system-restore) и [классы WMI для восстановления системы](/windows/desktop/sr/system-restore-wmi-classes).

</dd> <dt>

<span id="Trusted_Platform_Module"></span><span id="trusted_platform_module"></span><span id="TRUSTED_PLATFORM_MODULE"></span>[доверенный платформенный модуль (TPM)](/windows/desktop/SecProv/trusted-platform-module-provider)
</dt> <dd>

Предоставляет доступ к данным об устройстве безопасности, представленном экземпляром [**\_ TPM Win32**](/windows/desktop/SecProv/win32-tpm), который является корнем отношения доверия для системы компьютеров с доверенной платформой Microsoft Windows.

</dd> <dt>

<span id="Trustmon"></span><span id="trustmon"></span><span id="TRUSTMON"></span>[Средство TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider)
</dt> <dd>

Поставщик [средство TrustMon](/previous-versions/windows/desktop/trustmonprov/trustmon-provider) — это поставщик экземпляров, который создает классы со сведениями о доверительных отношениях между доменами.

</dd> <dt>

<span id="User_Access_Logging"></span><span id="user_access_logging"></span><span id="USER_ACCESS_LOGGING"></span>[Ведение журнала доступа пользователей](/previous-versions/windows/desktop/ual/user-access-logging)
</dt> <dd>

Ведение журнала доступа пользователей (UAL) — это общая платформа для ролей Windows Server, сообщающая о соответствующих метриках потребления.

</dd> <dt>

<span id="UserProfileProvider"></span><span id="userprofileprovider"></span><span id="USERPROFILEPROVIDER"></span>[усерпрофилепровидер](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes)
</dt> <dd>

Поставщик [усерпрофилепровидер](/previous-versions/windows/desktop/userprofileprov/userprofileprovider-provider-classes) предоставляет классы, предоставляющие сведения о профиле пользователя в системе Windows, а также о состоянии работоспособности перенаправленной папки пользователя.

</dd> <dt>

<span id="User_State_Management"></span><span id="user_state_management"></span><span id="USER_STATE_MANAGEMENT"></span>[Управление пользовательской областью](/previous-versions/windows/desktop/usm/user-state-management-api-portal)
</dt> <dd>

Поставщик управления пользовательской среды предоставляет API управления и отчетов для корпоративных сценариев.

</dd> <dt>

<span id="View"></span><span id="view"></span><span id="VIEW"></span>[Режиме](/windows/desktop/WmiSdk/view-provider)
</dt> <dd>

Создает новые экземпляры и методы на основе экземпляров других классов. На 64-разрядных платформах доступны две версии поставщика представления.

</dd> <dt>

<span id="VPNClientPSProvider"></span><span id="vpnclientpsprovider"></span><span id="VPNCLIENTPSPROVIDER"></span>[впнклиентпспровидер](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client)
</dt> <dd>

Поставщик [впнклиентпспровидер](/previous-versions/windows/desktop/vpnclientpsprov/remote-access-client) предоставляет платформу для автоматизации подключения к клиенту виртуальной частной сети.

</dd> <dt>

<span id="WDM"></span><span id="wdm"></span>[ПОТОКА](/windows/desktop/WmiCoreProv/wdm-provider)
</dt> <dd>

Предоставляет доступ к классам, экземплярам, методам и событиям драйверов оборудования, которые соответствуют WDM (WDM).

</dd> <dt>

<span id="WFasCim"></span><span id="wfascim"></span><span id="WFASCIM"></span>[вфасЦим](/previous-versions/windows/desktop/wfascimprov/network-security-classes)
</dt> <dd>

Поставщик [вфасЦим](/previous-versions/windows/desktop/wfascimprov/network-security-classes) предоставляет функции сетевой безопасности и фильтрации.

</dd> <dt>

<span id="WhqlProvider"></span><span id="whqlprovider"></span><span id="WHQLPROVIDER"></span>[вхклпровидер](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes)
</dt> <dd>

Поставщик [вхклпровидер](/previous-versions/windows/desktop/whqlprov/whqlprovider-provider-classes) предоставляет сведения о цифровых подписях для драйверов.

</dd> <dt>

<span id="Win32ClockProvider"></span><span id="win32clockprovider"></span><span id="WIN32CLOCKPROVIDER"></span>[Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes)
</dt> <dd>

Поставщик [Win32ClockProvider](/previous-versions/windows/desktop/wmitimepprov/win32clockprovider-provider-classes) отображает текущие, локальные и временные метки времени на основе времени в формате UTC в компьютерной системе.

</dd> <dt>

<span id="Windows_Data_Access_Components__WDAC_"></span><span id="windows_data_access_components__wdac_"></span><span id="WINDOWS_DATA_ACCESS_COMPONENTS__WDAC_"></span>[Компоненты доступа к данным Windows (WDAC)](/previous-versions/windows/desktop/wdacwmiprov/windows-data-access-components-wmi-provider-portal)
</dt> <dd>

Предоставляет управление WDAC.

</dd> <dt>

<span id="Windows_Defender"></span><span id="windows_defender"></span><span id="WINDOWS_DEFENDER"></span>[Защитник Windows](/previous-versions/windows/desktop/defender/windows-defender-wmiv2-apis-portal)
</dt> <dd>

Поставщик защитника Windows предоставляет функции безопасности защитника Windows.

</dd> <dt>

<span id="Windows_Installer"></span><span id="windows_installer"></span><span id="WINDOWS_INSTALLER"></span>[установщик Windows](/previous-versions/windows/desktop/msiprov/windows-installer-provider)
</dt> <dd>

Поставщик установщик Windows, также известный как поставщик MSI, позволяет приложениям получать доступ к информации, собранной из приложений, совместимых с установщик Windows.

</dd> <dt>

<span id="Windows_Product_Activation"></span><span id="windows_product_activation"></span><span id="WINDOWS_PRODUCT_ACTIVATION"></span>[Активация продуктов Windows](/previous-versions/windows/desktop/licwmiprov/windows-product-activation-provider)
</dt> <dd>

Поставщик активации Windows (WPA) — это технология борьбы с пиратством, предназначенная для уменьшения случайного копирования программного обеспечения.

</dd> <dt>

<span id="Windows_Server_Manager"></span><span id="windows_server_manager"></span><span id="WINDOWS_SERVER_MANAGER"></span>[диспетчер сервера Windows](/previous-versions/windows/desktop/mgmtprovider/windows-server-manager-wmi-provider-portal)
</dt> <dd>

Поставщик обеспечивает доступ к конфигурации, управляемой приложением диспетчер сервера, и управление ею.

</dd> <dt>

<span id="Windows_Server_Storage_Management__MsftStrgMan_"></span><span id="windows_server_storage_management__msftstrgman_"></span><span id="WINDOWS_SERVER_STORAGE_MANAGEMENT__MSFTSTRGMAN_"></span>[Управление хранилищем Windows Server (Мсфтстргман)](/previous-versions/windows/desktop/msftstrgmanprov/windows-storage-management-wmi-provider-portal)
</dt> <dd>

Поставщик Мсфтстргман обеспечивает управление системами хранения данных в продуктах Windows Server.

</dd> <dt>

<span id="Windows_Storage_Management__StrgMgmt_"></span><span id="windows_storage_management__strgmgmt_"></span><span id="WINDOWS_STORAGE_MANAGEMENT__STRGMGMT_"></span>[Управление хранилищем Windows (Стргмгмт)](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)
</dt> <dd>

Поставщик Стргмгмт можно использовать для управления широким спектром конфигураций хранилища, от планшетов до внешних массивов хранения данных на серверах.

</dd> <dt>

<span id="Windows_System_Assessment_Tool"></span><span id="windows_system_assessment_tool"></span><span id="WINDOWS_SYSTEM_ASSESSMENT_TOOL"></span>[Средство оценки системы Windows](/windows/desktop/WinSAT/winsat-mof-classes)
</dt> <dd>

Средство Windows System оценке (WinSAT) предоставляет ряд классов, оценивающих характеристики и возможности производительности компьютера.

</dd> <dt>

<span id="WMI_Core"></span><span id="wmi_core"></span><span id="WMI_CORE"></span>[Ядро WMI](/windows/desktop/WmiCoreProv/wmi-core-provider-)
</dt> <dd>

Поставщик ядра WMI определяет классы, составляющие основные функциональные возможности WMI.

</dd> <dt>

<span id="Msft_ProviderSubSystem"></span><span id="msft_providersubsystem"></span><span id="MSFT_PROVIDERSUBSYSTEM"></span>[MSFT \_ провидерсубсистем](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-)
</dt> <dd>

Поставщик [MSFT \_ провидерсубсистем](/previous-versions/windows/desktop/wmisystemprov/msft-providersubsystem-provider-) поддерживает поставщиков.

</dd> <dt>

<span id="Win32_Perf"></span><span id="win32_perf"></span><span id="WIN32_PERF"></span>[Производительность \_ Win32](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov)
</dt> <dd>

Абстрактный класс [**\_ производительности Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perf-wmiprov) является базовым классом для классов счетчиков производительности [**Win32 \_ перфравдата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) и [**Win32 \_ перфформаттеддата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov). Он определяет требуемые свойства timestamp и Frequency, используемые в алгоритмах CounterType для классов счетчиков производительности.

</dd> <dt>

<span id="Win32_PerfFormattedData"></span><span id="win32_perfformatteddata"></span><span id="WIN32_PERFFORMATTEDDATA"></span>[**\_Перфформаттеддата Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfformatteddata-wmiprov)
</dt> <dd>

Абстрактный базовый класс для предварительно установленных и вычисляемых классов данных.

</dd> <dt>

<span id="Win32_PerfRawData"></span><span id="win32_perfrawdata"></span><span id="WIN32_PERFRAWDATA"></span>[**\_Перфравдата Win32**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov)
</dt> <dd>

Класс счетчика производительности [**Win32 \_ перфравдата**](/previous-versions/windows/desktop/wmisystemprov/win32-perfrawdata-wmiprov) является абстрактным базовым классом для всех конкретных классов необработанных счетчиков производительности. Для отображения в системном мониторе классы счетчиков производительности должны быть добавлены в \\ пространство имен root CIMv2 и быть производными от **Win32 \_ перфравдата**.

</dd> <dt>

<span id="WMIPerfClass"></span><span id="wmiperfclass"></span><span id="WMIPERFCLASS"></span>[вмиперфкласс](/windows/desktop/WmiSdk/wmiperfclass-provider)
</dt> <dd>

Создает [Классы счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes)WMI. Данные в эти классы производительности динамически передаются поставщиком Вмиперфинст.

</dd> <dt>

<span id="WmiPerfInst"></span><span id="wmiperfinst"></span><span id="WMIPERFINST"></span>[вмиперфинст](/windows/desktop/WmiSdk/wmiperfinst-provider)
</dt> <dd>

Динамически предоставляет необработанные и отформатированные данные счетчиков производительности из определений [классов счетчиков производительности](/windows/desktop/CIMWin32Prov/performance-counter-classes) .

</dd> <dt>

<span id="Work_Folders"></span><span id="work_folders"></span><span id="WORK_FOLDERS"></span>[Рабочие папки](/previous-versions/windows/desktop/syncshareservermgmt/sync-share-server-management-portal)
</dt> <dd>

Рабочие папки используются для синхронизации файлов с несколькими компьютерами и мобильными устройствами.

</dd> </dl>

 

 
