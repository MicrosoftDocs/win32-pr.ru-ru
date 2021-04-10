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
# <a name="netshexe"></a>Netsh.exe

Команды Netsh для IPv6 предоставляют программу командной строки, которую можно использовать для запроса и настройки интерфейсов IPv6, адресов, кэшей и маршрутов. Команды netsh interface IPv6 поддерживаются в Windows XP с пакетом обновления 1 (SP1) и более поздних версий.

Netsh.exe имеет множество подкоманд для IPv6. Полный список параметров для netsh interface IPv6 можно найти в командной строке в Windows XP с пакетом обновления 1 (SP1) и более поздних версий, введя следующую команду:

**netsh interface IPv6/?**

Документация по всем командам **netsh** для IPv6 также доступна в Интернете на сайте TechNet. Дополнительные сведения о **netsh** в Windows Server 2008 см. в разделе [команды Netsh для интерфейса (IPv4 и IPv6)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770948(v=ws.10)). Дополнительные сведения о **netsh** в Windows Server 2003 см. в разделе [команды Netsh для интерфейса IPv6](/previous-versions/windows/it-pro/windows-server-2003/cc740203(v=ws.10)).

Ниже приведены несколько часто используемых команд для IPv6, хотя поддерживаются и многие другие команды.

<dl> <dt>

<span id="netsh_interface_ipv6_add_address"></span><span id="NETSH_INTERFACE_IPV6_ADD_ADDRESS"></span>**Добавление адреса netsh interface IPv6**
</dt> <dd>

Добавляет IPv6-адрес к определенному интерфейсу на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_add_dns"></span><span id="NETSH_INTERFACE_IPV6_ADD_DNS"></span>**Добавление DNS для netsh interface IPv6**
</dt> <dd>

Добавляет адрес IPv6 DNS-сервера в статически настроенный список DNS-серверов для указанного интерфейса на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_add_route"></span><span id="NETSH_INTERFACE_IPV6_ADD_ROUTE"></span>**Добавление маршрута netsh interface IPv6**
</dt> <dd>

Добавляет маршрут для указанного IPv6-адреса на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_address"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ADDRESS"></span>**IPv6-адрес удаления интерфейса Netsh**
</dt> <dd>

Удаляет указанный IPv6-адрес из указанного интерфейса на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_dns"></span><span id="NETSH_INTERFACE_IPV6_DELETE_DNS"></span>**netsh interface IPv6 удаление DNS**
</dt> <dd>

Удаляет адрес DNS-сервера из статически настроенного списка DNS-серверов для указанного интерфейса на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_interface"></span><span id="NETSH_INTERFACE_IPV6_DELETE_INTERFACE"></span>**интерфейс удаления netsh interface IPv6**
</dt> <dd>

Удаляет указанный интерфейс из стека IPv6 на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_delete_route"></span><span id="NETSH_INTERFACE_IPV6_DELETE_ROUTE"></span>**Удаление маршрута netsh interface IPv6**
</dt> <dd>

Удаляет маршрут для указанного IPv6-адреса на локальном компьютере. Эта команда содержит параметры подпараметров, которые необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_dump"></span><span id="NETSH_INTERFACE_IPV6_DUMP"></span>**дамп Netsh интерфейса IPv6**
</dt> <dd>

Создает скрипт, содержащий команды для создания текущей конфигурации. Сохранив этот скрипт в файл, с его помощью можно восстановить параметры конфигурации.

</dd> <dt>

<span id="netsh_interface_ipv6_install"></span><span id="NETSH_INTERFACE_IPV6_INSTALL"></span>**Установка netsh interface IPv6**
</dt> <dd>

Устанавливает протокол IPv6 на локальном компьютере.

</dd> <dt>

<span id="netsh_interface_ipv6_renew"></span><span id="NETSH_INTERFACE_IPV6_RENEW"></span>**обновление интерфейса Netsh IPv6**
</dt> <dd>

Перезапускает интерфейсы IPv6 на локальном компьютере.

</dd> <dt>

<span id="netsh_interface_ipv6_reset"></span><span id="NETSH_INTERFACE_IPV6_RESET"></span>**сброс интерфейса Netsh IPv6**
</dt> <dd>

Сбрасывает состояние конфигурации IPv6 на локальном компьютере.

</dd> <dt>

<span id="netsh_interface_ipv6_show_global"></span><span id="NETSH_INTERFACE_IPV6_SHOW_GLOBAL"></span>**netsh interface IPv6 показывать глобальное**
</dt> <dd>

Отображает глобальные параметры конфигурации для IPv6 на локальном компьютере.

</dd> <dt>

<span id="netsh_interface_ipv6_show_address"></span><span id="NETSH_INTERFACE_IPV6_SHOW_ADDRESS"></span>**Интерфейс Netsh IPv6 демонстрация адреса**
</dt> <dd>

Отображает все IPv6-адреса или все IPv6-адреса в определенном интерфейсе на локальном компьютере. Эта команда содержит параметры подпараметров, которые, возможно, необходимо указать.

</dd> <dt>

<span id="netsh_interface_ipv6_uninstall"></span><span id="NETSH_INTERFACE_IPV6_UNINSTALL"></span>**Удаление интерфейса Netsh IPv6**
</dt> <dd>

Удаляет протокол IPv6 на локальном компьютере.

</dd> </dl>

## <a name="netsh-commands-for-ipv4"></a>Команды Netsh для IPv4

Аналогичные команды netsh доступны для IPv4. Полный список параметров команд Netsh для использования с IPv4 можно найти в командной строке в Windows XP с пакетом обновления 1 (SP1) и более поздних версий, введя следующую команду:

**netsh interface IP/?**

Документация по всем командам Netsh для IPv4 также доступна в Интернете на сайте TechNet. Дополнительные сведения см. в разделе [команды Netsh для интерфейса IP](/previous-versions/windows/it-pro/windows-server-2003/cc738592(v=ws.10)) .

 

 
