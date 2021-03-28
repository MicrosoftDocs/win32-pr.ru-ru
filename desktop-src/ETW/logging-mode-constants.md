---
description: Следующие константы представляют возможные режимы ведения журнала для сеанса трассировки событий.
ms.assetid: d12aaecb-776a-4476-9ba4-16af30fde9c2
title: Константы режима ведения журнала
ms.topic: article
ms.date: 06/03/2020
ms.openlocfilehash: daa0233346718040653edbc75a10615f9fd31765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984573"
---
# <a name="logging-mode-constants"></a>Константы режима ведения журнала

Следующие константы представляют возможные режимы ведения журнала для сеанса трассировки событий.

Константы используются в элементах **логфилемоде** [**\_ \_ журнала трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea), [**\_ \_ свойствах трассировки событий**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) и структурах [**\_ \_ заголовка файла журнала трассировки**](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header) . Эти константы определены в файле заголовка *евнтраце. h* .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Режим</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NONE</strong> (0x00000000)</td>
<td>То же, что <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> без указанного максимального размера файла.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong> (0x00000001)</td>
<td>Последовательное запись событий в файл журнала; останавливается, когда файл достигает максимального размера. Не используйте с <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> или <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong> (0x00000002)</td>
<td>Записывает события в файл журнала. Когда файл достигает максимального размера, самые старые события заменяются входящими событиями. Обратите внимание, что содержимое циклического файла журнала может отображаться неупорядоченно на многопроцессорных компьютерах.<br/> Не используйте с <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>или <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_APPEND</strong> (0x00000004)</td>
<td>Добавляет события в существующий последовательный файл журнала. Если файл не существует, он будет создан. Используйте только в том случае, если задано <a href="wnode-header.md"><strong>системное время</strong></a> для разрешения часов, в противном случае <a href="/windows/win32/api/evntrace/nf-evntrace-processtrace"><strong>процесстраце</strong></a> будет возвращать события с неправильными штампами времени. При использовании <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>значения для <strong>bufferSize</strong>, <strong>NumberOfProcessors</strong>и <strong>клокктипе</strong> должны быть указаны явно и должны быть одинаковыми в средстве ведения журнала и в добавляемом файле.<br/> Не используйте с <strong>EVENT_TRACE_REAL_TIME_MODE</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>или <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong> (0x00000008)</td>
<td>Автоматически переключается на новый файл журнала, когда файл достигает максимального размера. Необходимо <strong></strong> задать элемент максимумфилесизе <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a> . Указанное имя файла должно быть отформатированной строкой (например, строка содержит% d, например к:\тест%д.ЕТЛ). Каждый раз, когда создается новый файл, счетчик увеличивается и используется его значение, отформатированная строка обновляется, а результирующая строка используется в качестве имени файла.<br/> Этот параметр не разрешен для сеансов трассировки частных событий и не должен использоваться для сеансов ведения журнала ядра NT.<br/> Не используйте с <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong> или <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_FILE_MODE_PREALLOCATE</strong>(0x00000020)</td>
<td>Резервирует <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. Максимумфилесизе</strong></a> байты места на диске для файла журнала заранее. Файл занимает все пространство во время ведения журнала для циклического и последовательного файлов журнала. При прерывании сеанса размер файла журнала уменьшается до необходимого размера. Необходимо задать <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES. Максимумфилесизе</strong></a>.<br/> Вы не можете использовать режим для сеансов трассировки закрытых событий.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NONSTOPPABLE_MODE</strong>(0x00000040)</td>
<td>Не удается остановить сеанс ведения журнала. Этот режим поддерживается только авторегистратором. Этот параметр поддерживается в Windows Vista и более поздних версиях.<br/>.</td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_SECURE_MODE</strong> (0X00000080)</td>
<td>Позволяет ограничивать регистрацию событий в сеансе с помощью разрешения <a href="/windows/desktop/api/Evntcons/nf-evntcons-eventaccesscontrol"><strong>TRACELOG_LOG_EVENT</strong></a> . Этот параметр поддерживается в Windows Vista и более поздних версиях.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_REAL_TIME_MODE</strong> (0x00000100)</td>
<td>Предоставляет события потребителям в режиме реального времени. События доставляются при очистке буферов, а не на момент записи события поставщиком. Не следует включать режим реального времени, если нет потребителей для использования событий, так как вызовы для журнала событий будут завершаться сбоем при заполнении буферов. До Windows Vista, если события не использовались, события были отклонены. Не указывайте более одного потребителя в режиме реального времени в одном процессе на Windows XP Орвиндовс Server 2003. Вместо этого один поток потребляет события и распределяет события среди других.<br/> <strong>До Windows Vista:</strong> Не следует использовать режим реального времени, так как Поддерживаемая частота событий намного ниже, чем при чтении из файла журнала (события могут быть удалены). Кроме того, порядок событий не гарантируется на компьютерах с несколькими процессорами. Режим реального времени более подходит для событий низкого уровня трафика, типов уведомлений.<br/> <br/> Этот режим можно сочетать с другими режимами файла журнала. Однако не используйте этот режим с EVENT_TRACE_PRIVATE_LOGGER_MODE. Обратите внимание, что при объединении этого режима с другими режимами файла журнала буферы будут сбрасываться каждую секунду, что приведет к записи в файл журнала частично заполненных буферов. Например, если вы используете буферы размером 64 КБ и скорость ведения журнала составляет 1 событие каждую секунду, служба запишет в файл журнала 64 КБ/с.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_DELAY_OPEN_FILE_MODE</strong>(0x00000200)</td>
<td>Этот режим используется для задержки открытия файла журнала до возникновения события. <br/>
<blockquote>
<strong>Примечание</strong>.<br />
В Windows Vista и более поздних версиях этот режим не применяется, не следует использовать.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_BUFFERING_MODE</strong> (0x00000400)</td>
<td>Этот режим записывает события в буфер кольцевой памяти. События, записанные за пределами общего размера буфера, проудаляют самые старые события, оставшиеся в буфере. Размер этого буфера памяти является продуктом <strong>MinimumBuffers</strong> и <strong>bufferSize</strong> (см. <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>). Как следствие этой формулы, любой буфер, использующий <strong>EVENT_TRACE_BUFFERING_MODE</strong> , будет игнорировать значение <strong>максимумбуфферс</strong> .<br/> События не записываются в файл журнала или доставляются в режиме реального времени, а ETW не очищает буферы. Чтобы получить моментальный снимок буфера, вызовите функцию <a href="/windows/win32/api/evntrace/nf-evntrace-flushtracea"><strong>флуштраце</strong></a> .<br/> Этот режим особенно полезен для отладки драйверов устройств в сочетании с возможностью просмотра содержимого буферов в памяти с помощью расширения отладчика ядра <a href="/windows-hardware/drivers/devtest/trace-session">вмитраце</a> .<br/> Не используйте с <strong>EVENT_TRACE_FILE_MODE_SEQUENTIAL</strong>, <strong>EVENT_TRACE_FILE_MODE_CIRCULAR</strong>, <strong>EVENT_TRACE_FILE_MODE_APPEND</strong>, <strong>EVENT_TRACE_FILE_MODE_NEWFILE</strong>или <strong>EVENT_TRACE_REAL_TIME_MODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> (0x00000800)</td>
<td>Создает сеанс отслеживания событий пользовательского режима, который выполняется в том же процессе, что и его поставщик трассировки событий. Память для буферов берется из памяти процесса. Процессы, не требующие данных от ядра, могут исключить издержки, связанные с переходами в режиме ядра, с помощью закрытого сеанса трассировки событий.<br/> Если поставщик регистрируется несколькими процессами, ETW добавляет идентификатор процесса в имя файла журнала, чтобы создать уникальное имя файла журнала. Например, если контроллер определяет имена файлов журнала как к:\милогс\мипривателог.ЕТЛ, ETW создает файл журнала как к:\милогс\ myprivatelog.etl_nnnn, где nnnn — это идентификатор процесса. Идентификатор процесса не добавляется к первому процессу, который регистрирует поставщик. он добавляется только в последующие процессы, регистрирующие поставщик.<br/> Сеансы трассировки закрытых событий имеют следующие ограничения.<br/>
<ul>
<li>Закрытый сеанс может записывать события только для потоков процесса, в котором он выполняется.</li>
<li>На процесс может быть до восьми частных сеансов.</li>
<li>Нельзя использовать частные сеансы с доставкой в режиме реального времени.</li>
<li>События, создаваемые частным сеансом, не включают время выполнения для инструкций в режиме ядра и инструкции пользовательского режима или сведения об используемом времени ЦП на уровне потока.</li>
</ul>
Фильтры ИДЕНТИФИКАТОРов процессов и имена исполняемых файлов теперь можно передавать в интерфейсы API управления сеансами при запуске общедоступных служебных средств ведения журнала. Для получения наилучших результатов в сценариях кросс-обработка одни и те же фильтры должны передаваться каждой операции управления во время сеанса, включая вызовы Enable/диасбле поставщика. Обратите внимание, что фильтры имеют тот же формат, который используется <a href="/windows/win32/api/evntrace/nf-evntrace-enabletraceex2"><strong>EnableTraceEx2</strong></a>. <br/> Этот режим можно использовать в сочетании с режимом <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> .<br/> <strong>До Windows 10, версия 1703:</strong> Только учетные записи LocalSystem, Administrator и Users в группе администраторов, которые выполняются в процессе с повышенными правами, могут создать частный сеанс. Если включить флаг <strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> , любой пользователь может создать внутрипроцессный частный сеанс. Кроме того, в предыдущих версиях Windows для одного процесса может существовать только один частный сеанс (кроме случая, когда также указан режим EVENT_TRACE_PRIVATE_IN_PROC. в этом случае можно создать до трех в процессе частных сеансов). <br/> <strong>До Windows Vista:</strong> Пользователи из группы "Пользователи журнала производительности" могут также создать частный сеанс.<br/> <br/> Не используйте с EVENT_TRACE_REAL_TIME_MODE.<br/> <strong>До Windows 7 и Windows Server 2008 R2:</strong> Не используйте с EVENT_TRACE_FILE_MODE_NEWFILE.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_ADD_HEADER_MODE</strong>(0x00001000)</td>
<td>Этот параметр добавляет заголовок в файл журнала.<br/>
<blockquote>
<strong>Примечание</strong>.<br />
В Windows Vista и более поздних версиях этот режим не применяется, не следует использовать.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_KBYTES_FOR_SIZE</strong>(0x00002000)</td>
<td>Используйте килобайты в качестве единицы измерения для указания размера файла. Единицей измерения по умолчанию является мегабайт. Этот режим применяется к значению реестра <strong>MaxFileSize</strong> для сеанса <a href="configuring-and-starting-an-autologger-session.md">авторегистратора</a> и элементу <strong>максимумфилесизе</strong> в <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_properties"><strong>EVENT_TRACE_PROPERTIES</strong></a>. Этот параметр поддерживается в Windows Vista и более поздних версиях.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong>(0x00004000)</td>
<td>Использует порядковые номера, уникальные для сеансов трассировки событий. Этот режим применяется только к событиям, регистрируемым с помощью функции <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>трацемессаже</strong></a> . Дополнительные сведения см. в разделе <strong>трацемессаже</strong> to Usage Details.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> и <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> являются взаимоисключающими.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> (0x00008000)</td>
<td>Использует порядковые номера, уникальные только для отдельного сеанса трассировки событий. Этот режим применяется только к событиям, регистрируемым с помощью функции <a href="/windows/win32/api/evntrace/nf-evntrace-tracemessage"><strong>трацемессаже</strong></a> . Дополнительные сведения см. в разделе <strong>трацемессаже</strong> to Usage Details.<br/> <strong>EVENT_TRACE_USE_GLOBAL_SEQUENCE</strong> и <strong>EVENT_TRACE_USE_LOCAL_SEQUENCE</strong> являются взаимоисключающими.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_RELOG_MODE</strong> (0x00010000)</td>
<td>Регистрирует событие, не включая <a href="/windows/win32/api/evntrace/ns-evntrace-event_trace_header"><strong>EVENT_TRACE_HEADER</strong></a>.
<blockquote>
<strong>Примечание</strong>.<br />
Этот режим не следует использовать. Он зарезервирован для внутреннего использования.
</blockquote>
<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_PRIVATE_IN_PROC</strong> (0x00020000)</td>
<td>Используйте в сочетании с режимом <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> для запуска закрытого сеанса. Этот режим гарантирует, что только процесс, который зарегистрировал GUID поставщика, может запустить сеанс ведения журнала с этим GUID.<br/> Для каждого процесса можно создать до трех процессов в виде частных сеансов.<br/> Этот параметр поддерживается в Windows Vista и более поздних версиях.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_MODE_RESERVED</strong>(0x00100000)</td>
<td>Этот параметр используется для сигнализации трассировки кучи и критической секции. Этот параметр поддерживается в Windows Vista и более поздних версиях.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong>(0x00400000)</td>
<td>Этот параметр останавливает ведение журнала гибридного завершения работы. Если не указано ни <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> , ни <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW выбирает значение по умолчанию в зависимости от того, поступает ли вызывающий объект из сеанса 0. Этот параметр поддерживается в Windows 8 и Windows Server 2012. <br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong>(0x00800000)</td>
<td>Этот параметр позволяет продолжить ведение журнала гибридного завершения работы. Если не указано ни <strong>EVENT_TRACE_STOP_ON_HYBRID_SHUTDOWN</strong> , ни <strong>EVENT_TRACE_PERSIST_ON_HYBRID_SHUTDOWN</strong> , ETW выбирает значение по умолчанию в зависимости от того, поступает ли вызывающий объект из сеанса 0. Этот параметр поддерживается в Windows 8 и Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_USE_PAGED_MEMORY</strong> (0x01000000)</td>
<td>Использует страничную память. Этот параметр рекомендуется использовать, чтобы события не использовали нестраничную память. Нестраничные буферы используют память в невыгружаемом страничном пространстве для буферного пространства. Поскольку буферы без страничного обмена никогда не выгружаются, сеанс ведения журнала работает нормально. Использование страничных буферов снижает нагрузку на ресурсы.<br/> Поставщики режима ядра и системные средства ведения журнала не могут регистрировать события в сеансах, в которых указан этот режим ведения журнала.<br/> Этот режим игнорируется, если задан параметр <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong> .<br/> Этот режим нельзя использовать с журналом ядра NT.<br/> <strong>Windows 2000:</strong> Это значение не поддерживается.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_SYSTEM_LOGGER_MODE</strong>(0x02000000)</td>
<td>Этот параметр позволяет получить события от Системтрацепровидер. Если параметр <a href="/windows/win32/api/evntrace/nf-evntrace-starttracea"><strong>старттраце</strong></a><em>Properties</em> <strong>логфилемоде</strong> включает этот флаг, средство ведения журнала будет системным средством ведения журнала. Этот параметр поддерживается в Windows 8 и Windows Server 2012. <br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_INDEPENDENT_SESSION_MODE</strong>(0x08000000)</td>
<td>Указывает, что для сеанса ведения журнала не должны быть затронуты сбои <a href="/windows/desktop/api/Evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> в других сеансах. Без этого флага, если событие не может быть опубликовано в одном из сеансов, на которое включен поставщик, событие не будет опубликовано ни в одном из сеансов. Если этот флаг установлен, ошибка записи события в один сеанс не приведет к возврату функцией <strong>EventWrite</strong> кода ошибки в других сеансах. <br/> Не используйте с <strong>EVENT_TRACE_PRIVATE_LOGGER_MODE</strong>. <br/> Этот параметр поддерживается в Windows 8.1, Windows Server 2012 R2 и более поздних версиях.<br/></td>
</tr>
<tr class="odd">
<td><strong>EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING</strong> (0x10000000)</td>
<td>Записывает события, которые были зарегистрированы на разных процессорах, в общий буфер. Использование этого режима может устранить проблемы, возникшие при публикации событий на разных процессорах с помощью системного времени. Этот режим также позволяет устранить проблемы с циклическими журналами, которые появляются для удаления событий на нескольких процессорных компьютерах.<br/> Если этот режим не используется и используется системное время, события могут отображаться не по порядку на нескольких процессорных компьютерах. Это обусловлено тем, что буферы ETW связаны с процессором, а не с потоком. В результате, если поток переключается с одного ЦП на другой, буфер, связанный с последним ПРОЦЕССОРом, может быть записан на диск до того, как он был связан с предыдущим ПРОЦЕССОРом.<br/> Если вы ожидаете большой объем событий (например, более 1 000 событий в секунду), не следует использовать этот режим.<br/> Обратите внимание, что номер процессора не входит в состав события.<br/> Этот параметр поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.<br/></td>
</tr>
<tr class="even">
<td><strong>EVENT_TRACE_ADDTO_TRIAGE_DUMP</strong>(0x80000000)</td>
<td>Этот параметр добавляет буферы ETW к дампам рассмотрения. Этот параметр поддерживается в Windows 8 и Windows Server 2012. <br/></td>
</tr>
</tbody>
</table>
