---
description: новые возможности в Windows 7
ms.assetid: C3FE15EF-CBF0-4A5D-ADCC-108795F8CE7A
ms.tgt_platform: multiple
title: новые возможности в Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000a3460366855df65096333a8b847a6d2c0c0a48a89c91f6791db3286d634fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502864"
---
# <a name="whats-new-in-windows-7"></a>новые возможности в Windows 7

## <a name="new-security-feature-in-windows-7"></a>новая функция безопасности в Windows 7

ниже перечислены новые функции безопасности инструментарий управления Windows (WMI) (WMI), доступные в Windows 7.

<dl> <dt>

<span id="Controlling_provider_security"></span><span id="controlling_provider_security"></span><span id="CONTROLLING_PROVIDER_SECURITY"></span>Управление безопасностью поставщика
</dt> <dd>

Изменения, повышающие безопасность хост-процесса общего поставщика WMI (wmiprvse.exe). Эти изменения предоставляют три новые групповые политики и два режима работы для общего узла WMI, которые называются безопасными и совместимыми режимами. Дополнительные сведения см. в разделе [разделы реестра для управления безопасностью поставщика](registry-keys-for-controlling-provider-security-.md).

</dd> </dl>

## <a name="other-new-or-updated-features-in-windows-7"></a>другие новые или обновленные функции в Windows 7

в следующем списке перечислены новые функции WMI, доступные в Windows 7.

<dl> <dt>

<span id="CIM_schema_compatibility"></span><span id="cim_schema_compatibility"></span><span id="CIM_SCHEMA_COMPATIBILITY"></span>Совместимость со схемой CIM
</dt> <dd>

начиная с версии Windows 7 WMI совместим с версией схемы модель CIM (CIM) 2.17.1. Дополнительные сведения см. в разделе [Совместимость схемы CIM](cim-schema-compatibility.md).

</dd> <dt>

<span id="Cross-namespace_association_traversal"></span><span id="cross-namespace_association_traversal"></span><span id="CROSS-NAMESPACE_ASSOCIATION_TRAVERSAL"></span>Просмотр связей между пространствами имен
</dt> <dd>

Инструментарий WMI реализовал стандартный механизм обнаружения профилей с помощью схемы CIM. Дополнительные сведения см. в разделе [обход взаимосвязей между пространствами имен](cross-namespace-association-traversal.md).

</dd> <dt>

<span id="Association_providers"></span><span id="association_providers"></span><span id="ASSOCIATION_PROVIDERS"></span>Поставщики ассоциаций
</dt> <dd>

Сведения о записи и регистрации поставщика взаимосвязей. Поставщики ассоциаций используются для предоставления стандартных профилей, таких как профиль питания. Дополнительные сведения см. в разделе [запись поставщика взаимосвязей для взаимодействия](writing-an-association-provider-for-interop.md).

</dd> <dt>

<span id="Optional_feature_status"></span><span id="optional_feature_status"></span><span id="OPTIONAL_FEATURE_STATUS"></span>Необязательное состояние компонента
</dt> <dd>

WMI реализовала класс [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) . Этот класс запрашивает и возвращает состояние дополнительных компонентов, имеющихся на компьютере. примеры запросов с использованием Windows PowerShell см. [в разделе запрос состояния дополнительных функций](querying-the-status-of-optional-features.md).

</dd> <dt>

<span id="Changing_the_default_behavior_for_the_AutoRestore_repository_feature"></span><span id="changing_the_default_behavior_for_the_autorestore_repository_feature"></span><span id="CHANGING_THE_DEFAULT_BEHAVIOR_FOR_THE_AUTORESTORE_REPOSITORY_FEATURE"></span>Изменение поведения по умолчанию для функции репозитория автовосстановления
</dt> <dd>

В WMI имеется новый раздел реестра для включения или отключения функции автоматического восстановления репозитория. Дополнительные сведения см. в разделе раздел [реестра для конфигурации репозитория](registry-key-for-repository-configuration.md).

</dd> <dt>

<span id="New__PowerShell_command_classes"></span><span id="new__powershell_command_classes"></span><span id="NEW__POWERSHELL_COMMAND_CLASSES"></span>новые классы команд Windows PowerShell
</dt> <dd>

командлеты Windows PowerShell позволяют пользователям выполнять комплексные задачи, необходимые для управления локальными и удаленными компьютерами. Дополнительные сведения см. в разделе [управляемый Справочник по классам команд WMI PowerShell](managed-reference-for-wmi-powershell-command-classes.md).

</dd> <dt>

<span id="New_mechanism_to_connect_to_remote_computers"></span><span id="new_mechanism_to_connect_to_remote_computers"></span><span id="NEW_MECHANISM_TO_CONNECT_TO_REMOTE_COMPUTERS"></span>Новый механизм подключения к удаленным компьютерам
</dt> <dd>

Windows PowerShell предоставляет простой механизм подключения к инструментарию WMI на удаленном компьютере. Дополнительные сведения см. в статье [Подключение к WMI на удаленном компьютере с помощью PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).

</dd> <dt>

<span id="Changes_to_the_software_licensing_classes"></span><span id="changes_to_the_software_licensing_classes"></span><span id="CHANGES_TO_THE_SOFTWARE_LICENSING_CLASSES"></span>Изменения в классах лицензирования программного обеспечения
</dt> <dd>

[Классы лицензирования программного обеспечения](/previous-versions/windows/desktop/sppwmi/software-license-provider-) имеют новые методы и свойства для предоставления дополнительных данных о лицензировании программного обеспечения. Кроме того, добавлен класс [**софтварелиценсингтокенактиватионлиценсе**](/previous-versions/windows/desktop/sppwmi/softwarelicensingtokenactivationlicense) .

</dd> <dt>

<span id="New_power_metering_and_budgeting_classes"></span><span id="new_power_metering_and_budgeting_classes"></span><span id="NEW_POWER_METERING_AND_BUDGETING_CLASSES"></span>Новые классы измерения питания и бюджетирования
</dt> <dd>

[Классы управления питанием и бюджетированием](/previous-versions/windows/desktop/powermeterprov/power-meter-provider-) являются основным интерфейсом для запроса информации о Power измерителя из базовых показателей питания в системе.

</dd> <dt>

<span id="New_power_policy_classes"></span><span id="new_power_policy_classes"></span><span id="NEW_POWER_POLICY_CLASSES"></span>Новые классы политики управления питанием
</dt> <dd>

[Классы политики управления питанием](/previous-versions/windows/desktop/powerwmiprov/power-policy-provider-) позволяют удаленно управлять всеми инфраструктурами политик электропитания.

</dd> <dt>

<span id="Changes_to_the_Win32_ServerFeature_class"></span><span id="changes_to_the_win32_serverfeature_class"></span><span id="CHANGES_TO_THE_WIN32_SERVERFEATURE_CLASS"></span>Изменения в классе [**Win32 \_ ServerFeature**](win32-serverfeature.md)
</dt> <dd>

Свойство **ID** объекта [**Win32 \_ ServerFeature**](win32-serverfeature.md) было обновлено.

</dd> </dl>

дополнительные сведения о новых возможностях в предыдущих версиях операционной системы см. в статье [новые возможности Windows Vista](what-s-new-in-windows-vista.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения об инструментарии WMI](about-wmi.md)
</dt> </dl>

 

 
