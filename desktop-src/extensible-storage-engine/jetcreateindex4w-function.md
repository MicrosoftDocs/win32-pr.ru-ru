---
description: Дополнительные сведения о функции JetCreateIndex4W
title: Функция JetCreateIndex4W
TOCTitle: JetCreateIndex4W Function
ms:assetid: 968745a2-66ce-4c7f-ab5b-43282adc5313
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835044(v=EXCHG.10)
ms:contentKeyID: 49894666
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetCreateIndex4W
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c79f1638645f0dcd7e4306f543a9ee15b9668843
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987447"
---
# <a name="jetcreateindex4w-function"></a>Функция JetCreateIndex4W


_**Применимо к:** Windows | Windows Сервером_

функция **JetCreateIndex4W** создает индексы для данных служба хранилища в базе данных ESE, которая может быть использована для быстрого поиска конкретных данных.

функция **JetCreateIndex4W** была введена в операционной системе Windows 8.

``` c++
JET_ERR JET_API JetCreateIndex4W(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in          JET_INDEXCREATE2* pindexcreate,
  __in          unsigned long cIndexCreate
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, в которой будет создан индекс.

*пиндекскреате*

Массив структур [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) , каждый из которых определяет создаваемый индекс.

*Циндекскреате*

Число элементов в массиве *пиндекскреате* .

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errCannotIndex</p> | <p>Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Предпринята попытка индексировать несуществующий столбец. Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> присвоено число меньше 20 или больше 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Была выполнена попытка определить два одинаковых индекса.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины этой ошибки.</p><ul><li><p>Первичный индекс является условным (<strong>грбит</strong> член <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет <strong>JET_bitIndexPrimary</strong> набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> больше нуля).</p></li><li><p>применимо к версиям Windows, начиная с Windows Server 2003. Предпринята попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> (то есть <em>грбит</em> имеет набор <strong>JET_bitIndexTupleLimits</strong> , но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li><li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> . Сведения о допустимых определениях см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>.</p></li><li><p>Установка для элемента <strong>кбварсегмак</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> значение больше <strong>JET_cbPrimaryKeyMost</strong> (для первичного индекса) или больше <strong>JET_cbSecondaryKeyMost</strong> (для вторичного индекса).</p></li><li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит <strong>JET_bitIndexUnicode</strong> , заданный в элементе <strong>грбит</strong> в <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a>). Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</p></li><li><p>Указание многозначного столбца для первичного индекса.</p></li><li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен быть больше <strong>JET_ccolKeyMost</strong>.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>применимо к версиям Windows начиная с Windows XP. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. Дополнительные сведения см. в разделе "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>применимо к версиям Windows начиная с Windows XP. Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как <strong>JET_bitIndexTuples</strong> , так <strong>JET_bitIndexUnique</strong> Set).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>применимо к версиям Windows начиная с Windows XP. Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет <strong>JET_bitIndexTuples</strong> набор, а элемент <strong>сзкэй</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> указывает более одного столбца).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>применимо к версиям Windows начиная с Windows XP. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не должен иметь одновременно <strong>JET_bitIndexPrimary</strong> и <strong>JET_bitIndexTuples</strong> ).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>применимо к версиям Windows начиная с Windows XP. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к <strong>JET_errIndexTuplesTextColumnsOnly</strong>.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>применимо к версиям Windows начиная с Windows XP. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка создать индекс без сведений о версии во время транзакции.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит неправильные значения. Ниже приведены некоторые возможные причины.</p><ul><li><p>В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из <strong>JET_bitIndexIgnoreNull</strong>, <strong>JET_bitIndexIgnoreAnyNull</strong>или <strong>JET_bitIndexIgnoreFirstNull</strong>).</p></li><li><p>Пустой индекс не игнорирует какие-либо поля null (т. е. элемент <strong>грбит</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> <strong>JET_bitIndexEmpty</strong> задан, но не имеет набора <strong>JET_bitIndexIgnoreAnyNull</strong> ).</p></li><li><p>Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> . См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</p><ul><li><p><strong>JET_bitIndexPrimary</strong></p></li><li><p><strong>JET_bitIndexUnversioned</strong></p></li><li><p><strong>JET_bitIndexEmpty</strong></p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> ).</p> | 
| <p>JET_errInvalidName</p> | <p>Указано недопустимое имя индекса. Дополнительные сведения см. в разделе <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> .</p> | 
| <p>JET_errInvalidParameter</p> | <p>В API передан недопустимый параметр. Ниже приведены некоторые причины, по которым может быть возвращена эта ошибка:</p><ul><li><p>Поле <strong>cbKey</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> имеет значение 0.</p></li><li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg294082(v=exchg.10).md">JET_INDEXCREATE2</a> не присвоено значение sizeof (JET_INDEXCREATE2).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Произошла ошибка при попытке нормализовать столбец в Юникоде. Это может быть вызвано недостатком системных ресурсов.</p> | 
| <p>JET_errSpaceHintsInvalid</p> | <p>Неверное или неправильное действие элемента структуры подсказок пространства JET.</p> | 



#### <a name="remarks"></a>Комментарии

Функция **JetCreateIndex4W** выполняет итерацию индексов, заданных в параметре *пиндекскреате* , и иногда прерывается при первом сбое. Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE2](./jet-indexcreate2-structure.md) содержит JET_errSuccess.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Требуется Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также раздел

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE2](./jet-indexcreate2-structure.md)  
[жеткреатеиндекс](./jetcreateindex-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)  
[JET_SPACEHINTS](./jet-spacehints-structure.md)
