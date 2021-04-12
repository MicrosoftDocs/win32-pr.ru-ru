---
description: Дополнительные сведения о функции Жетренаметабле
title: Функция Жетренаметабле
TOCTitle: JetRenameTable Function
ms:assetid: face9341-58e3-450b-980d-08eb1dc3e9d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294142(v=EXCHG.10)
ms:contentKeyID: 32765756
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetRenameTableW
- JetRenameTableA
- JetRenameTable
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 624b194a1cad836b8927e6e7e4b8490fcad250b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348765"
---
# <a name="jetrenametable-function"></a>Функция Жетренаметабле


_**Применимо к:** Windows | Windows Server_

## <a name="jetrenametable-function"></a>Функция Жетренаметабле

Функцию **жетренаметабле** можно использовать для изменения имени существующей таблицы.

```cpp
    JET_ERR JET_API JetRenameTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szName,
      __in          const tchar* szNameNew
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*DBID*

База данных, используемая для этого вызова.

*szName*

Текущее имя таблицы, которая будет переименована.

*сзнаменев*

Новое имя таблицы, которая будет переименована.

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
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidDatabase</p></td>
<td><p>Указана недопустимая база данных.</p>
<p>Эта ошибка возвращается в Windows 2000 только при попытке выполнить операцию переименования таблицы во временной базе данных. JET_errInvalidDatabaseId возвращается в этом случае в более поздних выпусках.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidDatabaseId</p></td>
<td><p>Указан недопустимый идентификатор базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidName</p></td>
<td><p>Одно из указанных имен объектов недопустимо. Все имена объектов должны соответствовать одному и тому же набору правил. Ниже приведены эти правила.</p>
<ul>
<li><p>Имена объектов должны состоять из символов ASCII.</p></li>
<li><p>Имена объектов должны иметь длину по крайней мере один символ.</p></li>
<li><p>Длина имен объектов не может превышать JET_cbNameMost (64) символов.</p></li>
<li><p>Имена объектов не могут начинаться с пробела.</p></li>
<li><p>Имена объектов не могут содержать управляющие символы ASCII (0x00 – 0x1F).</p></li>
<li><p>Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]) после проверки. для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется). Это фактически означает, что имена объектов не могут содержать пробелы.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Это может произойти для <strong>жетренаметабле</strong> в следующих случаях:</p>
<ul>
<li><p><em>szName</em> имеет значение null.</p></li>
<li><p><em>сзнаменев</em> имеет значение null.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errObjectNotFound</p></td>
<td><p>Указанная таблица не существует для этой базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Обновление невозможно выполнить в рамках транзакции, доступной только для чтения. Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly.</p>
<p>Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении имя указанной таблицы в заданной базе данных постоянно меняется на новое имя.

В случае сбоя не произойдет никаких изменений в состоянии базы данных.

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
<tr class="even">
<td><p><strong>Юникод</strong></p></td>
<td><p>Реализуется как <strong>жетренаметаблев</strong> (Юникод) и <strong>жетренаметаблеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)
