---
description: В двух случаях необходимо переименовать функции, которые используются в сокетах Berkeley, чтобы избежать конфликта с другими функциями Microsoft Windows API.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Переименованные функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898582"
---
# <a name="renamed-functions"></a>Переименованные функции

В двух случаях необходимо переименовать функции, которые используются в сокетах Berkeley, чтобы избежать конфликта с другими функциями Microsoft Windows API.

## <a name="close-and-closesocket"></a>Закрыть и функции closesocket

Сокеты представлены стандартными дескрипторами файлов в сокетах Berkeley, поэтому функцию **Close** можно использовать для закрытия сокетов, а также обычных файлов. Хотя ни одно из сокетов Windows не позволяет реализовать использование обычных дескрипторов файлов для обнаружения сокетов, ничего не требуется. В Windows сокеты должны быть закрыты с помощью подпрограммы [**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) . В Windows использование функции **Close** для закрытия сокета неверно, и последствия этого действия не определены в этой спецификации.

## <a name="ioctl-and-ioctlsocketwsaioctl"></a>IOCTL и Иоктлсоккет/Всаиоктл

Различные системы времени выполнения языка C используют IOCTL для целей, не связанных с сокетами Windows. Как следствие, функция [**иоктлсоккет**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) и функция [**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) были определены для выполнения функций сокета, которые были выполнены с помощью **ioctl** и **fcntl** в распределении программного обеспечения Berkeley.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**функции closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[**иоктлсоккет**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[Перенос приложений сокета в Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Вопросы программирования Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**всаиоктл**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



