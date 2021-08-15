---
description: Мфтраце — это средство для создания журналов трассировки для Microsoft Media Foundation приложений.
ms.assetid: f93060dc-cb64-4623-847d-5d78bca59d50
title: Использование Мфтраце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a03cb19f17978236b3e4edd8415f524913c90d99d7a7caf4183dd885d340cfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737327"
---
# <a name="using-mftrace"></a>Использование Мфтраце

Мфтраце — это средство для создания журналов трассировки для Microsoft Media Foundation приложений.

Мфтраце использует библиотеку "краткие обзора" для подключения к Media Foundationным вызовам API и создания журналов трассировки. мфтраце также может записывать трассировки из любого компонента, использующего трассировку событий для Windows (ETW) или препроцессора трассировки программного обеспечения (WPP) для создания трассировок. Журналы трассировки можно создавать путем запуска нового процесса из Мфтраце или путем присоединения Мфтраце к существующему процессу.

## <a name="usage"></a>Использование

**мфтраце** \[ **-a** *Process* \] \[ **-c** *файл ConfigurationFile* \] \[ **-DC** \] \[ **-ES** \] \[ **-k** *keywords* \] \[ **-l** *Level* \] \[ **-o** *выходной_файл* \] \[ **-v** \] \[ **-** ? \] \[ {*Команда* \| *ETL_FILE*}\]



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>аргументов командной строки;</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="-a_Process_ID_or_Process_Name"></span><span id="-a_process_id_or_process_name"></span><span id="-A_PROCESS_ID_OR_PROCESS_NAME"></span><strong>-a</strong> <strong></strong> <em>Идентификатор процесса или имя процесса</em><br/></td>
<td>Присоединение к выполняющемуся процессу.<br/></td>
</tr>
<tr class="even">
<td><span id="-c_Configuration_File"></span><span id="-c_configuration_file"></span><span id="-C_CONFIGURATION_FILE"></span><strong>-c</strong> <strong></strong> <em>Файл конфигурации</em><br/></td>
<td>Чтение параметров из указанного файла конфигурации. См. раздел <a href="mftrace-configuration-file.md">файл конфигурации мфтраце</a>.<br/></td>
</tr>
<tr class="odd">
<td><span id="-dc"></span><span id="-DC"></span><strong>-DC</strong><br/></td>
<td>Отключить трассировку для дочерних процессов. По умолчанию трассировка включена для дочерних процессов.<br/></td>
</tr>
<tr class="even">
<td><span id="-es"></span><span id="-ES"></span><strong>-ES</strong><br/></td>
<td>Включите открытые символы.<br/></td>
</tr>
<tr class="odd">
<td><span id="-k_Keywords"></span><span id="-k_keywords"></span><span id="-K_KEYWORDS"></span><strong>-k</strong> <strong></strong> <em>Ключевые слова</em><br/></td>
<td>Список ключевых слов с разделителями-запятыми. См. <a href="mftrace-keywords.md">Ключевые слова мфтраце</a>.<br/></td>
</tr>
<tr class="even">
<td><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span><strong>-l</strong> <strong></strong> <em>Уровень</em><br/></td>
<td>Уровень трассировки.<br/>
<ul>
<li>0 — нет.</li>
<li>1: критическая</li>
<li>2: ошибка</li>
<li>3: предупреждение</li>
<li>4: информативные</li>
<li>5: подробный</li>
<li>16: Отладка</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="-o_Output_File"></span><span id="-o_output_file"></span><span id="-O_OUTPUT_FILE"></span><strong>-o</strong> <strong></strong> <em>Выходной файл</em><br/></td>
<td>Запись выходных данных трассировки в указанный файл. По умолчанию вывод переходит в <strong>stdout</strong>.<br/> Если указан выходной файл, то расширение имени файла должно быть одним из следующих:<br/>
<ul>
<li>. ETL: файл журнала трассировки событий (ETL).</li>
<li>. log или .txt: текстовый файл.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="-v"></span><span id="-V"></span><strong>-v</strong><br/></td>
<td>Включить подробный режим.<br/></td>
</tr>
<tr class="odd">
<td><span id="-_"></span><strong>-?</strong><br/></td>
<td>Отобразить сведения об использовании.<br/></td>
</tr>
<tr class="even">
<td><span id="COMMAND"></span><span id="command"></span><em>КНОПКИ</em><br/></td>
<td>Аргументы командной строки для создания нового процесса.<br/></td>
</tr>
<tr class="odd">
<td><span id="ETL_FILE"></span><span id="etl_file"></span><em>ETL_FILE</em><br/></td>
<td>Имя существующего ETL-файла. Если этот аргумент указан, ETL-файл преобразуется в текстовый вывод.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="environment-variables"></a>Переменные среды

<dl> <dt>

<span id="TRACE_FORMAT_SEARCH_PATH"></span><span id="trace_format_search_path"></span>TRACE_FORMAT_SEARCH_PATH
</dt> <dd>

для трассировки компонентов, использующих препроцессорную трассировку Windows программного обеспечения (WPP), задайте для этой переменной среды значение, определяющее путь к файлам трассировки сообщений (тмф) для компонента.

</dd> <dt>

<span id="_NT_SYMBOL_PATH"></span><span id="_nt_symbol_path"></span>_NT_SYMBOL_PATH
</dt> <dd>

Если поиск символов включен (**-ES**), задайте эту переменную среды, чтобы указать путь к символам.

</dd> </dl>

## <a name="examples"></a>Примеры

Создайте новый процесс и выполните трассировку этого процесса:

``` syntax
mftrace.exe wmplayer.exe Wildlife.wmv
```

Присоединить Мфтраце к существующему процессу:

``` syntax
mftrace.exe -a wmplayer.exe
mftrace.exe -a 9132
```

Отправка выходных данных трассировки в текстовый файл:

``` syntax
mftrace.exe -a wmplayer.exe -o trace.txt
```

Трассировка ETW или события КОНВЕЙЕРа событий Windows:

``` syntax
mftrace.exe -c config.xml -o trace.txt
mftrace.exe -c config.xml -o trace.etl
```

> [!Note]  
> В первом примере создается текстовый файл. Во втором примере создается ETL-файл.

 

Преобразование ETL-файла в текстовый файл:

``` syntax
mftrace.exe -o trace.txt trace.etl
```

## <a name="remarks"></a>Remarks

По умолчанию Мфтраце создает только трассировки. Чтобы создать трассировки ETW или WPP, необходимо предоставить файл конфигурации. Файл конфигурации содержит имена поставщиков трассировки. Дополнительные сведения см. в разделе [Мфтраце Configuration File](mftrace-configuration-file.md).

Мфтраце может отправить выходные данные в следующие места назначения:

-   **stdout** (значение по умолчанию).
-   Текстовый файл.
-   Двоичный ETL-файл.

Если вы ведете запись трассировок трассировки событий Windows или КОНВЕЙЕРа, ETL-файл является наиболее эффективным вариантом, поскольку данные трассировки сохраняются в виде двоичных BLOB. После завершения сеанса трассировки можно использовать Мфтраце для преобразования ETL-файла в текстовый файл.

> [!Note]  
> Для трассировки обзора текстовый вывод настолько же эффективен, как и ETL-файл. Поэтому, если вы регистрируете только трассировки (без трассировок ETW и WPP), рекомендуется выводить текстовые выходные данные.

 

Для трассировки обзора необходимо присоединить Мфтраце к выполняющемуся процессу (**-a**) или использовать мфтраце для создания нового процесса. Для трассировок ETW и WPP Мфтраце прослушивает любой поставщик событий, указанный в файле конфигурации.

Результаты трассировки можно отфильтровать, указав ключевые слова трассировки либо с помощью параметра командной строки **-k** , либо в файле конфигурации. Более типичное использование заключается в регистрации всех трассировок и последующем использовании сценария или **grep** для поиска определенных строковых шаблонов.

## <a name="interpreting-the-trace-results"></a>Интерпретация результатов трассировки

Мфтраце можно использовать для получения ответов на вопросы о том, что происходит внутри приложения или компонента Media Foundation. В следующей таблице перечислены некоторые типичные вопросы. Второй столбец содержит строку поиска, которая может помочь ответить на вопрос.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Вопрос</th>
<th>Поиск по строкам</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Произошла ошибка?</td>
<td>&quot;0xc00d&quot;</td>
</tr>
<tr class="even">
<td>Правильно ли разрешается топология?</td>
<td>&quot;Ктопологихелперс:: Trace&quot;</td>
</tr>
<tr class="odd">
<td>Начался ли сеанс мультимедиа?</td>
<td>&quot;месессионстартед&quot;</td>
</tr>
<tr class="even">
<td>Какой файл был воспроизведен?</td>
<td>&quot;кмфсаурцересолвердетаурс&quot;</td>
</tr>
<tr class="odd">
<td>Какие типы носителей используются для исходных потоков?</td>
<td>&quot;Новый поток &quot; , &quot; меневстреам &quot; , &quot; кмфмедиасаурцедетаурс:: трацепд&quot;</td>
</tr>
<tr class="even">
<td>Были ли исходные потоки формировать образцы?</td>
<td>&quot;Кмфмедиастреамдетаурс:: Хандливент &quot; , &quot; мемедиасампле&quot;</td>
</tr>
<tr class="odd">
<td>Было ли воспроизведение достигнуто до конца данных?</td>
<td>&quot;Миндофстреам &quot; , &quot; миндофпресентатион&quot;</td>
</tr>
<tr class="even">
<td>Изменилось ли форматирование?</td>
<td>&quot;Местреамформатчанжед &quot; (источники мультимедиа), &quot; новый формат &quot; , &quot; месессионстреамсинкформатчанжед &quot; (приемники мультимедиа)</td>
</tr>
<tr class="odd">
<td>Какие объекты были созданы?</td>
<td>&quot;COle32ExportDetours:: CoCreateInstance&quot;</td>
</tr>
<tr class="even">
<td>Были ли Media Foundation преобразования (МФТС) в конвейере обработки любых данных?</td>
<td>&quot;Кмфтрансформдетаурс::P Роцессаутпут &quot; , &quot; кмфтрансформдетаурс::P роцессинпут&quot;</td>
</tr>
<tr class="odd">
<td>Какие состояния были заданы для МФТС?</td>
<td>&quot;Кмфтрансформдетаурс::P Роцессмессаже&quot;</td>
</tr>
<tr class="even">
<td>Запрашивал ли запрос MFT входные данные?</td>
<td>&quot;MF_E_TRANSFORM_NEED_MORE_INPUT &quot; (синхронная MFT), &quot; метрансформнидинпут &quot; (асинхронная MFT).</td>
</tr>
<tr class="odd">
<td>Создает ли асинхронный файл MFT выходные данные?</td>
<td>&quot;Процессаутпутс доступно&quot;</td>
</tr>
<tr class="even">
<td>Были ли примеры запросов приемника мультимедиа?</td>
<td>&quot;местреамсинкрекуестсампле&quot;</td>
</tr>
<tr class="odd">
<td>Получил ли приемник мультимедиа примеры?</td>
<td>&quot;Кмфстреамсинкдетаурс::P Роцесссампле&quot;</td>
</tr>
<tr class="even">
<td>DirectShow: какие образцы были обработаны?</td>
<td>&quot;Пример &quot; , &quot; кмеминпутпиндетаурс&quot;</td>
</tr>
<tr class="odd">
<td>DirectShow: какой граф фильтра использовался?</td>
<td>&quot;Кграфхелперс:: Trace&quot;</td>
</tr>
<tr class="even">
<td>Есть ли несколько процессов?</td>
<td>&quot;CreateProcess&quot;
<blockquote>
[!Note]<br />
Также найдите идентификатор процесса, который отображается в начале каждой строки трассировки.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[мфтраце](mftrace.md)
</dt> </dl>

 

 




