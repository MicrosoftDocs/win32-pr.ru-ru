---
description: Установка сеанса PGM похожа на подпрограммы установки соединения, связанные с сеансом TCP.
ms.assetid: 777e0106-0314-4ec8-b064-88ceb694614b
title: Отправителей и получателей PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559ac30ace4374b48c86efeb579e1426cc455b00adb803e97244a37d8df7fda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741071"
---
# <a name="pgm-senders-and-receivers"></a>Отправителей и получателей PGM

Установка сеанса PGM похожа на подпрограммы установки соединения, связанные с сеансом TCP. Однако значительная отклонить от сеанса TCP заключается в том, что семантика клиента и сервера отменяется. сервер (отправитель PGM) подключается к группе многоадресной рассылки, а клиент (получатель PGM) ожидает принятия подключения. Следующие абзацы представляют собой сведения о программных действиях, необходимых для создания отправителя PGM и получателя PGM. На этой странице также описаны доступные режимы данных для сеансов PGM.

## <a name="pgm-sender"></a>Отправитель PGM

**Чтобы создать отправителя PGM, выполните следующие действия.**

1.  Создайте сокет PGM.
2.  [**привяжите**](/windows/desktop/api/winsock/nf-winsock-bind) сокет к адресу \_ .
3.  [**подключитесь**](/windows/desktop/api/Winsock2/nf-winsock2-connect) к адресу передачи группы многоадресной рассылки.

Для клиентов не выполняются подтверждения формальных сеансов. Процесс подключения аналогичен протоколу UDP [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), в котором он связывает адрес конечной точки (группу многоадресной рассылки) с сокетом. По завершении данные могут быть отправлены на сокет.

Когда отправитель создает сокет PGM и подключает его к адресу многоадресной рассылки, создается сеанс PGM. Надежный сеанс многоадресной рассылки определяется сочетанием глобального уникального идентификатора (GUID) и исходного порта. Идентификатор GUID создается транспортом. Порт Ссаурце задается транспортом, и не предоставляется контроль над тем, какой порт источника используется.

> [!Note]  
> Получение данных в сокете отправителя запрещено и приводит к ошибке.

 

В следующем фрагменте кода показано, как настроить отправителя PGM.


```C++

SOCKET        s;
SOCKADDR_IN   salocal, sasession;
int           dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

salocal.sin_family = AF_INET;
salocal.sin_port   = htons (0);    // Port is ignored here
salocal.sin_addr.s_addr = htonl (INADDR_ANY);

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant sender socket options here
//

//
// Now, connect <entity type="hellip"/>
// Setting the connection port (dwSessionPort) has relevance, and
// can be used to multiplex multiple sessions to the same
// multicast group address over different ports
//
dwSessionPort = 0;
sasession.sin_family = AF_INET;
sasession.sin_port   = htons (dwSessionPort);
sasession.sin_addr.s_addr = inet_addr ("234.5.6.7");

connect (s, (SOCKADDR *)&sasession, sizeof(sasession));

//
// We're now ready to send data!
//



```



## <a name="pgm-receiver"></a>Получатель PGM

**Чтобы создать приемник PGM, выполните следующие действия.**

1.  Создайте сокет PGM.
2.  [**привяжите**](/windows/desktop/api/winsock/nf-winsock-bind) сокет к адресу группы многоадресной рассылки, на которую отправляется отправитель.
3.  Вызовите функцию [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) на сокете, чтобы перевести сокет в режим прослушивания. Функция Listen Возвращает время обнаружения сеанса PGM по указанному адресу и порту группы многоадресной рассылки.
4.  Вызовите функцию [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) , чтобы получить новый маркер сокета, соответствующий сеансу.

Принятие нового сеанса инициируется только исходными данными PGM (ODATA). Таким образом, транспорт может получить другой трафик PGM (например, пакеты SPM или RDATA), но не приводит к возврату функции [**Listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) .

После принятия сеанса для получения данных используется возвращенный маркер сокета.

> [!Note]  
> Отправка данных через сокет приема запрещена и приводит к ошибке.

 

В следующем фрагменте кода показано, как настроить приемник PGM.


```C++

SOCKET        s,
              sclient;
SOCKADDR_IN   salocal,
              sasession;
int           sasessionsz, dwSessionPort;

s = socket (AF_INET, SOCK_RDM, IPPROTO_RM);

//
// The bind port (dwSessionPort) specified should match that
// which the sender specified in the connect call
//
dwSessionPort = 0;
salocal.sin_family = AF_INET;
salocal.sin_port   = htons (dwSessionPort);    
salocal.sin_addr.s_addr = inet_addr ("234.5.6.7");

bind (s, (SOCKADDR *)&salocal, sizeof(salocal));

//
// Set all relevant receiver socket options here
//

listen (s, 10);

sasessionsz = sizeof(sasession);
sclient = accept (s, (SOCKADDR *)&sasession, &sasessionsz);

//
// accept will return the client socket and we are now ready
// to receive data on the new socket!
//



```



## <a name="data-modes"></a>Режимы данных

Сеансы PGM имеют два варианта режима данных: режим сообщения и режим потока.

Режим сообщения подходит для приложений, которые должны отсылать дискретные сообщения и задается типом сокета Сокк \_ RDM. Режим потока подходит для приложений, которым требуется передавать потоковые данные получателям, таким как приложения видео или голоса, и задается типом сокета \_ потока Сокк. Режим выбора влияет на то, как Winsock обрабатывает данные.

Рассмотрим следующий пример: в режиме сообщения отправитель PGM выполняет три вызова функции [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) , каждая с буфером 100 байт. Эта операция отображается в сети как три отдельных пакета PGM. На стороне получателя каждый вызов функции [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) возвращает только 100 байт, даже если предоставлен больший буфер получения. В отличие от этого, при использовании отправителя PGM в режиме потока эти 3 100 байт могут сообщаться менее чем с тремя физическими пакетами по сети (или объединены в один большой двоичный объект данных на стороне получателя). таким образом, когда получатель вызывает одну из функций получения сокетов Windows, любой объем данных, полученных транспортом PGM, может быть возвращен в приложение без учета того, как данные были физически переданы или получены.

 

 



