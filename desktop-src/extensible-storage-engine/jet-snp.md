---
description: 'Дополнительные сведения: JET_SNP'
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: 35ffb2d17c01c3d157fc7ed66a320529f844ff9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662163"
---
# <a name="jet_snp"></a>JET_SNP


_**Применимо к:** Windows | Windows Server_

## <a name="jet_snp"></a>JET_SNP

**JET_SNP** группа констант описывает тип операции, для которой необходимо получить сведения о ходе выполнения. Эти константы используются в качестве параметра *SNP* функции обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

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
<td><p>JET_snpRepair<br />
2</p></td>
<td><p>Обратный вызов предназначен для операции исправления.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpCompact<br />
4</p></td>
<td><p>Обратный вызов предназначен для дефрагментации базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpRestore<br />
8</p></td>
<td><p>Обратный вызов предназначен для операции восстановления.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpBackup<br />
9</p></td>
<td><p>Обратный вызов предназначен для операции резервного копирования.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgrade<br />
10</p></td>
<td><p>Не поддерживается.</p>
<p><strong>Windows 2000:</strong>  Обратный вызов предназначен для операции обновления формата базы данных.</p></td>
</tr>
<tr class="even">
<td><p>JET_snpScrub<br />
11</p></td>
<td><p>Обратный вызов предназначен для операции обнуления (т. е. очистки) базы данных.</p>
<p><strong>Windows server 2003 и windows 2000 Server:</strong>  Не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>JET_snpUpgradeRecordFormat<br />
12</p></td>
<td><p>Обратный вызов предназначен для процесса обновления формата записей всех страниц базы данных.</p>
<p><strong>Windows server 2003 и windows 2000 Server:</strong>  Не поддерживается.</p></td>
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

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
