---
description: Дополнительные сведения о функции Жетидле
title: Функция Жетидле
TOCTitle: JetIdle Function
ms:assetid: 77e036eb-b894-4ff7-b14f-1564bf21873f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269301(v=EXCHG.10)
ms:contentKeyID: 32765593
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetIdle
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0adf2845997b97eb93b39b779da4ad19bb9ee066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911439"
---
# <a name="jetidle-function"></a>Функция Жетидле


_**Применимо к:** Windows | Windows Server_

## <a name="jetidle-function"></a>Функция Жетидле

Функция **жетидле** уничтожена, и ее следует использовать только в целях тестирования. **Жетидле** можно использовать для выполнения задач очистки после простоя или для проверки состояния хранилища версий в ESE.

```cpp
    JET_ERR JET_API JetIdle(
      __in          JET_SESID sesid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Сеанс, который будет использоваться для этого вызова.

*грбит*

Группа битов, содержащая параметры, которые должны использоваться для этого вызова, включая ноль или более следующих битов:

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
<td><p>JET_bitIdleCompact</p></td>
<td><p>Запускает очистку хранилища версий.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitIdleFlushBuffers</p></td>
<td><p>Зарезервировано для последующего использования. Если этот флаг указан, API возвратит JET_errInvalidgrbit.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitIdleStatus</p></td>
<td><p>Возвращает JET_wrnIdleFull, если хранилище версий больше половины места.</p></td>
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
<td><p>JET_errInvalidParameter</p></td>
<td><p>Недопустимый параметр <em>грбит</em> , предоставленный API.</p></td>
</tr>
</tbody>
</table>


Если эта функция завершится с ошибкой, будет активирована соответствующая операция или код ошибки, указывающий, насколько заполнено хранилище версий в зависимости от предоставленной *грбит* .

Если эта функция завершается ошибкой, запрошенная операция не будет выполнена успешно.

#### <a name="remarks"></a>Комментарии

Хранилище версий поддерживает механизм изоляции моментальных снимков ESE. Если хранилище версий больше половины, программа может закрыть долго выполняющиеся транзакции. Если долго выполняющаяся транзакция приводит к исчерпанию хранилища версий, ESE прекращает разрешение операций записи в базу данных.

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
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[жеткоммиттрансактион](./jetcommittransaction-function.md)
