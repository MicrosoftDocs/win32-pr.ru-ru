---
description: Пример многоадресного программирования
ms.assetid: 87a6d3bb-3827-4a84-ba2d-c7bd2dd73eb2
title: Пример многоадресного программирования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cde6b8ab9ac0dd6b4fc16ae36bec4a4e939466b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711023"
---
# <a name="multicast-programming-sample"></a><span data-ttu-id="48e16-103">Пример многоадресного программирования</span><span class="sxs-lookup"><span data-stu-id="48e16-103">Multicast Programming Sample</span></span>

<span data-ttu-id="48e16-104">В следующем примере кода показано, как включить многоадресную функциональность в приложение Windows Sockets с помощью параметров сокета.</span><span class="sxs-lookup"><span data-stu-id="48e16-104">The following sample code illustrates how to include multicast functionality to a Windows Sockets application using socket options.</span></span>


```C++
#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <mswsock.h>

#define u_int32 UINT32  // Unix uses u_int32

// Need to link with Ws2_32.lib
#pragma comment (lib, "Ws2_32.lib")


int                  /* OUT: whatever setsockopt() returns */
join_source_group(int sd, u_int32 grpaddr, 
   u_int32 srcaddr, u_int32 iaddr)
{
   struct ip_mreq_source imr; 
   
   imr.imr_multiaddr.s_addr  = grpaddr;
   imr.imr_sourceaddr.s_addr = srcaddr;
   imr.imr_interface.s_addr  = iaddr;
   return setsockopt(sd, IPPROTO_IP, IP_ADD_SOURCE_MEMBERSHIP, (char *) &imr, sizeof(imr));  
}

int
leave_source_group(int sd, u_int32 grpaddr, 
   u_int32 srcaddr, u_int32 iaddr)
{
   struct ip_mreq_source imr;

   imr.imr_multiaddr.s_addr  = grpaddr;
   imr.imr_sourceaddr.s_addr = srcaddr;
   imr.imr_interface.s_addr  = iaddr;
   return setsockopt(sd, IPPROTO_IP, IP_DROP_SOURCE_MEMBERSHIP, (char *) &imr, sizeof(imr));
}
```



 

 



