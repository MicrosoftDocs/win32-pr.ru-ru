---
description: Дополнительные сведения о функции Жетренамеколумн
title: Функция Жетренамеколумн
TOCTitle: JetRenameColumn Function
ms:assetid: 30967765-355b-417c-b0d6-8b59e677cc98
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269218(v=EXCHG.10)
ms:contentKeyID: 32765521
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameColumn
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ab2dee1895e4148bb2ea0600464d7e9c4a6a358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702926"
---
# <a name="jetrenamecolumn-function"></a>Функция Жетренамеколумн


_**Применимо к:** Windows | Windows Server_

## <a name="jetrenamecolumn-function"></a>Функция Жетренамеколумн

Функцию **жетренамеколумн** можно использовать для изменения имени существующего столбца в таблице.

**Windows XP:**  **Жетренамеколумн** появился в Windows XP.

```cpp
    JET_ERR JET_API JetRenameColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szName,
      __in          JET_PCSTR szNameNew,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*szName*

Текущее имя столбца, который будет переименован.

*сзнаменев*

Новое имя для столбца, который будет переименован.

*грбит*

Этот параметр должен иметь значение 0.

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
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Указанный столбец не существует для этой таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Одно из указанных имен объектов недопустимо. Все имена объектов должны соответствовать одному и тому же набору правил. Ниже приведены эти правила.</p>
<ul>
<li><p>Имена объектов должны состоять из символов ASCII.</p></li>
<li><p>Имена объектов должны иметь длину по крайней мере один символ.</p></li>
<li><p>Длина имен объектов не может превышать JET_cbNameMost (64) символов.</p></li>
<li><p>Имена объектов не могут начинаться с имен объектов пробела, не могут содержать управляющие символы ASCII (0x00 – 0x1F).</p></li>
<li><p>Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</p></li>
<li><p>После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется). Это фактически означает, что имена объектов не могут содержать пробелы.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетренамеколумн</strong> в следующих случаях:</p>
<ul>
<li><p><em>szName</em> имеет значение null.</p></li>
<li><p><em>сзнаменев</em> имеет значение null.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInTransaction</p></td>
<td><p>Эта операция может быть выполнена только в том случае, если сеанс не находится в транзакции.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Обновление невозможно выполнить в рамках транзакции, доступной только для чтения. Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении имя указанного столбца в таблице, связанной с курсором, будет безвозвратно изменено на новое имя. Все индексы, ссылающиеся на этот столбец, также будут обновлены.

В случае сбоя не произойдет никаких изменений в состоянии базы данных.

#### <a name="remarks"></a>Комментарии

Операция переименования столбца нетипична, поскольку, в отличие от других операций с схемами, она не выполняется как транзакция. Когда столбец в заданной таблице переименовывается в одном сеансе, любой другой сеанс, использующий эту таблицу, сразу же увидит изменение, даже если они находятся в транзакции, препятствующей тому, что сеанс не сможет увидеть другие изменения, внесенные сеансом, выполняющим операцию переименования.

Операция переименования не затрагивает идентификатор столбца столбца.

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
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жетренамеколумнв</strong> (Юникод) и <strong>жетренамеколумна</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
