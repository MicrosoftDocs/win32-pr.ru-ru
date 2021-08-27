---
description: Набор тестов IFilter проверяет обработчики фильтров.
ms.assetid: 5ee02af1-1dc9-4d21-868f-4c439970b1ba
title: Тестирование обработчиков фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf58f14f0f8de4458dd887bf52b32fb68f869d64
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122621950"
---
# <a name="testing-filter-handlers"></a>Тестирование обработчиков фильтров

Набор тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) проверяет обработчики фильтров. Этот набор тестов выполняет следующие действия: вызов методов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и проверка возвращаемых значений на соответствие спецификации интерфейса **IFilter** ; и проверка того, что идентификаторы блоков уникальны и увеличиваются, что интерфейс **IFilter** ведет себя согласованно после повторной инициализации, и все вызовы методов **IFilter** с недопустимыми параметрами возвращают ожидаемые коды ошибок. Программы набора тестов также выводят дампы файлов, отфильтрованных обработчиком фильтров, и проверяют сведения о регистрации **IFilter** в реестре.

Этот раздел организован следующим образом:

- [Вызов из командной строки](#command-line-invocation)
  - [ifilttst.exe](#ifilttstexe)
  - [filtdump.exe](#filtdumpexe)
  - [filtreg.exe](#filtregexe)
  - [ifilttst.ini](#ifilttstini)
- [Тестовая процедура IFilter](#ifilter-test-procedure)
  - [Проверочный тест](#validation-test)
  - [Проверка согласованности](#consistency-test)
  - [Недопустимый входной тест](#invalid-input-test)
  - [Тестирование различных конфигураций IFilter](#testing-different-ifilter-configurations)
- [Проверка индексации зарегистрированных элементов](#ensuring-registered-items-get-indexed)
  - [Пример файла журнала](#sample-log-file)
  - [Пример файла дампа](#sample-dump-file)
- [Дополнительные ресурсы](#additional-resources)
- [Связанные темы](#related-topics)

> [!NOTE]  
> Если новый обработчик фильтра для типа файла устанавливается в качестве замены для существующей регистрации фильтра, установщик должен сохранить текущую регистрацию и восстановить ее при удалении нового обработчика фильтра. Механизм фильтрации цепочек отсутствует. Таким образом, новый обработчик фильтра отвечает за репликацию всех необходимых функций старого фильтра.

## <a name="command-line-invocation"></a>Вызов Command-Line

Набор тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) состоит из трех приложений командной строки: [ifilttst.exe](#ifilttstexe), [filtdump.exe](#filtdumpexe)и [filtreg.exe](#filtregexe) и файла инициализации [ifilttst.ini](#ifilttstini).

> [!IMPORTANT]
> в Windows 7 и более поздних версиях фильтры, написанные в управляемом коде, явным образом блокируются. Фильтры должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR при работе нескольких надстроек.

### <a name="ifilttstexe"></a>ifilttst.exe

Программа ifilttst.exe выполняет несколько тестов для проверки обработчика фильтра. В следующем примере показано, как вызвать программу ifilttst.exe из командной строки:


```
ifilttst /i test.htm /l /d /v 1
```

В этом примере выполняются следующие задачи.

- Направляет программу для фильтрации файла test.htm
- Перенаправляет сообщения журнала в test.htm. log
- Перенаправляет сообщения дампа в test.htm. dmp
- Задает уровень детализации 1

Чтобы Предыдущая команда работала, три файла должны находиться в текущем рабочем каталоге: `test.htm` , [ifilttst.exe](#ifilttstexe)и [ifilttst.ini](#ifilttstini). Параметры командной строки перечислены в следующей таблице.

<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Переключение и возможные переменные</th>
<th>Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>/i имя файла</strong></td>
<td>Входной файл или каталог для фильтрации. Имя файла может содержать подстановочные знаки <code>*</code> и <code>?</code> .</td>
</tr>
<tr class="even">
<td><strong>/l</strong></td>
<td>Сообщения журнала направляются в файл, а не на экран. Сообщения журнала описывают отдельные выполняемые тесты и результаты тестов с успехом или неудачей. Имя файла журнала совпадает с именем входного файла, но с расширением log.</td>
</tr>
<tr class="odd">
<td><strong>/d</strong></td>
<td>Сообщения дампа направляются в файл, а не на экран. Сообщения дампа описывают содержимое фрагментов. Структура блока создается дампом, если уровень детализации равен 3. Имя файла дампа совпадает с именем входного файла, но с расширением DMP.</td>
</tr>
<tr class="even">
<td><strong>/-л</strong></td>
<td>Отключить ведение журнала. Этот флаг переопределяет <code>/l</code> параметр.</td>
</tr>
<tr class="odd">
<td><strong>/-д</strong></td>
<td>Отключение дампа. Этот флаг переопределяет <code>/d</code> параметр.</td>
</tr>
<tr class="even">
<td><strong>/v целое число</strong></td>
<td>Уровень детализации. По умолчанию используется значение 3.
<ul>
<li>0 — тест записывает в журнал только сообщения об ошибках в интерфейсе <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> . Тест создает дамп содержимого фрагмента.</li>
<li>1 — тест заносит в журнал предупреждающие сообщения, а также для уровня 0.</li>
<li>2. тест записывает в журнал сообщения о тестах, пройденных, а также на уровне 1.</li>
<li>3. тест записывает информационные сообщения, а также для уровня 2. Кроме того, тест создает дамп структуры фрагмента.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>/t целое</strong></td>
<td>Число запускаемых потоков. Значение по умолчанию — 1.</td>
</tr>
<tr class="even">
<td><strong>/r целое число</strong>]</td>
<td>Рекурсивно фильтрует подкаталоги. Необязательный параметр целого числа задает глубину, до которой будет выполняться рекурсия. Если целое число не указано или целое число равно 0, предполагается полная рекурсия. По умолчанию глубина рекурсии равна 1.</td>
</tr>
<tr class="odd">
<td><strong>/c целое</strong></td>
<td>Число циклов. Если целое число равно 0, то тест циклически подбирается бесконечно. По умолчанию тест циклически обрабатывается только один раз.</td>
</tr>
</tbody>
</table>

> [!NOTE]  
> Необходимо включить пробел между параметром командной строки и значением.

### <a name="filtdumpexe"></a>filtdump.exe

Программа filtdump.exe загружает обработчик фильтра для указанного документа и выводит результат, созданный DLL-библиотекой [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . В следующем примере показано, как вызвать программу filtdump.exe.

```
filtdump filename.ext
```
Filtdump.exe использует метод [илоадфилтер:: лоадифилтер](/windows/desktop/api/filtereg/nf-filtereg-iloadfilter-loadifilter) для загрузки библиотеки DLL [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , подходящей для указанного расширения имени файла, и выводит результаты. Например, следующая команда указывает filtdump.exe загрузить обработчик фильтра smpfilt.dll для расширения SMP, извлечь весь текст и свойства из файла MyFile. SMP и распечатать результаты.

```
filtdump myfile.smp
```

### <a name="filtregexe"></a>filtreg.exe

Программа filtreg.exe проверяет сведения об установке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) в реестре. Чтобы вызвать программу filtreg.exe из командной строки, введите ее имя, как показано в следующем примере.

```
filtreg
```

Filtreg.exe перечисляет все расширения имен файлов, имеющие связанные с ними обработчики фильтров, путем печати расширения имени файла и имени DLL-библиотеки [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) для расширения. Это простой способ проверки правильности установки **IFilter**.

### <a name="ifilttstini"></a>ifilttst.ini

Интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) инициализируется путем вызова метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Метод **IFilter:: init** принимает следующие четыре параметра:

1. *грффлагс*
2. *cAttributes*
3. *ааттрибутес*
4. *пдвфлагс*

Пользователь ifilttst.exe программы в наборе тестов [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) может указать значения этих параметров в файле с именем ifilttst.ini. В следующей таблице описаны записи в файле ifilttst.ini, в которых указываются первые три параметра (входные параметры). Пример файла см. в разделе [sample ifilttst.ini File](#sample-ifilttstini-file).

> [!NOTE]  
> Отсутствует запись в таблице для параметра *пдвфлагс* , так как это выходной параметр. перед вызовом метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) не обязательно иметь никаких специальных значений.

 | Ввод         | Описание                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Флаги         | Имена флагов [**\_ инициализации IFilter**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) , которые должны быть соединены оператором или для формирования параметра *грффлагс* метода [**IFILTER:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) . Имена флагов должны быть в верхнем регистре и в той же строке.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| *cAttributes* | Десятичное целое число, представляющее значение параметра *cAttributes* .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| *ааттрибутес* | Эта запись должна начинаться с *ааттрибутес* и должна отличаться от других записей *ааттрибутес* в разделе. Допустимые имена для записи *ааттрибутес* : *ааттрибутес*, *aAttributes1*, *aAttributes2* и т. д. Первый токен должен быть идентификатором GUID. GUID должен быть отформатирован точно так же, как показано в `[Test3]` разделе [примера файла ifilttst.ini](#sample-ifilttstini-file). Второй токен может быть идентификатором свойства (PID), состоящим из числа в шестнадцатеричном формате, или указателя на строку расширенных символов (LPWSTR). LPWSTR можно указать, заключив строку в двойные кавычки, как показано в `[Test6]` разделе примера файла ifilttst.ini. |

Если флаги и записи *cAttributes* не указаны, они по умолчанию имеют значение 0. Если задать *cAttributes* равным 2, следует указать два имени *ааттрибутес* . В `[Test5]` разделе примера *cAttributes* имеет значение 1, но *ааттрибутес* не указаны. Затем тест вызывает метод [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) с *cAttributes* , равным 1, и *ааттрибутес* , равным **null**. Это полезный тестовый случай, так как, скорее всего, вызовет нарушение прав доступа в методе **IFilter:: init** .

Если ifilttst.exe не удается найти файл с именем ifilttst.ini в рабочем каталоге, для инициализации объекта [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) используется конфигурация по умолчанию. В следующем примере показана конфигурация по умолчанию.

```
[default]
            grfFlags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

```

### <a name="sample-ifilttstini-file"></a>Пример файла ifilttst.ini

Файл ifilttst.ini организован в разделы, имя раздела которых заключено в квадратные скобки. В этом примере разделам присваиваются имена `[Test1]` , `[Test2]` и т. д. Все имена разделов должны быть уникальными. Тест считывает значения из первого раздела и инициализирует [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с этими значениями. Затем выполняются все тесты с использованием этой конфигурации **IFilter** . Затем **IFilter** освобождается и повторно инициализируется с использованием параметров, перечисленных выше. Процесс повторяется до тех пор, пока все конфигурации не будут проверены.

```
; Only extract text from the object
            [Test1]
            Flags =
            cAttributes = 0

            // Get all attributes (text-type and internal value-type properties.
            [Test2]
            Flags = IFILTER_INIT_APPLY_INDEX_ATTRIBUTES
            cAttributes = 0

            // This also extracts just text from the object (the GUID is PSGUID_STORAGE, and the propid is
            // PID_STG_CONTENTS).
            [Test3]
            Flags = IFILTER_INIT_CANON_PARAGRAPHS IFILTER_INIT_HARD_LINE_BREAKS
            cAttributes = 1
            aAttributes1 = b725f130-47ef-101a-a5f1-02608c9eebac 13

            // Only extract requested attribute from the html object (the GUID corresponds to the HTML IFilter.
            [Test4]
            Flags = IFILTER_INIT_CANON_HYPHENS IFILTER_INIT_CANON_SPACES
            cAttributes = 1
            aAttributes1 = 70eb7a10-55d9-11cf-b75b-00aa0051fe20 2

            // Question: what happens if cAttributes is nonzero, but aAttributes is empty?
            [Test5]
            Flags = IFILTER_INIT_CANON_SPACES IFILTER_INIT_APPLY_INDEX_ATTRIBUTES IFILTER_INIT_APPLY_OTHER_ATTRIBUTES
            cAttributes = 1

            // Here is an attribute with a lpwstr instead of a propid (the lpwstr is enclosed in quotes).
            // The GUID corresponds to the meta tag clsid for the HTML IFilter.
            [Test6]
            Flags =
            cAttributes = 1
            aAttributes1 = D1B5D3F0-C0B3-11CF-9A92-00A0C908DBF1 "GENERATOR"
```

## <a name="ifilter-test-procedure"></a>Тестовая процедура IFilter

После инициализации [**фильтра IFilter**](/windows/win32/api/filter/nn-filter-ifilter) программа ifilttst.exe выполняет ряд тестов на **IFilter**. Помимо реализации процедур тестирования **IFilter** убедитесь, что реализация **IFilter** использует методы безопасного кода. см. раздел "рекомендации по обеспечению безопасного кода для Windowsного поиска" раздела [реализация обработчиков фильтров в Windowsном поиске](-search-ifilter-constructing-filters.md).

### <a name="validation-test"></a>Проверочный тест

Проверочный тест проходит через объект по одному блоку за раз, проверяя каждый отдельный фрагмент и все коды возврата. Проверочный тест сохраняет все возвращенные структуры [**\_ блока статистики**](/windows/win32/api/filter/ns-filter-stat_chunk) в списке.

Проверочный тест проверяет следующие условия.

- [**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).** идентификаторы фрагментов идчунк должны быть уникальными и увеличиваться.
- [**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*параметр flags* является распознаваемым состоянием блока, таким как [**чункстате**](/windows/win32/api/filter/ne-filter-chunkstate), текст фрагмента \_ или \_ константы ценабледхунк значений.
- [**\_ Блок stat**](/windows/win32/api/filter/ns-filter-stat_chunk).*параметр Бреактипе* является распознаваемым типом разрыва (0, 1, 2, 3, 4).
- Если атрибуты инициализации [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) указывают, что **IFilter** должен возвращать только фрагменты, содержащие внутренние свойства типа значения, то *идчунксаурце* должен равняться 0.
- Если фрагмент не является производным, то есть, если он не является внутренним свойством типа значения, то параметр [**stat- \_ блока**](/windows/win32/api/filter/ns-filter-stat_chunk).*Идчунксаурце* должен равняться **\_ блоку stat**.*Идчунк*.
- [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) noreturn возвращает S \_ ОК или другое допустимое возвращаемое значение, например фильтр \_ по \_ концу \_ \_ фрагментов, фильтр \_ e \_ \_ недоступен и т. д.
- Если фрагмент текста содержит текст, то функция [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) возвращает значение S \_ OK, фильтр \_ S \_ Last \_ Text или \_ фильтр \_ е \_ без \_ текста.
- Если [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) возвращает \_ \_ последний текст Filter S \_ , следующий вызов функции **IFilter:: GetText** вернет фильтр \_ E \_ без \_ \_ текста.
- Если блок содержит значение, то функция [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) возвращает \_ ОК или фильтр \_ E \_ больше не \_ содержит \_ значений.

### <a name="consistency-test"></a>Проверка согласованности

Программа ifilttxt.exe повторно инициализирует интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с теми же параметрами, что и в проверочном тесте, и выполняет проверку согласованности. Если реализация **IFilter** была инициализирована с флагом "только индексирование [**IFilter \_ init**](/previous-versions/windows/desktop/legacy/bb266511(v=vs.85)) \_ init" \_ \_ , тест освобождает интерфейс **IFilter** и повторно привязывает его перед другим вызовом метода [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init) .

Проверка согласованности проверяет следующие условия.

- Каждая [**Структура \_ блока stat**](/windows/win32/api/filter/ns-filter-stat_chunk) , возвращаемая методом [**IFilter::-блока**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) , идентична соответствующему **\_ блоку stat** , возвращенному в проверочном тесте.
- [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) noreturn возвращает S \_ ОК или другое допустимое возвращаемое значение, например фильтр \_ по \_ концу \_ \_ фрагментов, фильтр \_ e \_ \_ недоступен и т. д.

### <a name="invalid-input-test"></a>Недопустимый входной тест

Программа ifilttst.exe повторно инициализирует интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) с теми же параметрами и выполняет Недопустимый входной тест. Этот тест проходит по одному фрагменту документа за раз при неправильном вызове функции, например при вызове метода [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) , если текущий Чак содержит текст. Тест проверяет все коды возврата на соответствие спецификации **IFilter** .

Недопустимый входной тест проверяет следующие условия.

- Если текущий фрагмент содержит текст, функция [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) Возвращает фильтр \_ E \_ без \_ значений и вызов [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) завершается.
- Если текущий блок содержит значение, [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) Возвращает фильтр \_ E \_ без \_ текста, а вызов [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) завершается с ошибкой.
- Если предыдущий вызов функции [**IFilter:: GetText**](/windows/win32/api/filter/nf-filter-ifilter-gettext) вернул фильтр \_ e \_ без \_ \_ текста, последовательные вызовы **IFilter:: GetText** возвращают фильтр \_ e \_ без \_ \_ текста.
- Если предыдущий вызов функции [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) вернул фильтр \_ e \_ больше \_ \_ значений, последовательные вызовы функции **IFilter:: GetValue** возвращают фильтр \_ e \_ больше не имеют \_ \_ значений.
- Если предыдущий вызов функции [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) NORETURN вернул фильтр по \_ \_ концу \_ \_ фрагментов, последовательные вызовы **IFilter::** noreturn возвращают фильтр по \_ \_ концу \_ \_ фрагментов.

> [!NOTE]  
> Недопустимый входной тест сравнивает текущие структуры фрагментов с теми, которые возвращены в проверочном тесте, чтобы убедиться, что они идентичны.

### <a name="testing-different-ifilter-configurations"></a>Тестирование различных конфигураций IFilter

Программа ifilttst.exe освобождает интерфейс [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и выполняет повторную привязку, при этом инициализирует его со следующим набором параметров. Тест повторяет цикл: проверочный тест, тест согласованности и недопустимый входной тест, пока не будут протестированы все требуемые конфигурации **IFilter** , указанные в файле [ifilttst.ini](#ifilttstini) .

## <a name="ensuring-registered-items-get-indexed"></a>Проверка индексации зарегистрированных элементов

Окончательная проверка [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) гарантирует, что **IFilter** будет правильно зарегистрирована и вызвана для индексации элементов, которые вы зарегистрировали для использования. Можно использовать диспетчер каталогов для инициации повторного индексирования или использования диспетчера области сканирования (CSM) для настройки правил по умолчанию, указывающих URL-адреса, которые должен обходить индексатор. после завершения индексирования используйте пользовательский интерфейс поиска Windows, чтобы найти строку в содержимом или свойствах элементов. Если элементы были проиндексированы, они будут отображаться в результатах поиска.

Дополнительные сведения о повторной индексации см. в разделе [Использование диспетчера каталогов](-search-3x-wds-mngidx-catalog-manager.md) и [диспетчера области сканирования](-search-3x-wds-extidx-csm.md). В образце кода Реиндексматчингурлс показаны способы указания файлов для повторного индексирования и способа. В образце кода Кравлскопекоммандлине показано, как определить параметры командной строки для операций индексирования диспетчера области сканирования (CSM). Оба примера кода доступны на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).

### <a name="sample-log-file"></a>Пример файла журнала

По запросу программа Ifilttst.exe может создать журнал, содержащий описание действий, выполняемых во время выполнения. Следующие примеры являются выдержками из файла журнала с уровнем детализации, равным максимально возможное значение 3.

```
            1. INFO----**** New configuration ****
            2.
            3. Section name : Test2
            4. grfFlags     : 63
            5. cAttributes  : 0
            6. aAttributes  : NONE
            7. pdwFlags     : 0
            8.
            9. INFO----Successfully bound filter.
            10.
            11. PASS----Init() returned a valid value for pdwFlags.
            12.
            13. INFO----Successfully initialized filter.
            14.
            15. INFO----Performing validation test. In this part of the test, the chunks structures
            16.         returned by the IFilter are checked for correctness, and the return values
            17.         of the IFilter calls are checked.
            18.
            19. PASS----GetChunk() succeeded.
            20.
            21. PASS----The current chunk has a legal value for the flags field.

```

Первая строка представляет собой информационное сообщение, указывающее, что новая конфигурация загружена из файла ifilttst.ini. Line (3) указывает имя раздела в файле ifilttst.ini, из которого считывается текущая конфигурация. Строки (с 4) по (7). перечисление параметров в [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init). Строки, начинающиеся с `INFO` , являются информационными сообщениями о привязке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и запуске проверки. Строки, начинающиеся с `PASS` , — это сообщения о конкретных тестах, которые прошли.

Строка в следующем примере журнала является предупреждением. Предупреждения вызывают проблемы с поведением [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) , которое является проблематичным, хотя и юридическим. Это предупреждение означает, что метод [**IFilter::**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gettext вернул текстовый фрагмент, который не содержит текста.

```
WARNING-First call to GetText() returned FILTER_E_NO_MORE_TEXT.
```

В следующем примере появляется сообщение об ошибке, указывающее, что [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) выдал незапрошенный фрагмент.

```
            ERROR---The IFilter has emitted a chunk which it was not requested to emit.
            Check the initialization parameters in section Test1 of the initialization file.
            INFO----Current chunk propid : 0x5
```

В случае этого примера сообщения об ошибке [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) выдал фрагмент с идентификатором PID `0x5` . Проверка раздела `[Test1]` в ifilttst.ini покажет, что **Фильтр IFilter** был настроен так, чтобы не выдавал блоки с этим PID. Например, если ни один из методов инициализации IFILTER не применяет \_ \_ \_ \_ атрибуты индекса \_ и инициализация IFilter не \_ применяют \_ другие \_ атрибуты, указанные в записи flags, а если *cAttributes* — 0, то **IFILTER** выдаст только фрагменты с идентификатором PID `0x13` и соответствующим \_ \_ содержимому PID STG.

### <a name="sample-dump-file"></a>Пример файла дампа

По запросу программа Ifilttst.exe может создать дамп, содержащий фрагменты, которые он находит, и их содержимое. Следующий пример является выдержкой из такого файла дампа.

```
                1. Chunk ID: ........... 2
                2. Chunk Break Type: ... END OF SENTENCE
                3. Chunk State: ........ TEXT
                4. Chunk Locale: ....... 0x411
                5. Chunk Source ID: .... 2
                6. Chunk Start Source .. 0x0
                7. Chunk Length Source . 0x0
                8. GUID ................ b725f130-47ef-101a-a5f1-02608c9eebac
                9. Property ID ......... 0x13

                10. This is a HTML IFilter test page

                11. Chunk ID: ........... 3
                12. Chunk Break Type: ... END OF SENTENCE
                13. Chunk State: ........ TEXT
                14. Chunk Locale: ....... 0x411
                15. Chunk Source ID: .... 2
                16. Chunk Start Source .. 0x0
                17. Chunk Length Source . 0x0
                18. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                19. Property ID ......... 0x2

                20. This is a HTML IFilter test page

                21. Chunk ID: ........... 4
                22. Chunk Break Type: ... END OF SENTENCE
                23. Chunk State: ........ VALUE
                24. Chunk Locale: ....... 0x411
                25. Chunk Source ID: .... 2
                26. Chunk Start Source .. 0x0
                27. Chunk Length Source . 0x0
                28. GUID ................ f29f85e0-4ff9-1068-ab91-08002b27b3d9
                29. Property ID ......... 0x2

                30. This is an HTML IFilter test page
```

Первые девять строк описывают текущую структуру фрагмента. Идентификатор GUID и идентификатор процесса соответствуют \_ содержимому псгуид Storage/PID \_ STG \_ . Это блок, содержащий обычный текст. Текст находится в следующей структуре блоков:

```
10. This is an HTML IFilter test page
```

Следующий фрагмент кода, начиная с строки 11, имеет другой GUID, соответствующий `HTML IFilter` , и другой идентификатор процесса, соответствующий HTML href. Это внутреннее свойство типа значения, экспортируемое `HTML IFilter` .

Следующий фрагмент кода, начинающийся в строке 21, имеет тот же идентификатор GUID и идентификатор процесса, но его состояние блока — `VALUE` вместо `TEXT` . Обратите внимание, что текст в этих двух последних фрагментах такой же, как и для первого фрагмента. Но поскольку [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) предназначен для трех атрибутов (обычный текст, HTML href в качестве текста и HTML href как значение) для применения к этой фразе, результаты выдаются в трех отдельных блоках.

## <a name="additional-resources"></a>Дополнительные ресурсы

- пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**ifilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
- Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).
- Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Связанные темы

[Разработка обработчиков фильтров](-search-ifilter-conceptual.md)

[сведения о обработчиках фильтров в Windowsном поиске](-search-ifilter-about.md)

[рекомендации по созданию обработчиков фильтров в Windowsном поиске](-search-3x-wds-extidx-filters.md)

[Возвращение свойств из обработчика фильтра](-search-ifilter-property-filtering.md)

[Обработчики фильтров, поставляемые с Windows](-search-ifilter-implementations.md)

[реализация обработчиков фильтров в Windowsном поиске](-search-ifilter-constructing-filters.md)

[Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md)
