---
description: Дополнительные сведения о функции Жетжетинстанцеинфо
title: Функция Жетжетинстанцеинфо
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911443"
---
# <a name="jetgetinstanceinfo-function"></a>Функция Жетжетинстанцеинфо


_**Применимо к:** Windows | Windows Server_

## <a name="jetgetinstanceinfo-function"></a>Функция Жетжетинстанцеинфо

Функция **жетжетинстанцеинфо** извлекает сведения о выполняемых экземплярах.

**Windows XP: жетжетинстанцеинфо** появился в Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Параметры

*пЦинстанцеинфо*

Указатель на буфер, который получит количество элементов, хранящихся в *паинстанцеинфо*.

*паинстанцеинфо*

Указатель на буфер, который получит адрес первого элемента массива структур.

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
<td><p>Один из указанных параметров содержит непредвиденное значение или содержит значение, которое не имеет смысла при объединении со значением другого параметра. Эта ошибка будет возвращена <strong>жетжетинстанцеинфо</strong> в следующих случаях:</p>
<ul>
<li><p><em>пЦинстанцеинфо</em> или <em>паинстанцеинфо</em> имеют значение null.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>Недостаточно памяти для обработки запроса.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Комментарии

Ядро СУБД выделит массив структур [JET_INSTANCE_INFO](./jet-instance-info-structure.md) . Вызывающий объект отвечает за освобождение этой памяти с помощью [жетфрибуффер](./jetfreebuffer-function.md).

Если активных экземпляров нет, **жетжетинстанцеинфо** возвратит JET_errSuccess, а *пЦинстанцеинфо* получит значение 0.

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
<td><p>Реализуется как <strong>жетжетинстанцеинфов</strong> (Юникод) и <strong>жетжетинстанцеинфоа</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>См. также:

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[жетфрибуффер](./jetfreebuffer-function.md)
