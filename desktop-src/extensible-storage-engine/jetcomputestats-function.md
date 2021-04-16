---
description: Дополнительные сведения о функции Жеткомпутестатс
title: Функция Жеткомпутестатс
TOCTitle: JetComputeStats Function
ms:assetid: 142f6ab0-715f-493a-a762-7a83854498d2
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269192(v=EXCHG.10)
ms:contentKeyID: 32765495
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetComputeStats
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c6856a50ae2f1c01b1cfde0666d0c535ad37e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272854"
---
# <a name="jetcomputestats-function"></a>Функция Жеткомпутестатс


_**Применимо к:** Windows | Windows Server_

## <a name="jetcomputestats-function"></a>Функция Жеткомпутестатс

Функция **жеткомпутестатс** просматривает каждый индекс таблицы, чтобы точно вычислить количество записей в индексе и количество различных ключей в индексе. Эти сведения вместе с количеством страниц базы данных, выделенных для индекса, и текущим временем вычислений хранятся в метаданных индекса в базе данных. Эти данные можно впоследствии извлечь с помощью информационных операций.

```cpp
    JET_ERR JET_API JetComputeStats(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, который будет использоваться для этого вызова. Описывает таблицу для расчета статистики.

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
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p>Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
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
<td><p>JET_errRollbackError</p></td>
<td><p>При выполнении этой операции откат всех изменений произошла ошибка, но произошел сбой отката транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно для нескольких потоков.</p>
<p>Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении статистика сохраняется в каталогах базы данных для таблицы, описанной в данном курсоре.

В случае сбоя никакие изменения не вносятся в базу данных.

#### <a name="remarks"></a>Комментарии

Эта операция может быть расходом ресурсов, так как каждый индекс в таблице должен быть полностью изменяться. [Жетжетрекордпоситион](./jetgetrecordposition-function.md) можно использовать для грубой оценки количества записей в индексе, но сам по себе не может оценить количество уникальных значений в индексе.

Данные, вычисленные этой операцией, начинают устареть, а таблица впоследствии обновляется.

Обновления базы данных, внесенные **жеткомпутестатс** , выполняются отложенно. Это означает, что эта операция не приведет к сбросу журнала, а после возврата JET_errSuccess **жеткомпутестатс** по-прежнему может привести к потере этих обновлений.

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

[JET_ERR](./jet-err.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_SESID](./jet-sesid.md)  
[жетжетрекордпоситион](./jetgetrecordposition-function.md)  
[жетжеттаблеинфо](./jetgettableinfo-function.md)  
[жетжеттаблеиндексинфо](./jetgettableindexinfo-function.md)  
[жетстопсервице](./jetstopservice-function.md)
