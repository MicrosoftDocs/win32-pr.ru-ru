---
description: Функция GetHostByName в Winsock SPI.
ms.assetid: 3e63a6db-1ecc-4ce1-b772-25dc9a57e0d9
title: Функция GetHostByName в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a04f39ca00dc712ef7b8ce3bdef480aa253a5b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711036"
---
# <a name="gethostbyname-function-in-the-spi"></a>Функция GetHostByName в SPI

Запрос [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) использует свЦид \_ inet \_ хостаддрбинаме в качестве идентификатора GUID класса службы. Имя узла указывается в *лпсзсервицеинстанценаме*. *\_32.dllWS2* указывает Луп \_ \_ BLOB, а NSP помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (с использованием смещений вместо указателей, как описано выше). NSP также должны учитывать эти другие \_ \_ \* Флаги возврата Луп.



| Flag              | Описание                                                                                                                                                                                                                                                         |
|-------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_имя возврата \_ Луп | Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.                                                                                                                                                            |
| ЛУП \_ обратный \_ адрес | Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю. Обратите внимание, что эта подпрограммы не выполняет разрешение имен узлов, состоящих из строкового десятичного адреса IPv4. |



 

 

 
