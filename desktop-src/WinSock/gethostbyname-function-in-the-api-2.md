---
description: Функция GetHostByName в API Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Функция GetHostByName в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3881897a0c971c48ca9a02e6205ec1cae0476f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145064"
---
# <a name="gethostbyname-function-in-the-api"></a><span data-ttu-id="a59fd-103">Функция GetHostByName в API</span><span class="sxs-lookup"><span data-stu-id="a59fd-103">gethostbyname Function in the API</span></span>

<span data-ttu-id="a59fd-104">Функция [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) использует функцию [**ВСАЛУКУПСЕРВИЦЕБЕГИН**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса свЦид \_ inet \_ хостаддрбинаме в качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="a59fd-104">The [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTADDRBYNAME as the service class GUID.</span></span> <span data-ttu-id="a59fd-105">Имя узла указывается в элементе **лпсзсервицеинстанценаме** в структуре [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , передаваемой функции **всалукупсервицебегин** .</span><span class="sxs-lookup"><span data-stu-id="a59fd-105">The host name is supplied in the **lpszServiceInstanceName** member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="a59fd-106">32.dll Ws2 \_ указывает BLOB- \_ объект Луп Return \_ , а поставщик службы имен помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (используя смещения вместо указателей, как описано выше).</span><span class="sxs-lookup"><span data-stu-id="a59fd-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="a59fd-107">Поставщики службы имен должны также учитывать эти другие \_ \_ \* Флаги возврата Луп.</span><span class="sxs-lookup"><span data-stu-id="a59fd-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="a59fd-108">Flag</span><span class="sxs-lookup"><span data-stu-id="a59fd-108">Flag</span></span>              | <span data-ttu-id="a59fd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a59fd-109">Description</span></span>                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a59fd-110">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="a59fd-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="a59fd-111">Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="a59fd-111">Returns the **h\_name** member from the [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                           |
| <span data-ttu-id="a59fd-112">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="a59fd-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="a59fd-113">Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю.</span><span class="sxs-lookup"><span data-stu-id="a59fd-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> <span data-ttu-id="a59fd-114">Обратите внимание, что эта подпрограммы не разрешает имена узлов, состоящие из точечного IPv4-адреса.</span><span class="sxs-lookup"><span data-stu-id="a59fd-114">Note that this routine does not resolve host names that consist of a dotted IPv4 address.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a59fd-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a59fd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a59fd-116">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="a59fd-116">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="a59fd-117">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="a59fd-117">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="a59fd-118">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="a59fd-118">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
