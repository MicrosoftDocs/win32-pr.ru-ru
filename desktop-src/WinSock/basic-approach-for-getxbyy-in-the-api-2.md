---
description: Большинство функций Жетксбии преобразуются32.dll Ws2 \_ в последовательность всалукупсервицебегин, всалукупсервиценекст и всалукупсервицеенд, которая использует один из наборов специальных идентификаторов GUID в качестве класса службы.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Базовый подход для Жетксбии в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541634"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a>Базовый подход для Жетксбии в API

Большинство функций **жетксбии** преобразуются32.dll Ws2 \_ в последовательность [**Всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)и [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) , которая использует один из наборов специальных идентификаторов GUID в качестве класса службы. Эти идентификаторы GUID указывают тип **жетксбии** операции, для которой выполняется эмуляция. Запрос ограничен теми поставщиками службы имен, которые поддерживают AF \_ inet. Всякий раз, когда функция **жетксбии** возвращает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) или [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) , Ws2 \_32.dll указывает \_ флаг Луп Return \_ BLOB в **всалукупсервицебегин** , чтобы требуемые сведения возвращал поставщик службы имен. Эти структуры необходимо немного изменить, чтобы содержащиеся в них указатели в должны быть заменены смещениями относительно начала данных большого двоичного объекта. Все значения, на которые ссылаются эти параметры-указатели, должны быть полностью включены в большой двоичный объект, а все строки — ASCII.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Регистрация и разрешение имен](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



