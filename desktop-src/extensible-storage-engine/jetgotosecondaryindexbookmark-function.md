---
description: Дополнительные сведения о функции Жетготосекондариндексбукмарк
title: Функция Жетготосекондариндексбукмарк
TOCTitle: JetGotoSecondaryIndexBookmark Function
ms:assetid: 06983b1e-503a-469b-9be5-b37e7551de67
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269180(v=EXCHG.10)
ms:contentKeyID: 32765483
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 893833fd1770fe3d972033a4d10f9047b0f61dfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998659"
---
# <a name="jetgotosecondaryindexbookmark-function"></a>Функция Жетготосекондариндексбукмарк


_**Применимо к:** Windows | Windows Server_

## <a name="jetgotosecondaryindexbookmark-function"></a>Функция Жетготосекондариндексбукмарк

Функция **жетготосекондариндексбукмарк** устанавливает курсор на запись индекса, связанную с закладкой вторичного индекса. Закладку вторичного индекса необходимо использовать с тем же индексом для той же таблицы, из которой она была первоначально извлечена. Закладку вторичного индекса для записи индекса можно получить с помощью **жетготосекондариндексбукмарк**.

**Windows XP:**  **Жетготосекондариндексбукмарк** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGotoSecondaryIndexBookmark(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          void* pvSecondaryKey,
      __in          unsigned long cbSecondaryKey,
      __in_opt      void* pvPrimaryBookmark,
      __in          unsigned long cbPrimaryBookmark,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*пвсекондарикэй*

Буфер, содержащий вторичный ключ, используемый для позиционирования курсора.

*кбсекондарикэй*

Размер вторичного ключа в буфере.

*пвпримарибукмарк*

Буфер, содержащий закладку первичного ключа, используемую для позиционирования курсора.

*кбпримарибукмарк*

Размер закладки первичного ключа в буфере.

*грбит*

Группа битов, которая задает ноль или более следующих параметров.

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
<td><p>JET_bitBookmarkPermitVirtualCurrency</p></td>
<td><p>В случае, если запись индекса больше не может быть найдена, курсор будет расположен слева, где была найдена Эта запись индекса. Операция по-прежнему завершится ошибкой с JET_errRecordDeleted; Тем не менее, можно перейти к следующей или предыдущей записи индекса относительно записи индекса, которая сейчас отсутствует.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Операция не может быть завершена, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Операция не может быть завершена, так как в экземпляре, связанном с сеансом, произошла неустранимая ошибка, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidBookmark</p></td>
<td><p>Указана недопустимая закладка вторичного индекса. Эта ошибка могла произойти из-за того, что вторичный ключ равен нулю или указатель буфера вторичного ключа имеет <strong>значение NULL</strong>. Эта ошибка возникает из-за того, что</p>
<ul>
<li><p>Текущий вторичный индекс не имеет ограничения уникальности, а размер указанной закладки равен нулю.</p></li>
<li><p>Указатель буфера закладки имеет <strong>значение NULL</strong>.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentIndex</p></td>
<td><p>Курсор в данный момент не находится во вторичном индексе. Не имеет смысла переходить к закладке вторичного индекса, если в данный момент курсор не использует вторичный индекс. <a href="gg294053(v=exchg.10).md">Жетготобукмарк</a> следует использовать, если курсор не находится на вторичном индексе.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Операция не может быть завершена, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Не удалось найти запись индекса, связанную с закладкой вторичного индекса.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Операция не может быть завершена, так как выполняется операция восстановления на экземпляре, связанном с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p><strong>Windows XP:</strong>  Это возвращаемое значение введено в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Не удается выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


Если эта функция выполнена, курсор будет размещен в записи индекса, связанной с закладкой дополнительного индекса. Если запись подготовлена к обновлению, это обновление будет отменено. Если действует диапазон индексов, то диапазон индексов будет отменен. Если для использования курсора был создан ключ поиска, этот ключ поиска будет удален. Изменение состояния базы данных не выполняется.

Если эта функция завершается ошибкой, то позицию курсора остается неизменной, если не будет возвращен JET_errRecordDeleted и не будет указан JET_bitBookmarkPermitVirtualCurrency. В этом случае курсор будет размещен в том месте, где была бы запись индекса, связанная с заданной закладкой вторичного индекса. Курсор можно переместить относительно этой позиции, но по-прежнему не находится в допустимой записи индекса.

Если запись подготовлена к обновлению, это обновление будет отменено. Если действует диапазон индексов, то диапазон индексов будет отменен. Если для использования курсора был создан ключ поиска, этот ключ поиска будет удален. В любом случае изменение состояния базы данных не выполняется.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista или Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008 или Windows Server 2003.</p></td>
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

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжетсекондариндексбукмарк](./jetgetsecondaryindexbookmark-function.md)  
[жетготобукмарк](./jetgotobookmark-function.md)  
[жетстопсервице](./jetstopservice-function.md)
