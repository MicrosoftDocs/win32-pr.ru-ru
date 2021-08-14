---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 40d26ea1-3081-4afd-8b12-bc6521fad390
ms.tgt_platform: multiple
title: E (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffbd1ce4685ee9901dfedca2a4b3a1b948d91c8f5b56def28494eb6c4c63e726
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319223"
---
# <a name="e-wmi"></a>E (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) E [F](gloss-f.md) G [р](gloss-h.md) [.](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [O](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) [S](gloss-s.md) [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_event_class"></span><span id="WMI.GLOSS_EVENT_CLASS"></span>**класс событий**
</dt> <dd>

Класс WMI, с помощью которого *потребители событий* могут подписываться на *запросы событий*. Класс сообщает о конкретном типе вхождения. Например, класс [**Win32 \_ процессстоптраце**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace) сообщает, что конкретный процесс был остановлен.

</dd> <dt>

<span id="wmi.gloss_event_consumer"></span><span id="WMI.GLOSS_EVENT_CONSUMER"></span>**потребитель событий**
</dt> <dd>

Объект-получатель уведомлений о том, что произошло данное событие. Потребитель событий может быть [*временным*](gloss-t.md) или [*постоянным*](gloss-p.md).

</dd> <dt>

<span id="wmi.gloss_event_consumer_provider"></span><span id="WMI.GLOSS_EVENT_CONSUMER_PROVIDER"></span>**Поставщик потребителей событий**
</dt> <dd>

Поставщик, определяющий, какой постоянный объект-получатель события обрабатывает данное событие. Поставщик объекта-получателя событий регистрируется в инструментарии WMI экземпляром [**\_ \_ евентконсумерпровидеррегистратион**](--eventconsumerproviderregistration.md), который содержит список логических классов [*потребителей*](gloss-l.md) , поддерживаемых поставщиком объектов-получателей событий. Поставщик потребителей событий — это сервер COM, который сопоставляет [*физических потребителей*](gloss-p.md) с *логическими потребителями*. Поставщик потребителей событий поддерживает интерфейс [**ивбемевентконсумерпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) и является компонентом постоянной пользовательской архитектуры.

</dd> <dt>

<span id="wmi.gloss_event_filter"></span><span id="WMI.GLOSS_EVENT_FILTER"></span>**фильтр событий**
</dt> <dd>

Экземпляр системного класса [**\_ \_ EventFilter**](--eventfilter.md) , описывающий тип события и условия доставки уведомления. Потребитель использует фильтр событий для регистрации, чтобы получить уведомление о конкретном типе события.

</dd> <dt>

<span id="wmi.gloss_event_provider"></span><span id="WMI.GLOSS_EVENT_PROVIDER"></span>**поставщик событий**
</dt> <dd>

Поставщик WMI, отслеживающий источник событий и уведомляющий Инструментарий WMI о происходящих событиях. Поставщик событий реализует интерфейсы [**ивбемпровидеринит**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) и [**ивбемевентпровидер**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) , а иногда [**ивбемевентпровидеркуерисинк**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink).

</dd> <dt>

<span id="wmi.gloss_event_query"></span><span id="WMI.GLOSS_EVENT_QUERY"></span>**запрос события**
</dt> <dd>

Инструкция [*язык запросов WMI*](gloss-w.md) , используемая потребителями событий для регистрации для получения уведомлений о конкретных событиях. Поставщик событий использует запрос событий для регистрации на генерирование уведомлений о событиях определенного типа.

</dd> <dt>

<span id="wmi.gloss_extension_schema"></span><span id="WMI.GLOSS_EXTENSION_SCHEMA"></span>**Схема расширения**
</dt> <dd>

третий уровень [*схемы cim*](gloss-c.md), в который входят расширения схемы cim, зависящие от платформы, такие как Windows, UNIX и Exchange Server. См. также [*Общие*](gloss-c.md) модели и модель ядра.

</dd> <dt>

<span id="wmi.gloss_extrinsic_event"></span><span id="WMI.GLOSS_EXTRINSIC_EVENT"></span>**внешние события**
</dt> <dd>

Уведомление о событии от поставщика. Большинство поставщиков создают экземпляр класса событий, определенного в MOF-файлах поставщика. Внешнее событие наследует от [**\_ \_ екстринсицевент**](--extrinsicevent.md). Например, [Поставщик журнала событий](/previous-versions/windows/desktop/eventlogprov/event-log-provider) определяет класс событий [**Win32 \_ нтложевент**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). См. также [*Внутреннее событие*](gloss-i.md).

</dd> </dl>

 

 
