---
description: Функция сокета создала сокеты с атрибутом OVERLAPPED, установленным по умолчанию в первой Wsock32.dll, 32-разрядной версии сокетов Windows (1,1).
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Состояние по умолчанию для перекрывающихся атрибутов сокета
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145082"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="7f16a-103">Состояние по умолчанию для перекрывающихся атрибутов сокета</span><span class="sxs-lookup"><span data-stu-id="7f16a-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="7f16a-104">Функция [**сокета**](/windows/desktop/api/Winsock2/nf-winsock2-socket) создала сокеты с атрибутом OVERLAPPED, установленным по умолчанию в первой Wsock32.dll, 32-разрядной версии сокетов Windows (1,1).</span><span class="sxs-lookup"><span data-stu-id="7f16a-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="7f16a-105">Чтобы обеспечить обратную совместимость с развернутыми реализациями Wsock32.dll, это будет продолжаться и для сокетов Windows 2.</span><span class="sxs-lookup"><span data-stu-id="7f16a-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="7f16a-106">То есть, в сокетах Windows Sockets 2, созданных с помощью функции **сокета** , будет иметь атрибут OVERLAPPED.</span><span class="sxs-lookup"><span data-stu-id="7f16a-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="7f16a-107">Однако, чтобы быть более совместимым с остальной частью API Windows, сокеты, созданные с помощью [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , по умолчанию не будут иметь атрибут OVERLAPPED.</span><span class="sxs-lookup"><span data-stu-id="7f16a-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="7f16a-108">Этот атрибут будет применен только в том случае, \_ Если \_ установлен бит с перекрытием флага WSA.</span><span class="sxs-lookup"><span data-stu-id="7f16a-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



