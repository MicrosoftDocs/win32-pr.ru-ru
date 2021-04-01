---
description: 'Дополнительные сведения о: Есентресаурцеексцептион Class'
title: Класс EsentResourceException
TOCTitle: EsentResourceException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResourceException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresourceexception(v=EXCHG.10)
ms:contentKeyID: 55102627
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResourceException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResourceException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a7d4964bb4ed9c1305652d9425170bd934c9274e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265135"
---
# <a name="esentresourceexception-class"></a>Класс EsentResourceException

Базовый класс для исключений ресурсов.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентдискексцептион](./esentdiskexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион](./esentmemoryexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион](./esentquotaexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттаскдроппедексцептион](./esenttaskdroppedexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есенттуманиоексцептион](./esenttoomanyioexception-class.md)  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentResourceException _
    Inherits EsentOperationException
'Usage
Dim instance As EsentResourceException
```

``` csharp
[SerializableAttribute]
public abstract class EsentResourceException : EsentOperationException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентресаурцеексцептион](./esentresourceexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
