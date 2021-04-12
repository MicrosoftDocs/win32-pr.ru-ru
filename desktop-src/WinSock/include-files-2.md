---
description: Исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Включение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343502"
---
# <a name="include-files"></a>Включение файлов

Исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка *Winsock. h* . Для упрощения переноса существующего исходного кода, основанного на подсчете сокетов UNIX, в сокеты Windows, в комплектах средств разработки Windows Sockets для Winsock 1,1 было предложено несколько включаемых файлов с теми же именами, что и стандартные файлы UNIX (например, файлы заголовков *sys/Socket. h* и ARPA/inet. h). Однако эти файлы заголовков Winsock с одинаковыми именами просто содержали директиву для включения файла заголовка *Winsock2. h* .

При освобождении сокетов Windows 2 основной включаемый файл для использования с сокетами Windows был переименован в *Winsock2. h*. Старый исходный файл заголовка *Winsock. h* для Winsock 1,1 также был сохранен для совместимости с более старыми приложениями. Разработка приложений, совместимых с Winsock 1,1, устарела, так как была выпущена ОС Windows 2000. Теперь все приложения должны использовать директиву include *Winsock2. h* в исходных файлах приложения Winsock.

Файл заголовка *Winsock2. h* содержит большинство функций, структур и определений Winsock. Файл заголовка *Ws2tcpip. h* содержит определения, появившиеся в документе о приложении WinSock 2 Protocol-Specific для TCP/IP, который включает более новые функции и структуры, используемые для получения IP-адресов. К ним относятся семейство функций [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) , которые обеспечивают разрешение имен для адресов IPv4 или IPv6. Файл заголовка *Ws2tcpip. h* необходим только в том случае, если приложению требуются эти функции именования, не зависящие от IP.

Файл заголовка *мсвсокк. h* содержит определения для расширений, относящихся к Майкрософт, для сокетов Windows Sockets 2 (например,[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)и [**коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)). Файл заголовка *мсвсокк. h* обычно не требуется, если приложение не использует эти расширения, относящиеся к Microsoft.

Заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому \# в приложениях Winsock обычно отсутствует строка include для файла заголовка *Windows. h* . Если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define Win32 \_ экономичное \_ и \_ среднее. По историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для сокетов Windows 1,1. Объявления в файле заголовка *Winsock. h* конфликтуют с объявлениями в файле заголовков *Winsock2. h* , который требуется для Windows Sockets 2. \_Макрос экономичного \_ и \_ среднего значения Win32 предотвращает включение *библиотеки Winsock. h* в заголовок *Windows. h* . Пример, иллюстрирующий это, показан ниже.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Создание базового приложения Winsock](creating-a-basic-winsock-application.md)
</dt> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
