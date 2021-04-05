---
description: Порядок, в котором изначально устанавливаются поставщики транспортной службы, управляет порядком перечисления с помощью Всценумпротоколс и WSCEnumProtocols32 в интерфейсе поставщика услуг или через Всаенумпротоколс в интерфейсе приложения. Что более важно, этот порядок также управляет порядком, в котором протоколы и поставщики услуг рассматриваются, когда клиент запрашивает создание сокета на основе его семейства адресов, типа и идентификатора протокола.
ms.assetid: f76c63b3-9952-4aaf-813f-152f4838d3c4
title: Упорядочение поставщиков услуг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c23d9357d30c94b084bf6288013c38a2d46a4b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898578"
---
# <a name="service-provider-ordering"></a><span data-ttu-id="ba8e1-104">Упорядочение поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="ba8e1-104">Service Provider Ordering</span></span>

<span data-ttu-id="ba8e1-105">Порядок, в котором изначально устанавливаются поставщики транспортной службы, управляет порядком перечисления с помощью [**всценумпротоколс**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) и [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) в интерфейсе поставщика услуг или через [**всаенумпротоколс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) в интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-105">The order in which transport service providers are initially installed governs the order in which they are enumerated through [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) and [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) at the service provider interface, or through [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) at the application interface.</span></span> <span data-ttu-id="ba8e1-106">Что более важно, этот порядок также управляет порядком, в котором протоколы и поставщики услуг рассматриваются, когда клиент запрашивает создание сокета на основе его семейства адресов, типа и идентификатора протокола.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-106">More importantly, this order also governs the order in which protocols and service providers are considered when a client requests creation of a socket based on its address family, type, and protocol identifier.</span></span>

<span data-ttu-id="ba8e1-107">Сокеты Windows 2 включают приложение с именем Sporder.exe, которое позволяет интерактивно изменять каталог установленных протоколов после установки уже установленных протоколов.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-107">Windows Sockets 2 includes an applet called Sporder.exe that allows the catalog of installed protocols to be reordered interactively after protocols have already been installed.</span></span> <span data-ttu-id="ba8e1-108">Winsock также включает вспомогательную библиотеку DLL, Sporder.dll, которая экспортирует процедурный интерфейс для переупорядочения протоколов.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-108">Winsock also includes an auxiliary DLL, Sporder.dll, that exports a procedural interface for reordering protocols.</span></span> <span data-ttu-id="ba8e1-109">Этот процедурный интерфейс состоит из одной процедуры, именуемой [**всквритепровидерордер**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span><span class="sxs-lookup"><span data-stu-id="ba8e1-109">This procedural interface consists of a single procedure called [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).</span></span>

<span data-ttu-id="ba8e1-110">Определение интерфейса может быть импортировано в программу C или C++ с помощью include File-Order. h.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-110">The interface definition may be imported into a C or C++ program by means of the include file Sporder.h.</span></span> <span data-ttu-id="ba8e1-111">Точка входа может быть связана с помощью lib File Reorder. lib.</span><span class="sxs-lookup"><span data-stu-id="ba8e1-111">The entry point may be linked by means of the lib file Sporder.lib.</span></span>

 

 



