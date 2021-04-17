---
description: Дополнительные сведения о функции JetGetRecordSize2
title: Функция JetGetRecordSize2
TOCTitle: JetGetRecordSize2 Function
ms:assetid: 803cfb4e-44f3-447a-b642-018e6f2f713f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269314(v=EXCHG.10)
ms:contentKeyID: 32765604
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordSize2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5c68eafaaa53b5b88e6b003bdbafce287035cbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713139"
---
# <a name="jetgetrecordsize2-function"></a>Функция JetGetRecordSize2


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetrecordsize2-function"></a>Функция JetGetRecordSize2

Функция **JetGetRecordSize2** извлекает сведения о размере записи из нужного расположения.

**Windows 7: JetGetRecordSize2** появился в операционной системе Windows 7.

```cpp
    JET_ERR JET_API JetGetRecordSize2(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECSIZE2* precsize,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Определяет контекст сеанса базы данных, который будет использоваться для вызова API.

*TableID*

Определяет таблицу или курсор, которые будут использоваться для вызова API. Курсор должен быть размещен в записи или иметь подготовленное обновление.

*прексизе*

Указатель на выходной буфер для структуры [JET_RECSIZE2](./jet-recsize2-structure.md) .

*грбит*

Это одно или несколько из следующих значений.

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
<td><p>JET_bitRecordSizeInCopyBuffer</p></td>
<td><p>Это Извлекает размер записи, которая находится в буфере копирования, подготовленном для обновления. В противном случае <em>tableid</em> или курсор должны быть расположены в записи, и эта запись будет использоваться.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecordSizeRunningTotal</p></td>
<td><p>Если этот бит указан, то перед заполнением содержимого <a href="gg269174(v=exchg.10).md">JET_RECSIZE2</a> не обнуляются, эффективно выполняя сбор статистики по нескольким просмотренным или обновленным записям.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitRecordSizeLocal</p></td>
<td><p>Это приводит к тому, что API пропускает не внутренние значения long. Например, будет использоваться только локальная запись на странице.</p></td>
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
<td><p>JET_errInvalidGrbit</p></td>
<td><p>Один из запрошенных параметров недопустим или не реализован. Эта ошибка будет возвращена функцией <strong>JetGetRecordSize2</strong> при указании недопустимого <em>грбит</em> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, не был инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable будут возвращаться только операционной системой Windows XP и более поздними версиями Windows.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_errSessionSharingViolation</p></td>
<td><p>Нельзя использовать один сеанс для нескольких потоков одновременно.</p>
<p><strong>Windows XP:  </strong> JET_errInstanceUnavailable будут возвращаться только Windows XP и более поздними версиями Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoCurrentRecord</p></td>
<td><p>Это может произойти, если курсор был размещен неправильно.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRecordDeleted</p></td>
<td><p>Если курсор не был помещен в транзакцию, это может произойти, если другой поток удаляет запись из этого сеанса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Это может быть возвращено, если передано <strong>значение NULL</strong><em>прексизе</em> .</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Размер ключа, накопленного в поле **кбоверхеад** [JET_RECSIZE2](./jet-recsize2-structure.md), зависит от JET_bitRecordSizeInCopyBuffer. Если этот бит указан, размер ключа, накопленный в поле **кбоверхеад** , является полным размером ключа. Если этот бит не используется, размер ключа, накопленный, не будет включать размер, сохраненный из-за сжатия префикса ключа.

#### <a name="requirements"></a>Требования

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Клиент</strong></p></td>
<td><p>Требуется Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Server</strong></p></td>
<td><p>Требуется Windows Server 2008.</p></td>
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
[JET_RECSIZE](./jet-recsize-structure.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)
