---
description: В этом разделе описываются новые функции, добавленные в трассировку событий для Windows в каждом выпуске.
ms.assetid: 5d94a6d2-2280-4a97-aa5a-c9ca2c016c84
title: Новые возможности трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613433834e5a11f2886b6ee314fdb60114f66976
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810924"
---
# <a name="whats-new-in-event-tracing"></a>Новые возможности трассировки событий

В этом разделе описываются новые функции, добавленные в трассировку событий для Windows в каждом выпуске.

## <a name="windows-10-version-1709"></a>Windows 10 версии 1709

Теперь ETW может при необходимости отслеживаниь двоичных файлов для всех поставщиков, включенных в сеанс. Отслеживание применяет задним числом для поставщиков, которые были включены в сеанс до вызова, а также для всех будущих поставщиков, включенных в сеанс. Теперь вы также можете запросить текущее максимальное количество системных средств ведения журнала, разрешенное операционной системой. Дополнительные сведения см. в описании значений **трацепровидербинаритраккинг** и **трацемакслогжерскуери** в перечислении [**\_ \_ классов сведений трассировки**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) , а также при [извлечении дополнительных данных трассировки событий](retrieving-additional-event-tracing-data.md).

Теперь ETW может фильтровать события на основе имени события. Также можно определить, какие события получают свои стеки. Дополнительные сведения см. в разделе **\_ \_ \_ \_ имя события типа фильтра** событий, **\_ тип фильтра \_ событий \_ стакквалк \_ имя** и **\_ тип фильтра событий \_ \_ \_ \_ кВт *** значения структуры [**\_ \_ дескриптора**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) событий, а также связанные с ними [**\_ \_ \_ имя события фильтра**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_name) событий и [**\_ уровни фильтрации событий \_ \_ кВт ***](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_level_kw) .

## <a name="windows-10"></a>Windows 10

[Трацелоггинг](../tracelogging/trace-logging-portal.md) строится на трассировке событий Windows и предоставляет упрощенный способ инструментирования кода для разработчиков в машинном коде, .NET и WinRT. Трацелоггинг позволяет включать структурированные данные с событиями, сопоставлять события и не требует отдельного XML-файла манифеста инструментирования.

[Признаки поставщика](provider-traits.md) были добавлены как метод присоединения дополнительных данных к регистрации отдельного поставщика. Их можно использовать для поставщиков на основе манифеста или Трацелоггинг. В настоящее время это включает поддержку добавления имени поставщика и (или) группы поставщиков к регистрации отдельного поставщика. Группы поставщиков — это новая функция, позволяющая управлять несколькими поставщиками ETW в статистической обработке группой, к которой они принадлежат.

Состояние периодической записи — это способ, который позволяет регулярно отправлять уведомления о состоянии записи поставщикам. Если этот параметр включен, уведомления будут отправляться только в регистрации поставщиков, которые ранее были включены в текущий сеанс. Каждый поставщик может определить собственный ответ (если он есть) для уведомления. Сведения о реализации см. в разделе [**Трассировка \_ \_ \_ \_ сведений о состоянии периодической записи**](/windows/win32/api/evntrace/ns-evntrace-trace_periodic_capture_state_info).

## <a name="windows-81-and-windows-server-2012-r2"></a>Windows 8.1 и Windows Server 2012 R2

Следующие функции были добавлены в трассировку событий на Windows 8.1 и Windows Server 2012 R2.

Функции, поддерживающие использование полезных данных событий, областей и фильтров проверки стека, используемых функцией [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) , [**и \_ структуры \_**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) [**\_ \_ дескрипторов фильтров событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) для фильтрации конкретных условий в сеансе ведения журнала. Дополнительные сведения можно найти в разделе

-   [**тдхаггрегатепайлоадфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhaggregatepayloadfilters)
-   [**тдхклеануппайлоадевентфилтердескриптор**](/windows/desktop/api/Tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor)
-   [**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter)
-   [**тдхделетепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhdeletepayloadfilter)

Кроме того, ознакомьтесь с значительно пересмотренной документацией по функции [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2) и [**включите \_ \_ Параметры трассировки**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) и структуры [**\_ \_ дескрипторов фильтра событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_descriptor) , используемые этими функциями.

Структура, определяющая предикат фильтра полезных данных события, который описывает, как выполнить фильтрацию по одному полю в сеансе трассировки, используемом новой функцией [**тдхкреатепайлоадфилтер**](/windows/desktop/api/Tdh/nf-tdh-tdhcreatepayloadfilter) , и новую структуру, используемую фильтрами событий и проходами по стеку. Дополнительные сведения можно найти в разделе

-   [**\_ \_ идентификатор события фильтра \_ событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_event_id)
-   [**\_предикат фильтра полезных данных \_**](/windows/desktop/api/Tdh/ns-tdh-payload_filter_predicate)

Функции, которые извлекают сведения о событиях, имеющихся в манифесте поставщика. Дополнительные сведения можно найти в разделе

-   [**тдхенумератеманифестпровидеревентс**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents)
-   [**тдхжетманифестевентинформатион**](/windows/desktop/api/Tdh/nf-tdh-tdhgetmanifesteventinformation)

Структура, определяющая массив событий в манифесте поставщика, который используется новой функцией [**тдхенумератеманифестпровидеревентс**](/windows/desktop/api/Tdh/nf-tdh-tdhenumeratemanifestproviderevents) . Дополнительные сведения можно найти в разделе

-   [**\_сведения о событии поставщика \_**](/windows/desktop/api/Tdh/ns-tdh-provider_event_info)

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 и Windows Server 2012

В трассировку событий в Windows 8 и Windows Server 2012 добавлены следующие функции.

Функции, выполняющие операции с объектом регистрации, обеспечивают синтаксический анализ полезных данных событий, предоставляют возможности обзора поставщика трассировки, параметры сеанса трассировки событий запросов и обработку файла трассировки с повторным протоколированием. Дополнительные сведения можно найти в разделе

-   [**евентсетинформатион**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation)
-   [**тдхклоседекодингхандле**](/windows/desktop/api/Tdh/nf-tdh-tdhclosedecodinghandle)
-   [**тдхжетдекодингпараметер**](/windows/desktop/api/Tdh/nf-tdh-tdhgetdecodingparameter)
-   [**тдхжетвпппроперти**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppproperty)
-   [**тдхжетвппмессаже**](/windows/desktop/api/Tdh/nf-tdh-tdhgetwppmessage)
-   [**тдхлоадманифестфромбинари**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifestfrombinary)
-   [**тдхопендекодингхандле**](/windows/desktop/api/Tdh/nf-tdh-tdhopendecodinghandle)
-   [**тдхсетдекодингпараметер**](/windows/desktop/api/Tdh/nf-tdh-tdhsetdecodingparameter)
-   [**трацекуеринформатион**](/windows/win32/api/evntrace/nf-evntrace-tracequeryinformation)

Интерфейсы, предоставляющие сведения о процессе трассировки и регистрации событий, доступе к данным для определенного события и доступе к функциям повторного регистратора, которые позволяют управлять файлами журнала трассировки событий (ETL). Дополнительные сведения можно найти в разделе

-   [**итрацеевент**](/windows/desktop/api/Relogger/nn-relogger-itraceevent)
-   [**итрацеевенткаллбакк**](/windows/desktop/api/Relogger/nn-relogger-itraceeventcallback)
-   [**итрацерелогжер**](/windows/desktop/api/Relogger/nn-relogger-itracerelogger)

Дополнительные перечисления, используемые новыми функциями и интерфейсами. Дополнительные сведения можно найти в разделе

-   [**\_класс сведений о СОбытии \_**](/windows/desktop/api/Evntprov/ne-evntprov-event_info_class)
-   [**\_ \_ класс сведений о запросе трассировки \_**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 и Windows Server 2008 R2

В этом выпуске были добавлены следующие функции:

-   Способность поставщиков определять фильтры в манифесте. В Windows Vista контроллеры могут передавать данные фильтра поставщику. Однако макет данных фильтра не был определен в манифесте, поэтому поставщику пришлось бы использовать другие средства для предоставления определения фильтра контроллерам. В этом выпуске поставщики могут определять определение фильтра в манифесте (см. атрибут **Filters** сложного типа [**ProviderType**](../wes/eventmanifestschema-providertype-complextype.md) ). Затем контроллеры могут использовать функцию [**тдхенумератепровидерфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters) для определения фильтра. Поставщики, использующие фильтры, должны использовать функцию [**евентвритикс**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex) для записи события.
-   Возможность использования одного буфера для сбора событий, создаваемых на нескольких процессорах. Использование одного буфера устраняет неупорядоченные события на компьютерах с несколькими процессорами. Дополнительные сведения см. в [**статье \_ Трассировка событий \_ No \_ для каждого \_ процессора \_ в**](logging-mode-constants.md) режиме ведения журнала. По умолчанию ETW использует буферы каждого процессора.
-   Возможность захвата трассировки стека для событий. Сведения о включении трассировки стека для событий ядра см. в разделе Функция [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) . Сведения о включении трассировки стека для пользовательских событий см. в статье Включение флага **\_ \_ \_ \_ трассировки стека свойств** для элемента **енаблепроперти** в разделе [**включить \_ \_ Параметры трассировки**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters).
-   Возможность указать режим **\_ \_ буферизации \_ трассировки событий** или режим ведения журнала **событий \_ \_ \_ \_** с использованием **\_ \_ закрытого \_ \_** режима ведения журнала трассировки событий (см. раздел [константы режима ведения журнала](logging-mode-constants.md)).
-   Возможность синхронного включения поставщика. По умолчанию поставщики включены асинхронно. Чтобы включить поставщик в синхронном режиме, задайте параметр *timeout* для [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   Способность контроллера запрашивать состояние поставщика в журнале. Дополнительные сведения см. в описании флага **\_ \_ \_ \_ состояния записи кода управления событиями** для параметра *контролкоде* в [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2).
-   Возможность для потребителей форматировать данные событий с помощью функции [**тдхформатпроперти**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty) .
-   Возможность декодирования манифестных событий на компьютерах, которые не содержат поставщика. Дополнительные сведения см. в описании функции [**тдхлоадманифест**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest) .

В этом выпуске были добавлены следующие функции:

-   [**EnableTraceEx2**](/windows/win32/api/evntrace/nf-evntrace-enabletraceex2)
-   [**евентвритикс**](/windows/desktop/api/Evntprov/nf-evntprov-eventwriteex)
-   [**тдхенумератепровидерфилтерс**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfilters)
-   [**тдхформатпроперти**](/windows/desktop/api/Tdh/nf-tdh-tdhformatproperty)
-   [**тдхлоадманифест**](/windows/desktop/api/Tdh/nf-tdh-tdhloadmanifest)
-   [**тдхунлоадманифест**](/windows/desktop/api/Tdh/nf-tdh-tdhunloadmanifest)
-   [**трацесетинформатион**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation)

В этом выпуске были добавлены следующие структуры:

-   [**ИД КЛАССического \_ события \_**](/windows/win32/api/evntrace/ns-evntrace-classic_event_id)
-   [**ВКЛЮЧИТЬ \_ \_ Параметры трассировки**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters)
-   [**\_ \_ \_ TRACE32 стека РАСШИРЕНных элементов событий \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace32)
-   [**\_ \_ \_ TRACE64 стека РАСШИРЕНных элементов событий \_**](/windows/desktop/api/Evntcons/ns-evntcons-event_extended_item_stack_trace64)
-   [**\_заголовок фильтра \_ событий**](/windows/desktop/api/Evntprov/ns-evntprov-event_filter_header)
-   [**\_сведения о фильтре поставщика \_**](/windows/desktop/api/Tdh/ns-tdh-provider_filter_info)

В этом выпуске были добавлены следующие перечисления:

-   [**\_класс сведений \_ трассировки**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class)

В этом выпуске были добавлены следующие классы MOF:

-   [**стакквалк**](stackwalk.md)
-   [**\_Событие стакквалк**](stackwalk-event.md)

 

 
