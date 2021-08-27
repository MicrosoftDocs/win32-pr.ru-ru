---
description: Дополнительные сведения о функции Жетпререадиндексранжес
title: Функция Жетпререадиндексранжес
TOCTitle: JetPrereadIndexRanges Function
ms:assetid: ab49abcc-eaeb-438f-8e6d-b08bc94d7bc3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835045(v=EXCHG.10)
ms:contentKeyID: 49894667
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetPrereadIndexRanges
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ff2d9e7c538e8aa8cc862fe9a72c0308e497fd4
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122986667"
---
# <a name="jetprereadindexranges-function"></a>Функция Жетпререадиндексранжес


_**Применимо к:** Windows | Windows Сервером_

Функция **жетпререадиндексранжес** считывает индексы для повышения производительности.

функция **жетпререадиндексранжес** была введена в операционной системе Windows 8.

``` c++
JET_ERR JetPrereadIndexRanges(
  __in          const JET_SESID sesid,
  __in          const JET_TABLEID tableid,
  __in_ecount(cIndexRanges)  const JET_INDEX_RANGE* const rgIndexRanges,
  __in          const unsigned long cIndexRanges,
  __out_opt     unsigned long* const pcRangesPreread,
  __in_ecount(ccolumnidPreread)  const JET_COLUMNID* const rgcolumnidPreread,
  __in          const unsigned long ccolumnidPreread,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*TableID*

Таблица, для которой выдаются сведения о предчтении.

*ргиндексранжес*

Диапазоны ключей для чтения.

*Циндексранжес*

Число диапазонов ключей для предчтения, определяемое числом элементов в *ргиндексранжес*.

*пкранжеспререад*

Количество диапазонов ключей, которые фактически были считаны.

*ргколумнидпререад*

Список идентификаторов столбцов для столбцов с длинными значениями для чтения. По умолчанию предварительно считывается только запись на странице. Если необходимо предварительно прочитать столбцы с длинными значениями в виде страниц, их идентификаторы столбцов должны передаваться через этот параметр.

*кколумнидпререад*

Количество идентификаторов столбцов для столбцов с длинными значениями, которые должны быть считаны, определяется числом элементов в *ргколумнидпререад*.

*грбит*

Группа битов, указывающая ноль или более значений направления, перечисленных в следующей таблице.


| <p>Значение</p> | <p>Значение</p> | 
|--------------|----------------|
| <p>Вперед</p> | <p>Чтение вперед.</p> | 
| <p>Назад</p> | <p>Прочтите обратно.</p> | 
| <p>фирстпажеонли</p> | <p>Предварительное чтение только первой страницы любого столбца Long.</p> | 
| <p>нормализедкэй</p> | <p>Нормализованное значение ключа или закладки вместо значения столбца.</p> | 



### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) тип данных с одним из кодов возврата, перечисленных в следующей таблице. дополнительные сведения о служба хранилища возможных ошибках ESE см. в разделе [ошибки расширяемых](./extensible-storage-engine-errors.md) подсистемы служба хранилища и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 



#### <a name="remarks"></a>Комментарии

Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, следует запустить асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>Требуется Windows 8.</p> | 
| <p><strong>Server</strong></p> | <p>Требуется Windows Server 2012.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также раздел

[JET_ERR](./jet-err.md)
