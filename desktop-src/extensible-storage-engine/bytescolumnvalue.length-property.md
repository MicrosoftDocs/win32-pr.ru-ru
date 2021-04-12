---
description: Дополнительные сведения о свойстве Битесколумнвалуе. length
title: Битесколумнвалуе. length, свойство
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.bytescolumnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55107234
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.BytesColumnValue.Length
- Microsoft.Isam.Esent.Interop.BytesColumnValue.get_Length
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f49b38cdab8d5e4a7b3554651a7dc2f97f651b59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348375"
---
# <a name="bytescolumnvaluelength-property"></a>Битесколумнвалуе. length, свойство

Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае соответствует фактической длине массива байтов.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Overrides ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As BytesColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public override int Length { get; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Битесколумнвалуе](./bytescolumnvalue-class.md)

[Элементы Битесколумнвалуе](./bytescolumnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
