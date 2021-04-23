---
description: Net.exe можно использовать для завершения и запуска протокола IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897321"
---
# <a name="netexe"></a><span data-ttu-id="98027-103">Net.exe</span><span class="sxs-lookup"><span data-stu-id="98027-103">Net.exe</span></span>

<span data-ttu-id="98027-104">Net.exe можно использовать для завершения и запуска протокола IPv6.</span><span class="sxs-lookup"><span data-stu-id="98027-104">Net.exe can be used to stop and start the IPv6 protocol.</span></span> <span data-ttu-id="98027-105">Перезапуск IPv6 повторно инициализирует протокол, как если бы компьютер перезапускался, что может изменить номера интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="98027-105">Restarting IPv6 reinitializes the protocol as if the computer were restarting, which may change interface numbers.</span></span> <span data-ttu-id="98027-106">Net.exe имеет много подкоманд.</span><span class="sxs-lookup"><span data-stu-id="98027-106">Net.exe has many subcommands.</span></span> <span data-ttu-id="98027-107">Следующие команды относятся к протоколу IPv6:</span><span class="sxs-lookup"><span data-stu-id="98027-107">The following commands are relevant to IPv6:</span></span>

<dl> <dt>

<span data-ttu-id="98027-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET tcpip6**</span><span class="sxs-lookup"><span data-stu-id="98027-108"><span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="98027-109">Останавливает протокол IPv6 и выгружает его из памяти.</span><span class="sxs-lookup"><span data-stu-id="98027-109">Stops the IPv6 protocol and unloads it from memory.</span></span> <span data-ttu-id="98027-110">Эта команда завершается ошибкой, если открыты какие-либо сокеты IPv6.</span><span class="sxs-lookup"><span data-stu-id="98027-110">This command fails if any IPv6 sockets are open.</span></span>

</dd> <dt>

<span data-ttu-id="98027-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET start tcpip6**</span><span class="sxs-lookup"><span data-stu-id="98027-111"><span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**</span></span>
</dt> <dd>

<span data-ttu-id="98027-112">Запускает протокол IPv6, если он был остановлен.</span><span class="sxs-lookup"><span data-stu-id="98027-112">Starts the IPv6 protocol if it was stopped.</span></span> <span data-ttu-id="98027-113">Если в каталоге% SystemRoot% System32 имеется новый файл драйвера Tcpip6.sys \\ , он \\ загружается.</span><span class="sxs-lookup"><span data-stu-id="98027-113">If a new Tcpip6.sys driver file is present in the %systemroot%\\System32\\Drivers directory, that driver file is loaded.</span></span>

</dd> </dl>

 

 



