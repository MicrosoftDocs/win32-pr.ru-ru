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
# <a name="whats-new-in-windowsvista"></a>Новые возможности Windows Vista

Начиная с Windows Vista, Инструментарий WMI содержит множество новых функций, основанных на запросах пользователей WMI.

-   [Новое средство устранения неполадок](#new-troubleshooting-tool)
-   [Новые функции безопасности в Windows Vista](#new-security-features-in-windows-vista)
-   [Другие новые возможности в Windows Vista](#other-new-features-in-windows-vista)
-   [См. также](#related-topics)

## <a name="new-troubleshooting-tool"></a>Новое средство устранения неполадок

Для загрузки доступно новое средство устранения неполадок.

<dl> <dt>

<span id="WMI_Diagnosis_Utility"></span><span id="wmi_diagnosis_utility"></span><span id="WMI_DIAGNOSIS_UTILITY"></span>служебная программа для диагностики WMI
</dt> <dd>

Эта программа проверяет текущее состояние службы WMI и связанные компоненты, параметры DCOM и параметры реестра на локальном компьютере. Программа сообщает о проблемах и предлагает варианты их восстановления. Дополнительные сведения и о загрузке программы см. в разделе [служебная программа для диагностики WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en).

</dd> </dl>

## <a name="new-security-features-in-windows-vista"></a>Новые функции безопасности в Windows Vista

В следующем списке перечислены новые функции безопасности WMI, доступные в Windows Vista.

<dl> <dt>

<span id="Tracing_and_logging_events"></span><span id="tracing_and_logging_events"></span><span id="TRACING_AND_LOGGING_EVENTS"></span>События трассировки и ведения журнала
</dt> <dd>

Служба WMI больше не использует большинство [файлов журналов WMI](wmi-log-files.md). Вместо этого он использует [трассировку событий](/windows/desktop/ETW/event-tracing-portal) (ETW) и события, доступные через пользовательский интерфейс **Просмотр событий** или программу командной строки wevtutil. Дополнительные сведения см. в разделе [Трассировка действия WMI](tracing-wmi-activity.md).

</dd> <dt>

<span id="Setting_WMI_namespace_security_in_the_MOF_file"></span><span id="setting_wmi_namespace_security_in_the_mof_file"></span><span id="SETTING_WMI_NAMESPACE_SECURITY_IN_THE_MOF_FILE"></span>Настройка безопасности пространства имен WMI в MOF-файле
</dt> <dd>

Квалификатор **намеспацесекуритисддл** можно использовать для защиты любого пространства имен. Дополнительные сведения см. [в разделе Настройка безопасности пространства имен при создании пространства имен](setting-namespace-security-when-the-namespace-is-created.md).

</dd> <dt>

<span id="Security_Auditing_of_WMI_namespaces"></span><span id="security_auditing_of_wmi_namespaces"></span><span id="SECURITY_AUDITING_OF_WMI_NAMESPACES"></span>Аудит безопасности пространств имен WMI
</dt> <dd>

Инструментарий WMI использует системные списки управления доступом (SACL) пространства имен для аудита действий пространства имен и событий отчетов в журнале событий безопасности. Дополнительные сведения см. в статьях [доступ к пространствам имен WMI](access-to-wmi-namespaces.md) и [Задание дескрипторов безопасности пространства имен](setting-namespace-security-descriptors.md).

</dd> <dt>

<span id="Get_and_Set_security_descriptor_methods_for_securable_objects"></span><span id="get_and_set_security_descriptor_methods_for_securable_objects"></span><span id="GET_AND_SET_SECURITY_DESCRIPTOR_METHODS_FOR_SECURABLE_OBJECTS"></span>Получение и установка методов дескриптора безопасности для защищаемых объектов
</dt> <dd>

К [**\_ принтерам Win32**](/windows/desktop/CIMWin32Prov/win32-printer), [**\_ службам Win32**](/windows/desktop/CIMWin32Prov/win32-service), [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov), [**Win32 \_ дкомаппликатионсеттинг**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)и [**\_ \_ системсекурити**](--systemsecurity.md)добавлены новые методы с скриптами для получения и установки дескрипторов безопасности. Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="Manipulate_Security_Descriptors_in_scripts"></span><span id="manipulate_security_descriptors_in_scripts"></span><span id="MANIPULATE_SECURITY_DESCRIPTORS_IN_SCRIPTS"></span>Обработка дескрипторов безопасности в скриптах
</dt> <dd>

Класс [**Win32 \_ секуритидескрипторхелпер**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) содержит методы, позволяющие сценариям преобразовывать двоичные дескрипторы безопасности защищаемых объектов в объекты [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) или строки [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) . Дополнительные сведения см. [в разделе Изменение параметров безопасности доступа к защищаемым объектам](changing-access-security-on-securable-objects.md).

</dd> <dt>

<span id="User_Account_Control"></span><span id="user_account_control"></span><span id="USER_ACCOUNT_CONTROL"></span>Контроль учетных записей пользователей
</dt> <dd>

Управление учетными записями пользователей (UAC) влияет на то, какие данные WMI возвращаются, удаленный доступ и как должны выполняться сценарии. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](user-account-control-and-wmi.md). Дополнительные сведения о UAC см. в разделе [Начало работы с контролем учетных записей в Windows Vista](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

</dd> </dl>

## <a name="other-new-features-in-windows-vista"></a>Другие новые возможности в Windows Vista

В следующем списке перечислены новые функции WMI, доступные в Windows Vista.

<dl> <dt>

<span id="New_performance_counter_data_providers"></span><span id="new_performance_counter_data_providers"></span><span id="NEW_PERFORMANCE_COUNTER_DATA_PROVIDERS"></span>Новые поставщики данных счетчиков производительности
</dt> <dd>

Процесс автоопределения и автоочистки (ADAP) больше не передает объекты счетчиков производительности в классы производительности WMI в репозитории WMI. Дополнительные сведения см. в разделе [библиотеки производительности и инструментарий WMI](performance-libraries-and-wmi.md). [Поставщик вмиперфкласс](wmiperfclass-provider.md) создает классы счетчиков производительности WMI. Данные динамически передаются этим классам производительности WMI [поставщиком вмиперфинст](wmiperfinst-provider.md).

</dd> <dt>

<span id="Indexer_for_collections"></span><span id="indexer_for_collections"></span><span id="INDEXER_FOR_COLLECTIONS"></span>Индексатор для коллекций
</dt> <dd>

Метод [**SWbemObject. итеминдекс**](swbemobjectset-itemindex.md) возвращает объект, связанный с указанным индексом, в коллекцию.

</dd> <dt>

<span id="Support_for_IPv6_and_IPv4"></span><span id="support_for_ipv6_and_ipv4"></span><span id="SUPPORT_FOR_IPV6_AND_IPV4"></span>Поддержка IPv6 и IPv4
</dt> <dd>

[Поставщик IP-маршрута](/previous-versions/windows/desktop/wmiiprouteprov/ip-route-provider) WMI и классы сетевых классов предоставляют данные для адресов IPv4. Начиная с Windows Vista, Инструментарий WMI также обеспечивает ограниченную поддержку возможностей сети IPv6. Дополнительные сведения см. [в разделе Поддержка IPv6 и IPv4 в WMI](ipv6-and-ipv4-support-in-wmi.md).

</dd> <dt>

<span id="Changes_to_remote_connections"></span><span id="changes_to_remote_connections"></span><span id="CHANGES_TO_REMOTE_CONNECTIONS"></span>Изменения удаленных подключений
</dt> <dd>

Для подключения к пространству имен WMI на удаленном компьютере под управлением Windows Vista могут потребоваться изменения параметров [брандмауэра Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx), [управления учетными записями пользователей](/previous-versions/aa905108(v=msdn.10))или DCOM. Дополнительные сведения см. [в статье удаленное подключение к WMI, начиная с ОС Vista](connecting-to-wmi-remotely-starting-with-vista.md).

</dd> <dt>

<span id="Changes_to_________Win32_QuickFixEngineering"></span><span id="changes_to_________win32_quickfixengineering"></span><span id="CHANGES_TO_________WIN32_QUICKFIXENGINEERING"></span>Изменения в [ **Win32 \_ куиккфиксенгиниринг**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering)
</dt> <dd>

Для систем, работающих в операционной системе Windows Vista и более поздних версий, этот класс возвращает только обновления, предоставляемые компонентом обслуживания на основе компонентов (CBS). Эти обновления не перечислены в реестре. Обновления, предоставляемые установщик Windows (MSI) или [Центр обновления Windows](https://update.microsoft.com/microsoftupdate/v6/default.aspx?ln=en-us) , не возвращаются [**\_ куиккфиксенгиниринг Win32**](/windows/desktop/CIMWin32Prov/win32-quickfixengineering).

</dd> <dt>

<span id="Enabling_and_disabling_a_NIC"></span><span id="enabling_and_disabling_a_nic"></span><span id="ENABLING_AND_DISABLING_A_NIC"></span>Включение и отключение сетевой карты
</dt> <dd>

[**Win32 \_ Сетевого адаптера**](/windows/desktop/CIMWin32Prov/win32-networkadapter) содержит новые методы включения и отключения сетевого адаптера.

</dd> <dt>

<span id="Windows_Installer_Provider_changes"></span><span id="windows_installer_provider_changes"></span><span id="WINDOWS_INSTALLER_PROVIDER_CHANGES"></span>Изменения поставщика установщик Windows
</dt> <dd>

[**Win32 \_ У продукта**](/previous-versions/windows/desktop/legacy/aa394378(v=vs.85)) есть новые свойства и методы для предоставления дополнительных данных о продукте.

</dd> <dt>

<span id="New_display_monitor_classes"></span><span id="new_display_monitor_classes"></span><span id="NEW_DISPLAY_MONITOR_CLASSES"></span>Новые классы монитора отображения
</dt> <dd>

[Мониторы отображаемых классов](/windows/desktop/WmiCoreProv/wmi-core-provider-) содержат данные, предоставляемые [поставщиком WDM](/windows/desktop/WmiCoreProv/wdm-provider) , который предоставляет данные о мониторах отображения.

</dd> <dt>

<span id="Intelligent_Platform_Management_Interface_provider"></span><span id="intelligent_platform_management_interface_provider"></span><span id="INTELLIGENT_PLATFORM_MANAGEMENT_INTERFACE_PROVIDER"></span>Поставщик интерфейса интеллектуального управления платформой
</dt> <dd>

[Поставщик IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider) WMI предоставляет данные из операций контроллера управления основной платой (BMC) операционной системе. Поставщик предоставляет сведения для классов сведений об управлении платформой, которые предоставляют данные датчиков и данные сообщений журнала системных событий (SEL) BMC.

</dd> <dt>

<span id="Detecting_hyperthreading_and_multicore_processors"></span><span id="detecting_hyperthreading_and_multicore_processors"></span><span id="DETECTING_HYPERTHREADING_AND_MULTICORE_PROCESSORS"></span>Обнаружение технологии Hyper и многоядерных процессоров
</dt> <dd>

[**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) Система ComputerSystem [**и \_ процессор Win32**](/windows/desktop/CIMWin32Prov/win32-processor) имеют новые свойства, позволяющие создавать сценарии для определения того, имеет ли компьютер многоядерные процессоры или обработчики технологии hypering.

</dd> <dt>

<span id="Event_messages"></span><span id="event_messages"></span><span id="EVENT_MESSAGES"></span>Сообщения о событиях
</dt> <dd>

В Windows Vista имеются новые сообщения о событиях. Дополнительные сведения см. в разделе [события WMI](wmi-events.md).

</dd> <dt>

<span id="Inventory_improvements"></span><span id="inventory_improvements"></span><span id="INVENTORY_IMPROVEMENTS"></span>Усовершенствования инвентаризации
</dt> <dd>

Многие классы оборудования имели изменения для улучшения инвентаризации оборудования. Например, свойство серийного номера было добавлено в [**Win32 \_ Кдромдриве**](/windows/desktop/CIMWin32Prov/win32-cdromdrive) и [**Win32 \_ дискдриве**](/windows/desktop/CIMWin32Prov/win32-diskdrive).

</dd> <dt>

<span id="New_provider_hosting_models"></span><span id="new_provider_hosting_models"></span><span id="NEW_PROVIDER_HOSTING_MODELS"></span>Новые модели размещения поставщика
</dt> <dd>

В Windows Vista добавлены новые модели размещения поставщиков. Дополнительные сведения см. в разделе [размещение и безопасность поставщика](provider-hosting-and-security.md).

</dd> </dl>

## <a name="related-topics"></a>См. также

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> </dl>

 

 
