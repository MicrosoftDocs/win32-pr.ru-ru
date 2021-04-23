---
description: В этом приложении показана перезаписанная версия примеров приложений Симплек. c и Simple. c, которые корректно обрабатывают серверный код CodeIPv6-Enabled клиента с поддержкой IPv4 или IPv6.
ms.assetid: ffcbd59e-63ea-4df3-9db9-e7d4634eefeb
title: Приложение б. Независимый от IP-версии исходный код
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333e344376695122ebcd650ebf2595d70afbf7ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897361"
---
# <a name="appendix-b-ip-version-agnostic-source-code"></a><span data-ttu-id="cd2a1-103">Приложение б. Независимый от IP-версии исходный код</span><span class="sxs-lookup"><span data-stu-id="cd2a1-103">Appendix B: IP-version Agnostic Source Code</span></span>

<span data-ttu-id="cd2a1-104">В этом приложении показана перезаписанная версия примеров приложений Симплек. c и Simple. c, которые корректно обрабатывают IPv4 или IPv6.</span><span class="sxs-lookup"><span data-stu-id="cd2a1-104">This appendix illustrates a rewritten version of the Simplec.c and Simples.c sample applications that gracefully handles either IPv4 or IPv6.</span></span>

-   [<span data-ttu-id="cd2a1-105">Код клиента с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="cd2a1-105">IPv6-Enabled Client Code</span></span>](ipv6-enabled-client-code-2.md)
-   [<span data-ttu-id="cd2a1-106">Серверный код с поддержкой IPv6</span><span class="sxs-lookup"><span data-stu-id="cd2a1-106">IPv6-Enabled Server Code</span></span>](ipv6-enabled-server-code-2.md)

<span data-ttu-id="cd2a1-107">Этот код обладает рекомендации, установленные в этом руководстве по IPv6, и включает в себя, чтобы предоставить исходный код, который был успешно изменен для добавления поддержки IPv6.</span><span class="sxs-lookup"><span data-stu-id="cd2a1-107">This code exemplifies the guidelines set forth in this IPv6 guide, and is included to provide source code that has been successfully modified to add support for IPv6.</span></span> <span data-ttu-id="cd2a1-108">Этот пример намеренно прост, но предоставляет практический пример для изучения и просмотра.</span><span class="sxs-lookup"><span data-stu-id="cd2a1-108">This sample is intentionally simple, but provides a hands-on sample for perusing and reviewing.</span></span> <span data-ttu-id="cd2a1-109">Только IPv4-версия этого исходного кода предоставляется в [приложении а: исходный код только для IPv4](appendix-a-ipv4-only-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="cd2a1-109">An IPv4 only version of this source code is provided in [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md).</span></span>

<span data-ttu-id="cd2a1-110">Сравнивая исходный код в приложении A (только IPv4) и приложение б (независимо от версии IP), вы получаете представление об изменениях, необходимых для изменения приложения Windows Sockets для добавления поддержки IPv6.</span><span class="sxs-lookup"><span data-stu-id="cd2a1-110">By comparing the source code in Appendix A (IPv4 only) and Appendix B (IP-version agnostic), you get a sense of the changes necessary to modify your Windows Sockets application to add support for IPv6.</span></span>

 

 



