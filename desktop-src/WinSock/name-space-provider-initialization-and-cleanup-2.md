---
description: Использование Нспстартуп и Нспклеануп для инициализации поставщика пространства имен и очистки в списке SPI для сокетов Windows (Winsock).
ms.assetid: c9f55845-190d-440f-8b27-1be9585137e2
title: Инициализация и очистка поставщика пространства имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fedd7b40d79e755262df581c92e1fe3bdbfb06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541543"
---
# <a name="namespace-provider-initialization-and-cleanup"></a><span data-ttu-id="18c56-103">Инициализация и очистка поставщика пространства имен</span><span class="sxs-lookup"><span data-stu-id="18c56-103">Namespace Provider Initialization and Cleanup</span></span>

-   [<span data-ttu-id="18c56-104">**нспстартуп**</span><span class="sxs-lookup"><span data-stu-id="18c56-104">**NSPStartup**</span></span>](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup)
-   [<span data-ttu-id="18c56-105">**нспклеануп**</span><span class="sxs-lookup"><span data-stu-id="18c56-105">**NSPCleanup**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup)

<span data-ttu-id="18c56-106">Как и в случае с транспортным SPI, поставщик пространства имен инициализируется вызовом [**нспстартуп**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) и завершается окончательным вызовом [**нспклеануп**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span><span class="sxs-lookup"><span data-stu-id="18c56-106">As is the case for the transport SPI, a namespace provider is initialized with a call to [**NSPStartup**](/windows/desktop/api/Ws2spi/nf-ws2spi-nspstartup) and is terminated with a final call to [**NSPCleanup**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspcleanup).</span></span> <span data-ttu-id="18c56-107">Вызовы функции Startup могут быть вложенными, но они будут сопоставляться с помощью соответствующих вызовов функции Cleanup.</span><span class="sxs-lookup"><span data-stu-id="18c56-107">Calls to the startup function may be nested, but will be matched by corresponding calls to the cleanup function.</span></span> <span data-ttu-id="18c56-108">Поставщик должен использовать подсчет ссылок, чтобы определить, когда произошло окончательное обращение к **нспклеануп** .</span><span class="sxs-lookup"><span data-stu-id="18c56-108">A provider should employ reference counting to determine when the final call to **NSPCleanup** has occurred.</span></span>

 

 



