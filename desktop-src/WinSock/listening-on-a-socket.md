---
description: После привязки сокета к IP-адресу и порту в системе сервер должен прослушивать IP-адрес и порт для входящих запросов на подключение.
ms.assetid: 83c9f0e7-2e6d-449b-8d97-3d13154112cd
title: Прослушивание на сокете
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48c36fe1718493d1b92ca52bb3c648ebd1aa5b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692280"
---
# <a name="listening-on-a-socket"></a>Прослушивание на сокете

После привязки сокета к IP-адресу и порту в системе сервер должен прослушивать IP-адрес и порт для входящих запросов на подключение.

## <a name="to-listen-on-a-socket"></a>Прослушивание сокета

Вызовите функцию [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) , передав в качестве параметров созданный сокет и значение для *невыполненной работы*, максимальную длину очереди ожидающих подключений для приема. В этом примере параметру *невыполненной работы* было присвоено значение **сомаксконн**. Это значение представляет собой специальную константу, которая указывает поставщику Winsock для этого сокета максимально допустимое число ожидающих подключений в очереди. Проверьте возвращаемое значение для общих ошибок.


```C++
if ( listen( ListenSocket, SOMAXCONN ) == SOCKET_ERROR ) {
    printf( "Listen failed with error: %ld\n", WSAGetLastError() );
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```



Следующий шаг: [принятие подключения](accepting-a-connection.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Серверное приложение Winsock](winsock-server-application.md)
</dt> <dt>

[Привязка сокета](binding-a-socket.md)
</dt> </dl>

 

 



