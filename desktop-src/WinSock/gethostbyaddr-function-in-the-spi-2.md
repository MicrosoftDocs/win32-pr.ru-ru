---
description: Запрос Всалукупсервицебегин использует СВЦИД \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.
ms.assetid: 6fd54708-dbd0-4402-8eb8-9cdc42cd56ad
title: Функция жесостбяддр в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94f4cdead3a19814e535e2dee80dfdcd0c9fa26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541586"
---
# <a name="gethostbyaddr-function-in-the-spi"></a>Функция жесостбяддр в SPI

Запрос [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) использует свЦид \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы. Адрес узла указывается в *лпсзсервицеинстанценаме* в виде строки с точками в десятичном формате IPv4 (например, 192.9.200.120). *\_32.dllWS2* указывает Луп \_ \_ BLOB, а NSP помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (с использованием смещений вместо указателей, как описано выше). NSP также должны учитывать эти другие \_ \_ \* Флаги возврата Луп.



| Flag              | Описание                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_имя возврата \_ Луп | Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.                                                     |
| ЛУП \_ обратный \_ адрес | Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю. |



 

 

 
