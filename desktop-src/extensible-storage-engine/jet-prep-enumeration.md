---
description: 'Дополнительные сведения: перечисление JET_prep'
title: Перечисление JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693434"
---
# <a name="jet_prep-enumeration"></a>Перечисление JET_prep

Типы обновления для Жетпрепареупдате.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a>Члены

<table>
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
<td>Вставить</td>
<td>Этот флаг заставляет курсор подготовиться к вставке новой записи. Все данные инициализируются в состояние по умолчанию для записи. Если в таблице есть столбец с автоматическим приращением, то эта запись назначается новому значению независимо от того, завершилось ли обновление в конечном итоге успешно, завершается сбоем или отменяется.</td>
</tr>
<tr class="even">
<td></td>
<td>Заменить</td>
<td>Этот флаг заставляет курсор подготовиться к замене текущей записи. Если таблица имеет столбец Version, то для столбца Version устанавливается следующее значение в последовательности. Если это обновление не завершено, то значение версии в записи не изменится. Для записи была снята блокировка обновления, чтобы другие сеансы не обновляли эту запись до завершения этого сеанса.</td>
</tr>
<tr class="odd">
<td></td>
<td>Отменить</td>
<td>Этот флаг приводит к тому, что Жетпрепареупдате отменяет обновление для данного курсора.</td>
</tr>
<tr class="even">
<td></td>
<td>реплаценолокк</td>
<td>Этот флаг аналогичен JET_prepReplace, но блокировка не предпринимается, чтобы другие сеансы не обновляли эту запись. Вместо этого этот сеанс может получить JET_errWriteConflict при вызове Жетупдате для завершения обновления.</td>
</tr>
<tr class="odd">
<td></td>
<td>инсерткопи</td>
<td>Этот флаг заставляет курсор подготовиться к вставке копии существующей записи. При использовании этого параметра должна существовать текущая запись. Начальное состояние новой записи копируется из текущей записи. Длинные значения, хранящиеся за пределами записи, практически копируются.</td>
</tr>
<tr class="even">
<td></td>
<td>инсерткопиделетеоригинал</td>
<td>Этот флаг заставляет курсор подготовиться к вставке той же записи, а также к удалению или исходной записи. Он используется в случаях, когда первичный ключ изменился.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
