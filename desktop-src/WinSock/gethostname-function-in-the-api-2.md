---
description: Функция @ hostname использует функцию Всалукупсервицебегин для запроса \_ имени узла свЦид в качестве идентификатора GUID класса службы.
ms.assetid: 39498c2f-6047-484d-a8ea-253461e5b0f5
title: Функция onhostname в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8629083c49e3915dd0ec4f1cfeb9363caabf8b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711035"
---
# <a name="gethostname-function-in-the-api"></a><span data-ttu-id="e5853-103">Функция onhostname в API</span><span class="sxs-lookup"><span data-stu-id="e5853-103">gethostname Function in the API</span></span>

<span data-ttu-id="e5853-104">Функция @ [**HostName**](/windows/desktop/api/winsock/nf-winsock-gethostname) использует функцию [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса имени узла свЦид в \_ качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="e5853-104">The [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) function uses the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="e5853-105">Если элемент **лпсзсервицеинстанценаме** структуры [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , переданный функции **всалукупсервицебегин** , имеет **значение NULL** или ссылается на **пустую** строку (то есть.</span><span class="sxs-lookup"><span data-stu-id="e5853-105">If the **lpszServiceInstanceName** member of the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function is **NULL** or references a **NULL** string (that is .</span></span> <span data-ttu-id="e5853-106">""), локальный узел должен быть разрешен.</span><span class="sxs-lookup"><span data-stu-id="e5853-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="e5853-107">В противном случае происходит поиск по указанному имени узла.</span><span class="sxs-lookup"><span data-stu-id="e5853-107">Otherwise, a lookup on a specified host name occurs.</span></span> <span data-ttu-id="e5853-108">В целях имитации имени **узла** Ws2 \_32.dll указывает указатель **null** для элемента **ЛПСЗСЕРВИЦЕИНСТАНЦЕНАМЕ** и указывает \_ возвращаемое имя Луп, \_ чтобы имя узла возвращалось в элементе **лпсзсервицеинстанценаме** .</span><span class="sxs-lookup"><span data-stu-id="e5853-108">For the purposes of emulating **gethostname** the Ws2\_32.dll specifies a **NULL** pointer for the **lpszServiceInstanceName** member, and specifies LUP\_RETURN\_NAME so that the host name is returned in the **lpszServiceInstanceName** member.</span></span> <span data-ttu-id="e5853-109">Если приложение использует этот запрос и указывает \_ возвращаемый Луп, \_ адрес узла предоставляется в структуре [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .</span><span class="sxs-lookup"><span data-stu-id="e5853-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address is provided in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span> <span data-ttu-id="e5853-110">\_ \_ Действие возврата BLOB-объекта Луп не определено для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="e5853-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="e5853-111">Сведения о порте по умолчанию равны нулю, если только элемент **лпсзкуеристринг** структуры **всакуерисет** , переданный в функцию **всалукупсервицебегин** , не ссылается на службу, например FTP, и в этом случае предоставляется полный транспортный адрес указанной службы.</span><span class="sxs-lookup"><span data-stu-id="e5853-111">Port information is defaulted to zero unless the **lpszQueryString** member of the **WSAQUERYSET** structure passed to the **WSALookupServiceBegin** function references a service such as FTP, in which case the complete transport address of the indicated service is supplied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5853-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e5853-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5853-113">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="e5853-113">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="e5853-114">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="e5853-114">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="e5853-115">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="e5853-115">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
