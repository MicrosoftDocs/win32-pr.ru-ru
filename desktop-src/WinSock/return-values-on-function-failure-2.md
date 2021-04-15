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
# <a name="return-values-on-function-failure"></a>Возвращаемые значения при сбое функции

**\_ Ошибка сокета** константы манифеста предназначена для проверки сбоя функции. Хотя использование этой константы не является обязательным, рекомендуется. В следующем примере показано использование константы **\_ ошибки сокета** .

Типичный стиль BSD (не будет работать в Windows)


```C++
        r = recv(ClientSocket, recvbuf, recvbuflen, 0);
        if (r == -1     /* or r < 0 */
            && errno == EWOULDBLOCK) {
            printf("recv failed with error: EWOULDBLOCK\n");
        }    
```



Стиль Windows


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



## <a name="related-topics"></a>См. также

<dl> <dt>

[Коды ошибок — код возврата, h \_ и всажетластеррор](error-codes-errno-h-errno-and-wsagetlasterror-2.md)
</dt> <dt>

[Обработка ошибок Winsock](handling-winsock-errors.md)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> <dt>

[Коды ошибок сокетов Windows](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



