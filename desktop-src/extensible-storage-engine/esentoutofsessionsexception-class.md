---
description: 'Дополнительные сведения о: Есентаутофсессионсексцептион Class'
title: Класс Есентаутофсессионсексцептион
TOCTitle: EsentOutOfSessionsException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoutofsessionsexception(v=EXCHG.10)
ms:contentKeyID: 55102494
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOutOfSessionsException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70b3c466586551f67f451d8ecc6ad108da52089a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423917"
---
# <a name="esentoutofsessionsexception-class"></a>Класс Есентаутофсессионсексцептион

Базовый класс для JET_err. Исключения Аутофсессионс.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион](./esentresourceexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион](./esentmemoryexception-class.md)  
              Microsoft. ISAM. ESENT. Interop. Есентаутофсессионсексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentOutOfSessionsException _
    Inherits EsentMemoryException
'Usage
Dim instance As EsentOutOfSessionsException
```

``` csharp
[SerializableAttribute]
public sealed class EsentOutOfSessionsException : EsentMemoryException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентаутофсессионсексцептион](./esentoutofsessionsexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
