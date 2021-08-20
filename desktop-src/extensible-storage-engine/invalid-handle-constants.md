---
description: 'Дополнительные сведения: недопустимые константы Handle'
title: Недопустимые константы Handle
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 1b6b87a75f8f0afc8a2f84c6f248c8b071ee5bb5682b2006772df118a0113fde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118076414"
---
# <a name="invalid-handle-constants"></a>Недопустимые константы Handle


_**Применимо к:** Windows | Windows Сервером_

## <a name="invalid-handle-constants"></a>Недопустимые константы Handle

Следующие константы указывают недопустимые дескрипторы для различных аспектов ESE.

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
<td><p>JET_instanceNil<br />
(~ (JET_INSTANCE) 0)</p></td>
<td><p>Недопустимый обработчик для экземпляра базы данных.<br />
<strong>Windows XP:</strong> появилось в Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_sesidNil<br />
(~ (JET_SESID) 0)</p></td>
<td><p>Недопустимый обработчик для идентификатора сеанса.</p></td>
</tr>
<tr class="odd">
<td><p>JET_tableidNil<br />
(~ (JET_TABLEID) 0)</p></td>
<td><p>Недопустимый обработчик для идентификатора таблицы.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitNil<br />
((JET_GRBIT) 0)</p></td>
<td><p>Недопустимый маркер для группы битов.</p></td>
</tr>
<tr class="odd">
<td><p>JET_LSNil<br />
(~ (JET_LS) 0)</p></td>
<td><p>недопустимый обработчик для локального служба хранилища.</p></td>
</tr>
<tr class="even">
<td><p>JET_dbidNil<br />
((JET_DBID) 0xFFFFFFFF)</p></td>
<td><p>Недопустимый обработчик для идентификатора базы данных.</p></td>
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
<td><p>требуется Windows Vista, Windows XP или Windows 2000 Professional.</p></td>
</tr>
<tr class="even">
<td><p><strong>Сервер</strong></p></td>
<td><p>требуется Windows server 2008, Windows server 2003 или сервер Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Header</strong></p></td>
<td><p>Объявлено в ESENT. h.</p></td>
</tr>
</tbody>
</table>

