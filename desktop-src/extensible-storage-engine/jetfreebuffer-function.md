---
description: Дополнительные сведения о функции Жетфрибуффер
title: Функция Жетфрибуффер
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fe638e2aab1d37324a6fd6bf477a578f02b9ac58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702927"
---
# <a name="jetfreebuffer-function"></a>Функция Жетфрибуффер


_**Применимо к:** Windows | Windows Server_

## <a name="jetfreebuffer-function"></a>Функция Жетфрибуффер

Функция **жетфрибуффер** освобождает память, выделенную вызовом ядра СУБД.

**Windows XP: жетфрибуффер** появился в Windows XP.

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a>Параметры

*пббуф*

Указатель на область памяти, которая была ранее выделена вызовом ядра СУБД. **Значение NULL** допустимо и будет игнорироваться.

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
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Не определено поведение для передачи памяти, которая не была выделена ядром СУБД в для *пббуф*.

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
[жетжетинстанцеинфо](./jetgetinstanceinfo-function.md)
