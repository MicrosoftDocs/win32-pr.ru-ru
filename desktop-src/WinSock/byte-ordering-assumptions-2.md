---
description: SOCKADDR структуры и предположения порядка байтов в Winsock.
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: Предположения порядка байтов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701565"
---
# <a name="byte-ordering-assumptions"></a><span data-ttu-id="b15c3-103">Предположения порядка байтов</span><span class="sxs-lookup"><span data-stu-id="b15c3-103">Byte Ordering Assumptions</span></span>

<span data-ttu-id="b15c3-104">Поставщик услуг должен обрабатывать все компоненты [**SOCKADDR**](sockaddr-2.md) , за исключением параметра семейства адресов, как если бы они направляются в сетевой последовательности байтов, а параметр семейства Address — в порядке байтов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="b15c3-104">A service provider should treat all [**sockaddr**](sockaddr-2.md) components exclusive of the address family parameter as if they are in the network byte order, and the address family parameter as in the local computer's byte order.</span></span> <span data-ttu-id="b15c3-105">Это обязанность приложения Winsock, обеспечивающая правильную компоновку адресов, содержащихся в структурах **SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="b15c3-105">It is the Winsock application's responsibility to make sure that addresses contained in **sockaddr** structures are properly arranged.</span></span> <span data-ttu-id="b15c3-106">API Winsock предоставляет ряд подпрограмм преобразования для упрощения этой задачи.</span><span class="sxs-lookup"><span data-stu-id="b15c3-106">The Winsock API provides a number of conversion routines to simplify this task.</span></span> <span data-ttu-id="b15c3-107">В настоящее время эти подпрограммы понимают преобразование между естественным порядком байтов на локальном узле и порядком байтов в сети с обратным порядком байтов или с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="b15c3-107">Currently these routines understand conversion between the local host's natural byte order and either big-Endian or little-Endian network byte ordering.</span></span> <span data-ttu-id="b15c3-108">Архитектура Winsock может поддерживать другие схемы порядка байтов в будущем.</span><span class="sxs-lookup"><span data-stu-id="b15c3-108">The Winsock architecture can support other byte ordering schemes in the future.</span></span>

 

 



