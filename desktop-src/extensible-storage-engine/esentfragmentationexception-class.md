---
description: 'Дополнительные сведения о: Есентфрагментатионексцептион Class'
title: Класс EsentFragmentationException
TOCTitle: EsentFragmentationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentFragmentationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentfragmentationexception(v=EXCHG.10)
ms:contentKeyID: 55101771
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentFragmentationException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2db8934cfdbfb58b44d3de14c13c72bc7d5ce5afa4f5b2bdfaec0a05926469af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838724"
---
# <a name="esentfragmentationexception-class"></a>Класс EsentFragmentationException

Базовый класс для исключений фрагментации.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион  
            

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentFragmentationException _
    Inherits EsentDataException
'Usage
Dim instance As EsentFragmentationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentFragmentationException : EsentDataException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Элементы Есентфрагментатионексцептион](./esentfragmentationexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a>Производные типы

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион  
            [Microsoft. ISAM. ESENT. Interop. Есентлогсекторсиземисматчексцептион](./esentlogsectorsizemismatchexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогсекуенцеенддатабасесконсистентексцептион](./esentlogsequenceenddatabasesconsistentexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентлогсекуенцеендексцептион](./esentlogsequenceendexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентаутофаутоинкрементвалуесексцептион](./esentoutofautoincrementvaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентаутофдбтимевалуесексцептион](./esentoutofdbtimevaluesexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентаутофлонгвалуеидсексцептион](./esentoutoflongvalueidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентаутофобжектидсексцептион](./esentoutofobjectidsexception-class.md)  
            [Microsoft. ISAM. ESENT. Interop. Есентаутофсекуентиалиндексвалуесексцептион](./esentoutofsequentialindexvaluesexception-class.md)