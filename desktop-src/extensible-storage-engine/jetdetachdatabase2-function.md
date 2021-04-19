---
description: Дополнительные сведения о функции JetDetachDatabase2
title: Функция JetDetachDatabase2
TOCTitle: JetDetachDatabase2 Function
ms:assetid: d79c06ab-d470-4d83-a0f4-fa0f4e5f80b3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294105(v=EXCHG.10)
ms:contentKeyID: 32765720
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabase2
- JetDetachDatabase2W
- JetDetachDatabase2A
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7688df9a18d8e13a85e4a244fc8502a7147e154f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693350"
---
# <a name="jetdetachdatabase2-function"></a>Функция JetDetachDatabase2


_**Применимо к:** Windows | Windows Server_

## <a name="jetdetachdatabase2-function"></a>Функция JetDetachDatabase2

Функция **JetDetachDatabase2** освобождает файл базы данных, который ранее был присоединен к сеансу базы данных.

**Windows XP:**  **JetDetachDatabase2** появился в Windows XP.

```cpp
    JET_ERR JET_API JetDetachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Параметры

*сесид*

Контекст сеанса базы данных, используемый для вызова API.

*сзфиленаме*

Имя базы данных для отсоединения. Если *сзфиленаме* имеет **значение NULL** или является пустой строкой, все базы данных, прикрепленные к *сесид* , будут отсоединены.

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
<td><p>JET_bitForceCloseAndDetach</p></td>
<td><p>Принудительное закрытие и отсоединение базы данных. Если JET_bitForceCloseAndDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitForceDetach</p></td>
<td><p>Принудительное отключение базы данных. Если JET_bitForceDetach не поддерживается, будет возвращено JET_errForceDetachNotAllowed.</p></td>
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
<td><p>JET_errBackupInProgress</p></td>
<td><p>База данных архивируется и не может быть отсоединена.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errDatabaseInUse</p></td>
<td><p>База данных открыта с помощью <a href="gg269299(v=exchg.10).md">жетопендатабасе</a>. Перед отсоединением базы данных должны быть закрыты.</p></td>
</tr>
<tr class="even">
<td><p>JET_errDatabaseNotFound</p></td>
<td><p>База данных не была присоединена ранее (см. <a href="gg294074(v=exchg.10).md">жетаттачдатабасе</a> или <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errForceDetachNotAllowed</p></td>
<td><p>JET_bitForceDetach не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInTransaction</p></td>
<td><p>Предпринята попытка отсоединить базу данных во время транзакции.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Если присоединенная база данных была открыта (с [жетаттачдатабасе](./jetattachdatabase-function.md)), ее необходимо закрыть с помощью [жетклоседатабасе](./jetclosedatabase-function.md) перед отсоединением.

Только Windows 2000. базы данных, которые не были отсоединены до вызова [жеттерм](./jetterm-function.md) , будут автоматически присоединены при следующем вызове [жетинит](./jetinit-function.md) .

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
<td><p>Реализуется как <strong>JetDetachDatabase2W</strong> (Юникод) и <strong>JetDetachDatabase2A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[жетаттачдатабасе](./jetattachdatabase-function.md)  
[JetAttachDatabase2](./jetattachdatabase2-function.md)  
[жетклоседатабасе](./jetclosedatabase-function.md)  
[жеткреатедатабасе](./jetcreatedatabase-function.md)  
[JetCreateDatabase2](./jetcreatedatabase2-function.md)  
[жетинит](./jetinit-function.md)  
[жетопендатабасе](./jetopendatabase-function.md)  
[жеттерм](./jetterm-function.md)
