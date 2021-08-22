---
description: 'Дополнительные сведения о свойстве: JET_ENUMCOLUMN. Ценумколумнвалуе'
title: Свойство JET_ENUMCOLUMN. Ценумколумнвалуе
TOCTitle: 'cEnumColumnValue property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumn.cenumcolumnvalue(v=EXCHG.10)
ms:contentKeyID: 55103498
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.get_cEnumColumnValue
- Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMN.set_cEnumColumnValue
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d862a3d49dbcc468bb08e60ffc396cf9b1a274634c247eba7defd8a5c25e9830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401824"
---
# <a name="jet_enumcolumncenumcolumnvalue-property"></a>Свойство JET_ENUMCOLUMN. Ценумколумнвалуе

Возвращает количество значений столбца, перечисленных для столбца. Этот элемент используется только в том случае, если [Err](./jet-enumcolumn.err-property.md) не [колумнсинглевалуе](./jet-wrn-enumeration.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property cEnumColumnValue As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_ENUMCOLUMN
Dim value As Integer

value = instance.cEnumColumnValue
```

``` csharp
public int cEnumColumnValue { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_ENUMCOLUMN](./jet-enumcolumn-class.md)

[Элементы JET_ENUMCOLUMN](./jet-enumcolumn-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
