---
description: Команды Netsh для IPv6 предоставляют программу командной строки, которую можно использовать для запроса и настройки интерфейсов IPv6, адресов, кэшей и маршрутов. Команды netsh interface IPv6 поддерживаются в Windows XP с пакетом обновления 1 (SP1) и более поздних версий.
ms.assetid: 68e17a55-4dd5-40cd-8996-25fa278ddd19
title: Netsh.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aab092def0dc12071ee9dd62fd7554a53c9a7f97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144995"
---
# <a name="netshexe"></a><span data-ttu-id="9667a-104">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="9667a-104">Netsh.exe</span></span>

<span data-ttu-id="9667a-105">Команды Netsh для IPv6 предоставляют программу командной строки, которую можно использовать для запроса и настройки интерфейсов IPv6, адресов, кэшей и маршрутов.</span><span class="sxs-lookup"><span data-stu-id="9667a-105">The Netsh commands for IPv6 provide a command-line tool that you can use to query and configure IPv6 interfaces, address, caches, and routes.</span></span> <span data-ttu-id="9667a-106">Команды netsh interface IPv6 поддерживаются в Windows XP с пакетом обновления 1 (SP1) и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="9667a-106">The Netsh interface IPv6 commands are supported on Windows XP with Service Pack 1 (SP1) and later.</span></span>

<span data-ttu-id="9667a-107">Netsh.exe имеет множество подкоманд для IPv6.</span><span class="sxs-lookup"><span data-stu-id="9667a-107">Netsh.exe has many subcommands for IPv6.</span></span> <span data-ttu-id="9667a-108">Полный список параметров для netsh interface IPv6 можно найти в командной строке в Windows XP с пакетом обновления 1 (SP1) и более поздних версий, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9667a-108">A complete list of options for Netsh Interface IPv6 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="9667a-109">**netsh interface IPv6/?**</span><span class="sxs-lookup"><span data-stu-id="9667a-109">**netsh interface ipv6 /?**</span></span>

<span data-ttu-id="9667a-110">Документация по всем командам **netsh** для IPv6 также доступна в Интернете на сайте TechNet.</span><span class="sxs-lookup"><span data-stu-id="9667a-110">Documentation on all of the **netsh** commands for IPv6 is also available online on Technet.</span></span> <span data-ttu-id="9667a-111">Дополнительные сведения о **netsh** в Windows Server 2008 см. в разделе [команды Netsh для интерфейса (IPv4 и IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9667a-111">For more information on **netsh** on Windows Server 2008, please see [Netsh commands for Interface (IPv4 and IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)).</span></span> <span data-ttu-id="9667a-112">Дополнительные сведения о **netsh** в Windows Server 2003 см. в разделе [команды Netsh для интерфейса IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9667a-112">For more information on **netsh** on Windows Server 2003, please see [Netsh commands for Interface IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).</span></span>

<span data-ttu-id="9667a-113">Ниже приведены несколько часто используемых команд для IPv6, хотя поддерживаются и многие другие команды.</span><span class="sxs-lookup"><span data-stu-id="9667a-113">The following are a few commonly used commands for IPv6, although many other commands are supported:</span></span>

<dl> <dt>

<span data-ttu-id="9667a-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Добавление адреса netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-114"><span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**netsh interface ipv6 add address**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-115">Добавляет IPv6-адрес к определенному интерфейсу на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-115">Adds an IPv6 address to a specific interface on the local computer.</span></span> <span data-ttu-id="9667a-116">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-116">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**Добавление DNS для netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-117"><span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**netsh interface ipv6 add dns**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-118">Добавляет адрес IPv6 DNS-сервера в статически настроенный список DNS-серверов для указанного интерфейса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-118">Adds a DNS server IPv6 address to the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="9667a-119">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-119">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**Добавление маршрута netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-120"><span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**netsh interface ipv6 add route**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-121">Добавляет маршрут для указанного IPv6-адреса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-121">Adds a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="9667a-122">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-122">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**IPv6-адрес удаления интерфейса Netsh**</span><span class="sxs-lookup"><span data-stu-id="9667a-123"><span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**netsh interface ipv6 delete address**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-124">Удаляет указанный IPv6-адрес из указанного интерфейса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-124">Deletes the specified IPv6 address from a specific interface on the local computer.</span></span> <span data-ttu-id="9667a-125">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-125">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 удаление DNS**</span><span class="sxs-lookup"><span data-stu-id="9667a-126"><span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface ipv6 delete dns**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-127">Удаляет адрес DNS-сервера из статически настроенного списка DNS-серверов для указанного интерфейса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-127">Deletes a DNS server address from the statically-configured list of DNS servers for the specified interface on the local computer.</span></span> <span data-ttu-id="9667a-128">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-128">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**интерфейс удаления netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-129"><span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**netsh interface ipv6 delete interface**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-130">Удаляет указанный интерфейс из стека IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-130">Deletes a specified interface from the IPv6 stack on the local computer.</span></span> <span data-ttu-id="9667a-131">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-131">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**Удаление маршрута netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-132"><span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**netsh interface ipv6 delete route**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-133">Удаляет маршрут для указанного IPv6-адреса на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-133">Deletes a route for a specified IPv6 prefix address on the local computer.</span></span> <span data-ttu-id="9667a-134">Эта команда содержит параметры подпараметров, которые необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-134">This command has suboption parameters that must to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**дамп Netsh интерфейса IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-135"><span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**netsh interface ipv6 dump**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-136">Создает скрипт, содержащий команды для создания текущей конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9667a-136">Creates a script that contains the commands to create the current configuration.</span></span> <span data-ttu-id="9667a-137">Сохранив этот скрипт в файл, с его помощью можно восстановить параметры конфигурации.</span><span class="sxs-lookup"><span data-stu-id="9667a-137">If saved to a file, this script can be used to restore altered configuration settings.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**Установка netsh interface IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-138"><span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**netsh interface ipv6 install**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-139">Устанавливает протокол IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-139">Installs the IPv6 protocol on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**обновление интерфейса Netsh IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-140"><span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**netsh interface ipv6 renew**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-141">Перезапускает интерфейсы IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-141">Restarts the IPv6 interfaces on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**сброс интерфейса Netsh IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-142"><span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**netsh interface ipv6 reset**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-143">Сбрасывает состояние конфигурации IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-143">Resets the IPv6 configuration state on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface IPv6 показывать глобальное**</span><span class="sxs-lookup"><span data-stu-id="9667a-144"><span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface ipv6 show global**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-145">Отображает глобальные параметры конфигурации для IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-145">Displays the global configuration parameters for IPv6 on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**Интерфейс Netsh IPv6 демонстрация адреса**</span><span class="sxs-lookup"><span data-stu-id="9667a-146"><span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**netsh interface ipv6 show address**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-147">Отображает все IPv6-адреса или все IPv6-адреса в определенном интерфейсе на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-147">Displays all IPv6 addresses or all IPv6 addresses on a specific interface on the local computer.</span></span> <span data-ttu-id="9667a-148">Эта команда содержит параметры подпараметров, которые, возможно, необходимо указать.</span><span class="sxs-lookup"><span data-stu-id="9667a-148">This command has suboption parameters that may need to be specified.</span></span>

</dd> <dt>

<span data-ttu-id="9667a-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**Удаление интерфейса Netsh IPv6**</span><span class="sxs-lookup"><span data-stu-id="9667a-149"><span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**netsh interface ipv6 uninstall**</span></span>
</dt> <dd>

<span data-ttu-id="9667a-150">Удаляет протокол IPv6 на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="9667a-150">Uninstalls the IPv6 protocol on the local computer.</span></span>

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a><span data-ttu-id="9667a-151">Команды Netsh для IPv4</span><span class="sxs-lookup"><span data-stu-id="9667a-151">Netsh commands for IPv4</span></span>

<span data-ttu-id="9667a-152">Аналогичные команды netsh доступны для IPv4.</span><span class="sxs-lookup"><span data-stu-id="9667a-152">Similar Netsh commands are available for IPv4.</span></span> <span data-ttu-id="9667a-153">Полный список параметров команд Netsh для использования с IPv4 можно найти в командной строке в Windows XP с пакетом обновления 1 (SP1) и более поздних версий, введя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9667a-153">A complete list of options for Netsh commands for use with IPv4 is available from the command prompt on Windows XP with SP1 and later by typing the following:</span></span>

<span data-ttu-id="9667a-154">**netsh interface IP/?**</span><span class="sxs-lookup"><span data-stu-id="9667a-154">**netsh interface ip /?**</span></span>

<span data-ttu-id="9667a-155">Документация по всем командам Netsh для IPv4 также доступна в Интернете на сайте TechNet.</span><span class="sxs-lookup"><span data-stu-id="9667a-155">Documentation on all of the Netsh commands for IPv4 is also available online on Technet.</span></span> <span data-ttu-id="9667a-156">Дополнительные сведения см. в разделе [команды Netsh для интерфейса IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10)) .</span><span class="sxs-lookup"><span data-stu-id="9667a-156">For more information, please see [Netsh commands for Interface IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10))</span></span>

 

 
