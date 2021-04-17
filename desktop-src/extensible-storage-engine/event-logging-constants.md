---
description: 'Дополнительные сведения: константы ведения журнала событий'
title: Константы ведения журнала событий
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
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
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702430"
---
# <a name="event-logging-constants"></a>Константы ведения журнала событий


_**Применимо к:** Windows | Windows Server_

## <a name="event-logging-constants"></a>Константы ведения журнала событий

Следующие константы указывают уровень детализации для сообщений журнала событий для системного параметра [JET_ParamEventLoggingLevel](./event-log-parameters.md) .

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
<td><p>JET_EventLoggingDisable<br />
0</p></td>
<td><p>Отключает ведение журнала событий.</p></td>
</tr>
<tr class="even">
<td><p>JET_EventLoggingLevelMax<br />
100</p></td>
<td><p>Задает максимальный уровень, используемый для журналов событий, который в настоящее время 100 символов.</p></td>
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

[Параметры журнала событий](./event-log-parameters.md)
