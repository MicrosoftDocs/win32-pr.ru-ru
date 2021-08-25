---
description: в следующем списке описаны новые и обновленные функциональные области для Windows Server 2012 и Windows Server 2012 R2. дополнительные сведения о новых технологиях Windows 8 и Windows 8.1 см. в разделе технологии Windows 8 и Windows 8.1.
ms.assetid: bd8b4dd8-e0b7-4340-a6bd-1baa42d9a1dd
title: 'новые возможности: Windows Server 2012 R2 & Windows Server 2012'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df654e7c448ef4e4f6f4f1599204883cad11bf5e56ccd13c47c76d204f7587f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867508"
---
# <a name="whats-new-windows-server-2012-r2--windows-server-2012"></a>новые возможности: Windows Server 2012 R2 & Windows Server 2012

в следующем списке описаны новые и обновленные функциональные области для Windows Server 2012 и Windows Server 2012 R2. дополнительные сведения о новых технологиях Windows 8 и Windows 8.1 см. в разделе [технологии Windows 8 и Windows 8.1](/previous-versions/windows/desktop/whatsnew/windows-8-technologies).

## <a name="whats-new-for-windows-server-2012-r2"></a>новые возможности Windows Server 2012 R2

-   [Дедупликация данных](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    При дедупликации данных выполняется поиск и удаление дублирования в данных на томе, при этом гарантируется правильность и полнота данных. Применение этой функции позволяет уменьшить потребление дискового пространства. для Windows Server 2012 R2 были активированы ряд параметров и кодов ошибок, а также добавлен класс [**MSFT \_ дедупфилеметадата**](/previous-versions/windows/desktop/dedup/msft-dedupfilemetadata) .

-   [Ведение журнала инвентаризации программного обеспечения](/previous-versions/windows/desktop/sil/software-inventory-logging-portal)

    **Новинка!** ведение журнала инвентаризации программного обеспечения собирает данные лицензирования о программном обеспечении, установленном на Windows сервере, и предоставляет удаленный доступ к данным, чтобы их можно было легко объединить с помощью центра обработки данных.

-   [Целевой сервер iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    сервер цели iSCSI API предоставляет поставщики инструментарий управления Windows (WMI) (WMI) для управления сервер цели iSCSI майкрософт, такие как создание виртуальных дисков и их представление клиенту. для Windows Server 2012 R2 было добавлено несколько новых функций.

-   [Регистрация управления мобильными устройствами](../mdmreg/mobile-device-management-registration-portal.md)

    **Новинка!** Тенденция в отрасли разрабатывается в том случае, когда сотрудники подключаются к корпоративной сети и ресурсам (локально или через облако) для выполнения задач рабочей среды. Эта тенденция требует поддержки простой настройки сети и ресурсов, чтобы сотрудники могли регистрировать персональные устройства в Организации для целей работы. Приложения и технологии, поддерживающие простую настройку, должны также позволить ИТ-специалистам управлять риском, связанным с неуправляемыми устройствами, подключенными к корпоративной сети. Регистрация устройства в системе управления мобильными устройствами (MDM) регистрируется в службе управления.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell — это оболочка командной строки на основе задач и язык сценариев, разработанный специально для администрирования системы. новые средства Windows Server 2012 R2 Windows PowerShell v4 поддерживают Desired State Configuration, то есть новую платформу управления в Windows PowerShell, которая позволяет развертывать данные конфигурации и управлять ими для программных служб и управлять средой, в которой выполняются эти службы.

## <a name="whats-new-for-windows-server-2012"></a>Новые возможности для Windows Server 2012

-   [Windows Кластеризации](/previous-versions/windows/desktop/mscs/windows-clustering)

    Windows Кластеризация позволяет управлять как кластерами с балансировкой сетевой нагрузки, так и отказоустойчивыми кластерами. В этот выпуск Добавлено несколько новых функций, включая новые функции управления группами, общие свойства и интеграцию с WMI.

-   [Ведение журнала доступа пользователей](/previous-versions/windows/desktop/ual/user-access-logging)

    **Новинка!** ведение журнала доступа пользователей (UAL) — это общая платформа для Windows ролей сервера, которая сообщает о соответствующих метриках потребления. Эта платформа UAL — это базовый и важный компонент более крупного решения по управлению лицензиями.

-   [Удаленное управление Windows](../winrm/portal.md)

    С помощью удаленного управления Windows (WinRM) корпорация Майкрософт реализует стандартный протокол WS-Management, основанный на протоколе SOAP. Он удобен для брандмауэров и обеспечивает взаимодействие оборудования и операционных систем различных поставщиков. Windows Server 2012 включает в себя несколько API подключения, которые касаются взаимодействия с выполняющимися экземплярами и оболочками.

-   [Windows Инфраструктура управления](/previous-versions/windows/desktop/wmi_v2/what-s-new-in-mi)

    **Новинка!** функции инфраструктуры управления Windows (MI) представляют собой последнюю версию технологий инструментарий управления Windows (WMI) (WMI), основанную на CIM standard от DMTF (распределенная задача управления Force). MI полностью совместима с предыдущими версиями инструментария WMI и предоставляет множество функций и преимуществ, которые упрощают разработку и разработку поставщиков и клиентов проще, чем когда-либо.

-   [Дедупликация данных](/previous-versions/windows/desktop/dedup/data-deduplication-api-portal)

    **Новинка!** При дедупликации данных выполняется поиск и удаление дублирования в данных на томе, при этом гарантируется правильность и полнота данных. Применение этой функции позволяет уменьшить потребление дискового пространства.

-   [Целевой сервер iSCSI](/previous-versions/windows/desktop/iscsitarg/iscsi-software-target-api-portal)

    **Новинка!** сервер цели iSCSI API предоставляет поставщики инструментарий управления Windows (WMI) (WMI) для управления сервер цели iSCSI майкрософт, такие как создание виртуальных дисков и их представление клиенту.

-   [Поставщик NFS для WMI](/previous-versions/windows/desktop/nfswmi/wmi-provider-for-nfs-portal)

    **Новинка!** Поставщик WMI для NFS предоставляет средства управления NFS-сервером и параметрами клиентов, общими папками, сетевыми группами и клиентской группой.

-   [Автономные файлы](../devnotes/offline-files.md)

    Автономные файлы API позволяет приложениям контролировать и отслеживать поведение автономные файлы программным способом. Windows Server 2012 добавляет функции [**оффлинефилескуеристатусекс**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesquerystatusex), [**оффлинефилесстарт**](/previous-versions/windows/desktop/api/cscapi/nf-cscapi-offlinefilesstart) и [**ренамеитем**](/previous-versions/windows/desktop/offlinefiles/win32-offlinefilescache-renameitem) .

-   [Управление SMB](/previous-versions/windows/desktop/smb/smb-management-api-portal)

    **Новинка!** API управления SMB предоставляет классы и методы WMI для управления общими ресурсами и предоставления общего доступа.

-   [Server Core](/previous-versions/windows/desktop/legacy/hh846323(v=vs.85))

    Windows сервер предоставляет минимальные варианты установки сервера для компьютеров, работающих в операционной системе Windows server 2008 или более поздней версии. Windows Server 2012 предлагает Server Core как к конфигурации, так и к вариантам установки.

-   [Система архивации данных Windows Server](/previous-versions/windows/desktop/wsb/windows-server-backup-portal)

    функция cистема архивации данных Windows Server автоматически создает резервные копии и восстанавливает данные приложений. Windows Server 2012 включает API поставщика облачных резервных копий.

-   [Windows Общий доступ к рабочему столу](/previous-versions/windows/desktop/rdp/rdp-portal)

    Windows Совместный доступ к рабочему столу — это многосторонняя технология совместного использования экрана. Windows Server 2012 реализует эту технологию с помощью API дублирования Windows.

-   [Службы удаленных рабочих столов](../termserv/terminal-services-portal.md)

    Windows Совместное использование рабочего стола позволяет пользователю удаленно обращаться к экземпляру операционной системы. Windows Server 2012 включает ряд новых функций, включая дочерние сеансы, RemoteFX перенаправление носителей и клиент удаленный рабочий стол Broker.

-   [Windows PowerShell](https://msdn.microsoft.com/library/Dd835506(v=VS.85).aspx)

    Windows PowerShell — это оболочка командной строки на основе задач и язык сценариев, разработанный специально для администрирования системы. новое в Windows Server 2012, Windows PowerShell v3 поддерживает Windows PowerShell рабочий процесс, который использует преимущества Windows Workflow Foundation, чтобы обеспечить автоматизацию длительно выполняемых задач.

-   [OData управления](/powershell/scripting/developer/webservices/creating-a-management-odata-web-service?view=powershell-7&preserve-view=true)

    **Новинка!** также известные как Windows PowerShell веб-службы, управление OData, новое в Windows PowerShell v3, позволяет создавать конечную точку веб-службы ASP.NET, которая предоставляет данные управления, ацессед через Windows PowerShell команды в качестве сущностей веб-службы OData.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Server 2012 R2 на сайте TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 и Windows Server 2012 в библиотеке TechNet](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh801901(v=ws.11))
</dt> <dt>

[Windows Server 2012 R2 на Microsoft.Com](https://www.microsoft.com/evalcenter/evaluate-windows-server-2012-r2-essentials)
</dt> </dl>

 

 
