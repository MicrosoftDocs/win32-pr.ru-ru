---
description: В некоторых экземплярах сокеты, присоединенные к сеансу MultiPoint, могут иметь некоторые различия в поведении от сокетов типа "точка — точка".
ms.assetid: e59b701f-f85f-4fd6-8d6d-e46199250c22
title: Флаг битов для Всасоккет
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51fede5d160d89b08064d8dff1c1a901c048526f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701529"
---
# <a name="flag-bits-for-wsasocket"></a><span data-ttu-id="8d7b8-103">Флаг битов для Всасоккет</span><span class="sxs-lookup"><span data-stu-id="8d7b8-103">Flag Bits for WSASocket</span></span>

<span data-ttu-id="8d7b8-104">В некоторых экземплярах сокеты, присоединенные к сеансу MultiPoint, могут иметь некоторые различия в поведении от сокетов типа "точка — точка".</span><span class="sxs-lookup"><span data-stu-id="8d7b8-104">In some instances sockets joined to a multipoint session may have some differences in behavior from point-to-point sockets.</span></span> <span data-ttu-id="8d7b8-105">Например, \_ конечный сокет d в схеме с корневой плоскости данных может передавать данные только \_ участнику-корневому элементу d.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-105">For example, a d\_leaf socket in a rooted data plane scheme can only send information to the d\_root participant.</span></span> <span data-ttu-id="8d7b8-106">Это создает необходимость, чтобы приложение могло указать предполагаемое использование сокета коинЦидент с его созданием.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-106">This creates a need for the application to be able to indicate the intended use of a socket coincident with its creation.</span></span> <span data-ttu-id="8d7b8-107">Это делается с помощью битов с четырьмя флагами, которые можно задать в параметре *dwFlags* равным [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span><span class="sxs-lookup"><span data-stu-id="8d7b8-107">This is done through four-flag bits that can be set in the *dwFlags* parameter to [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa):</span></span>

-   <span data-ttu-id="8d7b8-108">\_Флаг WSA \_ \_ \_ — корневой элемент управления MULTIPOINT для создания сокета, выступающего в качестве \_ корня c, и допускается только в том случае, если в соответствующей записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) указана плоскость с корневым контролем.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-108">WSA\_FLAG\_MULTIPOINT\_C\_ROOT, for the creation of a socket acting as a c\_root, and only allowed if a rooted control plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d7b8-109">\_Флаг WSA \_ MULTIPOINT \_ \_ на конечном диске для создания сокета, выступающего в качестве \_ конечного листа c, и допускается только в том случае, если XP1 \_ поддерживает \_ MULTIPOINT в соответствующей записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="8d7b8-109">WSA\_FLAG\_MULTIPOINT\_C\_LEAF, for the creation of a socket acting as a c\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d7b8-110">\_Флаг WSA \_ \_ , корень MULTIPOINT d \_ , для создания сокета, выступающего в качестве \_ корня d, и допускается только в том случае, если в соответствующей записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) указана плоскость с корнем данных.</span><span class="sxs-lookup"><span data-stu-id="8d7b8-110">WSA\_FLAG\_MULTIPOINT\_D\_ROOT, for the creation of a socket acting as a d\_root, and only allowed if a rooted data plane is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>
-   <span data-ttu-id="8d7b8-111">\_Флаг WSA \_ MULTIPOINT \_ D \_ конечный объект для создания сокета, выступающего в качестве \_ листа d, и допускается только в том случае, если XP1 \_ поддерживает \_ MULTIPOINT в соответствующей записи [**всапротокол \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="8d7b8-111">WSA\_FLAG\_MULTIPOINT\_D\_LEAF, for the creation of a socket acting as a d\_leaf, and only allowed if XP1\_SUPPORT\_MULTIPOINT is indicated in the corresponding [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) entry.</span></span>

<span data-ttu-id="8d7b8-112">Обратите внимание, что при создании сокета MultiPoint ровно один из двух флагов плоскости управления и один из двух флагов плоскости данных должен быть задан в параметре *DwFlags* [**всасоккет**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="8d7b8-112">Note that when creating a multipoint socket, exactly one of the two control-plane flags, and one of the two data-plane flags must be set in [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)'s *dwFlags* parameter.</span></span> <span data-ttu-id="8d7b8-113">Таким образом, четыре варианта создания сокетов MultiPoint:</span><span class="sxs-lookup"><span data-stu-id="8d7b8-113">Thus, the four possibilities for creating multipoint sockets are:</span></span>

-   <span data-ttu-id="8d7b8-114">" \_ корень c/d \_ root"</span><span class="sxs-lookup"><span data-stu-id="8d7b8-114">"c\_root/d\_root"</span></span>
-   <span data-ttu-id="8d7b8-115">" \_ корневой/d-конечный диск c \_ "</span><span class="sxs-lookup"><span data-stu-id="8d7b8-115">"c\_root/d\_leaf"</span></span>
-   <span data-ttu-id="8d7b8-116">"c \_ конечный/d- \_ корневой"</span><span class="sxs-lookup"><span data-stu-id="8d7b8-116">"c\_leaf/d\_root"</span></span>
-   <span data-ttu-id="8d7b8-117">"c \_ конечным \_ листом/d"</span><span class="sxs-lookup"><span data-stu-id="8d7b8-117">"c\_leaf /d\_leaf"</span></span>

 

 
