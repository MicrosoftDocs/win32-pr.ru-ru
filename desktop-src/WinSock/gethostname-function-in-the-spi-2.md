---
description: Запрос Всалукупсервицебегин использует \_ имя узла свЦид в качестве идентификатора GUID класса службы.
ms.assetid: 6f073e1a-2985-4e94-8174-94b1fcaf13d1
title: Функция onhostname в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9aef10be48b264eb607184caf38bd687a5fe307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711034"
---
# <a name="gethostname-function-in-the-spi"></a><span data-ttu-id="112bf-103">Функция onhostname в SPI</span><span class="sxs-lookup"><span data-stu-id="112bf-103">gethostname Function in the SPI</span></span>

<span data-ttu-id="112bf-104">Запрос [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) использует \_ имя узла СВЦИД в качестве идентификатора GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="112bf-104">The [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) query uses SVCID\_HOSTNAME as the service class GUID.</span></span> <span data-ttu-id="112bf-105">Если *лпсзсервицеинстанценаме* имеет значение null или ссылается на пустую строку (то есть.</span><span class="sxs-lookup"><span data-stu-id="112bf-105">If *lpszServiceInstanceName* is null or references a null string (that is .</span></span> <span data-ttu-id="112bf-106">""), локальный узел должен быть разрешен.</span><span class="sxs-lookup"><span data-stu-id="112bf-106">""), the local host is to be resolved.</span></span> <span data-ttu-id="112bf-107">В противном случае должно произойти Поиск по указанному имени узла.</span><span class="sxs-lookup"><span data-stu-id="112bf-107">Otherwise, a lookup on a specified host name shall occur.</span></span> <span data-ttu-id="112bf-108">В целях эмуляции Зовите Ws2 [**,**](/windows/desktop/api/winsock/nf-winsock-gethostname) \_32.dll задаст указатель null для *лпсзсервицеинстанценаме* и укажите имя возвращаемого значения Луп, \_ \_ чтобы имя узла возвращалось в параметре *лпсзсервицеинстанценаме* .</span><span class="sxs-lookup"><span data-stu-id="112bf-108">For the purposes of emulating [**gethostname**](/windows/desktop/api/winsock/nf-winsock-gethostname) the Ws2\_32.dll will specify a null pointer for *lpszServiceInstanceName*, and specify LUP\_RETURN\_NAME so that the host name is returned in the *lpszServiceInstanceName* parameter.</span></span> <span data-ttu-id="112bf-109">Если приложение использует этот запрос и указывает \_ возвращаемый Луп, \_ адрес узла будет указан в структуре **ксаддр \_ info** .</span><span class="sxs-lookup"><span data-stu-id="112bf-109">If an application uses this query and specifies LUP\_RETURN\_ADDR then the host address will be provided in a **CSADDR\_INFO** structure.</span></span> <span data-ttu-id="112bf-110">\_ \_ Действие возврата BLOB-объекта Луп не определено для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="112bf-110">The LUP\_RETURN\_BLOB action is undefined for this query.</span></span> <span data-ttu-id="112bf-111">Сведения о порте будут по умолчанию равняться нулю, если только *лпсзкуеристринг* не ссылается на службу, например FTP, и в этом случае будет предоставляться полный транспортный адрес указанной службы.</span><span class="sxs-lookup"><span data-stu-id="112bf-111">Port information will be defaulted to zero unless the *lpszQueryString* references a service such as ftp, in which case the complete transport address of the indicated service will be supplied.</span></span>

 

 



