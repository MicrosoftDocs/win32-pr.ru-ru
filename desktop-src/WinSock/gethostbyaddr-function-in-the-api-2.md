---
description: Функция жесостбяддр использует функцию Всалукупсервицебегин для запроса СВЦИД \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Функция жесостбяддр в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04141d65161831a60ec663f0dee4a9647792ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711037"
---
# <a name="gethostbyaddr-function-in-the-api"></a><span data-ttu-id="a499c-103">Функция жесостбяддр в API</span><span class="sxs-lookup"><span data-stu-id="a499c-103">gethostbyaddr Function in the API</span></span>

<span data-ttu-id="a499c-104">Функция [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) использует функцию [**ВСАЛУКУПСЕРВИЦЕБЕГИН**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса свЦид \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="a499c-104">The [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_HOSTNAMEBYADDR as the service class GUID.</span></span> <span data-ttu-id="a499c-105">Адрес узла указывается в виде деЦимнал строки IPv4 (например, "192.9.200.120") в элементе *лпсзсервицеинстанценаме* структуры [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , передаваемой функции **всалукупсервицебегин** .</span><span class="sxs-lookup"><span data-stu-id="a499c-105">The host address is supplied as a dotted decimnal IPv4 string (for example, "192.9.200.120") in the *lpszServiceInstanceName* member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function.</span></span> <span data-ttu-id="a499c-106">32.dll Ws2 \_ указывает BLOB- \_ объект Луп Return \_ , а поставщик службы имен помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (используя смещения вместо указателей, как описано выше).</span><span class="sxs-lookup"><span data-stu-id="a499c-106">The Ws2\_32.dll specifies LUP\_RETURN\_BLOB and the name service provider places a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="a499c-107">Поставщики службы имен должны также учитывать эти другие \_ \_ \* Флаги возврата Луп.</span><span class="sxs-lookup"><span data-stu-id="a499c-107">Name service providers should honor these other LUP\_RETURN\_\* flags as well.</span></span> 

| <span data-ttu-id="a499c-108">Flag</span><span class="sxs-lookup"><span data-stu-id="a499c-108">Flag</span></span>              | <span data-ttu-id="a499c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a499c-109">Description</span></span>                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a499c-110">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="a499c-110">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="a499c-111">Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="a499c-111">Returns the **h\_name** member from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) structure in *lpszServiceInstanceName*.</span></span>                                                     |
| <span data-ttu-id="a499c-112">ЛУП \_ обратный \_ адрес</span><span class="sxs-lookup"><span data-stu-id="a499c-112">LUP\_RETURN\_ADDR</span></span> | <span data-ttu-id="a499c-113">Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю.</span><span class="sxs-lookup"><span data-stu-id="a499c-113">Returns addressing information from [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) in [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structures, port information is defaulted to zero.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a499c-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a499c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a499c-115">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="a499c-115">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="a499c-116">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="a499c-116">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="a499c-117">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="a499c-117">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
