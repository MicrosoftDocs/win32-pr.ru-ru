---
description: 'Дополнительные сведения: структура JET_INDEXCREATE2'
title: Структура JET_INDEXCREATE2
TOCTitle: JET_INDEXCREATE2 Structure
ms:assetid: c574500e-8695-4f29-8e9d-6dff987af2a2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294082(v=EXCHG.10)
ms:contentKeyID: 32765697
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ac0d9a40e159a8aa5054228d18e431cee8d0319f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999727"
---
# <a name="jet_indexcreate2-structure"></a>Структура JET_INDEXCREATE2


_**Применимо к:** Windows | Windows Server_

Структура **JET_INDEXCREATE2** содержит сведения, необходимые для создания индекса данных в базе данных подсистемы расширенного хранилища (ESE). Структура используется такими функциями, как [JetCreateIndex2](./jetcreateindex2-function.md), и в таких структурах, как [JET_TABLECREATE](./jet-tablecreate-structure.md) и [JET_TABLECREATE2](./jet-tablecreate2-structure.md).

Структура **JET_INDEXCREATE2** была введена в операционной системе Windows 7.

```cpp
typedef struct tagJET_INDEXCREATE2 {
  unsigned long cbStruct;
  tchar* szIndexName;
  tchar* szKey;
  unsigned long cbKey;
  JET_GRBIT grbit;
  unsigned long ulDensity;
  union {
    unsigned long lcid;
    JET_UNICODEINDEX* pidxunicode;
  };
  union {
    unsigned long cbVarSegMac;
    JET_TUPLELIMITS* ptuplelimits;
  };
  JET_CONDITIONALCOLUMN* rgconditionalcolumn;
  unsigned long cConditionalColumn;
  JET_ERR err;
    unsigned long cbKeyMost;
  JET_SPACEHINTS* pSpacehints;
} JET_INDEXCREATE;
```

### <a name="members"></a>Элементы

**кбструкт**

Размер данной структуры (в байтах). Присвойте этому элементу значение sizeof (JET_INDEXCREATE2).

**сзиндекснаме**

Имя создаваемого индекса.

Имя должно соответствовать следующим условиям.

  - Оно должно быть меньше JET_cbNameMost, не включая завершающее значение null.

  - Он должен состоять из следующего набора символов: от 0 (нуля) до 9, от A до Z, от a до z и всех остальных знаков препинания, за исключением " \! " (восклицательный знак), "," (запятая), " \[ " (открывающая скобка) и " \] " (закрывающая скобка), т. е. символы ASCII 0x20, 0x22 до 0x2D, 0x2F через 0x5A, 0x5c и 0x5d до 0x7F.

  - Оно не должно начинаться с пробела.

  - Он должен содержать по крайней мере один символ, не являющийся пробелом.

**сзкэй**

Указатель на строку токена с разделителями null, завершающуюся символом двойного значения NULL.

Каждый токен имеет форму " \<direction-specifier\> \<column-name\> ", где Direction-спецификация имеет значение "+" или "-". Например, **сзкэй** "+ ABC \\ 0-DEF \\ 0 + GHI \\ 0" будет индексировать три столбца "ABC" (в порядке возрастания), "def" (в убывающем порядке) и "GHI" (в возрастающем порядке). В языке C строковые литералы имеют подразумеваемый знак завершения **null** , поэтому приведенная выше строка будет завершаться двойным значением NULL.

Число столбцов, указанное в **сзкэй** , не должно превышать JET_ccolKeyMost (константа, зависящая от версии).

По крайней мере один столбец должен иметь имя в **сзкэй**.

Устаревшее поведение. после символа-конца с двойным НУЛЕМ можно указать идентификатор языка (слово, которое передается в МАКЕЛЦИД (LangID, SORT_DEFAULT)) в качестве способа указания кода языка для индекса. Недопустимо указывать идентификатор языка в **сзкэй** и LCID в [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) (путем установки JET_bitIndexUnicode в *грбит*).

Устарело: после идентификатора языка можно передать **кбварсегмак** как тип данных **UShort** . Поведение не определено, если USHORT задан как в **сзкэй** , так и при задании **кбварсегмак** в структуре.

**cbKey**

Длина **сзкэй** в байтах, включая два завершающих значения NULL.

**грбит**

Группа битов, которая содержит ноль или более параметров значения, перечисленных в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitIndexUnique</p></td>
<td><p>Дублирующиеся записи индекса (ключи) запрещены. Это применяется при вызове <a href="gg269288(v=exchg.10).md">жетупдате</a> , а не при вызове <a href="gg294137(v=exchg.10).md">жетсетколумн</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexPrimary</p></td>
<td><p>Индекс является первичным (кластеризованным) индексом. Каждая таблица должна иметь ровно один первичный индекс. Если первичный индекс явно не определен в таблице, ядро СУБД создаст собственный первичный индекс.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexDisallowNull</p></td>
<td><p>Ни один из столбцов, по которым создается индекс, может содержать значение <strong>null</strong> .</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreNull</p></td>
<td><p>Не добавляйте элемент индекса для строки, если все индексируемые столбцы имеют <strong>значение NULL</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexIgnoreAnyNull</p></td>
<td><p>Не добавляйте элемент индекса для строки, если какие-либо индексируемые столбцы имеют <strong>значение NULL</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexIgnoreFirstNull</p></td>
<td><p>Не добавляйте элемент индекса для строки, если первый индексируемый столбец имеет <strong>значение NULL</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexLazyFlush</p></td>
<td><p>Указывает, что операции с индексами будут регистрироваться неактивно.</p>
<p>JET_bitIndexLazyFlush не влияет на отложенность обновлений данных. Если операция индексирования прервана завершением процесса, то при мягком восстановлении все равно удастся получить целостное состояние базы данных, но индекс может отсутствовать.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexEmpty</p></td>
<td><p>Не пытайтесь построить индекс, так как все записи будут иметь <strong>значение NULL</strong>. <strong>грбит</strong> НЕОБХОДИМО также указать JET_bitIgnoreAnyNull при передаче JET_bitIndexEmpty. Это улучшение производительности. Например, если новый столбец добавляется в таблицу, а затем создается индекс поверх этого вновь добавленного столбца, то все записи в таблице просматриваются, даже если они не добавляются в индекс. При указании JET_bitIndexEmpty пропускается сканирование таблицы, что может занять длительное время.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnversioned</p></td>
<td><p>JET_bitIndexUnversioned приводит к тому, что создание индекса станет видимым для других транзакций. Как правило, сеанс в транзакции не сможет увидеть операцию создания индекса в другом сеансе. Этот флаг может быть полезен, если другая транзакция, скорее всего, создаст тот же индекс. Второй индекс-Create просто завершится сбоем, а не может вызвать множество ненужных операций с базой данных. Вторая транзакция может не иметь возможности немедленно использовать индекс. Операция создания индекса должна быть завершена, прежде чем ее можно будет использовать. В настоящее время сеанс не должен находиться в транзакции, чтобы создать индекс без сведений о версии.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexSortNullsHigh</p></td>
<td><p>Задание этого флага приводит к сортировке значений <strong>null</strong> после данных для всех столбцов в индексе.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexUnicode</p></td>
<td><p>Указание этого флага влияет на интерпретацию поля объединения LCID/пидксуникде в структуре. Установка бита означает, что поле пидксуникоде фактически указывает на структуру <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> . JET_bitIndexUnicode не требуется для индексирования данных в Юникоде. Это необходимо только для настройки нормализации данных в Юникоде.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexTuples</p></td>
<td><p>Указывает, что индекс является индексом кортежа. Описание индекса кортежа см. в разделе <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p>
<p>Значение JET_bitIndexTuples было введено в операционной системе Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexTupleLimits</p></td>
<td><p>Указание этого флага влияет на интерпретацию поля объединения <strong>кбварсегмак/птуплелимитс</strong> в структуре. Установка этого бита означает, что поле <strong>птуплелимитс</strong> действительно указывает на структуру <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , чтобы разрешить пользовательские ограничения индекса кортежа (подразумевает JET_bitIndexTuples).</p>
<p>Значение <strong>JET_bitIndexTupleLimits</strong> было введено в операционной системе Windows Server 2003.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexCrossProduct<br />
0x00004000</p></td>
<td><p>Если задать этот флаг для индекса, имеющего более одного ключевого столбца, который является многозначным, будет создана запись индекса для каждого результата перекрестного произведения всех значений в этих ключевых столбцах. В противном случае индекс будет иметь только одну запись для каждого многозначного ключевого столбца, который является многозначным столбцом, и каждая из этих элементов индекса будет использовать первый многозначный из всех ключевых столбцов, которые являются многозначными столбцами.</p>
<p>Например, если вы указали этот флаг для индекса для столбца A, который имеет значения &quot; Red &quot; и Blue &quot; , &quot; а столбец B со значениями &quot; 1 &quot; и &quot; 2 &quot; , будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; красный &quot; , &quot; 2 &quot; ; &quot; синий &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 2 &quot; . В противном случае будут созданы следующие записи индекса: &quot; Red &quot; , &quot; 1 &quot; ; &quot; синий &quot; , &quot; 1 &quot; .</p>
<p>Значение <strong>JET_bitIndexCrossProduct</strong> было введено в Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIndexKeyMost<br />
0x00008000</p></td>
<td><p>При указании этого флага индекс будет использовать максимальный размер ключа, указанный в поле <strong>кбкэймост</strong> структуры. В противном случае индекс будет использовать JET_cbKeyMost (255) в качестве максимального размера ключа.</p>
<p>Значение <strong>JET_bitIndexKeyMost</strong> было введено в Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIndexDisallowTruncation<br />
0x00010000</p></td>
<td><p>При указании этого флага любое обновление индекса приведет к сбою усечения ключа с кодом ответа JET_errKeyTruncated. В противном случае ключи будут обрезаны без уведомления. Дополнительные сведения о усечении ключа см. в разделе <a href="gg269329(v=exchg.10).md">жетмакекэй</a>.</p>
<p>Значение <strong>JET_bitIndexDisallowTruncation</strong> было введено в Windows Vista.</p></td>
</tr>
</tbody>
</table>


**улденсити**

Процентная плотность начального дерева B +. При указании числа меньше 100 используется больше места для первоначального создания индекса, но обеспечивается дальнейшее увеличение индекса, что позволяет избежать внутренней фрагментации.

**lcid**

Код локали (LCID), используемый при нормализации данных, если значение JET_bitIndexUnicode не указано в параметре *грбит* . Код языка (LCID) влияет на нормализацию, если индекс превышает столбцы в Юникоде.

**пидксуникоде**

Указатель на структуру [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) , если значение JET_bitIndexUnicode задано в параметре *грбит* . Это позволяет пользователю указать пользовательские флаги, которые передаются функции [LCMapString завершилось ошибкой](https://msdn.microsoft.com/library/dd318700\(vs.85\).aspx) во время нормализации Юникода.

**кбварсегмак**

Максимальная длина (в байтах) каждого столбца, сохраняемого в индексе, если значение JET_bitIndexTupleLimits не указано в параметре *грбит* .

Указание значения 0 (ноль) для этого поля эквивалентно следующему:

  - Указание JET_cbPrimaryKeyMost для первичного индекса.

  - Указание JET_cbSecondaryKeyMost для вторичного индекса.

**птуплелимитс**

Указатель на структуру [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) , если значение JET_bitIndexTupleLimits задано в параметре *грбит* .

**птуплелимитс** появился в Windows Server 2003.

**ргкондитионалколумн**

Необязательный параметр для массива структур [JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md) , которые используются для указания условных столбцов в индексе.

**ккондитионалколумн**

Число структур в массиве **ргкондитионалколумн** .

**Err**

Содержит код возврата для создания этого индекса.

**кбкэймост**

Указывает максимально допустимый размер (в байтах) для ключей в индексе. Этот параметр игнорируется, если JET_bitIndexKeyMost не указан в параметре *грбит* . Если этот параметр имеет значение 0, а JET_bitIndexKeyMost указан в члене *грбит* , вызывающая функция завершится ошибкой с JET_err_InvalidDef.

Минимальный поддерживаемый максимальный размер ключа — JET_cbKeyMostMin (255), который является устаревшим максимальным размером ключа.

Максимальный размер ключа зависит от размера страницы базы данных (JET_paramDatabasePageSize) следующим образом:

  - Если JET_paramDatabasePageSize = 2048, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost2KBytePage (500)

  - Если JET_paramDatabasePageSize = 4096, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost4KBytePage (1000)

  - Если JET_paramDatabasePageSize = 8192, то JET_cbKeyMostMin (255) \< =  **кбкэймост** \< = JET_cbKeyMost8KBytePage (2000)

Максимальный поддерживаемый максимальный размер ключа для экземпляра можно также прочитать из системного параметра JET_paramKeyMost.

**кбкэймост** появился в Windows Vista.

**пспацехинтс**

Указатель на структуру [JET_SPACEHINTS](./jet-spacehints-structure.md) .

**пспацехинтс** появился в Windows 7.

### <a name="remarks"></a>Комментарии

ESE поддерживает индексирование по ключевым столбцам, содержащим несколько значений. Чтобы использовать эту функцию, столбец должен быть типом столбца с тегами (JET_bitColumnTagged) и должен быть помечен для индексации нескольких значений с помощью JET_bitColumnMultiValued. В версиях Windows, предшествующих Windows Vista, значения в индексе будут развернуты только в первом многозначном ключевом столбце индекса. Все другие многозначные и помеченные столбцы будут иметь только первые значения, развернутые в индексе.

Предположим, что в таблице существуют следующие строки (столбец Alpha не является многозначным, а столбцы бета, гамма и Дельта являются многозначными), а индекс создается как "+ Альфа \\ 0 + бета-версия \\ 0 + гамма 0 + \\ Дельта 0 \\ \\ 0":

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Коэффициент альфа</p></th>
<th><p>Бета;</p></th>
<th><p>Gamma</p></th>
<th><p>Разностная версия</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>ABC<br />
GHI<br />
JKL</p></td>
<td><p>MNO<br />
PQR<br />
STU</p></td>
<td><p>ввкс<br />
из</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p>ТОТ</p></td>
<td><p>ДОЖДЯ<br />
Испания</p></td>
<td><p>IN<br />
ПОПАДАЕТ</p></td>
</tr>
</tbody>
</table>


Будут сохранены следующие индексные кортежи:

{1, ABC, MNO, ВВКС}  
{1, GHI, MNO, ВВКС}  
{1, ЖКЛ, MNO, ВВКС}  
{2, ДОЖДЯ, IN}

Обратите внимание, что {2,, Испания, IN} не хранится, несмотря на то, что столбец Alpha во второй строке имеет один многозначный.

В версиях Windows, начиная с Windows Vista, все Многозначные столбцы можно расширить в индексе, указав JET_bitIndexCrossProduct.

### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008, Windows Server 2003 или Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>JET_ INDEXCREATE2_W</strong> (Юникод) и <strong>JET_ INDEXCREATE2_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>См. также раздел

[JET_COLTYP](./jet-coltyp.md)  
[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_TABLECREATE](./jet-tablecreate-structure.md)  
[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[жетсетколумн](./jetsetcolumn-function.md)  
[жетупдате](./jetupdate-function.md)
