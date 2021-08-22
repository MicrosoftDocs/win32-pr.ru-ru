---
description: 'Дополнительные сведения о: Есентмеморексцептион Class'
title: Класс EsentMemoryException
TOCTitle: EsentMemoryException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentMemoryException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 67ae3f11109ec025c0b0b0c1d907c09be3ca9393e39bd56f7b7cd190bdbb9acc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119040782"
---
# <a name="esentmemoryexception-class"></a>Класс EsentMemoryException

Базовый класс для исключений памяти.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион  
              

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentMemoryException _
    Inherits EsentResourceException
'Usage
Dim instance As EsentMemoryException
```

``` csharp
[SerializableAttribute]
public abstract class EsentMemoryException : EsentResourceException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентмеморексцептион](./esentmemoryexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентоператионексцептион](./esentoperationexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентресаурцеексцептион](./esentresourceexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентмеморексцептион  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофбуфферсексцептион](./esentoutofbuffersexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофкурсорсексцептион](./esentoutofcursorsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентаутоффилехандлесексцептион](./esentoutoffilehandlesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофмеморексцептион](./esentoutofmemoryexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофсессионсексцептион](./esentoutofsessionsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есентаутофсреадсексцептион](./esentoutofthreadsexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есенттуманимемпулентриесексцептион](./esenttoomanymempoolentriesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есенттуманйопениндексесексцептион](./esenttoomanyopenindexesexception-class.md)  
              [Microsoft. ISAM. ESENT. Interop. Есенттуманисортсексцептион](./esenttoomanysortsexception-class.md)