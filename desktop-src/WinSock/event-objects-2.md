---
description: Для введения перекрывающихся операций ввода-вывода требуется механизм, позволяющий приложениям однозначно связывать запросы Send и Receive со своими последующими событиями завершения.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: объекты событий (сокеты Windows 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34820d7df92704d86f7dbdc100816789488426e2fdd553456be94da921811c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132597"
---
# <a name="event-objects-windows-sockets-2"></a>объекты событий (сокеты Windows 2)

Для введения перекрывающихся операций ввода-вывода требуется механизм, позволяющий приложениям однозначно связывать запросы Send и Receive со своими последующими событиями завершения. в сокетах Windows 2 это осуществляется с помощью объектов событий, которые моделируются после Windows событий. Windows Объекты событий сокетов являются довольно простыми конструкциями, которые можно создавать и закрывать, устанавливать и очищать, а также ожидать и запрашивать. Их основной служебной программой является способность приложения блокировать и ожидать, пока один или несколько объектов событий становятся установленными.

Приложения используют [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) для получения обработчика объекта события, который затем может быть предоставлен в качестве обязательного параметра для перекрывающихся версий вызовов Send и Receive ( [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**всасендто**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). Объект события, который удаляется при первом создании, задается поставщиками транспорта при завершении связанной перекрывающейся операции ввода-вывода (либо успешно, либо с ошибками). Каждый объект события, созданный **всакреативент** , должен иметь соответствующий [**всаклосивент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) для уничтожения.

Объекты событий также используются в [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) для связывания одного или нескольких \_ сетевых событий демона XXX с объектом события. Это описано в разделе [Асинхронное уведомление с использованием объектов событий](asynchronous-notification-using-event-objects-2.md).

в 32-разрядных средах функции, связанные с объектами событий, включая [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**всаклосивент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**всасетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**всаресетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)и [**всаваитформултипливентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , напрямую сопоставляются с соответствующими собственными функциями Windows, используя одно и то же имя функции, но без префикса WSA.

 

 



