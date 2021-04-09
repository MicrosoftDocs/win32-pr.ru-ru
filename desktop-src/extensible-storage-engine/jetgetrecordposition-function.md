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
ms.openlocfilehash: d4301b25ca111228b742ce7b35ab9ae28e170526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080884"
---
# <a name="jetgetrecordposition-function"></a>Функция JetGetRecordPosition


_**Применимо к:** Windows | Windows Server_

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

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. Дополнительные сведения о возможных ошибках ESE см. в разделе [ошибки подсистемы хранилища](./extensible-storage-engine-errors.md) и [Параметры обработки ошибок](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Код возврата</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>Операция выполнена успешно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Эта операция не может быть завершена, так как экземпляр, связанный с сеансом, обнаружил неустранимую ошибку. Чтобы защитить целостность данных, необходимо отозвать доступ ко всем данным.</p>
<p><strong>Windows 2000:</strong>  Эта ошибка не будет возвращена операционной системой Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Размер выделенной памяти на <em>прекпос</em> не является достаточным размером.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Курсор в настоящий момент не находится в записи и не может вернуть позицию.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows 2000:</strong>  Эта ошибка не будет возвращена операционной системой Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, завершает работу.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении приблизительное количество записей индекса, предшествующее текущей записи в индексе, возвращается в прекпос- \> центриеслт. 1 возвращается в прекпос- \> центриесинранже. Приблизительное число записей в индексе возвращается в прекпос- \> центриестотал.

В случае сбоя в память, выделенную в *прекпос*, не вносятся изменения.

#### <a name="remarks"></a>Комментарии

Эта операция возвращает различные данные, когда обновления происходят непрерывно в таблице. Изменения в значениях не всегда будут соответствовать ожиданиям на основе знаний об обновлениях, так как значения являются приближениями на основе физических свойств индекса. Изоляция транзакций не применяется к позициям из **жетжетрекордпоситион** , так как значения зависят от физических свойств индекса, которые не являются изолированными транзакциями.

[JET_RECPOS](./jet-recpos-structure.md) не следует использовать для описания записи в таблице или перемещения записи, близкой к существующей записи. Вместо этого необходимо извлечь закладки для существующей записи, а затем использовать ее для перемещения той же записи.

#### <a name="requirements"></a>Требования

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
<td><p><strong>Библиотека</strong></p></td>
<td><p>Используйте ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>КОМПОНОВКИ</strong></p></td>
<td><p>Требуется ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[жетготопоситион](./jetgotoposition-function.md)  
[жетстопсервице](./jetstopservice-function.md)
