---
description: Начиная с Windows Vista, Инструментарий WMI содержит множество новых функций, основанных на запросах пользователей WMI.
ms.assetid: 604a86d2-9a8e-4266-93b8-13676f768b29
ms.tgt_platform: multiple
title: Новые возможности Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee950becb906f89445f9ddfb258f4f7a608ce1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713019"
---
# <a name="whats-new-in-windowsvista"></a><span data-ttu-id="36795-103">Новые возможности Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36795-103">Whats New in Windows�Vista</span></span>

<span data-ttu-id="36795-104">Начиная с Windows Vista, Инструментарий WMI содержит множество новых функций, основанных на запросах пользователей WMI.</span><span class="sxs-lookup"><span data-stu-id="36795-104">Starting with Windows Vista, WMI contains many new features based upon requests by WMI users.</span></span>

-   [<span data-ttu-id="36795-105">Новое средство устранения неполадок</span><span class="sxs-lookup"><span data-stu-id="36795-105">New Troubleshooting Tool</span></span>](#new-troubleshooting-tool)
-   [<span data-ttu-id="36795-106">Новые функции безопасности в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36795-106">New Security Features in Windows Vista</span></span>](#new-security-features-in-windows-vista)
-   [<span data-ttu-id="36795-107">Другие новые возможности в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36795-107">Other New Features in Windows Vista</span></span>](#other-new-features-in-windows-vista)
-   [<span data-ttu-id="36795-108">См. также</span><span class="sxs-lookup"><span data-stu-id="36795-108">Related topics</span></span>](#related-topics)

## <a name="new-troubleshooting-tool"></a><span data-ttu-id="36795-109">Новое средство устранения неполадок</span><span class="sxs-lookup"><span data-stu-id="36795-109">New Troubleshooting Tool</span></span>

<span data-ttu-id="36795-110">Для загрузки доступно новое средство устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="36795-110">A new troubleshooting tool is available for download.</span></span>

<dl> <dt>

<span data-ttu-id="36795-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>служебная программа для диагностики WMI</span><span class="sxs-lookup"><span data-stu-id="36795-111"><span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>WMI Diagnosis Utility</span></span>
</dt> <dd>

<span data-ttu-id="36795-112">Эта программа проверяет текущее состояние службы WMI и связанные компоненты, параметры DCOM и параметры реестра на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="36795-112">This utility examines the current state of the WMI service and related components, DCOM settings, and registry settings on the local computer.</span></span> <span data-ttu-id="36795-113">Программа сообщает о проблемах и предлагает варианты их восстановления.</span><span class="sxs-lookup"><span data-stu-id="36795-113">The utility reports problems and offers suggestions for repair.</span></span> <span data-ttu-id="36795-114">Дополнительные сведения и о загрузке программы см. в разделе [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span><span class="sxs-lookup"><span data-stu-id="36795-114">For more information and to download the utility, see [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).</span></span>

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a><span data-ttu-id="36795-115">Новые функции безопасности в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36795-115">New Security Features in Windows Vista</span></span>

<span data-ttu-id="36795-116">В следующем списке перечислены новые функции безопасности WMI, доступные в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36795-116">The following list lists the new WMI security features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="36795-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>События трассировки и ведения журнала</span><span class="sxs-lookup"><span data-stu-id="36795-117"><span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>Tracing and logging events</span></span>
</dt> <dd>

<span data-ttu-id="36795-118">Служба WMI больше не использует большинство [файлов журналов WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="36795-118">WMI service no longer uses most of the [WMI Log Files](wmi-log-files.md).</span></span> <span data-ttu-id="36795-119">Вместо этого он использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события, доступные через пользовательский интерфейс **Просмотр событий** или программу командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="36795-119">Instead it uses [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) and events are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="36795-120">Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).</span><span class="sxs-lookup"><span data-stu-id="36795-120">For more information, see [Tracing WMI Activity](tracing-wmi-activity.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Настройка безопасности пространства имен WMI в MOF-файле</span><span class="sxs-lookup"><span data-stu-id="36795-121"><span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Setting WMI namespace security in the MOF file</span></span>
</dt> <dd>

<span data-ttu-id="36795-122">Квалификатор **намеспацесекуритисддл** можно использовать для защиты любого пространства имен.</span><span class="sxs-lookup"><span data-stu-id="36795-122">The **NamespaceSecuritySDDL** qualifier can be used to secure any namespace.</span></span> <span data-ttu-id="36795-123">Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="36795-123">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Аудит безопасности пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="36795-124"><span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Security Auditing of WMI namespaces</span></span>
</dt> <dd>

<span data-ttu-id="36795-125">Инструментарий WMI использует системные списки управления доступом (SACL) пространства имен для аудита действий пространства имен и событий отчетов в журнале событий безопасности.</span><span class="sxs-lookup"><span data-stu-id="36795-125">WMI uses the namespace system access control lists (SACL) to audit namespace activity and report events to the Security event log.</span></span> <span data-ttu-id="36795-126">Дополнительные сведения см. в статьях [доступ к пространствам имен WMI](access-to-wmi-namespaces.md) и [Задание дескрипторов безопасности пространства имен](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="36795-126">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Получение и установка методов дескриптора безопасности для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="36795-127"><span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Get and Set security descriptor methods for securable objects</span></span>
</dt> <dd>

<span data-ttu-id="36795-128">К [**\_ принтерам Win32**](/windows/desktop/CIMWin32Prov/win32-printer), [**\_ службам Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ дкомаппликатионсеттинг**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)и [**\_ \_ системсекурити**](--systemsecurity.md)добавлены новые методы с скриптами для получения и установки дескрипторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="36795-128">New scriptable methods to get and set security descriptors have been added to [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer), [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32\_DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting), and [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="36795-129">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="36795-129">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Обработка дескрипторов безопасности в скриптах</span><span class="sxs-lookup"><span data-stu-id="36795-130"><span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Manipulate Security Descriptors in scripts</span></span>
</dt> <dd>

<span data-ttu-id="36795-131">Класс [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) содержит методы, позволяющие сценариям преобразовывать двоичные дескрипторы безопасности защищаемых объектов в объекты [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) или строки [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="36795-131">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class has methods that allow scripts to convert binary security descriptors on securable objects to [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) objects or [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language) strings.</span></span> <span data-ttu-id="36795-132">Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="36795-132">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Контроль учетных записей пользователей</span><span class="sxs-lookup"><span data-stu-id="36795-133"><span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>User Account Control</span></span>
</dt> <dd>

<span data-ttu-id="36795-134">Управление учетными записями пользователей (UAC) влияет на то, какие данные WMI возвращаются, удаленный доступ и как должны выполняться сценарии.</span><span class="sxs-lookup"><span data-stu-id="36795-134">User Account Control (UAC) affects what WMI data is returned, remote access, and how scripts must be run.</span></span> <span data-ttu-id="36795-135">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="36795-135">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span> <span data-ttu-id="36795-136">Дополнительные сведения о UAC см. в разделе [Начало работы с контролем учетных записей в Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span><span class="sxs-lookup"><span data-stu-id="36795-136">For more information about UAC, see [Getting Started with User Account Control on Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).</span></span>

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a><span data-ttu-id="36795-137">Другие новые возможности в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36795-137">Other New Features in Windows Vista</span></span>

<span data-ttu-id="36795-138">В следующем списке перечислены новые функции WMI, доступные в Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="36795-138">The following list lists new WMI features that are available in Windows Vista.</span></span>

<dl> <dt>

<span data-ttu-id="36795-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Новые поставщики данных счетчиков производительности</span><span class="sxs-lookup"><span data-stu-id="36795-139"><span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>New performance counter data providers</span></span>
</dt> <dd>

<span data-ttu-id="36795-140">Процесс автоопределения и автоочистки (ADAP) больше не передает объекты счетчиков производительности в классы производительности WMI в репозитории WMI.</span><span class="sxs-lookup"><span data-stu-id="36795-140">The AutoDiscovery/AutoPurge (ADAP) process no longer transfers performance counter objects into WMI performance classes in the WMI repository.</span></span> <span data-ttu-id="36795-141">Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="36795-141">For more information, see [Performance Libraries and WMI](performance-libraries-and-wmi.md).</span></span> <span data-ttu-id="36795-142">[Поставщик вмиперфкласс](wmiperfclass-provider.md) создает классы счетчиков производительности WMI.</span><span class="sxs-lookup"><span data-stu-id="36795-142">The [WMIPerfClass Provider](wmiperfclass-provider.md) creates the WMI Performance Counter Classes.</span></span> <span data-ttu-id="36795-143">Данные динамически передаются этим классам производительности WMI [поставщиком вмиперфинст](wmiperfinst-provider.md).</span><span class="sxs-lookup"><span data-stu-id="36795-143">Data is dynamically supplied to these WMI performance classes by the [WMIPerfInst Provider](wmiperfinst-provider.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Индексатор для коллекций</span><span class="sxs-lookup"><span data-stu-id="36795-144"><span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Indexer for collections</span></span>
</dt> <dd>

<span data-ttu-id="36795-145">Метод [**SWbemObject. итеминдекс**](swbemobjectset-itemindex.md) возвращает объект, связанный с указанным индексом, в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="36795-145">The [**SWbemObject.ItemIndex**](swbemobjectset-itemindex.md) method returns the object associated with a specified index into a collection.</span></span>

</dd> <dt>

<span data-ttu-id="36795-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Поддержка IPv6 и IPv4</span><span class="sxs-lookup"><span data-stu-id="36795-146"><span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Support for IPv6 and IPv4</span></span>
</dt> <dd>

<span data-ttu-id="36795-147">[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI и классы сетевых классов предоставляют данные для адресов IPv4.</span><span class="sxs-lookup"><span data-stu-id="36795-147">WMI [IP Route Provider](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) and network classes supply data for IPv4 addresses.</span></span> <span data-ttu-id="36795-148">Начиная с Windows Vista, Инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6.</span><span class="sxs-lookup"><span data-stu-id="36795-148">Starting with Windows Vista, WMI also provides limited support for IPv6 network capabilities.</span></span> <span data-ttu-id="36795-149">Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="36795-149">For more information, see [IPv6 and IPv4 Support in WMI](ipv6-and-ipv4-support-in-wmi.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Изменения удаленных подключений</span><span class="sxs-lookup"><span data-stu-id="36795-150"><span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Changes to remote connections</span></span>
</dt> <dd>

<span data-ttu-id="36795-151">Для подключения к пространству имен WMI на удаленном компьютере под управлением Windows Vista могут потребоваться изменения параметров [брандмауэра Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [управления учетными записями пользователей](/previous-versions/aa905108(v=msdn.10))или DCOM.</span><span class="sxs-lookup"><span data-stu-id="36795-151">Connecting to a WMI namespace on a remote computer running Windows Vista may require changes to settings for [Windows Firewall](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [User Account Control](/previous-versions/aa905108(v=msdn.10)), or DCOM.</span></span> <span data-ttu-id="36795-152">Дополнительные сведения см. [в статье удаленное подключение к WMI, начиная с ОС Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span><span class="sxs-lookup"><span data-stu-id="36795-152">For more information, see [Connecting to WMI Remotely Starting with Vista](connecting-to-wmi-remotely-starting-with-vista.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Изменения в [ **Win32 \_ куиккфиксенгиниринг**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span><span class="sxs-lookup"><span data-stu-id="36795-153"><span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Changes to [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)</span></span>
</dt> <dd>

<span data-ttu-id="36795-154">Для систем, работающих в операционной системе Windows Vista и более поздних версий, этот класс возвращает только обновления, предоставляемые компонентом обслуживания на основе компонентов (CBS).</span><span class="sxs-lookup"><span data-stu-id="36795-154">For systems running on the Windows Vista and later operating system, this class returns only the updates supplied by Component Based Servicing (CBS).</span></span> <span data-ttu-id="36795-155">Эти обновления не перечислены в реестре.</span><span class="sxs-lookup"><span data-stu-id="36795-155">These updates are not listed in the registry.</span></span> <span data-ttu-id="36795-156">Обновления, предоставляемые установщик Windows (MSI) или [Центр обновления Windows](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) , не возвращаются [**\_ куиккфиксенгиниринг Win32**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span><span class="sxs-lookup"><span data-stu-id="36795-156">Updates supplied by Windows Installer (MSI) or the [Windows Update](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) are not returned by [**Win32\_QuickFixEngineering**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).</span></span>

</dd> <dt>

<span data-ttu-id="36795-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Включение и отключение сетевой карты</span><span class="sxs-lookup"><span data-stu-id="36795-157"><span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Enabling and disabling a NIC</span></span>
</dt> <dd>

<span data-ttu-id="36795-158">[**Win32 \_ Сетевого адаптера**](/windows/desktop/CIMWin32Prov/win32-networkadapter) содержит новые методы включения и отключения сетевого адаптера.</span><span class="sxs-lookup"><span data-stu-id="36795-158">[**Win32\_NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) has new methods to enable and disable the network adapter.</span></span>

</dd> <dt>

<span data-ttu-id="36795-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Изменения поставщика установщик Windows</span><span class="sxs-lookup"><span data-stu-id="36795-159"><span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Windows Installer Provider changes</span></span>
</dt> <dd>

<span data-ttu-id="36795-160">[**Win32 \_ У продукта**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) есть новые свойства и методы для предоставления дополнительных данных о продукте.</span><span class="sxs-lookup"><span data-stu-id="36795-160">[**Win32\_Product**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) has new properties and methods to provide more data about the product.</span></span>

</dd> <dt>

<span data-ttu-id="36795-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Новые классы монитора отображения</span><span class="sxs-lookup"><span data-stu-id="36795-161"><span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>New display monitor classes</span></span>
</dt> <dd>

<span data-ttu-id="36795-162">[Мониторы отображаемых классов](/windows/desktop/WmiCoreProv/wmi-core-provider-) содержат данные, предоставляемые [поставщиком WDM](/windows/desktop/WmiCoreProv/wdm-provider) , который предоставляет данные о мониторах отображения.</span><span class="sxs-lookup"><span data-stu-id="36795-162">[Monitor Display Classes](/windows/desktop/WmiCoreProv/wmi-core-provider-) contain data supplied by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) that provides data about display monitors.</span></span>

</dd> <dt>

<span data-ttu-id="36795-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Поставщик интерфейса интеллектуального управления платформой</span><span class="sxs-lookup"><span data-stu-id="36795-163"><span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Intelligent Platform Management Interface provider</span></span>
</dt> <dd>

<span data-ttu-id="36795-164">[Поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI предоставляет данные из операций контроллера управления основной платой (BMC) операционной системе.</span><span class="sxs-lookup"><span data-stu-id="36795-164">The WMI [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) supplies data from baseboard management controller (BMC) operations to the operating system.</span></span> <span data-ttu-id="36795-165">Поставщик предоставляет сведения для классов сведений об управлении платформой, которые предоставляют данные датчиков и данные сообщений журнала системных событий (SEL) BMC.</span><span class="sxs-lookup"><span data-stu-id="36795-165">The provider supplies information to the Intelligent Platform Management Information Classes, which provide sensors data and BMC System Event Log (SEL) message data.</span></span>

</dd> <dt>

<span data-ttu-id="36795-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Обнаружение технологии Hyper и многоядерных процессоров</span><span class="sxs-lookup"><span data-stu-id="36795-166"><span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Detecting hyperthreading and multicore processors</span></span>
</dt> <dd>

<span data-ttu-id="36795-167">[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) Система ComputerSystem [**и \_ процессор Win32**](/windows/desktop/CIMWin32Prov/win32-processor) имеют новые свойства, позволяющие создавать сценарии для определения того, имеет ли компьютер многоядерные процессоры или обработчики технологии hypering.</span><span class="sxs-lookup"><span data-stu-id="36795-167">[**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) and [**Win32\_Processor**](/windows/desktop/CIMWin32Prov/win32-processor) have new properties that enable you to write scripts to determine whether the computer system has multicore or hyperthreading processors.</span></span>

</dd> <dt>

<span data-ttu-id="36795-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Сообщения о событиях</span><span class="sxs-lookup"><span data-stu-id="36795-168"><span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Event messages</span></span>
</dt> <dd>

<span data-ttu-id="36795-169">В Windows Vista имеются новые сообщения о событиях.</span><span class="sxs-lookup"><span data-stu-id="36795-169">Windows Vista has new event messages.</span></span> <span data-ttu-id="36795-170">Дополнительные сведения см. в разделе [события WMI](wmi-events.md).</span><span class="sxs-lookup"><span data-stu-id="36795-170">For more information, see [WMI Events](wmi-events.md).</span></span>

</dd> <dt>

<span data-ttu-id="36795-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Усовершенствования инвентаризации</span><span class="sxs-lookup"><span data-stu-id="36795-171"><span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Inventory improvements</span></span>
</dt> <dd>

<span data-ttu-id="36795-172">Многие классы оборудования имели изменения для улучшения инвентаризации оборудования.</span><span class="sxs-lookup"><span data-stu-id="36795-172">Many hardware classes have had changes to improve hardware inventory.</span></span> <span data-ttu-id="36795-173">Например, свойство серийного номера было добавлено в [**Win32 \_ Кдромдриве**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) и [**Win32 \_ дискдриве**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span><span class="sxs-lookup"><span data-stu-id="36795-173">For example, a serial number property was added to [**Win32\_CDROMDrive**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) and [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive).</span></span>

</dd> <dt>

<span data-ttu-id="36795-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Новые модели размещения поставщика</span><span class="sxs-lookup"><span data-stu-id="36795-174"><span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>New provider hosting models</span></span>
</dt> <dd>

<span data-ttu-id="36795-175">В Windows Vista добавлены новые модели размещения поставщиков.</span><span class="sxs-lookup"><span data-stu-id="36795-175">New provider hosting models have been added for Windows Vista.</span></span> <span data-ttu-id="36795-176">Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="36795-176">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="36795-177">См. также</span><span class="sxs-lookup"><span data-stu-id="36795-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36795-178">Сведения об инструментарии WMI</span><span class="sxs-lookup"><span data-stu-id="36795-178">About WMI</span></span>](about-wmi.md)
</dt> </dl>

 

 
