---
description: Ошибка СОКЕТа константы манифеста предназначена \_ для проверки сбоя функции. Хотя использование этой константы не является обязательным, рекомендуется. В следующем примере показано использование \_ константы ошибки сокета.
ms.assetid: b46203dc-5666-413b-90fe-8432318f3037
title: Возвращаемые значения при сбое функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94280d47d705833528c03c0d98a4a31232a0c6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263826"
---
# <a name="return-values-on-function-failure"></a><span data-ttu-id="4fd14-105">Возвращаемые значения при сбое функции</span><span class="sxs-lookup"><span data-stu-id="4fd14-105">Return Values on Function Failure</span></span>

<span data-ttu-id="4fd14-106">**\_ Ошибка сокета** константы манифеста предназначена для проверки сбоя функции.</span><span class="sxs-lookup"><span data-stu-id="4fd14-106">The manifest constant **SOCKET\_ERROR** is provided for checking function failure.</span></span> <span data-ttu-id="4fd14-107">Хотя использование этой константы не является обязательным, рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4fd14-107">Although use of this constant is not mandatory, it is recommended.</span></span> <span data-ttu-id="4fd14-108">В следующем примере показано использование константы **\_ ошибки сокета** .</span><span class="sxs-lookup"><span data-stu-id="4fd14-108">The following example illustrates the use of the **SOCKET\_ERROR** constant.</span></span>

<span data-ttu-id="4fd14-109">Типичный стиль BSD (не будет работать в Windows)</span><span class="sxs-lookup"><span data-stu-id="4fd14-109">Typical BSD Style (will not work on Windows)</span></span>


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



<span data-ttu-id="4fd14-110">Стиль Windows</span><span class="sxs-lookup"><span data-stu-id="4fd14-110">Windows Style</span></span>


```C++
        iResult = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (iResult == SOCKET_ERROR ) {
            iError = WSAGetLastError();
            if (iError == WSAEWOULDBLOCK)
                printf("recv failed with error: WSAEWOULDBLOCK\n");
            else
                printf("recv failed with error: %ld\n", iError);

            closesocket(ClientSocket);
            WSACleanup();
            return 1;
        }    
```



## <a name="related-topics"></a><span data-ttu-id="4fd14-111">См. также</span><span class="sxs-lookup"><span data-stu-id="4fd14-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fd14-112">Коды ошибок — код возврата, h \_ и всажетластеррор</span><span class="sxs-lookup"><span data-stu-id="4fd14-112">Error Codes - errno, h\_errno and WSAGetLastError</span></span>](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[<span data-ttu-id="4fd14-113">Обработка ошибок Winsock</span><span class="sxs-lookup"><span data-stu-id="4fd14-113">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="4fd14-114">Перенос приложений сокета в Winsock</span><span class="sxs-lookup"><span data-stu-id="4fd14-114">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="4fd14-115">Вопросы программирования Winsock</span><span class="sxs-lookup"><span data-stu-id="4fd14-115">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="4fd14-116">Коды ошибок сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="4fd14-116">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



