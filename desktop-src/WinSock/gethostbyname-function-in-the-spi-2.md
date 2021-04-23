---
description: Функция GetHostByName в Winsock SPI.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Функция GetHostByName в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711036"
---
# <a name="gethostbyname-function-in-the-spi"></a><span data-ttu-id="308dd-103">Функция GetHostByName в SPI</span><span class="sxs-lookup"><span data-stu-id="308dd-103">gethostbyname Function in the SPI</span></span>

<span data-ttu-id="308dd-104">Запрос [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) использует свЦид \_ inet \_ хостаддрбинаме в качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="308dd-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="308dd-105">Имя узла указывается в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="308dd-105">The host name is supplied in *lpszServiceInstanceName*.</span></span> <span data-ttu-id="308dd-106">*\_32.dllWS2* указывает Луп \_ \_ BLOB, а NSP помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (с использованием смещений вместо указателей, как описано выше).</span><span class="sxs-lookup"><span data-stu-id="308dd-106">The *Ws2\_32.dll* specifies LUP\_RETURN\_BLOB and the NSP places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="308dd-107">NSP также должны учитывать эти другие \_ \_ \* Флаги возврата Луп.</span><span class="sxs-lookup"><span data-stu-id="308dd-107">NSPs should honor these other LUP\_RETURN\_\* flags as well.</span></span>



| <span data-ttu-id="308dd-108">Flag</span><span class="sxs-lookup"><span data-stu-id="308dd-108">Flag</span></span>              | <span data-ttu-id="308dd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="308dd-109">Description</span></span>                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308dd-110">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="308dd-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="308dd-111">Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="308dd-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                            |
| <span data-ttu-id="308dd-112">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="308dd-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="308dd-113">Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю.</span><span class="sxs-lookup"><span data-stu-id="308dd-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="308dd-114">Обратите внимание, что эта подпрограммы не выполняет разрешение имен узлов, состоящих из строкового десятичного адреса IPv4.</span><span class="sxs-lookup"><span data-stu-id="308dd-114">Note that this routine does not resolve host names consisting of a dotted-decimal IPv4 address string.</span></span> |



 

 

 
