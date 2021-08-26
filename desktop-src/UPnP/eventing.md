---
title: Обработка событий
description: Размещенная служба должна реализовывать интерфейс Иупнпевентсаурце, если он имеет переменные состояния события.
ms.assetid: 7558496d-c909-4602-bfaa-d21108392fed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313f979072a447f41b9edadfeec7bf4407463be67c86e9c3b34f43f4dcc47874
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008084"
---
# <a name="eventing"></a>Обработка событий

Размещенная служба должна реализовывать интерфейс [**иупнпевентсаурце**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsource) , если он имеет переменные состояния события. Этот интерфейс имеет два метода: [**advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) и [**unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise). Этот интерфейс предоставляет механизм для подписки узла устройства на уведомления о событиях, созданные размещенной службой. В каждый момент времени будет зарегистрировано больше одного приемника событий.

Размещенная служба должна реализовать метод [**advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise) , задерживая ссылку на интерфейс [**иупнпевентсинк**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpeventsink) , который был передан в качестве параметра. Если интерфейс найден, метод **advise** содержит ссылку на этот интерфейс до вызова метода [**unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) или до тех пор, пока объект размещенной службы не будет удален. Предложение **advise** вызывается только один раз.

Чтобы удалить подписку, узел устройства вызывает метод [**unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise) и передает указатель на объект, используемый при вызове [**advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). Размещенная служба удаляет подписку, если указатель совпадает с именем, передаваемым в предложение **advise**.

При изменении значения переменной состояния размещенная служба должна сообщить о возникновении события. Эти службы выполняет это путем вызова метода [**иупнпевентсинк:: онстатечанжед**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsink-onstatechanged) .

Когда узлу устройства больше не требуется получать уведомления от размещенной службы, он вызывает [**иупнпевентсаурце:: unadvise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-unadvise), передавая тот же указатель объекта, который был получен от [**advise**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpeventsource-advise). Узел устройства вызывает этот метод, когда устройство больше не будет находиться в сети.

 

 




