---
description: Начиная с Windows Server 2008, поставщик компонентов сервера предоставляет сведения о том, какие компоненты сервера установлены на сервере. Этот класс позволяет администраторам выполнять инвентаризацию и управлять ролями и компонентами сервера.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Поставщик компонентов сервера
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702364"
---
# <a name="server-feature-provider"></a><span data-ttu-id="8f7fa-104">Поставщик компонентов сервера</span><span class="sxs-lookup"><span data-stu-id="8f7fa-104">Server Feature Provider</span></span>

<span data-ttu-id="8f7fa-105">Начиная с Windows Server 2008, поставщик компонентов сервера предоставляет сведения о том, какие компоненты сервера установлены на сервере.</span><span class="sxs-lookup"><span data-stu-id="8f7fa-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="8f7fa-106">Этот класс позволяет администраторам выполнять инвентаризацию и управлять ролями и компонентами сервера.</span><span class="sxs-lookup"><span data-stu-id="8f7fa-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="8f7fa-107">Роль сервера определяется как группа компонентов, предоставляющих функции для определенной области функций, таких как печать, файлы, Управление доменами и т. д.</span><span class="sxs-lookup"><span data-stu-id="8f7fa-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="8f7fa-108">Типичными ролями сервера являются файловый сервер, почтовый сервер, DNS-сервер, контроллер домена, сервер приложений и т. д.</span><span class="sxs-lookup"><span data-stu-id="8f7fa-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="8f7fa-109">Если на предприятии не запущена программа управления, сообщающая роли сервера, например Microsoft Operations Manager с установленными пакетами управления, эти сведения можно получить, запросив класс [**Win32 \_ ServerFeature**](win32-serverfeature.md) .</span><span class="sxs-lookup"><span data-stu-id="8f7fa-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="8f7fa-110">Роль сервера и сведения о компонентах с удаленных компьютеров доступны через обычные удаленные подключения WMI или с помощью службы служба удаленного управления Windows (WinRM).</span><span class="sxs-lookup"><span data-stu-id="8f7fa-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="8f7fa-111">Дополнительные сведения об удаленных DCOM-подключениях WMI см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="8f7fa-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="8f7fa-112">Дополнительные сведения о подключениях с помощью протокола [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) см. в разделе [Служба удаленного управления Windows](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="8f7fa-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="8f7fa-113">Поставщик компонентов сервера поддерживает следующие классы WMI:</span><span class="sxs-lookup"><span data-stu-id="8f7fa-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="8f7fa-114">**\_ServerFeature Win32**</span><span class="sxs-lookup"><span data-stu-id="8f7fa-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="8f7fa-115">См. также</span><span class="sxs-lookup"><span data-stu-id="8f7fa-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f7fa-116">Поставщики WMI</span><span class="sxs-lookup"><span data-stu-id="8f7fa-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
