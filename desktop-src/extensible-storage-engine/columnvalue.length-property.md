---
description: Дополнительные сведения о свойстве Колумнвалуе. length
title: Колумнвалуе. length, свойство
TOCTitle: 'Length property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Length
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.length(v=EXCHG.10)
ms:contentKeyID: 55101208
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Length
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Length
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 93ff15d348b2d47f76c680547d6e7939ebbd2c5faeaa240d9d18b1c3f523b93f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118083667"
---
# <a name="columnvaluelength-property"></a>Колумнвалуе. length, свойство

Возвращает длину в байтах значения столбца, равного нулю, если столбец имеет значение null, в противном случае он соответствует размеру для столбцов фиксированного размера и представляет фактическую длину байт для столбцов переменного размера (т. е. двоичного и строкового). Для строк длина определяется в предположении 2 байта на символ.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public MustOverride ReadOnly Property Length As Integer
    Get
'Usage
Dim instance As ColumnValue
Dim value As Integer

value = instance.Length
```

``` csharp
public abstract int Length { get; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс Колумнвалуе](./columnvalue-class.md)

[Элементы Колумнвалуе](./columnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
