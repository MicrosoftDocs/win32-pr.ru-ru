---
description: 'Дополнительные сведения о: Есентфиленотфаундексцептион Class'
title: Класс Есентфиленотфаундексцептион
TOCTitle: EsentFileNotFoundException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFileNotFoundException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfilenotfoundexception(v=EXCHG.10)
ms:contentKeyID: 55101712
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFileNotFoundException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFileNotFoundException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5e3339d084f785841cdd93e4938bf6f96d3014e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712025"
---
# <a name="esentfilenotfoundexception-class"></a>Класс Есентфиленотфаундексцептион

Базовый класс для JET_err. Исключения FileNotFound.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентфиленотфаундексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentFileNotFoundException _
    Inherits EsentStateException
'Usage
Dim instance As EsentFileNotFoundException
```

``` csharp
[SerializableAttribute]
public sealed class EsentFileNotFoundException : EsentStateException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентфиленотфаундексцептион](./esentfilenotfoundexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
