---
title: IP-адреса и имена компьютеров
description: Небезопасно предполагать, что имя компьютера или IP-адрес , назначенные компьютеру, связаны с одним пользователем, так как на сервере узла сеансов удаленных рабочих столов могут одновременно находиться несколько пользователей.
ms.assetid: 17cfd14e-1fff-4154-89a6-8dbbf19a6cae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574ab1ca0ae10996212fc555b22c2c21663c4b1e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338889"
---
# <a name="ip-addresses-and-computer-names"></a><span data-ttu-id="035ea-103">IP-адреса и имена компьютеров</span><span class="sxs-lookup"><span data-stu-id="035ea-103">IP addresses and computer names</span></span>

<span data-ttu-id="035ea-104">Несколько пользователей могут одновременно войти в систему на сервере узла сеансов удаленный рабочий стол (удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="035ea-104">Multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="035ea-105">Следовательно, нельзя считать, что имя компьютера или IP-адрес, назначенный компьютеру, связаны с одним пользователем.</span><span class="sxs-lookup"><span data-stu-id="035ea-105">Consequently, it is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user.</span></span> <span data-ttu-id="035ea-106">Это отличается от среды Windows с одним пользователем, в которой только один пользователь вошел в систему одновременно.</span><span class="sxs-lookup"><span data-stu-id="035ea-106">This differs from a single-user Windows environment, in which only one user is logged on at a time.</span></span>

<span data-ttu-id="035ea-107">Приложения, использующие имя компьютера или IP-адрес для лицензирования или способ идентификации итерации приложения в сети, не будут правильно работать в среде службы удаленных рабочих столов, так как имя компьютера или IP-адрес сервера могут быть связаны с несколькими пользователями.</span><span class="sxs-lookup"><span data-stu-id="035ea-107">Applications that use the computer name or IP address for licensing or as a means of identifying an iteration of the application on the network will not work properly in a Remote Desktop Services environment, because the server's computer name or IP address can be associated with many users.</span></span>

<span data-ttu-id="035ea-108">В среде службы удаленных рабочих столов каждый клиентский терминал или эмулятор терминала имеет отдельный IP-адрес и имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="035ea-108">In a Remote Desktop Services environment, each client terminal or terminal emulator has a separate IP address and computer name.</span></span> <span data-ttu-id="035ea-109">Чтобы получить IP-адрес и имя компьютера клиента, вызовите функцию [**втскуерисессионинформатион**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) .</span><span class="sxs-lookup"><span data-stu-id="035ea-109">To retrieve the IP address and computer name of a client, call the [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) function.</span></span> <span data-ttu-id="035ea-110">Другие функции, извлекающие эти сетевые адреса и имена компьютеров, извлекают имя и адрес сервера узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="035ea-110">Other functions that retrieve these network addresses and computer names retrieve the name and address of the RD Session Host server.</span></span> <span data-ttu-id="035ea-111">Например, функция [**предполагался сбой getcomputernameex**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) возвращает имя компьютера сервера.</span><span class="sxs-lookup"><span data-stu-id="035ea-111">For example, the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function returns the computer name of the server.</span></span>

 

 