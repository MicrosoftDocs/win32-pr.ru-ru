---
description: Дополнительные сведения о функции Жетжетлс
title: Функция Жетжетлс
TOCTitle: JetGetLS Function
ms:assetid: 411baf34-d167-4633-81af-be4886f4a646
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269234(v=EXCHG.10)
ms:contentKeyID: 32765536
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetLS
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7a89cf4e20798a2c412ba6eb39b08f99a60a464
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712869"
---
# <a name="jetgetls-function"></a>Функция Жетжетлс


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetls-function"></a>Функция Жетжетлс

Функция **жетжетлс** позволяет приложению получить описатель контекста, известный как локальное хранилище, связанное с курсором, или с таблицей, связанной с этим курсором. Этот обработчик контекста должен быть ранее задан с помощью [жетсетлс](./jetsetls-function.md). **Жетжетлс** также можно использовать для одновременной выборки текущего контекста для курсора или таблицы и сброса дескриптора контекста.

**Windows XP: жетжетлс** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_LS* pls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*pls*

Выходной буфер, который получает обработчик контекста, который в текущий момент связан с курсором или таблицей.

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
<td><p>JET_bitLSCursor</p></td>
<td><p>Указывает, что должен быть получен обработчик контекста, связанный с заданным курсором.</p>
<p>Если не указано ни JET_bitLSCursor, ни JET_bitLSTable, предполагается JET_bitLSCursor.</p>
<p>Этот параметр нельзя использовать с JET_bitLSTable. Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSTable</p></td>
<td><p>Указывает, что должен быть получен обработчик контекста, связанный с таблицей, содержащей данный курсор. Использование этого параметра с JET_bitLSCursor недопустимо. Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Указывает, что обработчик контекста для выбранного объекта должен быть сброшен в JET_LSNil. Текущее значение маркера контекста возвращается в выходном буфере.</p></td>
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
<td><p>Невозможно выполнить операцию, так как все действия в экземпляре, связанном с сеансом, были прекращены в результате вызова <a href="gg269240(v=exchg.10).md">жетстопсервице</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных.</p>
<p>Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Один из запрошенных параметров недопустим, используется недопустимым образом или не реализован.</p>
<p>Это может произойти для <strong>жетжетлс</strong> , если заданы оба JET_bitLSCursor и JET_bitLSTable.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSNotSet</p></td>
<td><p>Не удалось вернуть контекстный маркер, так как с запрошенным объектом сейчас не связан ни один обработчик контекста.</p>
<p><strong>Примечание  </strong> . Эта ошибка не возвращается, если указан JET_bitLSReset, но с запрошенным объектом не связан ни один маркер контекста.</p></td>
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
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном завершении маркер контекста был успешно получен из запрошенного объекта. Если указан JET_bitLSReset, то этот маркер контекста также был успешно удален из объекта. Изменение состояния базы данных не выполняется.

В случае сбоя не произошло изменение состояния запрошенного объекта. Изменение состояния базы данных не выполняется.

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
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетсетлс](./jetsetls-function.md)
