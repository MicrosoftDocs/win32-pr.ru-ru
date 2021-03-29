---
description: При \_ использовании d конечных сокетов в некорневой плоскости данных желательно, чтобы трафик, отправленный на тот же сокет, был получен обратно. Для \_ \_ включения или отключения замыкания на себя трафика MultiPoint используется код команды замыкания на себя для всаиоктл.
ms.assetid: 5e267287-0ff5-4943-882f-5fe6687cca10
title: SIO_MULTIPOINT_LOOPBACK код команды для Всаиоктл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61e58a9f1db6f246e9e76ec527e57353bb35cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991109"
---
# <a name="sio_multipoint_loopback-command-code-for-wsaioctl"></a><span data-ttu-id="4f0e1-104">\_ \_ Код команды замыкания на себя для всаиоктл MULTIPOINT</span><span class="sxs-lookup"><span data-stu-id="4f0e1-104">SIO\_MULTIPOINT\_LOOPBACK Command Code for WSAIoctl</span></span>

<span data-ttu-id="4f0e1-105">При \_ использовании d конечных сокетов в некорневой плоскости данных желательно, чтобы трафик, отправленный на тот же сокет, был получен обратно.</span><span class="sxs-lookup"><span data-stu-id="4f0e1-105">When d\_leaf sockets are used in a nonrooted data plane, it is desirable to have traffic that is sent out received back on the same socket.</span></span> <span data-ttu-id="4f0e1-106">Для \_ \_ включения или отключения замыкания на себя трафика MultiPoint используется код команды замыкания на себя для [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) .</span><span class="sxs-lookup"><span data-stu-id="4f0e1-106">The SIO\_MULTIPOINT\_LOOPBACK command code for [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) is used to enable or disable loopback of multipoint traffic.</span></span>

 

 



