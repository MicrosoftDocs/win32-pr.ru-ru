---
description: 'Дополнительные сведения о: Есентпревиаусверсионексцептион Class'
title: Класс Есентпревиаусверсионексцептион
TOCTitle: EsentPreviousVersionException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentpreviousversionexception(v=EXCHG.10)
ms:contentKeyID: 55102535
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentPreviousVersionException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 803a019a531caf97888cf6f7067fba665447d8aaafa25e2e6016b219214ae9ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971484"
---
# <a name="esentpreviousversionexception-class"></a>Класс Есентпревиаусверсионексцептион

Базовый класс для JET_err. Исключения PreviousVersion.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        Microsoft. ISAM. ESENT. Interop. Есентпревиаусверсионексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentPreviousVersionException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentPreviousVersionException
```

``` csharp
[SerializableAttribute]
public sealed class EsentPreviousVersionException : EsentErrorException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентпревиаусверсионексцептион](./esentpreviousversionexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
