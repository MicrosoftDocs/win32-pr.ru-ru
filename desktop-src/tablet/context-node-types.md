---
description: Эти константы определяют значения, указывающие тип объектов Иконтекстноде.
ms.assetid: 333db79e-f503-4545-84fd-7c1a39a96728
title: Типы узлов контекста (Иагуид. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUID_CNT_ANALYSISHINT
- GUID_CNT_CUSTOMRECOGNIZER
- GUID_CNT_IMAGE
- GUID_CNT_INKBULLET
- GUID_CNT_INKDRAWING
- GUID_CNT_INKWORD
- GUID_CNT_LINE
- GUID_CNT_OBJECT
- GUID_CNT_PARAGRAPH
- GUID_CNT_ROOT
- GUID_CNT_TEXTWORD
- GUID_CNT_UNCLASSIFIEDINKNODE
api_type:
- HeaderDef
api_location:
- iaguid.h
ms.openlocfilehash: 918b7cf818ebcedc98f45bff7c41ee66ad4d1592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143000"
---
# <a name="context-node-types"></a>Типы узлов контекста

Эти константы определяют значения, указывающие тип объектов [**иконтекстноде**](icontextnode.md) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Константа/значение</th>
<th style="text-align: left;">Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_ANALYSISHINT"></span><span id="guid_cnt_analysishint"></span><dl> <dt><strong>GUID_CNT_ANALYSISHINT</strong></dt> <dt>(аналисишинт)</dt> </dl></td>
<td style="text-align: left;">Представляет узел, содержащий дополнительные сведения о контексте для региона, который <a href="iinkanalyzer.md"><strong>иинканализер</strong></a> использует для улучшения его анализа.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_CUSTOMRECOGNIZER"></span><span id="guid_cnt_customrecognizer"></span><dl> <dt><strong>GUID_CNT_CUSTOMRECOGNIZER</strong></dt> <dt>(кустомрекогнизер)</dt> </dl></td>
<td style="text-align: left;">Представляет узел, используемый для одной операции распознавания.<br/> Все штрихи и узлы, входящие в пользовательский узел распознавателя, распознаются независимой операцией распознавания и не анализируются <a href="iinkanalyzer.md"><strong>иинканализер</strong></a>.<br/> Пользовательский узел распознавателя должен быть прямым дочерним элементом корневого узла анализатора красок.<br/> Пользовательский узел распознавателя может содержать следующие типы дочерних элементов:<br/>
<ul>
<li>Любое количество узлов Унклассифиединк.</li>
<li>Любое количество узлов объектов.</li>
<li>Любое число узлов линий.</li>
<li>Любое количество узлов Инкворд.</li>
<li>Любое количество узлов с неизвестным значением идентификатора GUID.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_IMAGE"></span><span id="guid_cnt_image"></span><dl> <dt><strong>GUID_CNT_IMAGE</strong></dt> <dt>(изображение)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для двумерного региона, в котором в документе могут существовать любые изображения, отличные от рукописного ввода.<br/> <a href="iinkanalyzer.md"><strong>Иинканализер</strong></a> не создает узлы образа. Используйте <a href="icontextnode-createsubnode.md"><strong>иконтекстноде:: креатесубноде</strong></a> , чтобы добавить узел изображения в дерево узлов контекста. Затем <strong>иинканализер</strong> использует регионы, определенные узлом изображения, чтобы определить, какие заметки рукописного ввода заметок не являются изображениями рукописного ввода.<br/> Узел изображения не может содержать дочерние элементы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKBULLET"></span><span id="guid_cnt_inkbullet"></span><dl> <dt><strong>GUID_CNT_INKBULLET</strong></dt> <dt>(инкбуллет)</dt> </dl></td>
<td style="text-align: left;">Инкбуллет Контекстнодетипе представляет коллекцию штрихов, образующих маркер в маркированном списке.<br/> Контекстноде типа Инкбуллет не может иметь дочерних элементов. Он может быть только дочерним по отношению к Контекстноде абзаца. Только один Инкбуллет может находиться в одном абзаце Контекстноде.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_INKDRAWING"></span><span id="guid_cnt_inkdrawing"></span><dl> <dt><strong>GUID_CNT_INKDRAWING</strong></dt> <dt>(инкдравинг)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для коллекции штрихов, образующих рисование.<br/> Рисунки — это штрихи, которые определяются как фигуры или абстрактные эскизы. Обычно это любые штрихи, не классифицированные как написание штрихов.<br/> Узел рисования рукописного ввода не может содержать дочерние элементы.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_INKWORD"></span><span id="guid_cnt_inkword"></span><dl> <dt><strong>GUID_CNT_INKWORD</strong></dt> <dt>(инкворд)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для коллекции штрихов, образующих логическую группу для формирования распознаваемого слова.<br/> Узел рукописного слова не может содержать дочерние элементы.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_LINE"></span><span id="guid_cnt_line"></span><dl> <dt><strong>GUID_CNT_LINE</strong></dt> <dt>(строка)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для строки слов.<br/> Узел линии может содержать следующие типы дочерних элементов:<br/>
<ul>
<li>Любое количество узлов рукописных слов.</li>
<li>Любое количество узлов текстовых слов.</li>
<li>Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_OBJECT"></span><span id="guid_cnt_object"></span><dl> <dt><strong>GUID_CNT_OBJECT</strong></dt> <dt>(объект)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для объекта, возвращаемого &quot; &quot; пользовательским распознавателем объекта.<br/> Узел объекта не может содержать дочерние элементы.<br/> Узлы объектов могут содержать только пользовательские узлы распознавателя.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_PARAGRAPH"></span><span id="guid_cnt_paragraph"></span><dl> <dt><strong>GUID_CNT_PARAGRAPH</strong></dt> <dt>(абзац)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для коллекции узлов, образующих логическую группу строк.<br/> Точное определение абзаца определяется механизмами анализа. Как правило, абзац содержит группы строк, которые можно переформатировать вместе, если размер поля, содержащего строки, было изменено.<br/> Узел абзаца может содержать следующие типы дочерних элементов:<br/>
<ul>
<li>Любое количество узлов с маркерами ввода.</li>
<li>Любое число узлов линий.</li>
<li>Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_ROOT"></span><span id="guid_cnt_root"></span><dl> <dt><strong>GUID_CNT_ROOT</strong></dt> <dt>(корневой)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для верхнего узла дерева узлов, описывающих результаты анализа рукописного ввода.<br/> Корневые узлы обычно получаются из метода <a href="iinkanalyzer-getrootnode.md"><strong>метода иинканализер:: жетрутноде</strong></a> .<br/> Корневой узел может содержать следующие типы дочерних элементов:<br/>
<ul>
<li>Любое количество узлов подсказок анализа.</li>
<li>Любое число настраиваемых узлов распознавателя.</li>
<li>Любое количество узлов образа.</li>
<li>Любое количество узлов рисования рукописного ввода.</li>
<li>Любое количество узлов области записи.</li>
<li>Любое количество неклассифицированных узлов рукописного ввода.</li>
<li>Любое количество узлов с неизвестным значением <strong>идентификатора GUID</strong> .</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="GUID_CNT_TEXTWORD"></span><span id="guid_cnt_textword"></span><dl> <dt><strong>GUID_CNT_TEXTWORD</strong></dt> <dt>(текстворд)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для двумерного региона, в котором в документе может находиться любой нерукописный текст.<br/> <a href="iinkanalyzer.md"><strong>Иинканализер</strong></a> не создает узлы текстовых слов. Используйте <a href="icontextnode-createsubnode.md"><strong>иконтекстноде:: креатесубноде</strong></a> , чтобы добавить текстовый узел Word в дерево узлов контекста. Затем <strong>иинканализер</strong> использует регионы, определенные узлом текстового слова, чтобы определить, закомментировать ли рукописный ввод нерукописный текст.<br/> Будущие распознаватели могут использовать область, определенную узлом текстового слова, чтобы определить, какие примечания рукописного ввода не являются текстовыми.<br/> Узел текстового слова не может содержать дочерние элементы<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="GUID_CNT_UNCLASSIFIEDINKNODE"></span><span id="guid_cnt_unclassifiedinknode"></span><dl> <dt><strong>GUID_CNT_UNCLASSIFIEDINKNODE</strong></dt> <dt>(унклассифиединк)</dt> </dl></td>
<td style="text-align: left;">Представляет узел для всех штрихов, которые еще не классифицированы или не распознаны.<br/> Неклассифицированный узел рукописного ввода не может иметь дочерних элементов.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Комментарии

Дополнительные сведения о различных типах узлов контекста см. в разделе [Общие сведения об анализе рукописного текста](ink-analysis-overview.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                           |
| Header<br/>                   | <dl> <dt>Иагуид. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Иконтекстноде:: Креатепартиаллипопулатедсубноде**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**Иконтекстноде:: Креатесубноде**](icontextnode-createsubnode.md)
</dt> <dt>

[**Иконтекстноде:: GetType**](icontextnode-gettype.md)
</dt> <dt>

[**Метод Иинканализер:: Креатеаналисишинт**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Метод Иинканализер:: Креатекустомрекогнизер**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипе**](iinkanalyzer-findnodesoftype.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипефорстрокес**](iinkanalyzer-findnodesoftypeforstrokes.md)
</dt> <dt>

[**Метод Иинканализер:: Финднодесофтипеинсубтри**](iinkanalyzer-findnodesoftypeinsubtree.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

 




