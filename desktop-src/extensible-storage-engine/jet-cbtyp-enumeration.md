---
description: 'Дополнительные сведения: перечисление JET_cbtyp'
title: Перечисление JET_cbtyp
TOCTitle: JET_cbtyp enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_cbtyp
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_cbtyp(v=EXCHG.10)
ms:contentKeyID: 39511758
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeCursorLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.FreeTableLS
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Null
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterReplace
- Microsoft.Isam.Esent.Interop.JET_cbtyp
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterDelete
- Microsoft.Isam.Esent.Interop.JET_cbtyp.OnlineDefragCompleted
- Microsoft.Isam.Esent.Interop.JET_cbtyp.AfterInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.BeforeInsert
- Microsoft.Isam.Esent.Interop.JET_cbtyp.Finalize
- Microsoft.Isam.Esent.Interop.JET_cbtyp.UserDefinedDefaultValue
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3d2e545fea9c1942dc09df82eb93eafa1d3e4e89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673405"
---
# <a name="jet_cbtyp-enumeration"></a>Перечисление JET_cbtyp

Тип отчета о ходе выполнения.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration JET_cbtyp
'Usage
Dim instance As JET_cbtyp
```

``` csharp
[FlagsAttribute]
public enum JET_cbtyp
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
<td>NULL</td>
<td>Этот обратный вызов зарезервирован и всегда считается недопустимым.</td>
</tr>
<tr class="even">
<td></td>
<td>Завершение</td>
<td>Заключительный столбец имеет нулевое значение.</td>
</tr>
<tr class="odd">
<td></td>
<td>бефореинсерт</td>
<td>Этот обратный вызов выполняется непосредственно перед вставкой новой записи в таблицу с помощью вызова Жетупдате.</td>
</tr>
<tr class="even">
<td></td>
<td>афтеринсерт</td>
<td>Этот обратный вызов выполняется сразу после вставки новой записи в таблицу с помощью вызова Жетупдате, но до возврата Жетупдате.</td>
</tr>
<tr class="odd">
<td></td>
<td>бефоререплаце</td>
<td>Этот обратный вызов выполняется непосредственно перед существующей записью в таблице, измененной с помощью вызова Жетупдате.</td>
</tr>
<tr class="even">
<td></td>
<td>афтерреплаце</td>
<td>Этот обратный вызов выполняется сразу после изменения существующей записи в таблице с помощью вызова Жетупдате, но до Жетупдате возврата.</td>
</tr>
<tr class="odd">
<td></td>
<td>BeforeDelete</td>
<td>Этот обратный вызов выполняется непосредственно перед удалением существующей записи в таблице путем вызова Жетделете.</td>
</tr>
<tr class="even">
<td></td>
<td>афтерделете</td>
<td>Этот обратный вызов выполняется сразу после удаления существующей записи в таблице путем вызова Жетделете.</td>
</tr>
<tr class="odd">
<td></td>
<td>усердефинеддефаултвалуе</td>
<td>Этот обратный вызов выполняется, когда подсистеме требуется получить определенное пользователем значение столбца из приложения. Этот обратный вызов по сути является ограниченной реализацией Жетретриевеколумн, которая оценивается приложением. Для определяемого пользователем значения по умолчанию может быть возвращено не более одного значения столбца.</td>
</tr>
<tr class="even">
<td></td>
<td>онлинедефрагкомплетед</td>
<td>Этот обратный вызов происходит, когда оперативная дефрагментация базы данных, инициированной Жетдефрагмент, была остановлена из-за завершения процесса или превышения предельного значения времени.</td>
</tr>
<tr class="odd">
<td></td>
<td>фрикурсорлс</td>
<td>Этот обратный вызов происходит, когда приложению необходимо очистить контекстный обработчик для локального хранилища, связанного с курсором, который освобождается ядром СУБД. Дополнительные сведения см. в разделе Жетсетлс. Делегат для этой причины обратного вызова настраивается средствами Жетсетсистемпараметер с JET_paramRuntimeCallback.</td>
</tr>
<tr class="even">
<td></td>
<td>фритаблелс</td>
<td>Этот обратный вызов будет выполняться в результате необходимости в приложении очистить контекстный обработчик для локального хранилища, связанного с таблицей, которая освобождается ядром СУБД. Дополнительные сведения см. в разделе Жетсетлс. Делегат для этой причины обратного вызова настраивается средствами Жетсетсистемпараметер с JET_paramRuntimeCallback.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
