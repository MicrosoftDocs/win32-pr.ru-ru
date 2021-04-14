---
description: Для введения перекрывающихся операций ввода-вывода требуется механизм, позволяющий приложениям однозначно связывать запросы Send и Receive со своими последующими событиями завершения.
ms.assetid: 944d87bd-388f-420d-ac7d-69c4a28f8a5c
title: Объекты событий (сокеты Windows 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72b60442f9c56ae2c8e9af905bd14b6536b8e10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343522"
---
# <a name="event-objects-windows-sockets-2"></a>Объекты событий (сокеты Windows 2)

Для введения перекрывающихся операций ввода-вывода требуется механизм, позволяющий приложениям однозначно связывать запросы Send и Receive со своими последующими событиями завершения. В сокетах Windows 2 это выполняется с объектами событий, которые моделируются после событий Windows. Объекты событий сокетов Windows — это довольно простые конструкции, которые можно создавать и закрывать, устанавливать и очищать, а также ожидать и запрашивать. Их основной служебной программой является способность приложения блокировать и ожидать, пока один или несколько объектов событий становятся установленными.

Приложения используют [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) для получения обработчика объекта события, который затем может быть предоставлен в качестве обязательного параметра для перекрывающихся версий вызовов Send и Receive ( [**всасенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend), [**всасендто**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto), [**всарекв**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv), [**всареквфром**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)). Объект события, который удаляется при первом создании, задается поставщиками транспорта при завершении связанной перекрывающейся операции ввода-вывода (либо успешно, либо с ошибками). Каждый объект события, созданный **всакреативент** , должен иметь соответствующий [**всаклосивент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent) для уничтожения.

Объекты событий также используются в [**всаевентселект**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) для связывания одного или нескольких \_ сетевых событий демона XXX с объектом события. Это описано в разделе [Асинхронное уведомление с использованием объектов событий](asynchronous-notification-using-event-objects-2.md).

В 32-разрядных средах функции, связанные с объектами событий, включая [**всакреативент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent), [**всаклосивент**](/windows/desktop/api/Winsock2/nf-winsock2-wsacloseevent), [**всасетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetevent), [**всаресетевент**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)и [**Всаваитформултипливентс**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) , напрямую сопоставляются с соответствующими собственными функциями Windows, используя одно и то же имя функции, но без префикса WSA.

 

 



