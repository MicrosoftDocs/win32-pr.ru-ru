---
title: Начальная последовательность
description: Действия по запуску настраиваемого протокола.
ms.assetid: 34c6eb08-668b-43b7-b49b-9ab7536ab658
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29dbb899905dd96e806ffe17a0eafd0091ad97b547ba9f172527ab0acc1b2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000552"
---
# <a name="start-sequence"></a>Начальная последовательность

Чтобы запустить поставщик протокола, служба службы удаленных рабочих столов:

-   Извлекает имя прослушивателя и CLSID объекта диспетчера протоколов ([**иврдспротоколманажер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolmanager)) из реестра. Дополнительные сведения см. [в разделе Регистрация диспетчера протоколов](registering-the-custom-protocol.md).
-   Вызывает метод [**Initialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-initialize) для инициализации диспетчера протоколов.
-   Создает объект диспетчера протокола с помощью идентификатора CLSID. Даже если для одного поставщика протокола зарегистрировано несколько прослушивателей, служба создает только один объект диспетчера протокола.
-   Вызывает [**креателистенер**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-createlistener) , чтобы указать объекту диспетчера протокола создать объект прослушивателя [**иврдспротоколлистенер**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocollistener) и вернуть его в службу. Объект диспетчера протоколов должен добавить ссылку на объект прослушивателя, прежде чем возвратить его службе. Служба освободит объект при остановке службы или удалении прослушивателя.
-   Вызывает [**стартлистен**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-startlisten) для объекта прослушивателя, чтобы прослушиватель мог начать прослушивание входящих подключений.
-   Вызывает [**стоплистен**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistener-stoplisten) , чтобы предотвратить прослушивание объекта прослушивателя.
-   Вызывает [**Uninitialize**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocolmanager-uninitialize) , чтобы отменить инициализацию диспетчера протокола.

Прослушиватель создает объект [**иврдспротоколконнектион**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnection) , когда клиент пытается подключиться. Объект Listener вызывает [**Onconnected**](/windows/desktop/api/wtsprotocol/nf-wtsprotocol-iwrdsprotocollistenercallback-onconnected) для уведомления службы Службы удаленных рабочих столов о том, что новый клиент пытается подключиться или повторно подключиться, и передает объект **иврдспротоколконнектион** в этом вызове. Служба службы удаленных рабочих столов, в свою очередь, возвращает объект [**иврдспротоколконнектионкаллбакк**](/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolconnectioncallback) в этом вызове, чтобы протокол мог взаимодействовать со службой Службы удаленных рабочих столов по мере необходимости. Служба добавляет ссылку на объект обратного вызова перед возвратом, и протокол должен освободить эту ссылку при закрытии соединения.

На следующем рисунке показано взаимодействие между различными объектами во время запуска.

![RCM начальная последовательность](images/protocol-startsequence.png)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Последовательность вызовов методов](method-call-sequence.md)
</dt> <dt>

[Последовательность подключения](connection-sequence.md)
</dt> </dl>

 

 




