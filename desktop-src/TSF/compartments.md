---
title: Секции
description: Секции
ms.assetid: 7bffab6f-be40-4d3a-9342-6f81557a9656
keywords:
- Платформа текстовых служб (TSF), секции
- TSF (платформа текстовых служб), секции
- текстовые службы, секции
- Приложения с поддержкой TSF, секции
- секции
- Платформа текстовых служб (TSF), типы секций
- TSF (платформа текстовых служб), типы секций
- текстовые службы, типы секций
- Приложения с поддержкой TSF, типы секций
- Типы секций
- Платформа текстовых служб (TSF), уведомления об изменении секций
- TSF (платформа текстовых служб), уведомления об изменении секций
- текстовые службы, уведомления об изменении секций
- Приложения с поддержкой TSF, уведомления об изменении секций
- уведомления об изменении секций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76636c684ee74f7e452b5602ebfd59d6d1947b0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253028"
---
# <a name="compartments"></a>Секции

## <a name="compartment-types"></a>Типы секций

Существует несколько различных типов секций. Существует глобальная секция, и каждый диспетчер потоков, диспетчер документов и контекст могут содержать секцию.

Глобальная секция позволяет клиентам обмениваться данными между процессами. Чтобы получить глобальный Диспетчер секций, вызовите [**ITfThreadMgr:: жетглобалкомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment).

Диспетчер потоков содержит Диспетчер секций, который содержит секции для каждого потока. Это позволяет совместно использовать данные в потоке. Чтобы получить Диспетчер секций диспетчера потоков, вызовите **ITfThreadMgr:: QueryInterface** с IID \_ итфкомпартментмгр.

Каждый созданный диспетчер документов также содержит Диспетчер секций. Это позволяет предоставлять общий доступ к данным в определенном диспетчере документов. Чтобы получить Диспетчер секций диспетчера документов, вызовите **ITfDocumentMgr:: QueryInterface** с IID \_ итфкомпартментмгр.

Каждый созданный контекст также содержит Диспетчер секций. Это позволяет совместно использовать данные в определенном контексте. Чтобы получить Диспетчер секций контекста, вызовите **ITfContext:: QueryInterface** с IID \_ итфкомпартментмгр.

## <a name="creating-and-deleting-a-compartment"></a>Создание и удаление секции

Секция создается при первом вызове [**итфкомпартментмгр::-секции**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment) с идентификатором GUID секции. Клиент установки должен задать начальное значение секции с помощью [**итфкомпартмент:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue). Пока значение не будет задано, значение секции будет пустым. В связи с этим нет способа проверить, существовала ли секция до вызова методаического **отделения** . Чтобы избежать такой ситуации, при установке клиента следует задать некоторое начальное значение, чтобы другие клиенты могли определить, существует ли уже секция.

Метод [**итфкомпартментмгр:: клеаркомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment) используется для удаления секции. Все существующие ссылки на секцию помечаются как недопустимые.

## <a name="obtaining-compartments"></a>Получение секций

С помощью интерфейса [**итфкомпартментмгр**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr) клиент может перечислить секции, вызвав [**Итфкомпартментмгр:: енумкомпартментс**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments). Этот метод предоставляет объект **иенумгуид** , содержащий идентификаторы GUID всех установленных секций.

С помощью GUID секции **итфкомпартментмгр::-Секция** используется для получения определенной секции. Этот метод предоставляет вызывающему объекту объект [**итфкомпартмент**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment) , который может получать и задавать данные секции.

## <a name="receiving-compartment-change-notifications"></a>Получение уведомлений об изменениях секций

При изменении значения секции диспетчер TSF уведомляет все установленные приемники уведомлений о том, что Секция изменилась. Чтобы установить приемник рекомендаций для изменения секции, создайте объект, реализующий [**итфкомпартментевентсинк**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink). Затем вызовите **итфкомпартмент:: QueryInterface** с IID \_ итфсаурце в объекте секции для отслеживания, чтобы получить интерфейс [**итфсаурце**](/windows/desktop/api/Msctf/nn-msctf-itfsource) . Теперь вызовите [**итфсаурце:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink) с IID \_ итфкомпартментевентсинк и указателем на объект **итфкомпартментевентсинк** . При изменении значения секции [**итфкомпартментевентсинк:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange) приемника уведомлений вызывается с идентификатором GUID секции. Приемник уведомлений может вызвать метод [**итфкомпартмент:: GetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-getvalue) , чтобы получить новое значение.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**итфкомпартментмгр**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmentmgr)
</dt> <dt>

[**итфкомпартмент**](/windows/desktop/api/Msctf/nn-msctf-itfcompartment)
</dt> <dt>

[**итфкомпартментевентсинк**](/windows/desktop/api/Msctf/nn-msctf-itfcompartmenteventsink)
</dt> <dt>

[**тфклиентид**](tfclientid.md)
</dt> <dt>

[**ITfThreadMgr:: Жетглобалкомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-getglobalcompartment)
</dt> <dt>

[**Итфкомпартментмгр:: "Секция"**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-getcompartment)
</dt> <dt>

[**Итфкомпартмент:: SetValue**](/windows/desktop/api/Msctf/nf-msctf-itfcompartment-setvalue)
</dt> <dt>

[**Итфкомпартментмгр:: Клеаркомпартмент**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-clearcompartment)
</dt> <dt>

[**Итфкомпартментмгр:: Енумкомпартментс**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmentmgr-enumcompartments)
</dt> <dt>

[**итфсаурце**](/windows/desktop/api/Msctf/nn-msctf-itfsource)
</dt> <dt>

[**Итфсаурце:: AdviseSink**](/windows/desktop/api/Msctf/nf-msctf-itfsource-advisesink)
</dt> <dt>

[**Итфкомпартментевентсинк:: OnChange**](/windows/desktop/api/Msctf/nf-msctf-itfcompartmenteventsink-onchange)
</dt> </dl>

 

 




