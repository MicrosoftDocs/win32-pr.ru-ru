---
description: исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка Winsock. h.
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Включение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740bde9fae96aa3088a4317c66479bcc75176ee3b9ca9f5e390365c5ef481109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051532"
---
# <a name="include-files"></a>Включение файлов

исходный включаемый файл для использования с сокетами Windows 1,1 был файлом заголовка *Winsock. h* . чтобы упростить перенос существующего исходного кода на основе сокетов Berkeley UNIX для Windows сокетов, Windows пакетам средств разработки сокетов для Winsock 1,1 было предложено несколько включаемых файлов с теми же именами, что и стандартные UNIX включаемые файлы (например, файлы заголовков *sys/socket. h* и arpa/inet. h). Однако эти файлы заголовков Winsock с одинаковыми именами просто содержали директиву для включения файла заголовка *Winsock2. h* .

при освобождении Windows сокетов 2 основной включаемый файл для использования с сокетами Windows был переименован в *Winsock2. h*. Старый исходный файл заголовка *Winsock. h* для Winsock 1,1 также был сохранен для совместимости с более старыми приложениями. разработка приложений, совместимых с Winsock 1,1, устарела, так как Windows 2000 был выпущен. Теперь все приложения должны использовать директиву include *Winsock2. h* в исходных файлах приложения Winsock.

Файл заголовка *Winsock2. h* содержит большинство функций, структур и определений Winsock. Файл заголовка *Ws2tcpip. h* содержит определения, появившиеся в документе о приложении WinSock 2 Protocol-Specific для TCP/IP, который включает более новые функции и структуры, используемые для получения IP-адресов. К ним относятся семейство функций [**функцию getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) и [**жетнамеинфо**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) , которые обеспечивают разрешение имен для адресов IPv4 или IPv6. Файл заголовка *Ws2tcpip. h* необходим только в том случае, если приложению требуются эти функции именования, не зависящие от IP.

файл заголовка *мсвсокк. h* содержит определения для расширений, относящихся к Windowsным сокетам 2 (например,[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**акцептекс**](/windows/win32/api/mswsock/nf-mswsock-acceptex)и [**коннектекс**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)). Файл заголовка *мсвсокк. h* обычно не требуется, если приложение не использует эти расширения, относящиеся к Microsoft.

заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому \# в приложениях Winsock обычно отсутствует строка include для файла заголовка *Windows. h* . если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define WIN32 \_ экономичное \_ и \_ среднее. по историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для Windows сокетов 1,1. объявления в файле заголовка *Winsock. h* конфликтуют с объявлениями в файле заголовков *Winsock2. h* , который требуется для сокетов Windows 2. \_макрос экономичного \_ и \_ среднего значения WIN32 предотвращает включение *Winsock. h* в заголовок *Windows. h* . Пример, иллюстрирующий это, показан ниже.


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Создание базового приложения Winsock](creating-a-basic-winsock-application.md)
</dt> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
