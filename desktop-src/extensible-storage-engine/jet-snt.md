---
description: 'Дополнительные сведения: JET_SNT'
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 5d1d4fa75c8a41528e9868bc94fa638042d01cff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262868"
---
# <a name="jet_snt"></a>JET_SNT


_**Применимо к:** Windows | Windows Server_

## <a name="jet_snt"></a>JET_SNT

[JET_SNT]() группа констант описывает точки выполнения операции, сведения о которой запрашиваются при вызове функции обратного вызова [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md) .

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
<td><p>JET_sntBegin<br />
5</p></td>
<td><p>Начало операции</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRequirements<br />
7</p></td>
<td><p>Не поддерживается.</p>
<p><strong>Сервер Windows 2000:</strong>  Операция запущена. В этом случае последний параметр функции обратного вызова должен быть допустимым указателем на <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> структуру, указывающую общее количество единиц для выполнения.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntProgress<br />
0</p></td>
<td><p>Число завершенных единиц и количество единиц, которые еще не были выполнены. Эти сведения возвращаются в элементах структуры <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_sntComplete<br />
6</p></td>
<td><p>Завершение операции.</p></td>
</tr>
<tr class="odd">
<td><p>JET_sntFail<br />
3</p></td>
<td><p>Сбой операции.</p></td>
</tr>
<tr class="even">
<td><p>JET_sntRecoveryStep<br />
8</p></td>
<td><p>Управление восстановлением операции.</p>
<div class="alert">

> [!NOTE]
> <P>Это значение неприменимо к версиям операционной системы Windows, начиная с Windows 8.</P>


</div></td>
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
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
