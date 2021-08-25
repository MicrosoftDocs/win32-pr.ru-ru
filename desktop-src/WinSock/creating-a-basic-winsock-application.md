---
description: как создать базовое приложение Windows sockets (Winsock).
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Создание базового приложения Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67b13acc0ae80242fb747415d457e6809895c38cd81878224cad2ffe130b2536
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860954"
---
# <a name="creating-a-basic-winsock-application"></a>Создание базового приложения Winsock

**Создание базового приложения Winsock**

1.  Создайте новый пустой проект.
2.  Добавьте пустой исходный файл C++ в проект.
3.  убедитесь, что среда сборки ссылается на каталоги Include, Lib и Src пакета Microsoft Windows Software development kit (sdk) или пакета sdk для более ранней платформы.
4.  Убедитесь, что среда сборки ссылается на файл библиотеки Winsock Ws2 \_ 32. lib. Приложения, использующие Winsock, должны быть связаны с \_ файлом библиотеки Ws2 32. lib. \#Комментарий директивы pragma указывает компоновщику, что требуется файл *Ws2 \_ 32. lib* .
5.  Начните программировать приложение Winsock. Используйте API Winsock, включив файлы заголовков Winsock 2. Файл заголовка *Winsock2. h* содержит большинство функций, структур и определений Winsock. Файл заголовка *Ws2tcpip. h* содержит определения, появившиеся в документе о приложении WinSock 2 Protocol-Specific для TCP/IP, который включает более новые функции и структуры, используемые для получения IP-адресов.
    > [!Note]  
    > Stdio. h используется для стандартных входных и выходных данных, особенно для функции **printf ()** .

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> Файл заголовка *ифлпапи. h* необходим, если приложение использует API-интерфейсы вспомогательного приложения IP. Если требуется файл заголовка *ифлпапи. h* , \# необходимо поместить строку include для заголовочного файла *Winsock2. h* перед \# строкой include для заголовочного файла *ифлпапи. h* .
>
> заголовочный файл *Winsock2. h* внутренне включает основные элементы из файла заголовков *Windows. h* , поэтому \# в приложениях Winsock обычно отсутствует строка include для файла заголовка *Windows. h* . если \# для файла заголовка *Windows. h* требуется строка include, перед ней следует \# указать макрос define WIN32 \_ экономичное \_ и \_ среднее. по историческим причинам заголовок *Windows. h* по умолчанию включает в себя файл заголовка *Winsock. h* для Windows сокетов 1,1. объявления в файле заголовка *Winsock. h* конфликтуют с объявлениями в файле заголовков *Winsock2. h* , который требуется для Windows сокетов 2,0. \_макрос экономичного \_ и \_ среднего значения WIN32 предотвращает включение *Winsock. h* в заголовок *Windows. h* . Пример, иллюстрирующий это, показан ниже.

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



Следующий шаг: [Инициализация Winsock](initializing-winsock.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[начало работы с помощью Winsock](getting-started-with-winsock.md)
</dt> <dt>

[О серверах и клиентах](about-clients-and-servers.md)
</dt> </dl>

 

 



