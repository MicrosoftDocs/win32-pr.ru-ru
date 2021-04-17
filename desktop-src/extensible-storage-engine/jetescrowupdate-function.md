---
description: Дополнительные сведения о функции Жетескровупдате
title: Функция JetEscrowUpdate
TOCTitle: JetEscrowUpdate Function
ms:assetid: e509b6c9-a8ce-4898-a426-485e286869fa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294125(v=EXCHG.10)
ms:contentKeyID: 32765739
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEscrowUpdate
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb49d50ee7c529174fe4c5546efd7de1727892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702795"
---
# <a name="jetescrowupdate-function"></a>Функция JetEscrowUpdate


_**Применимо к:** Windows | Windows Server_

## <a name="jetescrowupdate-function"></a>Функция JetEscrowUpdate

Функция **жетескровупдате** выполняет атомарную операцию сложения для одного столбца. Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов.

```cpp
    JET_ERR JET_API JetEscrowUpdate(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_COLUMNID columnid,
      __in          void* pv,
      __in          unsigned long cbMax,
      __out_opt     void* pvOld,
      __in          unsigned long cbOldMax,
      __out_opt     unsigned long* pcbOldActual,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*columnid*

Значение *columnid* обновляемого столбца.

*PV*

Указатель на буфер, содержащий слагаемое для столбца.

*кбмакс*

Размер буфера, содержащего слагаемое.

*пволд*

Выходной буфер, получающий текущее значение столбца, хранимое в базе данных (управление версиями игнорируется).

*кболдмакс*

Максимальный размер выходного буфера, который будет принимать текущее значение столбца. В настоящее время поддерживается только JET_coltypLong, поэтому размер буфера должен составлять 4 байт или 0 байт. Если *пволд* имеет значение null, то *кболдмакс* должен быть равен 0.

*пкболдактуал*

Получает фактический объем данных необработанных значений, полученных в выходном буфере.

*грбит*

Группа битов, задающая ноль или более следующих параметров.

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
<td><p>JET_bitEscrowNoRollback</p></td>
<td><p>Даже если в сеансе, выполняющем Депонированное обновление, выполняется откат транзакций, это обновление не будет отменено. Обратите внимание, что так как записи журнала не могут быть записаны на диск, последние депонированные обновления, выполненные с помощью этого флага, могут быть утрачены в случае сбоя.</p></td>
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
<td><p>JET_errAlreadyPrepared</p></td>
<td><p>У курсора есть обновление, подготовленное с помощью <a href="gg269339(v=exchg.10).md">жетпрепареупдате</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidBufferSize</p></td>
<td><p>Передан недопустимый размер буфера. В настоящее время поддерживается только JET_coltypLong, поэтому размер буфера должен составлять 4 байта.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidOperation</p></td>
<td><p>Указан недопустимый столбец. Столбец должен быть создан с указанным JET_bitColumnEscrowUpdate. Только фиксированные столбцы JET_coltypLong можно указать как подобновляемые.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Для обновления столбца курсор должен находиться в записи.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInTransaction</p></td>
<td><p>Депонированные обновления могут выполняться только сеансами транзакции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errPermissionDenied</p></td>
<td><p>Курсор не может быть доступен только для чтения и обновлять запись.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Один и тот же сеанс нельзя использовать одновременно из нескольких потоков. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTransReadOnly</p></td>
<td><p>Для обновления записи сеанс должен иметь разрешения на запись.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errWriteConflict</p></td>
<td><p>Ошибка, возвращенная при запросе конфликтующего обновления.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Как правило, если два сеанса пытаются одновременно обновить запись, второй сеанс получит JET_errWriteConflict ошибку, если только сеансы не будут полностью сериализованы. Чтобы сериализовать два сеанса, которые обновляют одну и ту же запись, второй сеанс должен начать свою транзакцию после того, как первая транзакция зафиксирует свою транзакцию. Дополнительные сведения см. в разделе [жетбегинтрансактион](./jetbegintransaction-function.md) .

Несколько столбцов в одной записи можно условно обновить. Обновления не влияют друг на друга.

Только операции **жетескровупдате** совместимы друг с другом. Если два разных сеанса пытаются подготовить обновления или удалить одну и ту же запись, будет создан конфликт записи.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p></p></th>
<th><p>Сеанс б<br />
<strong>жетескровупдате</strong></p></th>
<th><p><a href="gg269339(v=exchg.10).md">жетпрепареупдате</a></p></th>
<th><p><a href="gg269315(v=exchg.10).md">жетделете</a></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><strong>жетескровупдате</strong></p></td>
<td><p>JET_errSuccess</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><a href="gg269288(v=exchg.10).md">жетупдате</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
<tr class="odd">
<td><p>Сеанс а</p></td>
<td><p><a href="gg269315(v=exchg.10).md">жетделете</a></p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
<td><p>JET_errWriteConflict</p></td>
</tr>
</tbody>
</table>


Для депонированных операций используется версия и они отменяются с помощью [жетроллбакк](./jetrollback-function.md) (если не указано JET_bitEscrowNoRollback). **Жетескровупдате** возвращает необработанное значение столбца, хранящегося в базе данных, так как приложению может потребоваться выполнить определенное действие при попадании в значение Sentinel. [Жетретриевеколумн](./jetretrievecolumn-function.md) возвращает правильное представление столбца с версиями, игнорируя обновления, сделанные параллельными сеансами.

При наличии двух сеансов, работающих в одном столбце одной и той же записи, можно увидеть, как это работает. Предположим, что столбец начинается со значения 0.

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Сеанс</p></th>
<th><p>Операция</p></th>
<th><p>Сохраненное значение</p></th>
<th><p>Возвращаемое значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект</p></td>
<td><p><a href="gg294083(v=exchg.10).md">жетбегинтрансатион</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Объект</p></td>
<td><p><a href="gg294083(v=exchg.10).md">жетбегинтрансатион</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>Объект</p></td>
<td><p><strong>Жетескровупдате</strong> (4)</p></td>
<td><p>4</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>Объект</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>4</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg294083(v=exchg.10).md">жетбегинтрансактион</a></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><strong>Жетескровупдате</strong> (3)</p></td>
<td><p>7</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="odd">
<td><p>A</p></td>
<td><p><strong>Жетескровупдате</strong> (2)</p></td>
<td><p>9</p></td>
<td><p>7</p></td>
</tr>
<tr class="even">
<td><p>Объект</p></td>
<td><p><strong>Жетескровупдате</strong> (-7)</p></td>
<td><p>2</p></td>
<td><p>9</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>A</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
<tr class="odd">
<td><p>B</p></td>
<td><p><a href="gg269273(v=exchg.10).md">жетроллбакк</a></p></td>
<td><p>-1</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Объект</p></td>
<td><p><a href="gg269198(v=exchg.10).md">жетретриевеколумн</a></p></td>
<td><p></p></td>
<td><p>-1</p></td>
</tr>
</tbody>
</table>


Не рекомендуется заменять запись в той же транзакции, которая выполняет депонированные обновления записи. В частности, если обновление записи подготовлено с помощью одной [JET_TABLEID](./jet-tableid.md) и для депонирования обновления записи используется другая [JET_TABLEID](./jet-tableid.md) , то при вызове [жетупдате](./jetupdate-function.md) будет утрачено значение «условно Обновлено». Это происходит, даже если во время обновления не был задан депонированный столбец.

Если столбец с подобновляемым значением имеет нулевое значение, можно запустить специальное поведение. Такое поведение происходит только в том случае, если операция **жетескровупдате** приводит к тому, что столбец имеет нулевое значение. Действие не происходит немедленно, но происходит после транзакции, которая привела к тому, что столбец имеет нулевое значение фиксаций. Столбец по-прежнему должен иметь нулевое значение (т. е. Если другие сеансы не изменили столбец). Если столбец был создан с помощью JET_bitColumnDeleteOnZero, то запись, содержащая столбец, будет удалена. Если столбец был создан с JET_bitColumnFinalize то будет выдан обратный вызов. Сбой может привести к тому, что эти действия не будут выполняться, но оперативное обслуживание (с помощью функции [жетдефрагмент](./jetdefragment-function.md) ) будет правильно повторять действия.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетбегинтрансактион](./jetbegintransaction-function.md)  
[жетдефрагмент](./jetdefragment-function.md)  
[жетпрепареупдате](./jetprepareupdate-function.md)  
[жетретриевеколумн](./jetretrievecolumn-function.md)  
[жетроллбакк](./jetrollback-function.md)  
[жетстопсервице](./jetstopservice-function.md)  
[жетупдате](./jetupdate-function.md)
