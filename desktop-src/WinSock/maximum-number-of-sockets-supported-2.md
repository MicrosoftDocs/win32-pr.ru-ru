---
description: максимальное число сокетов, поддерживаемое определенным поставщиком службы Windows sockets, зависит от реализации.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Максимальное число поддерживаемых сокетов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b567b9733dfb869c901ac499ca8dac66904c84bbe77d750780504acee076385f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569759"
---
# <a name="maximum-number-of-sockets-supported"></a>Максимальное число поддерживаемых сокетов

максимальное число сокетов, поддерживаемое определенным поставщиком службы Windows sockets, зависит от реализации. Поставщик Microsoft WinSock ограничивает максимальное количество сокетов, поддерживаемое только объемом доступной памяти на локальном компьютере. Однако сторонние поставщики Winsock могут иметь ограничения на число поддерживаемых сокетов. Приложение не должно делать никаких предположений о доступности определенного числа сокетов. Дополнительные сведения об этом разделе см. в разделе [**сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).

## <a name="fd_set-and-select"></a>Демон \_ установки и выбор

в \_ файле заголовков *Winsock2. h* определено несколько макросов, которые можно использовать в переносе приложений для Windows из среды UNIX. Эти макросы используются с функциями [**SELECT**](/windows/desktop/api/Winsock2/nf-winsock2-select) и [**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) для переноса приложений в Windows. максимальное число сокетов, которое может использовать приложение Windows sockets, не зависит от значения константы манифеста \_ . Это значение, определенное в файле заголовка *Winsock2. h* , используется для конструирования структур [**\_ набора**](/windows/desktop/api/winsock/nf-winsock-fd_set) , используемых с функцией **SELECT** . Значение по умолчанию в Winsock2. h — 64. Если приложение предназначено для работы с более чем 64 сокетами с помощью функций **SELECT** и **всаполл** , то разработчик должен определить создаваемый манифест \_ в каждом исходном файле перед включением файла заголовка *Winsock2. h* . Одним из способов это может быть включение определения в параметры компилятора в файле Makefile. Например, можно добавить "-DFD \_ SETSIZE = 128" в качестве параметра командной строки компилятора для Microsoft C++. необходимо подчеркнуть, что определение «\ \ \ \ \ "\ \ \_ "» не влияет на фактическое число сокетов, предоставляемых поставщиком услуг Windows sockets. Это значение влияет только на макросы "ДЕМОна XXX", \_ используемые функциями **SELECT** и **всаполл** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Установка ДЕМОна \_**](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**метьте**](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**Сбой WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[**всаполл**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
