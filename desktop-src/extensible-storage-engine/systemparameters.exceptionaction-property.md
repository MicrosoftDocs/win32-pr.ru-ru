---
description: 'Дополнительные сведения о свойстве: SystemParameters. Ексцептионактион'
title: SystemParameters. Ексцептионактион, свойство
TOCTitle: 'ExceptionAction property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.exceptionaction(v=EXCHG.10)
ms:contentKeyID: 55104042
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.get_ExceptionAction
- Microsoft.Isam.Esent.Interop.SystemParameters.set_ExceptionAction
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 217942d9827a715858c76a704092259a5c3df25f98bf4eac7d5835450f502e3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118484900"
---
# <a name="systemparametersexceptionaction-property"></a>SystemParameters. Ексцептионактион, свойство

Возвращает или задает кодировку значений, выполняемых с исключениями, созданными в JET.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Property ExceptionAction As JET_ExceptionAction
    Get
    Set
'Usage
Dim value As JET_ExceptionAction

value = SystemParameters.ExceptionAction

SystemParameters.ExceptionAction = value
```

``` csharp
public static JET_ExceptionAction ExceptionAction { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_ExceptionAction](./jet-exceptionaction-enumeration.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[SystemParameters - класс](./systemparameters-class.md)

[Элементы SystemParameters](./systemparameters-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
