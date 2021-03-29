---
description: Вспомогательная служба IP предоставляет возможности извлечения данных, которые полезны для сетевого администрирования локального компьютера.
ms.assetid: b50b3927-6c74-4282-b79b-c86d72d93ae3
title: Получение сведений о протоколе Интернета и протоколе управляющих сообщений Интернета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09b2768ff591b53db79bbbfb38fc2c6c2596ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990868"
---
# <a name="retrieving-information-on-the-internet-protocol-and-the-internet-control-message-protocol"></a><span data-ttu-id="cdae8-103">Получение сведений о протоколе Интернета и протоколе управляющих сообщений Интернета</span><span class="sxs-lookup"><span data-stu-id="cdae8-103">Retrieving Information on the Internet Protocol and the Internet Control Message Protocol</span></span>

<span data-ttu-id="cdae8-104">Вспомогательная служба IP предоставляет возможности извлечения данных, которые полезны для сетевого администрирования локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdae8-104">IP Helper provides information retrieval capabilities that are useful for the network administration of the local computer.</span></span> <span data-ttu-id="cdae8-105">Следующие функции извлекают статистику по протоколу IP и ICMP.</span><span class="sxs-lookup"><span data-stu-id="cdae8-105">The following functions retrieve statistics for the Internet Protocol (IP) and the Internet Control Message Protocol (ICMP).</span></span> <span data-ttu-id="cdae8-106">Эти функции также можно использовать для задания определенных параметров конфигурации для IP.</span><span class="sxs-lookup"><span data-stu-id="cdae8-106">You can also use these functions to set certain configuration parameters for IP.</span></span>

<span data-ttu-id="cdae8-107">Функция [**жетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) извлекает текущую статистику IP-адресов для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="cdae8-107">The [**GetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipstatistics) function retrieves the current IP statistics for the local computer.</span></span> <span data-ttu-id="cdae8-108">Примеры кода, включающие **жетипстатистикс** , см. [в разделе Получение сведений с помощью жетипстатистикс](retrieving-information-using-getipstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="cdae8-108">For code samples involving **GetIpStatistics** see [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md).</span></span>

<span data-ttu-id="cdae8-109">Функция [**жетикмпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) извлекает текущую статистику ICMP.</span><span class="sxs-lookup"><span data-stu-id="cdae8-109">The [**GetIcmpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-geticmpstatistics) function retrieves the current ICMP statistics.</span></span>

<span data-ttu-id="cdae8-110">Используйте функцию [**сетипстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) для включения или отключения IP-пересылки.</span><span class="sxs-lookup"><span data-stu-id="cdae8-110">Use the [**SetIpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipstatistics) function to enable or disable IP forwarding.</span></span> <span data-ttu-id="cdae8-111">Эта функция также дает возможность задать срок жизни (TTL) по умолчанию для IP-датаграмм.</span><span class="sxs-lookup"><span data-stu-id="cdae8-111">This function also makes it possible for you to set the default time-to-live (TTL) for IP datagrams.</span></span> <span data-ttu-id="cdae8-112">Кроме того, можно задать TTL с помощью функции [**сетипттл**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) .</span><span class="sxs-lookup"><span data-stu-id="cdae8-112">Alternatively, you can set the TTL by using the [**SetIpTTL**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipttl) function.</span></span>

 

 



