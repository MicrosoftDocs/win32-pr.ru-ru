---
description: Дополнительные сведения о перечислении Упдатегрбит
title: Перечисление Упдатегрбит (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: UpdateGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.updategrbit(v=EXCHG.10)
ms:contentKeyID: 39514938
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.None
- Microsoft.Isam.Esent.Interop.Server2003.UpdateGrbit.CheckESE97Compatibility
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d78d4d4321831d682f9e3da11ab694e7ac1cc5dab05050e86e59e0765099e97e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070481"
---
# <a name="updategrbit-enumeration"></a>Перечисление Упдатегрбит

Параметры для [JetUpdate2 (JET_SESID, JET_TABLEID, \[ \] , Int32, Int32, упдатегрбит)](./server2003api.jetupdate2-method.md).

Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration UpdateGrbit
'Usage
Dim instance As UpdateGrbit
```

``` csharp
[FlagsAttribute]
public enum UpdateGrbit
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
<td>CheckESE97Compatibility</td>
<td><strong>Устарело.</strong> этот флаг приводит к тому, что обновление будет возвращать ошибку, если обновление было невозможным в версии Windows 2000, которая требует меньшего максимального количества экземпляров столбцов с несколькими значениями в каждой записи, чем в более поздних версиях ESE. это важно только для приложений, которые хотят реплицировать данные между приложениями, размещенными на Windows 2000, и приложениями, размещенными на Windows 2003 или более поздних версиях ESE. Это не должно быть необходимо для большинства приложений.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
