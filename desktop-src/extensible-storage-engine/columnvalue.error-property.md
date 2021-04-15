---
description: 'Дополнительные сведения о свойстве: Колумнвалуе. Error'
title: Колумнвалуе. Error, свойство
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.ColumnValue.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columnvalue.error(v=EXCHG.10)
ms:contentKeyID: 55101202
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumnValue.Error
- Microsoft.Isam.Esent.Interop.ColumnValue.get_Error
- Microsoft.Isam.Esent.Interop.ColumnValue.set_Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ff03f39b1721aed9cb3793119e721184836ee74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701734"
---
# <a name="columnvalueerror-property"></a>Колумнвалуе. Error, свойство

Возвращает предупреждение, созданное путем извлечения или установки этого столбца.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property Error As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As ColumnValue
Dim value As JET_wrn

value = instance.Error
```

``` csharp
public JET_wrn Error { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Колумнвалуе](./columnvalue-class.md)

[Элементы Колумнвалуе](./columnvalue-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
