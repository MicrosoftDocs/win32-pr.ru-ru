---
title: Использование потока
description: Необходимо настроить и сбалансировать использование потоков приложения для многопользовательской многопроцессорной службы удаленных рабочих столов среды.
ms.assetid: 88f4e61f-4a59-4a84-8dca-fdb661835b51
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a3b432cf4960c6ec7a8e51b458b9f574663ffe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672023"
---
# <a name="thread-usage"></a><span data-ttu-id="9f340-103">Использование потока</span><span class="sxs-lookup"><span data-stu-id="9f340-103">Thread usage</span></span>

<span data-ttu-id="9f340-104">Потоки предоставляют удобный способ позволить приложению максимально увеличить использование ресурсов ЦП в системе, особенно в конфигурации с несколькими процессорами.</span><span class="sxs-lookup"><span data-stu-id="9f340-104">Threads provide a convenient way of allowing an application to maximize its usage of CPU resources in a system, especially in a multiple processor configuration.</span></span> <span data-ttu-id="9f340-105">Однако в среде службы удаленных рабочих столов несколько пользователей могут работать с многопоточными приложениями, и все потоки всех пользователей конкурируют за центральные ресурсы ЦП этой системы.</span><span class="sxs-lookup"><span data-stu-id="9f340-105">In a Remote Desktop Services environment, however, multiple users can be running multithreaded applications, and all of the threads for all of the users compete for the central CPU resources of that system.</span></span> <span data-ttu-id="9f340-106">Учитывая это, следует настроить и сбалансировать использование потоков приложения для многопользовательской, многопроцессорной службы удаленных рабочих столов среды.</span><span class="sxs-lookup"><span data-stu-id="9f340-106">With this in mind, you should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span> <span data-ttu-id="9f340-107">Хотя плохо спроектированное многопоточное приложение с неактивными и бездействующими потоками может обеспечить адекватное выполнение на клиентском компьютере, одно и то же приложение может не работать на многопользовательской службы удаленных рабочих столов сервере.</span><span class="sxs-lookup"><span data-stu-id="9f340-107">While a poorly designed multithreaded application with idle or wasted threads might perform adequately on a client computer, the same application might not perform well on a multiuser Remote Desktop Services server.</span></span>

 

 




