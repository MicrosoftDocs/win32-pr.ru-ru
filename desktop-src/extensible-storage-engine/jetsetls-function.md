---
description: Дополнительные сведения о функции Жетсетлс
title: Функция JetSetLS
TOCTitle: JetSetLS Function
ms:assetid: 4fc77e09-7173-42e8-9dfd-9a8d8de2fb9b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269243(v=EXCHG.10)
ms:contentKeyID: 32765545
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetLS
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae1c68a039c11cd8a3f9b1299494c5057513caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540767"
---
# <a name="jetsetls-function"></a>Функция JetSetLS


_**Применимо к:** Windows | Windows Server_

## <a name="jetsetls-function"></a>Функция JetSetLS

Функция **жетсетлс** позволяет приложению связать описатель контекста, известный как локальное хранилище, с курсором или с таблицей, связанной с этим курсором. Этот обработчик контекста может использоваться приложением для хранения вспомогательных данных, связанных с курсором или таблицей. После этого приложение будет уведомлено с помощью обратного вызова времени выполнения, когда должен быть освобожден обработчик контекста. Это дает возможность связать динамически выделенное состояние с курсором или таблицей.

**Windows XP:**  **Жетсетлс** появился в Windows XP.

```cpp
    JET_ERR JET_API JetSetLS(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_LS ls,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, используемый для этого вызова.

*TableID*

Курсор, используемый для этого вызова.

*ls*

Контекстный обработчик, связываемый с курсором или таблицей.

Если указано JET_bitLSReset, фактическое значение этого параметра игнорируется, и используется JET_LSNil.

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих значений.

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
<td><p>Этот параметр указывает, что маркер контекста должен быть связан с данным курсором.</p>
<p>Если не указано ни JET_bitLSCursor, ни JET_bitLSTable, предполагается JET_bitLSCursor.</p>
<p>Использование этого параметра с JET_bitLSTable недопустимо. Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSReset</p></td>
<td><p>Этот параметр указывает, что указанный обработчик контекста должен игнорироваться, а контекстный маркер для выбранного объекта должен быть сброшен в JET_LSNil.</p>
<p>Важно отметить, что это действие не приведет к обратному вызову для очистки предыдущего значения маркера контекста для выбранного объекта. Правильная очистка предыдущего маркера контекста может быть достигнута с помощью <a href="gg269234(v=exchg.10).md">жетжетлс</a> с JET_bitLSReset. Дополнительные сведения см. в разделе <a href="gg269234(v=exchg.10).md">жетжетлс</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Этот параметр указывает, что маркер контекста должен быть связан с таблицей, связанной с данным курсором.</p>
<p>Использование этого параметра с JET_bitLSCursor недопустимо. Операция завершится ошибкой с JET_errInvalidgrbit при попытке.</p></td>
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
<td><p>JET_errInvalidgrbit</p></td>
<td><p>Один из запрошенных параметров недопустим, используется неправильно или не реализован. Это может произойти для <strong>жетсетлс</strong> , если одновременно указаны значения JET_bitLSCursor и JET_bitLSTable.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Невозможно выполнить операцию, поскольку экземпляр, связанный с сеансом, обнаружил неустранимую ошибку, которая требует, чтобы доступ ко всем данным был отозван для защиты целостности этих данных. Эта ошибка будет возвращена только Windows XP и более поздних версий.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLSAlreadySet</p></td>
<td><p>Данный обработчик контекста не может быть связан с запрошенным объектом, так как с ним уже связан обработчик контекста.</p></td>
</tr>
<tr class="even">
<td><p>JET_errLSCallbackNotSpecified</p></td>
<td><p>Данный обработчик контекста не может быть связан с запрошенным объектом, так как обратный вызов времени выполнения не был настроен для экземпляра, связанного с сеансом.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Невозможно выполнить операцию, так как экземпляр, связанный с сеансом, еще не инициализирован.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как в экземпляре, связанном с сеансом, выполняется операция восстановления.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Невозможно выполнить операцию, так как выполняется завершение работы экземпляра, связанного с сеансом.</p></td>
</tr>
</tbody>
</table>


При успешном выполнении указанный обработчик контекста успешно связан с запрошенным объектом. Изменение состояния базы данных не выполняется.

В случае сбоя не произошло изменение состояния запрошенного объекта. Изменение состояния базы данных не выполняется.

#### <a name="remarks"></a>Комментарии

Локальное хранилище для курсора или таблицы следует просматривать как временный кэш. Приложение должно сначала попытаться получить маркер контекста с помощью [жетжетлс](./jetgetls-function.md). Если значение не задано (то есть JET_LSNil), приложение должно создать новый контекст и загрузить его в кэш с помощью **жетсетлс**. Приложение может очистить кэш с помощью вызова [жетжетлс](./jetgetls-function.md) с JET_bitLSReset. Если ядро СУБД удаляет кэш, будет создан обратный вызов времени выполнения, чтобы дать приложению возможность очистить этот контекст. Тип обратного вызова будет JET_cbtypFreeCursorLS для обработчика контекста, связанного с курсором, и JET_cbtypFreeTableLS для обработчика контекста, связанного с таблицей. В любом случае маркер контекста будет передан как pvArg1. Дополнительные сведения см. в разделе [JET_CALLBACK](./jet-callback-callback-function.md) .

Необходимо правильно настроить обратный вызов среды выполнения для экземпляра, связанного с данным сеансом, прежде чем можно будет использовать локальное хранилище. Этот обратный вызов можно задать с помощью [жетсетсистемпараметер](./jetsetsystemparameter-function.md) с [JET_paramRuntimeCallback](./callback-parameters.md). Дополнительные сведения см. в статье [жетсетсистемпараметер](./jetsetsystemparameter-function.md) и [JET_paramRuntimeCallback](./callback-parameters.md) в разделе Системные параметры.

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

[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_LS](./jet-ls.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетжетлс](./jetgetls-function.md)  
[жетсетсистемпараметер](./jetsetsystemparameter-function.md)  
[Системные параметры](./extensible-storage-engine-system-parameters.md)
