---
title: Использование IConnectionPoint
description: Использование IConnectionPoint
ms.assetid: afd50b84-1fd6-47ad-a3ef-e8b4a725b72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2449be5f1711457807666e9e2068d13defd8437bedee93402f7b974d5298d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129426"
---
# <a name="using-iconnectionpoint"></a>Использование IConnectionPoint

Если клиент имеет указатель на точку подключения, он может выполнять следующие операции, как показано в примере [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint):

-   Сначала [**IConnectionPoint:: жетконнектионинтерфаце**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) ИЗВЛЕКАЕТ интерфейс IID исходящего интерфейса, поддерживаемый точкой подключения. При использовании в сочетании с [**иенумконнектионпоинтс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnectionpoints)этот метод позволяет клиенту исследовать идентификаторов IID всех исходящих интерфейсов, поддерживаемых в объекте, доступном для подключения.
-   Во-вторых, клиент может перейти с точки соединения обратно в интерфейс [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) объекта, доступного через метод [**IConnectionPoint:: жетконнектионпоинтконтаинер**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectionpointcontainer) .
-   В третьих, наиболее интересными методами для клиента являются [**IConnectionPoint:: Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) и [**IConnectionPoint:: unadvise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-unadvise). Когда клиент хочет подключить собственный объект приемника к доступному объекту, клиент передает указатель [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) (или любой другой указатель интерфейса на тот же объект) для приема **уведомлений**. Точка соединения запрашивает приемник для конкретного исходящего интерфейса. Если этот интерфейс доступен в приемнике, точка соединения затем сохраняет указатель интерфейса. С этого момента до вызова метода **unadvise** подключаемый объект будет вызывать приемник через этот интерфейс при возникновении событий. Чтобы отключить приемник от точки подключения, клиент передает ключ, возвращенный методом **advise** , в метод **unadvise** . **Unadvise** должен вызывать [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) в интерфейсе приемника.
-   Наконец, клиент может запросить точку подключения для перечисления всех подключений к нему, которые существуют через [**IConnectionPoint:: енумконнектионс**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-enumconnections). Этот метод создает объект перечислителя (с отдельным счетчиком ссылок), возвращая в него указатель [**иенумконнектионс**](/windows/desktop/api/ocidl/nn-ocidl-ienumconnections) . Клиент должен вызвать метод [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , если перечислитель больше не нужен. Кроме того, перечислитель возвращает ряд структур [**коннектдата**](/windows/win32/api/ocidl/ns-ocidl-connectdata) , по одному для каждого соединения. Каждая структура описывает одно соединение, используя указатель [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) приемника, а также ключ соединения, изначально возвращенный из инструкции [**advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise). При использовании этих указателей интерфейсов приемников клиент должен вызвать **Release** для каждого указателя, возвращенного в структуре **коннектдата** .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подключаемые интерфейсы объектов](connectable-object-interfaces.md)
</dt> </dl>

 

 