---
description: 'Дополнительные сведения о свойстве: JET_COLUMNBASE. Сзбасетабленаме'
title: Свойство JET_COLUMNBASE. Сзбасетабленаме
TOCTitle: 'szBaseTableName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.szbasetablename(v=EXCHG.10)
ms:contentKeyID: 55103375
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.get_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.set_szBaseTableName
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.szBaseTableName
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 508695dfaed58ac2179cc904c8e04836b49cbb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818120"
---
# <a name="jet_columnbaseszbasetablename-property"></a>Свойство JET_COLUMNBASE. Сзбасетабленаме

Возвращает таблицу, из которой текущая таблица наследует свою DDL.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property szBaseTableName As String
    Get
    Friend Set
'Usage
Dim instance As JET_COLUMNBASE
Dim value As String

value = instance.szBaseTableName
```

``` csharp
public string szBaseTableName { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. String](/dotnet/api/system.string)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_COLUMNBASE](./jet-columnbase-class.md)

[Элементы JET_COLUMNBASE](./jet-columnbase-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
