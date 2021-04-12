---
description: 'Дополнительные сведения о: Есентдекомпрессионфаиледексцептион Class'
title: Класс Есентдекомпрессионфаиледексцептион
TOCTitle: EsentDecompressionFailedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdecompressionfailedexception(v=EXCHG.10)
ms:contentKeyID: 55101587
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentDecompressionFailedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 185f224883e3e2850e4a94c53c49d19a165528ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155755"
---
# <a name="esentdecompressionfailedexception-class"></a>Класс Есентдекомпрессионфаиледексцептион

Базовый класс для JET_err. Исключения Декомпрессионфаилед.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентдекомпрессионфаиледексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentDecompressionFailedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentDecompressionFailedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentDecompressionFailedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентдекомпрессионфаиледексцептион](./esentdecompressionfailedexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
