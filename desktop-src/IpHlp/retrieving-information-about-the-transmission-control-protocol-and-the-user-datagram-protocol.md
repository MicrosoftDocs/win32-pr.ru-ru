---
description: Вспомогательный модуль IP позволяет получить доступ к сведениям о сетевых протоколах, используемых на локальном компьютере.
ms.assetid: 3ae07fbd-0b69-42d6-81ab-cc239c354bbb
title: Получение сведений о протоколе управления передачей и протоколе датаграммы пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a73893bf379dda6a58f86854028967da806863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819481"
---
# <a name="retrieving-information-about-the-transmission-control-protocol-and-the-user-datagram-protocol"></a><span data-ttu-id="5d147-103">Получение сведений о протоколе управления передачей и протоколе датаграммы пользователя</span><span class="sxs-lookup"><span data-stu-id="5d147-103">Retrieving Information About the Transmission Control Protocol and the User Datagram Protocol</span></span>

<span data-ttu-id="5d147-104">Вспомогательный модуль IP позволяет получить доступ к сведениям о сетевых протоколах, используемых на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="5d147-104">IP Helper makes it possible to access information about network protocols that are used on the local computer.</span></span> <span data-ttu-id="5d147-105">Для получения сведений о протоколе TCP и UDP на локальном компьютере используйте функции, описанные в следующих параграфах.</span><span class="sxs-lookup"><span data-stu-id="5d147-105">Use the functions described in the following paragraphs to retrieve information about the Transmission Control Protocol (TCP) and User Datagram Protocol (UDP) on the local computer.</span></span>

<span data-ttu-id="5d147-106">Функция [**жетткпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) извлекает текущую СТАТИСТИКУ по протоколу TCP.</span><span class="sxs-lookup"><span data-stu-id="5d147-106">The [**GetTcpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcpstatistics) function retrieves the current statistics for TCP.</span></span> <span data-ttu-id="5d147-107">Примеры кода, включающие **жетткпстатистикс** , см. [в разделе Получение сведений с помощью жетткпстатистикс](retrieving-information-using-gettcpstatistics.md).</span><span class="sxs-lookup"><span data-stu-id="5d147-107">For code samples involving **GetTcpStatistics** see [Retrieving Information Using GetTcpStatistics](retrieving-information-using-gettcpstatistics.md).</span></span>

<span data-ttu-id="5d147-108">Функция [**жетудпстатистикс**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) извлекает текущую СТАТИСТИКУ по протоколу UDP.</span><span class="sxs-lookup"><span data-stu-id="5d147-108">The [**GetUdpStatistics**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudpstatistics) function retrieves the current statistics for UDP.</span></span>

<span data-ttu-id="5d147-109">Функция [**жетткптабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) ИЗВЛЕКАЕТ таблицу TCP-соединения.</span><span class="sxs-lookup"><span data-stu-id="5d147-109">The [**GetTcpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-gettcptable) function retrieves the TCP connection table.</span></span> <span data-ttu-id="5d147-110">[**Жетудптабле**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) извлекает таблицу прослушивателя UDP.</span><span class="sxs-lookup"><span data-stu-id="5d147-110">The [**GetUdpTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getudptable) retrieves the UDP listener table.</span></span>

<span data-ttu-id="5d147-111">Функция [**сетткпентри**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) позволяет разработчику установить состояние указанного TCP-подключения в MIB- \_ \_ состоянии TCP \_ DELETE \_ TCB.</span><span class="sxs-lookup"><span data-stu-id="5d147-111">The [**SetTcpEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-settcpentry) function enables a developer to set the state of a specified TCP connection to MIB\_TCP\_STATE\_DELETE\_TCB.</span></span>

 

 



