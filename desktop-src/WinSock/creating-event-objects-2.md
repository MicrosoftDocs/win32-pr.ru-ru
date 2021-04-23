---
description: Ws2 \_32.dll предоставляет средства для создания объектов событий как для приложений, так и для поставщиков служб, хотя в большинстве случаев объекты событий будут создаваться приложениями.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Создание объектов событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692292"
---
# <a name="creating-event-objects"></a><span data-ttu-id="0a476-103">Создание объектов событий</span><span class="sxs-lookup"><span data-stu-id="0a476-103">Creating Event Objects</span></span>

<span data-ttu-id="0a476-104">Ws2 \_32.dll предоставляет средства для создания объектов событий как для приложений, так и для поставщиков служб, хотя в большинстве случаев объекты событий будут создаваться приложениями.</span><span class="sxs-lookup"><span data-stu-id="0a476-104">The Ws2\_32.dll provides facilities for event object creation to both applications and service providers, although in most instances event objects will be created by applications.</span></span> <span data-ttu-id="0a476-105">Службы объектов событий становятся доступными поставщикам служб Windows Sockets через [**впукреативент**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) просто как удобный механизм для любой внутренней обработки, которая может выиграть от такой же.</span><span class="sxs-lookup"><span data-stu-id="0a476-105">Event object services are made available to Windows Sockets service providers through [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simply as a convenience mechanism for any internal processing that may benefit from same.</span></span> <span data-ttu-id="0a476-106">Обратите внимание, что обработчик объекта события допустим только в контексте вызывающего процесса.</span><span class="sxs-lookup"><span data-stu-id="0a476-106">Note that the event object handle is only valid in the context of the calling process.</span></span> <span data-ttu-id="0a476-107">В средах Windows реализация объектов событий осуществляется через собственные службы событий, предоставляемые операционной системой.</span><span class="sxs-lookup"><span data-stu-id="0a476-107">In Windows environments the realization of event objects is through the native event services provided by the operating system.</span></span>

 

 



