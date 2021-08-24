---
description: 'Дополнительные сведения о: Есентлогсекуенцеендексцептион Class'
title: Класс Есентлогсекуенцеендексцептион
TOCTitle: EsentLogSequenceEndException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogsequenceendexception(v=EXCHG.10)
ms:contentKeyID: 55102213
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogSequenceEndException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 535c44bbd9e3d0c16fbebb21a2f1748fb8ef7289131f4c78bed936720d50a774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119115644"
---
# <a name="esentlogsequenceendexception-class"></a>Класс Есентлогсекуенцеендексцептион

Базовый класс для JET_err. Исключения Логсекуенцеенд.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System.Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есентфрагментатионексцептион](./esentfragmentationexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентлогсекуенцеендексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogSequenceEndException _
    Inherits EsentFragmentationException
'Usage
Dim instance As EsentLogSequenceEndException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogSequenceEndException : EsentFragmentationException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентлогсекуенцеендексцептион](./esentlogsequenceendexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
