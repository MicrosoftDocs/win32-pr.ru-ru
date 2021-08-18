---
description: 'Дополнительные сведения о: Есентсессионшарингвиолатионексцептион Class'
title: Класс Есентсессионшарингвиолатионексцептион
TOCTitle: EsentSessionSharingViolationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentsessionsharingviolationexception(v=EXCHG.10)
ms:contentKeyID: 55102713
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentSessionSharingViolationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: acdb6388a7daa76be26bf207cb2ebf32a5ca7df0fa7c7ee60c088cc1f2042012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118981554"
---
# <a name="esentsessionsharingviolationexception-class"></a>Класс Есентсессионшарингвиолатионексцептион

Базовый класс для JET_err. Исключения Сессионшарингвиолатион.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентапиексцептион](./esentapiexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентусажеексцептион](./esentusageexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентсессионшарингвиолатионексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentSessionSharingViolationException _
    Inherits EsentUsageException
'Usage
Dim instance As EsentSessionSharingViolationException
```

``` csharp
[SerializableAttribute]
public sealed class EsentSessionSharingViolationException : EsentUsageException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентсессионшарингвиолатионексцептион](./esentsessionsharingviolationexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
