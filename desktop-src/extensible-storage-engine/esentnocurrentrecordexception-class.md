---
description: 'Дополнительные сведения о: Есентнокуррентрекордексцептион Class'
title: Класс Есентнокуррентрекордексцептион
TOCTitle: EsentNoCurrentRecordException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentnocurrentrecordexception(v=EXCHG.10)
ms:contentKeyID: 55102290
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentNoCurrentRecordException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed58890ccd410101ecc6e6f38fafa0d254f4c2d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713091"
---
# <a name="esentnocurrentrecordexception-class"></a>Класс Есентнокуррентрекордексцептион

Базовый класс для JET_err. Исключения Нокуррентрекорд.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентстатиксцептион](./esentstateexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентнокуррентрекордексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentNoCurrentRecordException _
    Inherits EsentStateException
'Usage
Dim instance As EsentNoCurrentRecordException
```

``` csharp
[SerializableAttribute]
public sealed class EsentNoCurrentRecordException : EsentStateException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентнокуррентрекордексцептион](./esentnocurrentrecordexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
