---
description: Функция жесостбяддр использует функцию Всалукупсервицебегин для запроса СВЦИД \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы.
ms.assetid: 9b1e3f3f-bfc0-4099-b699-af56019055e6
title: Функция жесостбяддр в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac84d30ba919a4fc61456d5ca4772c12df786d89241e8249b57068b9aac3f7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132327"
---
# <a name="gethostbyaddr-function-in-the-api"></a>Функция жесостбяддр в API

Функция [**жесостбяддр**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) использует функцию [**ВСАЛУКУПСЕРВИЦЕБЕГИН**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса свЦид \_ inet \_ хостнамебяддр в качестве идентификатора GUID класса службы. Адрес узла указывается в виде деЦимнал строки IPv4 (например, "192.9.200.120") в элементе *лпсзсервицеинстанценаме* структуры [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , передаваемой функции **всалукупсервицебегин** . 32.dll Ws2 \_ указывает BLOB- \_ объект Луп Return \_ , а поставщик службы имен помещает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в большой двоичный объект (используя смещения вместо указателей, как описано выше). Поставщики службы имен должны также учитывать эти другие \_ \_ \* Флаги возврата Луп. 

| Флаг              | Описание                                                                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_имя возврата \_ Луп | Возвращает элемент **h \_ Name** из структуры [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в *лпсзсервицеинстанценаме*.                                                     |
| ЛУП \_ обратный \_ адрес | Возвращает сведения об адресации из [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) в структурах [**ксаддр \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) , сведения о порте по умолчанию равны нулю. |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[Разрешение имен, не зависящее от протокола](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Регистрация и разрешение имен](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
