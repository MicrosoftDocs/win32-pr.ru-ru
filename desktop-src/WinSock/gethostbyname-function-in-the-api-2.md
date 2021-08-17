---
description: Функция GetHostByName в API Winsock.
ms.assetid: 015637ed-7a3e-49eb-96ef-8fe82d2902f5
title: Функция GetHostByName в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a63bf7884cd170721de9b7d5009ed53c7bcb60bb36869986862f5e81e03215b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132307"
---
# <a name="gethostbyname-function-in-the-api"></a>Функция GetHostByName в API

Функция [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) использует функцию [**ВСАЛУКУПСЕРВИЦЕБЕГИН**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса свЦид \_ inet \_ хостаддрбинаме в качестве идентификатора GUID класса службы. Имя узла указывается в элементе **лпсзсервицеинстанценаме** в структуре [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , передаваемой функции **всалукупсервицебегин** . 32.dll Ws2 \_ указывает BLOB- \_ объект Луп Return \_ , а поставщик службы имен помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (используя смещения вместо указателей, как описано выше). Поставщики службы имен должны также учитывать эти другие \_ \_ \* Флаги возврата Луп.

| Флаг              | Описание                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_имя возврата \_ Луп | Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.                                                                                                                                           |
| ЛУП \_ обратный \_ адрес | Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю. Обратите внимание, что эта подпрограммы не разрешает имена узлов, состоящие из точечного IPv4-адреса. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Регистрация и разрешение имен](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
