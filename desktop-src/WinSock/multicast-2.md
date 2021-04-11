---
description: Универсальные функции Winsock MultiPoint поддерживают многоадресную рассылку IP-адресов.
ms.assetid: 32fffca8-4f13-495b-afb6-bb57a9cce553
title: Многоадресная рассылка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c6b4ece06119d01e2661028f452985bb20b068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145016"
---
# <a name="multicast"></a><span data-ttu-id="d08b9-103">Многоадресная рассылка</span><span class="sxs-lookup"><span data-stu-id="d08b9-103">Multicast</span></span>

<span data-ttu-id="d08b9-104">Универсальные функции Winsock MultiPoint поддерживают многоадресную рассылку IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="d08b9-104">Generic Winsock multipoint functions support IP multicast.</span></span> <span data-ttu-id="d08b9-105">Однако поставщики транспорта TCP/IP, поддерживающие многоадресную рассылку, должны также предоставлять поддержку Berkeley Software Distribution (BSD), поддерживающую соответствующие параметры многоадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="d08b9-105">However, the TCP/IP transport providers that support multicast must also provide Berkeley Software Distribution (BSD) style–multicast support by supporting the corresponding multicast options.</span></span> <span data-ttu-id="d08b9-106">Это упрощает перенос существующих многоадресных приложений в сокеты Windows 2.</span><span class="sxs-lookup"><span data-stu-id="d08b9-106">This simplifies the porting of existing multicast applications to Windows Sockets 2.</span></span>

 

 



