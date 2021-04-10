---
description: Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows. Клиенты вызывают эти обработчики фильтров (которые являются реализациями интерфейса IFilter) для извлечения текста и свойств из документа.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Обработчики фильтров, поставляемые с Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144128"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Обработчики фильтров, поставляемые с Windows

Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows. Клиенты вызывают эти обработчики фильтров (которые являются реализациями интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) для извлечения текста и свойств из документа.

Этот раздел организован следующим образом:

- [Примечания по реализации поиска Windows](#windows-search-implementation-notes)
  - [Реализация Windows 7 и 10](#windows-7-and-10-implementation)
  - [Реализация Windows Vista](#windows-vista-implementation)
  - [Устаревшая реализация](#legacy-implementation)
- [Фильтры поиска Windows](#filter-handlers-that-ship-with-windows)
  - [Обработчик фильтра MIME](#mime-filter-handler)
  - [Обработчик фильтра HTML](#html-filter-handler)
  - [Обработчик фильтра документов](#document-filter-handler)
  - [Обработчик обычного текстового фильтра](#plain-text-filter-handler)
  - [Обработчик бинарного или неопределенного фильтра](#binary-or-null-filter-handler)
- [Дополнительные ресурсы](#additional-resources)
- [См. также](#related-topics)

## <a name="windows-search-implementation-notes"></a>Примечания по реализации поиска Windows

В Windows 7 и более поздних версиях фильтры, написанные в управляемом коде, явным образом блокируются. Фильтры должны быть написаны в машинном коде из-за потенциальных проблем с управлением версиями среды CLR в процессе выполнения нескольких надстроек.

### <a name="windows-7-and-10-implementation"></a>Реализация Windows 7 и 10

В Windows 7 и более поздних версиях существует новое поведение, возникающее при регистрации обработчика фильтра, обработчика свойств или нового расширения. При установке нового обработчика свойств и (или) обработчика фильтра файлы с соответствующими расширениями автоматически индексируются повторно.

В Windows 7 и более поздних версиях рекомендуется установить обработчик фильтра в сочетании с соответствующими обработчиками свойств и зарегистрировать обработчик фильтра перед обработчиком свойства. Регистрация обработчика свойств инициирует немедленную повторную индексацию ранее индексированных файлов без необходимости предварительной перезагрузки и использует преимущества всех ранее зарегистрированных обработчиков фильтров для индексирования содержимого.

Если только обработчик фильтра установлен без соответствующего обработчика свойства, то автоматическое повторное индексирование происходит либо после перезапуска службы индексирования, либо после перезапуска системы.

Для флагов описания свойств, характерных для Windows 7, см. следующие справочные разделы: [жетпропертисторефлагс](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [пропдеск \_ COLUMNINDEX \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) и [пропдеск \_ сеарчинфо \_ flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Реализация Windows Vista

В Windows Vista и более ранних версиях установка обработчика [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) или свойства не инициирует повторную индексацию существующих элементов, если только независимый поставщик программного обеспечения явно не вызывает перестроение или повторную индексацию соответствующих URL-адресов.

Существуют два основных различия между устаревшими приложениями, такими как служба индексирования и более новые приложения, такие как поиск Windows, которые следует учитывать при реализации фильтров:

- Использование интерфейса [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) .
- Использование обработчиков свойств.

Прежде всего, для Windows Vista и Windows Search 3,0 и более поздних версий требуется использовать [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) по следующим причинам:

- Для обеспечения производительности и будущей совместимости.
- Для повышения безопасности. Фильтры, реализованные с помощью [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) , более безопасны, поскольку контекст, в котором выполняется фильтр, не требует наличия прав на открытие файлов на диске или по сети.

Хотя в Windows Search используется только [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), в фильтрах можно также включить реализации интерфейса [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) и/или [иперсистстораже](/windows/win32/api/objidl/nn-objidl-ipersiststorage) , чтобы обеспечить обратную совместимость.

Второе основное отличие заключается в том, что Windows Vista и Windows Search 3,0 и более поздних версий имеют новую [систему свойств](../properties/building-property-handlers.md) , использующую обработчики свойств для перечисления свойств элементов.

Однако иногда требуется реализовать фильтр, который обрабатывает как содержимое, так и свойства, чтобы:

- Поддержка устаревших реализаций MSSearch.
- Просмотр ссылок.
- Сохранение сведений о языке.
- Рекурсивно фильтровать внедренные элементы.

В таких ситуациях требуется полная реализация фильтра, включая метод [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) для доступа к значениям свойств.

### <a name="legacy-implementation"></a>Устаревшая реализация

Как отмечалось ранее, Windows Vista и Windows Search включают новую систему свойств, которая инкапсулирует свойства элемента, которые отделены от содержимого элемента. Эта система свойств не существует в более ранних версиях Microsoft Windows Desktop Search (WDS) 2. x. Если фильтр должен поддерживать другие приложения, как описано выше, может потребоваться выполнить обработку как содержимого, так и свойств.

Дополнительные сведения о разработке совместимого фильтра см. в следующих разделах: [IFilter (для устаревших приложений)](/windows/win32/api/filter/nn-filter-ifilter)и [Разработка надстроек фильтров (для устаревших приложений)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Фильтры поиска Windows

Корпорация Майкрософт предоставляет несколько стандартных фильтров для поиска Windows. В следующей таблице приведены сводные данные по содержимому библиотеки [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . Щелкнув имя обработчика фильтра, можно перейти к описанию реализации **IFilter** .

| Обработчик фильтра                                                  | Отфильтрованные файлы                              | Библиотека DLL IFilter  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [Обработчик фильтра MIME](#mime-filter-handler)                     | Многоцелевое расширение электронной почты в Интернете (MIME) | mimefilt.dll |
| [Обработчик фильтра HTML](#html-filter-handler)                     | HTML 3,0 или более ранняя версия                         | nlhtml.dll   |
| [Обработчик фильтра документов](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Обработчик обычного текстового фильтра](#plain-text-filter-handler)         | Обычные текстовые файлы — IFilter по умолчанию          | query.dll    |
| [Обработчик бинарного или неопределенного фильтра](#binary-or-null-filter-handler) | Двоичные файлы-IFilter null                 | query.dll    |

### <a name="mime-filter-handler"></a>Обработчик фильтра MIME

Обработчик фильтра MIME (в mimefilt.dll) извлекает текст и сведения о свойствах из файлов с расширениями. EML,. MHT и. MHTML.

### <a name="html-filter-handler"></a>Обработчик фильтра HTML

Обработчик HTML-фильтра (в nlhtml.dll) извлекает из класса "хтмлфилес" текст и сведения о свойствах, чтобы их можно было индексировать с помощью поиска Windows. Описание связи между [**фильтрами IFilter**](/windows/win32/api/filter/nn-filter-ifilter) и File см. в разделе "поиск DLL-библиотеки IFilter для файла" статьи [Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md).

`META`Для передачи специальных запросов на обработку HTML [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)можно использовать функцию тегов HTML-документов. `META` Теги находятся рядом с началом HTML-файла в `HEAD ... /HEAD` тегах, как показано в следующем примере.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Некоторые HTML- `META` теги автоматически сопоставляются с хорошо известными набором свойств и ЗНАЧЕНИЯМИ идентификатора свойства (PID), поэтому запросы к этим свойствам будут искать сопоставленное содержимое. Некоторые примеры перечислены в следующей таблице. Список системных свойств, которые можно использовать для форматов файлов, см. в разделе [свойства, определяемые системой для пользовательских форматов файлов](-shell-systemdefinedpropertiesforfileformats.md).

| Пример свойства                              | Сопоставлено с                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| Meta Name = "author" Content = "Рут"             | Свойство Author в наборе свойств сводных данных.            |
| Meta Name = "subject" содержимое = "обработка текста" | Свойство Subject в наборе свойств сводных данных.           |
| Meta Name = "Ключевые слова" Content = "шрифты, Serif"   | Свойство keyword в наборе свойств сводных данных.           |
| Meta Name = "MS. Category" содержимое = "вымышление"     | Свойство Category в наборе свойств сведения о сводке документа. |

Некоторые функции [**интерфейса IFILTER**](/windows/win32/api/filter/nn-filter-ifilter) HTML перечислены в следующей таблице.

[comment]: # (Эта таблица должна быть HTML, чтобы правильно форматировать образцы в нем)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Задача</th>
<th>Действие</th>
<th>Пример</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Создание специальных абстракций из файлов</td>
<td>Используйте <code>META NAME=&quot;DESCRIPTION&quot;...</code> тег, чтобы указать <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> использовать строку, следующую за ключевым словом, в <code>CONTENT</code> качестве абстрактного документа.
<blockquote>
[!Note]<br />
Процесс фильтрации может формировать абстракции для каждого отфильтрованного файла, который по умолчанию является набором символов в начале файла.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Предотвращение фильтрации отдельных файлов</td>
<td>Добавьте <code>meta name</code> тег в файл.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Задание кода языка для файла (чтобы убедиться, что система выбирает правильные языковые разделители слов и файлы неучитываемых слов)</td>
<td>Добавьте следующий <code>meta name</code> тег в файл, где поле Content указывает соответствующий код языка (в символах или с использованием значения языкового стандарта).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Обработчик фильтра документов

Обработчик фильтра документов (в offilt.dll) Фильтрует файлы для некоторых расширений документов в Microsoft Office. К ним относятся файлы с расширениями DOC, MDB, PPT и xlt, например.

### <a name="plain-text-filter-handler"></a>Обработчик обычного текстового фильтра

Для обычных текстовых файлов в Windows Search используется обработчик текстовых фильтров, который фильтрует как системные свойства (например, имена файлов), так и содержимое файла. Если у типа файлов нет связи [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) в реестре, Windows Search индексирует только свойства оболочки для этого файла. Однако пользователь может использовать **Дополнительные параметры** на панели управления " **Параметры индексирования** " для **индексирования свойств** или **свойств индекса и содержимого файлов**.

![снимок экрана, отображающий диалоговое окно "Дополнительные параметры"](images/ifilteradvancedoptions.png)

Если пользователь выбирает этот параметр для типа файла без связанного с ним [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), для извлечения содержимого файла используется обработчик текстового фильтра. Обработчик текстового фильтра не «понимает» формат документа; при фильтрации содержимого файла файл обрабатывается как последовательность символов. Он проверяет метку порядка следования байтов Юникода в начале файла.

### <a name="binary-or-null-filter-handler"></a>Обработчик бинарного или неопределенного фильтра

При обнаружении зарегистрированного двоичного файла используется обработчик фильтра null. Обработчик фильтра null извлекает только системные свойства. Содержимое двоичного файла не фильтруется. Примерами системных свойств являются **filename**, **LastWriteTime**, **Размер файла** и **Attributes**.

## <a name="additional-resources"></a>Дополнительные ресурсы

- Пример кода [ифилтерсампле](-search-sample-ifiltersample.md) , доступный на [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), демонстрирует создание базового класса IFilter для реализации интерфейса [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Общие сведения о процессе индексирования см. [в разделе процесс индексирования](-search-indexing-process-overview.md).
- Общие сведения о типах файлов см. в разделе [типы файлов](../shell/fa-file-types.md).
- Сведения о запросе атрибутов сопоставления файлов для типа файлов см. в разделе [перцеиведтипес, системфилеассоЦиатионс и регистрация приложения](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>См. также

[Разработка обработчиков фильтров](-search-ifilter-conceptual.md)

[О обработчиках фильтров в поиске Windows](-search-ifilter-about.md)

[Рекомендации по созданию обработчиков фильтров в поиске Windows](-search-3x-wds-extidx-filters.md)

[Возвращение свойств из обработчика фильтра](-search-ifilter-property-filtering.md)

[Реализация обработчиков фильтров в поиске Windows](-search-ifilter-constructing-filters.md)

[Регистрация обработчиков фильтров](-search-ifilter-registering-filters.md)

[Тестирование обработчиков фильтров](-search-ifilter-testing-filters.md)
