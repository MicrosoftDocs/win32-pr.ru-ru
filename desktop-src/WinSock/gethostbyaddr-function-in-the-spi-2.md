---
description: Запрос Всалукупсервицебегин использует СВЦИД \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Функция жесостбяддр в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541586"
---
# <a name="gethostbyaddr-function-in-the-spi"></a><span data-ttu-id="689a1-103">Функция жесостбяддр в SPI</span><span class="sxs-lookup"><span data-stu-id="689a1-103">gethostbyaddr Function in the SPI</span></span>

<span data-ttu-id="689a1-104">Запрос [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) использует свЦид \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="689a1-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="689a1-105">Адрес узла указывается в *лпсзсервицеинстанценаме* в виде строки с точками в десятичном формате IPv4 (например, 192.9.200.120).</span><span class="sxs-lookup"><span data-stu-id="689a1-105">The host address is supplied in *lpszServiceInstanceName* as a dotted-decimal IPv4 address string (for example, 192.9.200.120).</span></span> <span data-ttu-id="689a1-106">*\_32.dllWS2* указывает Луп \_ \_ BLOB, а NSP помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (с использованием смещений вместо указателей, как описано выше).</span><span class="sxs-lookup"><span data-stu-id="689a1-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="689a1-107">NSP также должны учитывать эти другие \_ \_ \* Флаги возврата Луп.</span><span class="sxs-lookup"><span data-stu-id="689a1-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="689a1-108">Flag</span><span class="sxs-lookup"><span data-stu-id="689a1-108">Flag</span></span>              | <span data-ttu-id="689a1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="689a1-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="689a1-110">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="689a1-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="689a1-111">Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="689a1-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="689a1-112">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="689a1-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="689a1-113">Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю.</span><span class="sxs-lookup"><span data-stu-id="689a1-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

 

 
