---
description: 'Дополнительные сведения: обработка ошибок констант'
title: Константы обработки ошибок
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab59a8e0c721558e5c056d25798c5d1273bd86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703239"
---
# <a name="error-handling-constants"></a>Константы обработки ошибок


_**Применимо к:** Windows | Windows Server_

## <a name="error-handling-constants"></a>Константы обработки ошибок

Для задания диапазона [JET_paramExceptionAction](./error-handling-parameters.md) системных параметров используются следующие константы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа/значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ExceptionMsgBox<br />
0x0001</p></td>
<td><p>Отображает окно сообщения при возникновении исключения.</p></td>
</tr>
<tr class="even">
<td><p>JET_ExceptionNone<br />
0x0002</p></td>
<td><p>Не выполняет никаких действий при возникновении исключения.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Требования

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
</tbody>
</table>


### <a name="see-also"></a>См. также:

[Параметры обработки ошибок](./error-handling-parameters.md)
