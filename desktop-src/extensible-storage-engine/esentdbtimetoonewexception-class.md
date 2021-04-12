---
description: 'Дополнительные сведения о: Есентдбтиметуневексцептион Class'
title: Класс Есентдбтиметуневексцептион
TOCTitle: EsentDbTimeTooNewException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdbtimetoonewexception(v=EXCHG.10)
ms:contentKeyID: 55101468
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDbTimeTooNewException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de09cf8f20aca58c6e32fdf23766f416bf93f227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263754"
---
# <a name="esentdbtimetoonewexception-class"></a>Класс Есентдбтиметуневексцептион

Базовый класс для JET_err. Исключения Дбтиметунев.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентинконсистентексцептион](./esentinconsistentexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентдбтиметуневексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDbTimeTooNewException _
    Inherits EsentInconsistentException
'Usage
Dim instance As EsentDbTimeTooNewException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDbTimeTooNewException : EsentInconsistentException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентдбтиметуневексцептион](./esentdbtimetoonewexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
