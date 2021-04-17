---
description: В Windows XP позднее для настройки IPv4 и управления им предоставляется новое средство командной строки. В этом средстве используется \# команда &0034; netsh interface ip&\# 0034; для настройки и управления IPv4.
ms.assetid: d27eb0c2-4ae0-42d1-b92e-055a1c232e1c
title: Использование IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f759d938ebebbc0ddfbb2326dfb10932c16310a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703022"
---
# <a name="using-ipv6"></a><span data-ttu-id="afa38-104">Использование IPv6</span><span class="sxs-lookup"><span data-stu-id="afa38-104">Using IPv6</span></span>

<span data-ttu-id="afa38-105">В Windows XP позднее для настройки IPv4 и управления им предоставляется новое средство командной строки.</span><span class="sxs-lookup"><span data-stu-id="afa38-105">On Windows XP a later, a new command-line tool is provided for configuring and managing IPv4.</span></span> <span data-ttu-id="afa38-106">Это средство использует команду netsh interface IP для настройки протокола IPv4 и управления им.</span><span class="sxs-lookup"><span data-stu-id="afa38-106">This tool uses the "netsh interface ip" command for configuring and managing IPv4.</span></span>

<span data-ttu-id="afa38-107">В Windows XP с пакетом обновления 1 (SP1) и более поздних версиях это новое средство командной строки было усовершенствовано для поддержки настройки и управления IPv6.</span><span class="sxs-lookup"><span data-stu-id="afa38-107">On Windows XP with Service Pack 1 (SP1) and later, this new command-line tool was enhanced to support the configuration and management of IPv6.</span></span> <span data-ttu-id="afa38-108">Это усовершенствованное средство — команда netsh interface IPv6.</span><span class="sxs-lookup"><span data-stu-id="afa38-108">This enhanced tool is the "netsh interface ipv6" command.</span></span> <span data-ttu-id="afa38-109">Изменения конфигурации, выполненные с помощью команд Netsh.exe, являются постоянными и не теряются при перезапуске компьютера или протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="afa38-109">Configuration changes made using the Netsh.exe commands are permanent and are not lost when the computer or the IPv6 protocol is restarted.</span></span>

<span data-ttu-id="afa38-110">Следующая команда доступна в Windows XP с пакетом обновления 1 (SP1) и более поздних версий для запроса и настройки IPv6 на локальном компьютере:</span><span class="sxs-lookup"><span data-stu-id="afa38-110">The following command is available on Windows XP with SP1 and later to query and configure IPv6 on a local computer:</span></span>

-   [<span data-ttu-id="afa38-111">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="afa38-111">Netsh.exe</span></span>](netsh-exe.md)

<span data-ttu-id="afa38-112">До выхода Windows XP с пакетом обновления 1 (SP1) Конфигурация IPv6 и управление использовали несколько старых программ командной строки для настройки IPv6 и управления им.</span><span class="sxs-lookup"><span data-stu-id="afa38-112">Prior to Windows XP with Service Pack 1 (SP1), IPv6 configuration and management used several older command-line tools to configure and manage IPv6.</span></span> <span data-ttu-id="afa38-113">При использовании этих старых средств изменения IPv6 не являются постоянными и теряются при перезапуске компьютера или протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="afa38-113">Using these older tools, the IPv6 changes are not permanent and are lost when the computer or the IPv6 protocol was restarted.</span></span>

<span data-ttu-id="afa38-114">В Windows XP доступны следующие более старые команды</span><span class="sxs-lookup"><span data-stu-id="afa38-114">The following older commands are available on Windows XP</span></span>

-   [<span data-ttu-id="afa38-115">Net.exe</span><span class="sxs-lookup"><span data-stu-id="afa38-115">Net.exe</span></span>](net-exe-2.md)
-   [<span data-ttu-id="afa38-116">Ipv6.exe</span><span class="sxs-lookup"><span data-stu-id="afa38-116">Ipv6.exe</span></span>](ipv6-exe-2.md)
-   [<span data-ttu-id="afa38-117">Ipsec6.exe</span><span class="sxs-lookup"><span data-stu-id="afa38-117">Ipsec6.exe</span></span>](ipsec6-exe-2.md)

<span data-ttu-id="afa38-118">Эти старые средства были также предоставлены в предварительной версии технологии IPv6 для Windows 2000</span><span class="sxs-lookup"><span data-stu-id="afa38-118">These older tools were also provided in the IPv6 Technology Preview for Windows 2000</span></span>

<span data-ttu-id="afa38-119">Изменения конфигурации, использующие эти старые средства, можно сохранить, разместив их в виде командных строк в файле командного сценария (. cmd), который выполняется после перезагрузки компьютера или протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="afa38-119">Configuration changes using these older tools could be maintained by placing them as command lines in a command script file (.cmd) that is run after restarting the computer or the IPv6 protocol.</span></span> <span data-ttu-id="afa38-120">Чтобы восстановить изменения конфигурации после перезапуска, можно было использовать запланированные задачи Windows для запуска CMD-файла при запуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="afa38-120">To reinstate configuration changes automatically after restarting, is was possible to use the Windows Scheduled Tasks to run the .cmd file when the computer starts.</span></span>

<span data-ttu-id="afa38-121">Эти старые средства не предоставляются в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="afa38-121">These older tools are not provided on Windows Server 2003 and later.</span></span> <span data-ttu-id="afa38-122">Средство "netsh interface IPv6" предназначено для настройки IPv6 и управления им из командной строки в Windows Server 2003 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="afa38-122">The "netsh interface ipv6" tool is provided for configuring and managing IPv6 from the command-line on Windows Server 2003 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="afa38-123">См. также</span><span class="sxs-lookup"><span data-stu-id="afa38-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="afa38-124">Протокол IP версии 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="afa38-124">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="afa38-125">Рекомендации по IPv6 для приложений Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="afa38-125">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="afa38-126">Предварительный просмотр технологии IPv6 для Windows 2000</span><span class="sxs-lookup"><span data-stu-id="afa38-126">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> </dl>

 

 



