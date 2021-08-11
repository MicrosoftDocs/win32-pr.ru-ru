---
description: 'Дополнительные сведения: перечисление JET_SNT'
title: Перечисление JET_SNT
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d25137c9e976d05bd065837fed7753e26e3afdae020499b3388948e11733fd77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118252528"
---
# <a name="jet_snt-enumeration"></a>Перечисление JET_SNT

Тип отчета о ходе выполнения.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a>Члены

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Имя участника</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Начать</td>
<td>Обратный вызов для начала операции.</td>
</tr>
<tr class="even">
<td></td>
<td>Ход выполнения</td>
<td>Обратный вызов для хода выполнения операции.</td>
</tr>
<tr class="odd">
<td></td>
<td>Завершить</td>
<td>Обратный вызов для завершения операции.</td>
</tr>
<tr class="even">
<td></td>
<td>Ошибка</td>
<td>Обратный вызов для сбоя во время операции.</td>
</tr>
<tr class="odd">
<td></td>
<td>рековеристеп</td>
<td>Обратный вызов для управления восстановлением.
<p>используется для внутренней обработки в версиях Windows операционных систем, предшествующих Windows 8. это значение неприменимо к версиям Windows, начиная с Windows 8.</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
