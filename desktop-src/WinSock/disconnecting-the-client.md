---
description: После того как клиент завершит отправку и получение данных, клиент отключится от сервера и завершит работу сокета.
ms.assetid: 33165e5b-e304-42b1-9542-45d8fe8a5218
title: Отсоединение клиента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6ac34036cc92386d7d68b3d5debda4d37a92ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343532"
---
# <a name="disconnecting-the-client"></a>Отсоединение клиента

После того как клиент завершит отправку и получение данных, клиент отключится от сервера и завершит работу сокета.

**Отключение и завершение работы сокета**

1.  Когда клиент завершает отправку данных на сервер, функция [**завершения работы**](/windows/desktop/api/winsock/nf-winsock-shutdown) может быть вызвана указанием SD \_ Send для завершения отправной стороны сокета. Это позволяет серверу освобождать некоторые ресурсы для этого сокета. Клиентское приложение по-прежнему может принимать данные на сокете.
    ```C++
    // shutdown the send half of the connection since no more data will be sent
    iResult = shutdown(ConnectSocket, SD_SEND);
    if (iResult == SOCKET_ERROR) {
        printf("shutdown failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
    ```

    

2.  Когда клиентское приложение выполняет получение данных, вызывается функция [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) для закрытия сокета.

    После завершения работы клиентского приложения с помощью DLL-библиотеки Windows Sockets функция [**всаклеануп**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) вызывается для освобождения ресурсов.

    ```C++
    // cleanup
    closesocket(ConnectSocket);
    WSACleanup();

    return 0;
    ```

    

## <a name="complete-client-source-code"></a>Полный исходный код клиента

-   [Завершение клиентского кода](complete-client-code.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Клиентское приложение Winsock](winsock-client-application.md)
</dt> <dt>

[Отправка и получение данных на клиенте](sending-and-receiving-data-on-the-client.md)
</dt> </dl>

 

 



