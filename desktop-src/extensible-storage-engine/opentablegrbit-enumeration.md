---
description: Дополнительные сведения о перечислении Опентаблегрбит
title: Перечисление Опентаблегрбит
TOCTitle: OpenTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.OpenTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.opentablegrbit(v=EXCHG.10)
ms:contentKeyID: 39510721
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass1
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass11
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass14
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Sequential
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass2
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass5
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass8
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyRead
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.DenyWrite
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.PermitDDL
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass10
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass12
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass3
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.NoCache
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass9
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.OpenTableGrbit
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.None
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass4
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass7
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.Preread
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.ReadOnly
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass13
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass15
- Microsoft.Isam.Esent.Interop.OpenTableGrbit.TableClass6
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dfb2d75fc17e37dc669acf1fd84f38c957d467f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683593"
---
# <a name="opentablegrbit-enumeration"></a>Перечисление Опентаблегрбит

Параметры для Жетопентабле.

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration OpenTableGrbit
'Usage
Dim instance As OpenTableGrbit
```

``` csharp
[FlagsAttribute]
public enum OpenTableGrbit
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
<td>Нет</td>
<td>Параметры по умолчанию.</td>
</tr>
<tr class="even">
<td></td>
<td>дениврите</td>
<td>Эту таблицу нельзя открыть для доступа на запись в другом сеансе.</td>
</tr>
<tr class="odd">
<td></td>
<td>дениреад</td>
<td>Эта таблица не может быть открыта для доступа на чтение в другом сеансе.</td>
</tr>
<tr class="even">
<td></td>
<td>ReadOnly</td>
<td>Запрос доступа к таблице только для чтения.</td>
</tr>
<tr class="odd">
<td></td>
<td>Обновляется</td>
<td>Запросите доступ на запись в таблицу.</td>
</tr>
<tr class="even">
<td></td>
<td>пермитддл</td>
<td>Разрешение внесения изменений DDL в таблицу, помеченную как Фикседддл. Этот параметр следует использовать с Дениреад.</td>
</tr>
<tr class="odd">
<td></td>
<td>NoCache</td>
<td>Не кэшировать страницы для этой таблицы.</td>
</tr>
<tr class="even">
<td></td>
<td>Перед чтением</td>
<td>Предоставляет указание о том, что таблица, вероятно, не находится в буферном кэше, и что предварительное чтение может быть полезно для повышения производительности.</td>
</tr>
<tr class="odd">
<td></td>
<td>Последовательные</td>
<td>Предположим, что шаблон последовательного доступа и страницы базы данных с выборкой.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass1</td>
<td>Таблица принадлежит к классу stats 1.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass2</td>
<td>Таблица принадлежит к классу stats 2.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass3</td>
<td>Таблица принадлежит к классу stats 3.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass4</td>
<td>Таблица принадлежит к классу stats 4.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass5</td>
<td>Таблица принадлежит к классу stats класса 5.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass6</td>
<td>Таблица принадлежит к классу stats No 6.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass7</td>
<td>Таблица принадлежит к классу stats 7.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass8</td>
<td>Таблица принадлежит к классу stats класса 8.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass9</td>
<td>Таблица принадлежит к классу stats класса No 9.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass10</td>
<td>Таблица принадлежит к классу stats 10.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass11</td>
<td>Таблица принадлежит к классу stats 11.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass12</td>
<td>Таблица принадлежит к классу stats 12.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass13</td>
<td>Таблица принадлежит к классу stats 13.</td>
</tr>
<tr class="odd">
<td></td>
<td>TableClass14</td>
<td>Таблица принадлежит к классу stats 14.</td>
</tr>
<tr class="even">
<td></td>
<td>TableClass15</td>
<td>Таблица принадлежит к классу stats 15.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
