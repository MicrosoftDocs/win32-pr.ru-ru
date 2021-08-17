---
description: Дополнительные сведения о функции Жетсетколумндефаултвалуе
title: Функция Жетсетколумндефаултвалуе
TOCTitle: JetSetColumnDefaultValue Function
ms:assetid: 74bfaf50-6c2e-4907-b931-d50ad314b552
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269295(v=EXCHG.10)
ms:contentKeyID: 32765587
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetColumnDefaultValue
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff0f704c30737d6cfc2d8bd823da8207e8d7d8c3fb4458687baf8bc400718304
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117703852"
---
# <a name="jetsetcolumndefaultvalue-function"></a>Функция Жетсетколумндефаултвалуе


_**Применимо к:** Windows | Windows Сервером_

## <a name="jetsetcolumndefaultvalue-function"></a>Функция Жетсетколумндефаултвалуе

Функцию **жетсетколумндефаултвалуе** можно использовать для изменения значения существующего столбца по умолчанию.

```cpp
    JET_ERR JET_API JetSetColumnDefaultValue(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          JET_PCSTR szTableName,
      __in          JET_PCSTR szColumnName,
      __in          const void* pvData,
      __in          const unsigned long cbData,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*DBID*

База данных, используемая для этого вызова.

*сзтабленаме*

Имя таблицы, содержащей столбец, который будет затронут.

*сзколумннаме*

Имя столбца, значение по умолчанию которого будет изменено.

*пвдата*

Входной буфер, содержащий новое значение по умолчанию.

*cbData*

Размер входного буфера, содержащего новое значение по умолчанию.

*грбит*

Зарезервировано для последующего использования.

### <a name="return-value"></a>Возвращаемое значение

Эта функция возвращает [JET_ERR](./jet-err.md) DataType с одним из следующих кодов возврата. дополнительные сведения о возможных ошибках подсистемы ESE см. в разделе [ошибки расширенных служба хранилища Engine](./extensible-storage-engine-errors.md) и [параметры обработки ошибок](./error-handling-parameters.md).

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
<td><p>JET_errColumnIllegalNull</p></td>
<td><p>То же, что и JET_errNullInvalid.</p></td>
</tr>
<tr class="even">
<td><p>JET_errColumnInUse</p></td>
<td><p>Этот указанный столбец в настоящее время используется индексом.</p>
<p><strong>Жетсетколумндефаултвалуе</strong> не может изменить значение по умолчанию для столбца, на который указывает ссылка в определении индекса. Это связано с тем, что это может привести к изменению содержимого индекса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errColumnNotFound</p></td>
<td><p>Указанный столбец не существует для этой таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
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
<li><p>Имена объектов не могут содержать восклицательный знак (!), точку (.), открывающую квадратную скобку ([) или правую квадратную скобку (]).</p></li>
<li><p>После проверки для имени объекта будет использоваться только часть строки вплоть до первого пробела (если таковая имеется). Это означает, что имена объектов не могут содержать пробелы.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNullInvalid</p></td>
<td><p>Не удалось установить значение NULL для этого столбца. Это происходит для <strong>жетсетколумндефаултвалуе</strong> в следующих случаях:</p>
<ul>
<li><p><em>cbData</em> имеет нулевое значение.</p></li>
<li><p><strong>пвдата</strong> имеет значение null.</p></li>
</ul>
<p>Поэтому невозможно установить значение по умолчанию для столбца (Back) в NULL или значение нулевой длины.</p></td>
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
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTableInUse</p></td>
<td><p>Указанная таблица используется другим сеансом.</p>
<p><strong>жетсетколумндефаултвалуе</strong> требует монопольного доступа к таблице, чтобы изменить значение по умолчанию для столбца для выпусков до Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Попытка обновления недействительна в пределах транзакции, доступной только для чтения. Транзакция только для чтения — это транзакция, которая была запущена с помощью вызова <a href="gg269268(v=exchg.10).md">JetBeginTransaction2</a> с JET_bitTransactionReadOnly. эта ошибка будет возвращена только Windows XP и более поздних выпусках.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Другой сеанс ранее заблокировал запись для обновления. Обновление, которое попыталось этот сеанс, завершится ошибкой.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении значение по умолчанию указанного столбца в данной таблице в заданной базе данных постоянно меняется на новое значение по умолчанию.

В случае сбоя не произойдет никаких изменений в состоянии базы данных.

#### <a name="remarks"></a>Remarks

Невозможно изменить значение по умолчанию для столбца в таблице шаблона.

Ядро СУБД автоматически усекает значение столбца по умолчанию до 255 байт для длинных текстовых и длинных двоичных столбцов.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
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
<td><p>Реализуется как <strong>жетсетколумндефаултвалуев</strong> (Юникод) и <strong>жетсетколумндефаултвалуеа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также

[JET_DBID](./jet-dbid.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JetBeginTransaction2](./jetbegintransaction2-function.md)  
[жетстопсервице](./jetstopservice-function.md)
