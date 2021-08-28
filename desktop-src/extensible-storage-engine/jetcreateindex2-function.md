---
description: Дополнительные сведения о функции JetCreateIndex2
title: Функция JetCreateIndex2
TOCTitle: JetCreateIndex2 Function
ms:assetid: 8810eaed-40cb-4561-aafc-9a9bbdb0d05b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269324(v=EXCHG.10)
ms:contentKeyID: 32765614
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndex2W
- JetCreateIndex2A
- JetCreateIndex2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fc11fe1e5d2b4d6f14ad77cb98434b0daf6b81f1
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987457"
---
# <a name="jetcreateindex2-function"></a>Функция JetCreateIndex2


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetcreateindex2-function"></a>Функция JetCreateIndex2

Функция **JetCreateIndex2** создает индексы для данных в базе данных ESE, которая может быть использована для быстрого выявления конкретных данных.

```cpp
    JET_ERR JET_API JetCreateIndex2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_INDEXCREATE* pindexcreate,
      __in          unsigned long cIndexCreate
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, в которой будет создан индекс.

*пиндекскреате*

Массив структур [JET_INDEXCREATE](./jet-indexcreate-structure.md) , каждый из которых определяет создаваемый индекс.

*Циндекскреате*

Число элементов в массиве *пиндекскреате* .

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errCannotIndex</p> | <p>Предпринята попытка индексирования по столбцу с использованием типа "условно-Update" или "SLV" (Обратите внимание, что столбцы SLV устарели).</p> | 
| <p>JET_errColumnNotFound</p> | <p>Предпринята попытка индексировать несуществующий столбец. Эта ошибка также может возникнуть при попытке условного индексирования по несуществующему столбцу.</p> | 
| <p>JET_errDensityInvalid</p> | <p>Эта ошибка будет возвращена, если элементу <strong>улденсити</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> присвоено число меньше 20 или больше 100.</p> | 
| <p>JET_errIndexDuplicate</p> | <p>Была выполнена попытка определить два одинаковых индекса.</p> | 
| <p>JET_errIndexHasPrimary</p> | <p>Предпринята попытка указать более одного первичного индекса для таблицы. У таблицы должен быть ровно один первичный индекс. Если первичный индекс не указан, ядро СУБД будет прозрачно создавать его.</p> | 
| <p>JET_errIndexInvalidDef</p> | <p>Указано недопустимое определение индекса. Ниже приведены некоторые возможные причины получения этой ошибки:</p><ul><li><p>Первичный индекс является условным (<strong>грбит</strong> член <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexPrimary набор, а элемент <strong>ккондитионалколумн</strong> <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> больше нуля).</p></li><li><p>Windows Сервер 2003 и более поздней версии. Попытка создать индекс кортежа с ограничениями кортежей, но без передачи сведений в элемент <strong>птуплелимитс</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> (то есть <em>грбит</em> имеет набор JET_bitIndexTupleLimits, но указатель <strong>птуплелимитс</strong> имеет значение null).</p></li><li><p>Передача недопустимого определения ключа в элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> . Описание допустимых определений см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p></li><li><p>Установка для элемента <strong>кбварсегмак</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> значение больше JET_cbPrimaryKeyMost (для первичного индекса) или больше JET_cbSecondaryKeyMost (для вторичного индекса).</p></li><li><p>Передача недопустимого сочетания для определяемого пользователем индекса в Юникоде (одна из которых имеет бит JET_bitIndexUnicode, заданный в элементе <strong>грбит</strong> в <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a>). Некоторые распространенные причины могут быть вызваны тем, что поле пидксуникоде структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение null или код LCID, указанный в структуре пидксуникоде, является недопустимым.</p></li><li><p>Указание столбца с несколькими значениями для первичного индекса.</p></li><li><p>Попытка индексировать слишком много условных столбцов. Элемент <strong>ккондитионалколумн</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен быть больше JET_ccolKeyMost.</p></li></ul> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Windows XP и более поздних версий. Указана структура <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> , а ее ограничения не поддерживаются. См. раздел "Примечания" структуры <a href="gg269207(v=exchg.10).md">JET_TUPLELIMITS</a> .</p> | 
| <p>JET_errIndexTuplesNonUniqueOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть уникальным (<em>грбит</em> не должен содержать как JET_bitIndexTuples, так JET_bitIndexUnique Set).</p> | 
| <p>JET_errIndexTuplesOneColumnOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в одном столбце (то есть элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет JET_bitIndexTuples набор, а элемент <strong>сзкэй</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> указывает более одного столбца).</p> | 
| <p>JET_errIndexTuplesSecondaryIndexOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа не может быть первичным индексом (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не должен иметь одновременно JET_bitIndexPrimary и JET_bitIndexTuples).</p> | 
| <p>JET_errIndexTuplesTextColumnsOnly</p> | <p>Windows XP и более поздних версий. Индекс кортежа может находиться только в тексте или столбце Юникода. Попытка индексировать другие столбцы (например, двоичные столбцы) приведет к JET_errIndexTuplesTextColumnsOnly.</p> | 
| <p>JET_errIndexTuplesVarSegMacNotAllowed</p> | <p>Windows XP и более поздних версий. Индекс кортежа не позволяет установить элемент <strong>кбварсегмак</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p> | 
| <p>JET_errInTransaction</p> | <p>Предпринята попытка создать индекс без сведений о версии во время транзакции.</p> | 
| <p>JET_errInvalidgrbit</p> | <p>Определение индекса недопустимо, так как элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> содержит неправильные значения. Возможные причины:</p><ul><li><p>В первичном индексе указан бит игнорирования (JET_bitIndexPrimary был передан с одним из JET_bitIndexIgnoreNull, JET_bitIndexIgnoreAnyNull или JET_bitIndexIgnoreFirstNull).</p></li><li><p>Пустой индекс не игнорирует какие-либо поля NULL (т. е. элемент <strong>грбит</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> JET_bitIndexEmpty задан, но не имеет набора JET_bitIndexIgnoreAnyNull).</p></li><li><p>Передача структуры <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a> с недопустимым элементом <strong>грбит</strong> . См. <a href="gg269214(v=exchg.10).md">JET_CONDITIONALCOLUMN</a>.</p></li></ul><p>При создании нескольких индексов одновременно (то есть если параметр <em>Циндекскреате</em> больше единицы) ни один из индексов не может содержать следующие биты:</p><ul><li><p>JET_bitIndexPrimary</p></li><li><p>JET_bitIndexUnversioned</p></li><li><p>JET_bitIndexEmpty</p></li></ul> | 
| <p>JET_errInvalidLanguageId</p> | <p>Передан недопустимый код локали (LCID) (с помощью элемента <strong>LCID</strong> в структуре <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> , которой элемент <strong>пидксуникоде</strong> в структуре <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> содержит указатель на или с помощью элемента <strong>LCID</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p> | 
| <p>JET_errInvalidName</p> | <p>Указано недопустимое имя индекса. Дополнительные сведения см. в разделе <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p> | 
| <p>JET_errInvalidParameter</p> | <p>В API передан недопустимый параметр. Ниже приведены некоторые причины, по которым эта ошибка может быть возвращена.</p><ul><li><p>Поле <strong>cbKey</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> имеет значение 0.</p></li><li><p>Элементу <strong>кбструкт</strong> структуры <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> не присвоено значение sizeof (<a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> ).</p></li></ul> | 
| <p>JET_errUnicodeTranslationFail</p> | <p>Произошла ошибка при попытке нормализовать столбец в Юникоде. Это может быть вызвано недостатком системных ресурсов.</p> | 



#### <a name="remarks"></a>Комментарии

Возвращаемое значение JET_errSuccess при успешном завершении всех указанных индексов.

**JetCreateIndex2** перебирает индексы, заданные в **пиндекскреате**, и иногда прерываются при первом сбое. Любые индексы после первого индекса с ошибкой могут не попытаться, несмотря на то, что элемент **Err** структуры [JET_INDEXCREATE](./jet-indexcreate-structure.md) содержит JET_errSuccess.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 
| <p><strong>Юникод</strong></p> | <p>Реализуется как <strong>JetCreateIndex2W</strong> (Юникод) и <strong>JetCreateIndex2A</strong> (ANSI).</p> | 



#### <a name="see-also"></a>См. также:

[JET_CONDITIONALCOLUMN](./jet-conditionalcolumn-structure.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[жеткреатеиндекс](./jetcreateindex-function.md)  
[жеткреатетаблеколумниндекс](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
