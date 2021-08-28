---
description: Дополнительные сведения о функции Жетжетрекордпоситион
title: Функция JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd1e84b995485afd46119b78289c1cac23e19215
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982437"
---
# <a name="jetgetrecordposition-function"></a>Функция JetGetRecordPosition


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetgetrecordposition-function"></a>Функция JetGetRecordPosition

Функция **жетжетрекордпоситион** Возвращает дробную часть текущей записи в текущем индексе в виде структуры [JET_RECPOS](./jet-recpos-structure.md) . Эта структура описывает дробные положения с точки зрения приблизительного числа элементов индекса до текущей записи и приблизительного общего числа записей в индексе.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*прекпос*

Описание доли, используемой при получении позиции текущей записи в текущем индексе.

*кбрекпос*

Размер памяти, выделенной на *прекпос*.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).


| <p>Код возврата</p> | <p>Описание</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>Операция выполнена успешно.</p> | 
| <p>JET_errNotInitialized</p> | <p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Эта операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку. Чтобы защитить целостность данных, необходимо отозвать доступ ко всем данным.</p><p><strong>Windows 2000:</strong>  эта ошибка не будет возвращена операционной системой Windows 2000.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Размер выделенной памяти на <em>прекпос</em> не является достаточным размером.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Курсор в настоящий момент не находится в записи и не может вернуть позицию.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p><p><strong>Windows 2000:</strong>  эта ошибка не будет возвращена операционной системой Windows 2000.</p> | 
| <p>JET_errTermInProgress</p> | <p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</p> | 



При успешном выполнении приблизительное количество записей индекса, предшествующее текущей записи в индексе, возвращается в прекпос- \> центриеслт. 1 возвращается в прекпос- \> центриесинранже. Приблизительное число записей в индексе возвращается в прекпос- \> центриестотал.

В случае сбоя в память, выделенную в *прекпос*, не вносятся изменения.

#### <a name="remarks"></a>Комментарии

Эта операция возвращает различные данные, когда обновления происходят непрерывно в таблице. Изменения в значениях не всегда будут соответствовать ожиданиям на основе знаний об обновлениях, так как значения являются приближениями на основе физических свойств индекса. Изоляция транзакций не применяется к позициям из **жетжетрекордпоситион** , так как значения зависят от физических свойств индекса, которые не являются изолированными транзакциями.

[JET_RECPOS](./jet-recpos-structure.md) не следует использовать для описания записи в таблице или перемещения записи, близкой к существующей записи. Вместо этого необходимо извлечь закладки для существующей записи, а затем использовать ее для перемещения той же записи.

#### <a name="requirements"></a>Требования


| Требование | Применение |
|------------|----------|
| <p><strong>Клиент</strong></p> | <p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p> | 
| <p><strong>Server</strong></p> | <p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p> | 
| <p><strong>Header</strong></p> | <p>Объявлено в ESENT. h.</p> | 
| <p><strong>Библиотека</strong></p> | <p>Используйте ESENT. lib.</p> | 
| <p><strong>КОМПОНОВКИ</strong></p> | <p>Требуется ESENT.dll.</p> | 



#### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[жетготопоситион](./jetgotoposition-function.md)  
[жетстопсервице](./jetstopservice-function.md)
