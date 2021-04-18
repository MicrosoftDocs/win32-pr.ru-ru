---
description: Сокеты Windows 1,1 предоставили механизм асинхронного выбора для предоставления сетевых событий, не использующих опрос или блокировку.
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Сообщения Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711381"
---
# <a name="windows-messages"></a><span data-ttu-id="7639a-103">Сообщения Windows</span><span class="sxs-lookup"><span data-stu-id="7639a-103">Windows Messages</span></span>

<span data-ttu-id="7639a-104">Сокеты Windows 1,1 предоставили механизм асинхронного выбора для предоставления сетевых событий, не использующих опрос или блокировку.</span><span class="sxs-lookup"><span data-stu-id="7639a-104">Windows Sockets 1.1 introduced the async-select mechanism to provide network event indications that did not involve either polling or blocking.</span></span> <span data-ttu-id="7639a-105">Функция [**вспасинкселект**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) используется для регистрации интереса в одном или нескольких сетевых событиях, как указано в предыдущем примере, и для предоставления маркера окна, используемого для уведомления.</span><span class="sxs-lookup"><span data-stu-id="7639a-105">The [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) function is used to register an interest in one or more network events as listed in the preceding, and supply a window handle to be used for notification.</span></span> <span data-ttu-id="7639a-106">При возникновении назначенного сетевого события в указанное окно отправляется указанное клиентом сообщение Windows.</span><span class="sxs-lookup"><span data-stu-id="7639a-106">When a nominated network event occurs, a client-specified Windows message is sent to the indicated window.</span></span> <span data-ttu-id="7639a-107">Для выполнения этой задачи поставщик услуг должен использовать функцию [**впупостмессаже**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) .</span><span class="sxs-lookup"><span data-stu-id="7639a-107">The service provider must use the [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) function to accomplish this.</span></span>

<span data-ttu-id="7639a-108">В Windows это может быть не самым эффективным механизмом уведомлений и неудобным для управляющих программ и служб, которые не хотят открывать окна.</span><span class="sxs-lookup"><span data-stu-id="7639a-108">In Windows, this may not be the most efficient notification mechanism, and is inconvenient for daemons and services that do not want to open any windows.</span></span> <span data-ttu-id="7639a-109">Для решения этой проблемы появился механизм сигнализации объекта событий, описанный в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7639a-109">The event object signaling mechanism described in the following is introduced to solve this problem.</span></span>

 

 
