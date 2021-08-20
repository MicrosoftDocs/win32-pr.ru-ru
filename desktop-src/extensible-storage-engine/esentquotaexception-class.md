---
description: 'Дополнительные сведения о: Есенткуотаексцептион Class'
title: Класс EsentQuotaException
TOCTitle: EsentQuotaException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentQuotaException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentquotaexception(v=EXCHG.10)
ms:contentKeyID: 55102495
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentQuotaException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6350dfa9cbdddcf935b4f87fab964d40c1fc65765a254219c542d29b676fed36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782274"
---
# <a name="esentquotaexception-class"></a>Класс EsentQuotaException

Базовый класс для исключений квот.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есенткуотаексцептион  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофдатабасеспацеексцептион](./esentoutofdatabasespaceexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есенттуманинстанцесексцептион](./esenttoomanyinstancesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есенттуманйопентаблесексцептион](./esenttoomanyopentablesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентверсионстореаутофмеморексцептион](./esentversionstoreoutofmemoryexception-class.md)  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentQuotaException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentQuotaException
```

``` csharp
[SerializableAttribute]
public abstract class EsentQuotaException : EsentResourceException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есенткуотаексцептион](./esentquotaexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
