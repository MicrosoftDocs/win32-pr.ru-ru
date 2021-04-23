---
description: Объекты событий сокетов Windows — это простые конструкции, которые можно создавать и закрывать, устанавливать и очищать, ожидать и опрашивать.
ms.assetid: 65a7627e-150e-4ca3-bc17-d2b380ee02d1
title: Использование объектов событий (сокеты Windows 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26a9b70ff49bf7d46f2907c04fd8911d55dd623
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701494"
---
# <a name="using-event-objects-windows-sockets-2"></a><span data-ttu-id="1f033-103">Использование объектов событий (сокеты Windows 2)</span><span class="sxs-lookup"><span data-stu-id="1f033-103">Using Event Objects (Windows Sockets 2)</span></span>

<span data-ttu-id="1f033-104">Объекты событий сокетов Windows — это простые конструкции, которые можно создавать и закрывать, устанавливать и очищать, ожидать и опрашивать.</span><span class="sxs-lookup"><span data-stu-id="1f033-104">Windows Sockets event objects are simple constructs that can be created and closed, set and cleared, waited upon and polled.</span></span> <span data-ttu-id="1f033-105">Принятая модель предназначена для создания объекта события и предоставления маркера в виде параметра (или в виде компонента структуры параметра) в таких функциях, как [**вспсенд**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) и [**вспевентселект**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1f033-105">The accepted model is for clients to create an event object and supply the handle as a parameter (or as a component of a parameter structure) in functions such as [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPEventSelect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85)).</span></span> <span data-ttu-id="1f033-106">Когда возникло заданное условие, поставщик услуг использует этот обработчик для установки объекта события путем вызова [**впусетевент**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span><span class="sxs-lookup"><span data-stu-id="1f033-106">When the nominated condition has occurred, the service provider uses the handle to set the event object by calling [**WPUSetEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpusetevent).</span></span> <span data-ttu-id="1f033-107">В то же время клиент Winsock SPI может заблокировать и подождать или опросить, пока объект события не станет установленным (сигнальным).</span><span class="sxs-lookup"><span data-stu-id="1f033-107">Meanwhile, the Winsock SPI client may either block and wait or poll until the event object becomes set (signaled).</span></span> <span data-ttu-id="1f033-108">Клиент может впоследствии очистить или сбросить объект события и использовать его снова.</span><span class="sxs-lookup"><span data-stu-id="1f033-108">The client may subsequently clear or reset the event object and use it again.</span></span>

 

 
