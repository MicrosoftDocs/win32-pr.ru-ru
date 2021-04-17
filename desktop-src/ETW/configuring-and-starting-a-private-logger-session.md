---
description: Закрытый сеанс трассировки событий — это сеанс трассировки пользовательского режима, который выполняется в том же процессе, что и его поставщики трассировки событий&\# 8212; частный сеанс и поставщики, которые он включает, должны находиться в одном процессе.
ms.assetid: fb6a3899-194e-4cb7-b9e5-a7ff85fb7891
title: Настройка и запуск закрытого сеанса ведения журнала
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ef13728bfb3516197ab153cf90b301d5930ff2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497712"
---
# <a name="configuring-and-starting-a-private-logger-session"></a>Настройка и запуск закрытого сеанса ведения журнала

Закрытый сеанс трассировки событий — это сеанс трассировки пользовательского режима, который выполняется в том же процессе, что и его поставщики трассировки событий — частный сеанс и поставщики, которые он включает, должны находиться в одном процессе. Преимуществом использования закрытого сеанса является то, что частный сеанс не учитывает максимум 64 сеансов трассировки событий, выполняемых одновременно.

Настройка и запуск частного сеанса аналогичны запуску обычного сеанса трассировки событий. Разница заключается в том, что элемент **вноде. GUID** структуры [**\_ \_ свойств трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) должен содержать **идентификатор GUID** поставщика, а не сеанса, а поставщик должен уже зарегистрировать идентификатор GUID. Обратите внимание, что, если вы также настроили \_ функцию трассировки событий " \_ частный" \_ в \_ режиме ведения журнала, можно использовать другой **идентификатор GUID** для сеанса и поставщика. Дополнительные сведения о запуске обычного сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).

Обратите внимание, что нельзя запускать, прекращать или сбрасывать закрытый сеанс трассировки из DllMain; Это необходимо сделать в подпрограммых инициализации и финализации библиотеки DLL.

Из Windows 8.1 к Windows 10, версия 1607, полезные данные события, область действия и фильтры анализа стека могут использоваться функцией [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) , а [**параметры включения \_ трассировки \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) и [**\_ \_ дескриптора фильтра событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) — для фильтрации конкретных условий в сеансе ведения журнала. Дополнительные сведения о фильтрах полезных данных событий см. в статьях функции [**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)и [**тдхаггрегатепайлоадфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters) , а также структуры [**\_ \_ предикатов**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate) **включения \_ трассировки \_**, **\_ \_ дескриптора фильтра событий** и фильтра полезных данных.

Начиная с Windows 10, версия 1703, пользователи с низким уровнем привилегий теперь могут запускать закрытый сеанс ведения журнала в запущенных процессах. Перед включением или запуском закрытого сеанса поставщик больше не должен регистрироваться, что означает, что поставщик является "предварительно включенным", как и у поставщиков сеансов, не являющихся частными. Для отдельного процесса существует ограничение в 8 общесистемных служебных средств ведения журнала. Для повышения производительности в межпроцессных сценариях рекомендуется использовать фильтрацию для интерфейсов API сеанса (включая [**контролтраце**](/windows/win32/api/evntrace/nf-evntrace-controltracea), [**куеритраце**](/windows/win32/api/evntrace/nf-evntrace-querytrace), [**старттраце**](/windows/win32/api/evntrace/nf-evntrace-starttracea)и [**стоптраце**](/windows/win32/api/evntrace/nf-evntrace-stoptrace)) при запуске закрытого частного средства ведения журнала. Обратите внимание, что одни и те же фильтры должны передаваться всем API-интерфейсам сеанса. Дополнительные сведения о фильтрах см. в разделе [**\_ Свойства трассировки событий \_ \_ версии 2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2).

Дополнительные сведения о запуске сеанса трассировки событий см. в разделе [Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md).

Дополнительные сведения о запуске сеанса ведения журнала ядра NT см. в разделе [Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md).

Дополнительные сведения о запуске глобального сеанса ведения журнала см. в разделе [Настройка и запуск глобального сеанса ведения журнала](configuring-and-starting-the-global-logger-session.md).

Дополнительные сведения о запуске сеанса авторегистратора см. в разделе [Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Настройка и запуск сеанса Системтрацепровидер](configuring-and-starting-a-systemtraceprovider-session.md)
</dt> <dt>

[Настройка и запуск сеанса авторегистратора](configuring-and-starting-an-autologger-session.md)
</dt> <dt>

[Настройка и запуск сеанса трассировки событий](configuring-and-starting-an-event-tracing-session.md)
</dt> <dt>

[Настройка и запуск сеанса ведения журнала ядра NT](configuring-and-starting-the-nt-kernel-logger-session.md)
</dt> <dt>

[**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
</dt> <dt>

[**ВКЛЮЧИТЬ \_ \_ Параметры трассировки**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
</dt> <dt>

[**\_Свойства трассировки \_ событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
</dt> <dt>

[**\_Свойства трассировки \_ событий \_ версии 2**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties_v2)
</dt> <dt>

[**\_дескриптор фильтра \_ событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor)
</dt> <dt>

[**\_предикат фильтра полезных данных \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)
</dt> <dt>

[**тдхаггрегатепайлоадфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
</dt> <dt>

[**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
</dt> <dt>

[Обновление сеанса трассировки событий](updating-an-event-tracing-session.md)
</dt> </dl>

 

 
