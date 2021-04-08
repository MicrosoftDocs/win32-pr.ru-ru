---
description: В следующем списке описаны новые и обновленные функциональные области для Windows Server 2012 и Windows Server 2012 R2. Дополнительные сведения о новых технологиях Windows 8 и Windows 8.1 см. в разделе технологии Windows 8 и Windows 8.1.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'Новые возможности: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ba276ea8256299c5e667cbb5a1d2b0872bb282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911240"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>Новые возможности: Windows Server 2012 R2 & Windows Server 2012

В следующем списке описаны новые и обновленные функциональные области для Windows Server 2012 и Windows Server 2012 R2. Дополнительные сведения о новых технологиях Windows 8 и Windows 8.1 см. в разделе [технологии Windows 8 и Windows 8.1](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>Новые возможности Windows Server 2012 R2

-   [Дедупликация данных](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    При дедупликации данных выполняется поиск и удаление дублирования в данных на томе, при этом гарантируется правильность и полнота данных. Применение этой функции позволяет уменьшить потребление дискового пространства. Для Windows Server 2012 R2 были активированы ряд параметров и кодов ошибок, а также добавлен класс [**MSFT \_ дедупфилеметадата**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) .

-   [Ведение журнала инвентаризации программного обеспечения](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Новинка!** Ведение журнала инвентаризации программного обеспечения собирает данные лицензирования о программном обеспечении, установленном на сервере Windows Server, и предоставляет удаленный доступ к данным, чтобы их можно было легко объединить с центром обработки данных.

-   [Целевой сервер iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    API сервера цели iSCSI предоставляет поставщики инструментарий управления Windows (WMI) (WMI) для управления сервером Microsoft iSCSI Target Server, такие как создание виртуальных дисков и их представление клиенту. Для Windows Server 2012 R2 было добавлено несколько новых возможностей.

-   [Регистрация управления мобильными устройствами](../mdmreg/mobile-device-management-registration-portal.md)

    **Новинка!** Тенденция в отрасли разрабатывается в том случае, когда сотрудники подключаются к корпоративной сети и ресурсам (локально или через облако) для выполнения задач рабочей среды. Эта тенденция требует поддержки простой настройки сети и ресурсов, чтобы сотрудники могли регистрировать персональные устройства в Организации для целей работы. Приложения и технологии, поддерживающие простую настройку, должны также позволить ИТ-специалистам управлять риском, связанным с неуправляемыми устройствами, подключенными к корпоративной сети. Регистрация устройства в системе управления мобильными устройствами (MDM) регистрируется в службе управления.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell — это оболочка командной строки на основе задач и язык сценариев, разработанный специально для администрирования системы. Windows PowerShell V4, впервые реализованная в Windows Server 2012 R2, поддерживает настройку требуемого состояния, которая является новой платформой управления в Windows PowerShell, которая позволяет развертывать данные конфигурации и управлять ими для программных служб и управлять средой, в которой выполняются эти службы.

## <a name="whats-new-for-windows-server-2012"></a>Новые возможности Windows Server 2012

-   [Кластеризация Windows](/previous-versions/windows/desktop/mscs/windows-clustering)

    Кластеризация Windows позволяет управлять как кластерами с балансировкой сетевой нагрузки, так и отказоустойчивыми кластерами. В этот выпуск Добавлено несколько новых функций, включая новые функции управления группами, общие свойства и интеграцию с WMI.

-   [Ведение журнала доступа пользователей](/previous-versions/windows/desktop/ual/user-access-logging)

    **Новинка!** Ведение журнала доступа пользователей (UAL) — это общая платформа для ролей Windows Server, сообщающая о соответствующих метриках потребления. Эта платформа UAL — это базовый и важный компонент более крупного решения по управлению лицензиями.

-   [Удаленное управление Windows](../winrm/portal.md)

    С помощью удаленного управления Windows (WinRM) корпорация Майкрософт реализует стандартный протокол WS-Management, основанный на протоколе SOAP. Он удобен для брандмауэров и обеспечивает взаимодействие оборудования и операционных систем различных поставщиков. Windows Server 2012 включает в себя ряд API-интерфейсов подключения, которые касаются взаимодействия с выполняющимися экземплярами и оболочками.

-   [Инфраструктура управления Windows](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Новинка!** Функции инфраструктуры управления Windows (MI) представляют собой последнюю версию технологий инструментарий управления Windows (WMI) (инструментарий WMI), основанную на CIM Standard от DMTF (распределенная задача управления Force). MI полностью совместима с предыдущими версиями инструментария WMI и предоставляет множество функций и преимуществ, которые упрощают разработку и разработку поставщиков и клиентов проще, чем когда-либо.

-   [Дедупликация данных](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Новинка!** При дедупликации данных выполняется поиск и удаление дублирования в данных на томе, при этом гарантируется правильность и полнота данных. Применение этой функции позволяет уменьшить потребление дискового пространства.

-   [Целевой сервер iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Новинка!** API сервера цели iSCSI предоставляет поставщики инструментарий управления Windows (WMI) (WMI) для управления сервером Microsoft iSCSI Target Server, такие как создание виртуальных дисков и их представление клиенту.

-   [Поставщик NFS для WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Новинка!** Поставщик WMI для NFS предоставляет средства управления NFS-сервером и параметрами клиентов, общими папками, сетевыми группами и клиентской группой.

-   [Автономные файлы](../devnotes/offline-files.md)

    Автономные файлы API позволяет приложениям контролировать и отслеживать поведение автономные файлы программным способом. Windows Server 2012 добавляет функции [**оффлинефилескуеристатусекс**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**оффлинефилесстарт**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) и [**ренамеитем**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Управление SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Новинка!** API управления SMB предоставляет классы и методы WMI для управления общими ресурсами и предоставления общего доступа.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows Server предоставляет минимальные варианты установки сервера для компьютеров, работающих под управлением операционной системы Windows Server 2008 или более поздней версии. Windows Server 2012 предлагает Server Core как к конфигурации, так и к вариантам установки.

-   [Система архивации данных Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    Функция cистема архивации данных Windows Server автоматически создает резервные копии и восстанавливает данные приложений. Windows Server 2012 включает API поставщика облачных резервных копий.

-   [Общий доступ к рабочему столу Windows](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Desktop Sharing — это многосторонняя технология совместного использования экрана. В Windows Server 2012 эта технология реализована с помощью API дублирования Windows.

-   [Службы удаленных рабочих столов](../termserv/terminal-services-portal.md)

    Общий доступ к рабочему столу Windows позволяет пользователю осуществлять удаленный доступ к экземпляру операционной системы. Windows Server 2012 включает ряд новых функций, включая дочерние сеансы, перенаправление носителей RemoteFX и клиент удаленный рабочий стол Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell — это оболочка командной строки на основе задач и язык сценариев, разработанный специально для администрирования системы. Новое в Windows Server 2012, Windows PowerShell v3 поддерживает рабочий процесс Windows PowerShell, который использует преимущества Windows Workflow Foundation, чтобы обеспечить автоматизацию длительно выполняемых задач.

-   [OData управления](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Новинка!** Также известные как веб-службы Windows PowerShell, управление OData, новое в Windows PowerShell v3, позволяет создавать конечную точку веб-службы ASP.NET, которая предоставляет данные управления, ацессед с помощью команд Windows PowerShell, как сущности веб-службы OData.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Windows Server 2012 R2 на сайте TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 и Windows Server 2012 в библиотеке TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 на Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
