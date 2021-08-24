---
description: Дополнительные сведения о перечислении Обжектинфофлагс
title: Перечисление Обжектинфофлагс
TOCTitle: ObjectInfoFlags enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ObjectInfoFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.objectinfoflags(v=EXCHG.10)
ms:contentKeyID: 39515824
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.System
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableDerived
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.None
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableFixedDDL
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableNoFixedVarColumnsInDerivedTables
- Microsoft.Isam.Esent.Interop.ObjectInfoFlags.TableTemplate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 06cd7cecaa536106f70cc469e3b690a46bee8301fe2d1142bc3fa1ff2c045346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780274"
---
# <a name="objectinfoflags-enumeration"></a>Перечисление Обжектинфофлагс

Флаги для объектов ESENT (таблиц). Используется в [JET_OBJECTINFO](./jet-objectinfo-class.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ObjectInfoFlags
'Usage
Dim instance As ObjectInfoFlags
```

``` csharp
[FlagsAttribute]
public enum ObjectInfoFlags
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
<td>Система</td>
<td>Объект предназначен только для внутреннего использования.</td>
</tr>
<tr class="odd">
<td></td>
<td>таблефикседддл</td>
<td>Таблица DDL таблицы исправлена.</td>
</tr>
<tr class="even">
<td></td>
<td>таблетемплате</td>
<td>DDL таблицы является наследуемым.</td>
</tr>
<tr class="odd">
<td></td>
<td>табледеривед</td>
<td>DDL таблицы наследуется из таблицы шаблонов.</td>
</tr>
<tr class="even">
<td></td>
<td>табленофикседварколумнсиндериведтаблес</td>
<td>Фиксированные или переменные столбцы в производных таблицах (чтобы в будущем можно было добавить в шаблон фиксированные или переменные столбцы). Используется в сочетании с Таблетемплате.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
