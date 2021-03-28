---
description: Используйте квалификаторы, определенные в этом разделе, при создании класса MOF поставщика, класса MOF события, класса события типа MOF и свойств класса события типа MOF.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Квалификаторы MOF трассировки событий
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7b4250b73e84d46a19dab307d0c263ab1cc7782
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913280"
---
# <a name="event-tracing-mof-qualifiers"></a>Квалификаторы MOF трассировки событий

Используйте квалификаторы, определенные в этом разделе, при создании [класса MOF поставщика](#provider-mof-class-qualifiers), [класса MOF события](#event-mof-class-qualifiers), [класса события типа MOF](#event-type-mof-class-qualifiers)и [свойств класса события типа MOF](#property-qualifiers). Пример, включающий некоторые из этих квалификаторов, см. в разделе [Публикация схемы событий](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>Квалификаторы классов MOF поставщика

В следующей таблице перечислены квалификаторы, которые можно указать в классе MOF поставщика.



| Квалификатор | Тип данных  | Описание                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Устройства**  | **String** | Обязательный. Строковый идентификатор GUID, однозначно определяющий поставщика. Например, GUID ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Это тот же идентификатор GUID, который вы используете при вызове функции [**регистертрацегуидс**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) для регистрации поставщика. |



 

## <a name="event-mof-class-qualifiers"></a>Квалификаторы класса событий MOF

В следующей таблице перечислены квалификаторы, которые можно указать в классе событий (родительский класс, группирующий связанные классы типов событий).

| Квалификатор        | Тип данных   | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Устройства**         | **String**  | Обязательный. Строковый идентификатор GUID, определяющий класс событий. Например, GUID ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Поставщики событий используют идентификатор GUID для задания [**\_ заголовка трассировки событий \_ . Элемент GUID**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) , чтобы потребители могли определить класс событий, которые они получают.                                                                                                                                                                                                                                                                                  |
| **евентверсион** | **Integer** | Этот квалификатор является необязательным для последней версии класса трассировки событий и является обязательным для всех более старых версий класса. Последняя версия класса либо не указывает квалификатор **евентверсион** , либо имеет наивысший номер версии. Номера версий начинаются с 0, например Евентверсион (0). Как правило, при создании новой версии класса вы также переименовываете предыдущую версию в <classname> \_ VN, где n — это добавочный номер, начинающийся с 0. Пример см. в разделе [**FileIo**](fileio.md) and [**FileIo \_ v0**](fileio-v0.md).<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>Квалификаторы класса для типов событий MOF

В следующей таблице перечислены квалификаторы, которые можно указать в классе типа события (класс, определяющий данные свойства события).



| Квалификатор         | Значение       | Описание                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Integer** | Обязательный. Идентифицирует класс типа события. Например, EventType (1). Поставщик событий использует то же значение типа события для задания [**\_ заголовка трассировки событий \_ . Class. Type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Если один и тот же класс MOF используется для нескольких типов событий (так как они используют одинаковые данные событий), укажите значение типа события в виде массива целых чисел, например EventType {12,15} . |
| **EventTypeName** | **String**  | Необязательный параметр. Описывает тип события. Например, EventTypeName ("Start"). Если один и тот же класс MOF используется для нескольких типов событий (так как они используют одинаковые данные событий), укажите значение имени типа события в виде массива строк, например EventTypeName {"Start", "End"}. Элементы массива EventTypeName непосредственно соответствуют массиву EventType.                 |



 

## <a name="property-qualifiers"></a>Квалификаторы свойств

В следующей таблице перечислены квалификаторы, которые можно указать для свойства.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Квалификатор</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Массив</strong></td>
<td>Задает битовые позиции, которые сопоставляются со строковыми значениями. При указании этого квалификатора необходимо также указать квалификатор <strong>битвалуес</strong> .</td>
</tr>
<tr class="even">
<td><strong>битвалуес</strong></td>
<td>Строковые значения. Если также указан квалификатор <strong>Bitmap</strong> , строки непосредственно соответствуют значениям квалификатора <strong>точечного рисунка</strong> . В противном случае предположим, что значение свойства является однозначным индексом в строках значений (бит один соответствует первой строке в списке).</td>
</tr>
<tr class="odd">
<td><strong>Расширение</strong></td>
<td>Предоставляет дополнительные сведения о том, как использовать (интерпретировать) данные. Значение расширения не учитывает регистр. Включите значение в кавычки, например расширение ( &quot; GUID &quot; ). Возможные значения расширения: <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Устройства</dt> <dd> Указывает, что данные свойства являются идентификатором GUID. Тип данных MOF должен быть <strong>Object</strong>. Полезная нагрузка должна быть структурой <strong>GUID</strong> .<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>Reduce и IPAddrV4</dt> <dd> Данные представляют собой IPv4-адрес. Тип данных MOF должен быть <strong>Object</strong>. Полезные данные должны быть длинными без знака. Каждый байт беззнакового типа Long представляет одну из четырех частей IP-адреса (P1. P2. P3. P4). Байт нижнего порядка содержит значение для P1, следующий байт содержит значение для P2 и т. д.<br/> <strong>До Windows Vista:</strong> Расширение IPAddrV4 не поддерживается.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Данные представляют собой IPv6-адрес. Тип данных MOF должен быть <strong>Object</strong>. Полезная нагрузка должна быть структурой <strong>IN6_ADDR</strong> . <br/> <strong>До Windows Vista:</strong> Расширение IPAddrV6 не поддерживается.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>Печать непечатаемых страниц</dt> <dd> Указывает, что потребитель не должен печатать эти данные.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Порту</dt> <dd> Данные определяют номер порта. Тип данных MOF должен быть <strong>Object</strong>. Полезные данные должны быть короткими без знака.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RStr</dt> <dd> Символы новой строки были заменены пробелами. Полезная нагрузка должна быть строкой ANSI, завершающейся нулем.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>рвстринг</dt> <dd> Символы новой строки были заменены пробелами. Полезная нагрузка должна быть строкой расширенных символов, завершающейся нулем.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Трансляцию</dt> <dd> Данные представляют идентификатор безопасности двоичного объекта BLOB. Тип данных MOF должен быть <strong>Object</strong>. <br/> Идентификатор безопасности имеет переменную длину. Значение, содержащееся в первых 4-байтах (<strong>ulong</strong>), указывает, содержит ли большой двоичный объект идентификатор безопасности. Если первый 4-байтный (<strong>ulong</strong>) большой двоичный объект не равен нулю, BLOB-объект содержит идентификатор безопасности. Первая часть большого двоичного объекта содержит TOKEN_USER (структура соответствует 8-байтовой границе), а вторая часть содержит идентификатор безопасности. Чтобы устранить часть SID большого двоичного объекта, сделайте следующее:<br/>
<ul>
<li>Установка указателя байта на начало большого двоичного объекта</li>
<li>Умножьте размер указателя для журнала событий на 2 и добавьте продукт в указатель байта (элемент <strong>поинтерсизе</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> содержит значение размера указателя).</li>
</ul>
<br/> Чтобы определить длину идентификатора безопасности, можно использовать следующий макрос. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Указывает, что свойство содержит значение указателя. Размер значения указателя зависит от операционной системы, используемой для регистрации события. полезные данные будут содержать 4-байтное значение для 32-разрядных систем или 8-байтовые значения для 64-разрядных систем. Тип данных MOF должен быть <strong>Object</strong>.<br/> Потребители должны игнорировать тип данных и квалификатор <strong>формата</strong> , если свойство включает расширение <strong>size</strong> . Чтобы определить размер данных для чтения для свойства, используйте:
<ul>
<li>Член <strong>поинтерсизе</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Элемент <strong>flags</strong> в <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>До Windows Vista:</strong> Значение <strong>поинтерсизе</strong> может быть неточным. Например, на 64-разрядном компьютере 32-разрядное приложение будет регистрировать 4-байтовые указатели; Однако сеанс установит значение <strong>поинтерсизе</strong> равным 8.<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Значение</dt> <dd> Данные представляют большой двоичный объект. Первые четыре байта (UInt32) указывают размер большого двоичного объекта. Тип данных MOF должен быть <strong>Object</strong>. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>вмитиме</dt> <dd> Преобразует отметку времени в системное время. Тип данных MOF должен быть <strong>Object</strong>. Ожидается, что полезная нагрузка будет представлять собой 64-разрядное целое число без знака.<br/> <strong>До Windows Vista:</strong> Недоступно.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Формат</strong></td>
<td>Определяет формат данных свойства. Например, параметр Format ( &quot; w &quot; ) в строковом свойстве указывает, что строка является широкой строкой. Возможны следующие значения:
<table>
<thead>
<tr class="header">
<th>Термин</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>ц<br/></td>
<td>Отображение значения свойства в виде символа ASCII. Этот квалификатор можно использовать с типами данных <strong>Uint8</strong> .<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>#d0<br/></td>
<td>Обрабатывает массив символов как строку, завершающуюся нулем. Строка является строкой расширенных символов, если тип данных — <strong>Char16</strong>; в противном случае строка является строкой символов ASCII.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>Белая<br/></td>
<td>Значение свойства является строкой расширенных символов. Этот квалификатор можно использовать с <strong>строковыми</strong> типами данных. <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>x<br/></td>
<td>Отображение значения свойства в виде шестнадцатеричного числа. Этот квалификатор можно использовать с 16-, 32-и 64-разрядными целочисленными типами данных.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Указатель</strong></td>
<td><p>Указывает, что свойство содержит значение указателя. Размер значения указателя зависит от операционной системы, используемой для регистрации события. полезные данные будут содержать 4-байтное значение для 32-разрядных систем или 8-байтовые значения для 64-разрядных систем. Тип данных MOF должен быть <strong>Object</strong>.</p>
<p>Потребители должны игнорировать тип данных и квалификатор <strong>формата</strong> , если свойство включает расширение <strong>size</strong> . Чтобы определить размер данных для чтения для свойства, используйте:</p>
<ul>
<li>Член <strong>поинтерсизе</strong> <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Элемент <strong>flags</strong> в <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>До Windows Vista:</strong> Значение <strong>поинтерсизе</strong> может быть неточным. Например, на 64-разрядном компьютере 32-разрядное приложение будет регистрировать 4-байтовые указатели; Однако сеанс установит значение <strong>поинтерсизе</strong> равным 8.</p>
<p>Обратите внимание, что некоторые события используют <strong>поинтертипе</strong> вместо <strong>указателя</strong>; не используйте <strong>поинтертипе</strong>.</p></td>
</tr>
<tr class="even">
<td><strong>стрингтерминатион</strong></td>
<td>Указывает, как свойство строки завершается. Например, Стрингтерминатион ( &quot; NullTerminated &quot; ) указывает, что строковое свойство завершается нулем. Возможны следующие значения:
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Учитываться</strong></dt> <dd>
<p>Длина строки внедряется в начало строки в виде значения <strong>UShort</strong> .</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>ноткаунтед</strong></dt> <dd>
<p>Строка не завершается нулем, а длина строки не внедряется в начало строки. В этом случае строка должна быть последним элементом и занимать все пространство до конца данных события.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>Строка завершается нулем. Если не указать квалификатор <strong>стрингтерминатион</strong> , предполагается, что строка завершается нулем.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>реверсекаунтед</strong></dt> <dd>
<p>Длина строки внедряется в начало строки в виде значения <strong>UShort</strong> в формате с обратным порядком байтов.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>валуедескриптионс</strong></td>
<td>Содержит описания для каждого значения в квалификаторе <strong>Values</strong> . Функции <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>тдхенумератепровидерфиелдинформатион</strong></a> и <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>тдхкуерипровидерфиелдинформатион</strong></a> возвращают эти описания при попытке получить сведения о ключевом слове и уровне. Описания являются необязательными. Если описания не предоставлены, функции возвращают <strong>значение NULL</strong>. Дополнительные сведения см. <a href="#specifying-level-and-enable-flags-values-for-a-provider">в разделе Указание уровней и включение значений флагов для поставщика</a> .</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Задает целочисленный индекс или значения флага, которые сопоставляются со строковыми значениями. При указании этого квалификатора необходимо также указать квалификатор <strong>Values</strong> и, при необходимости, квалификатор <strong>ValueType</strong> . Обратите внимание, что ETW не поддерживает параметр WMI со строками для значений карт значений.
<p>В следующем примере показано, как использовать квалификаторы ValueMap, Values и ValueType.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Значения</strong></td>
<td>Строковые значения. Если также указан квалификатор <strong>ValueMap</strong> , строки непосредственно соответствуют значениям в квалификаторе <strong>ValueMap</strong> . В противном случае предположим, что значение свойства является индексом, начинающимся с нуля, в строки значения.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Указывает, являются ли значения <strong>ValueMap</strong> целочисленными значениями индекса или значениями битового флага. Если этот квалификатор не указан, предполагается целочисленное значение индекса. Чтобы указать, что значения являются целочисленными значениями индекса, используйте ValueType ( &quot; index &quot; ). Чтобы указать, что значения являются битовыми значениями флага, используйте ValueType ( &quot; флаг &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>вмидатаид</strong></td>
<td>Каждое свойство должно содержать квалификатор <strong>вмидатаид</strong> . <strong>Вмидатаид</strong> определяет порядок, в котором потребитель считывает данные события. Значение для <strong>вмидатаид</strong> начинается с 1 и увеличивается для каждого свойства в классе. Например, Вмидатаид (1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Указывает, что данные имеют формат XML и готовы к отображению без дальнейшего форматирования.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Указание значений уровня и включения флагов для поставщика

Чтобы задокументировать уровень и включить флаги, которые контроллер будет использовать для включения поставщика, включите свойства Level и flags в класс MOF поставщика. В именах свойств Level и flags учитывается регистр. Свойства должны включать квалификаторы **Values** и **ValueMap** , которые указывают возможные уровни и включают значения флагов. Значение **ValueMap** для значений флагов включения должно быть битовым (флагом) значением. Квалификатор **валуедескриптионс** является необязательным, но его следует использовать для предоставления описаний для каждого возможного значения. Описания используются, когда кто-то вызывает функции [**тдхенумератепровидерфиелдинформатион**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) и [**тдхкуерипровидерфиелдинформатион**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) для получения возможного уровня и включения значений Flags (keywords) для поставщика.

Ниже показан класс поставщика, который указывает возможные значения уровня и включения флагов.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
