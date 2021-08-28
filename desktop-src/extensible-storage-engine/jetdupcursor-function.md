---
description: Дополнительные сведения о функции Жетдупкурсор
title: Функция JetDupCursor
TOCTitle: JetDupCursor Function
ms:assetid: 154b7d2d-4656-46b3-873c-2e194a9059b4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269193(v=EXCHG.10)
ms:contentKeyID: 32765496
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDupCursor
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a96f93357bc3df143fa63ed690295e40980cfc94
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472660"
---
# <a name="jetdupcursor-function"></a>Функция JetDupCursor


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetdupcursor-function"></a>Функция JetDupCursor

Функция **жетдупкурсор** дублирует открытый курсор и возвращает указатель на дублирующийся курсор. Если курсор, который был продублирован, был курсором только для чтения, то дубликат курсора также является курсором только для чтения. Любое состояние, связанное с построением ключа поиска или обновлением записи, не копируется в дублирующийся курсор. Кроме того, положение исходного курсора не дублируется в повторяющемся курсоре. Дубликат курсора всегда открывается в кластеризованном индексе, и его расположение всегда находится в первой строке таблицы.

```cpp
    JET_ERR JET_API JetDupCursor(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_TABLEID* ptableid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*pTableID*

Указатель на *tableid*.

*грбит*

Зарезервировано для последующего использования.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errOutOfCursors</p> | <p>Нет доступных ресурсов курсора.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p> | 
| <p>JET_errTermInProgress</p> | <p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p> | 



При успешном выполнении *pTableID* задается дубликат курсора.

В случае сбоя изменения не вносятся. Состояние *tableid* не изменяется.

#### <a name="remarks"></a>Комментарии

Для повторяющегося курсора не скопировано полное состояние курсора. Расположение повторяющегося курсора, включая текущий индекс, обычно отличается от указанного курсора. Дубликат курсора всегда возвращается в кластеризованном индексе и в первой строке таблицы. Если таблица пуста, то дублирующийся курсор не находится ни в одной строке.

Таблицы, открытые с помощью **жетдупкурсор** , обычно должны быть закрыты с помощью [жетклосетабле](./jetclosetable-function.md). Исключение из этого правила происходит при вызове **жетдупкурсор** в транзакции и откате транзакции (WITH [жетроллбакк](./jetrollback-function.md)). При откате транзакции курсор автоматически закрывается. В этом случае возникает ошибка при закрытии таблицы с помощью [жетклосетабле](./jetclosetable-function.md).

Количество таблиц, которые могут быть открыты одновременно, повлияет непосредственно на [JET_paramMaxOpenTables](./resource-parameters.md). Дополнительные сведения см. в разделе [системные параметры](./extensible-storage-engine-system-parameters.md) .

#### <a name="requirements"></a>Требования


| | | <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | | <p><strong>Сервер</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | | <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | | <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | | <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетклосетабле](./jetclosetable-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
