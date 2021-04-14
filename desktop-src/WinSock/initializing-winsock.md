---
description: Все процессы (приложения или библиотеки DLL), вызывающие функции Winsock, должны инициализировать использование библиотеки DLL Windows Sockets перед выполнением других вызовов функций Winsock. Это также обеспечивает поддержку Winsock в системе.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Инициализация Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541570"
---
# <a name="initializing-winsock"></a>Инициализация Winsock

Все процессы (приложения или библиотеки DLL), вызывающие функции Winsock, должны инициализировать использование библиотеки DLL Windows Sockets перед выполнением других вызовов функций Winsock. Это также обеспечивает поддержку Winsock в системе.

**Инициализация Winsock**

1.  Создайте объект [**всадата**](/windows/desktop/api/winsock/ns-winsock-wsadata) с именем всадата.
    ```C++
    WSADATA wsaData;
    ```

    

2.  Вызовите [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) и верните его значение в виде целого числа и проверьте наличие ошибок.
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

Функция [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) вызывается для инициации использования WS2 \_32.dll.

Структура [**всадата**](/windows/desktop/api/winsock/ns-winsock-wsadata) содержит сведения о реализации сокетов Windows. Параметр МАКЕВОРД (2, 2) [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) отправляет запрос на использование Winsock версии 2,2 в системе и задает переданную версию в качестве наивысшей версии поддержки сокетов Windows, которую может использовать вызывающий объект.

Следующий шаг для клиента: [создание сокета для клиента](creating-a-socket-for-the-client.md)

Следующий шаг для сервера: [создание сокета для сервера](creating-a-socket-for-the-server.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Создание базового приложения Winsock](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



