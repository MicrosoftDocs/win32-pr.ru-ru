---
description: 'Дополнительные сведения о: Есентлогкорруптедексцептион Class'
title: Класс Есентлогкорруптедексцептион
TOCTitle: EsentLogCorruptedException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentlogcorruptedexception(v=EXCHG.10)
ms:contentKeyID: 55107292
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentLogCorruptedException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 962f27ee891434691531f44e400e39a19bfc98ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693534"
---
# <a name="esentlogcorruptedexception-class"></a>Класс Есентлогкорруптедексцептион

Базовый класс для JET_err. Исключения Логкорруптед.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  [System. Exception](/dotnet/api/system.exception)  
    [Microsoft. ISAM. ESENT. Есентексцептион](./esentexception-class.md)  
      [Microsoft. ISAM. ESENT. Interop. Есентеррорексцептион](./esenterrorexception-class.md)  
        [Microsoft. ISAM. ESENT. Interop. Есентдатаексцептион](./esentdataexception-class.md)  
          [Microsoft. ISAM. ESENT. Interop. Есенткорруптионексцептион](./esentcorruptionexception-class.md)  
            Microsoft. ISAM. ESENT. Interop. Есентлогкорруптедексцептион  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SerializableAttribute> _
Public NotInheritable Class EsentLogCorruptedException _
    Inherits EsentCorruptionException
'Usage
Dim instance As EsentLogCorruptedException
```

``` csharp
[SerializableAttribute]
public sealed class EsentLogCorruptedException : EsentCorruptionException
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентлогкорруптедексцептион](./esentlogcorruptedexception-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
