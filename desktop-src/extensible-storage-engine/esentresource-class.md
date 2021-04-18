---
description: 'Дополнительные сведения о: Есентресаурце Class'
title: Класс Есентресаурце
TOCTitle: EsentResource class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentResource
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentresource(v=EXCHG.10)
ms:contentKeyID: 55102575
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentResource
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentResource
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 607fb59d6f9f89c33e685ed411ae9dc95eaa6818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711233"
---
# <a name="esentresource-class"></a>Класс Есентресаурце

Это базовый класс для всех объектов ресурсов ESENT. Подклассы этого класса могут распределять и освобождать неуправляемые ресурсы.

## <a name="inheritance-hierarchy"></a>Иерархия наследования

[System.Object](/dotnet/api/system.object)  
  Microsoft. ISAM. ESENT. Interop. Есентресаурце  
    [Microsoft. ISAM. ESENT. Interop. Session](./session-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Table](./table-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Transaction](./transaction-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Update](./update-class.md)  
    [Microsoft. ISAM. ESENT. Interop. Windows8. Дураблекоммиткаллбакк](./durablecommitcallback-class.md)  

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public MustInherit Class EsentResource _
    Implements IDisposable
'Usage
Dim instance As EsentResource
```

``` csharp
public abstract class EsentResource : IDisposable
```

## <a name="thread-safety"></a>Потокобезопасность

Любые общедоступные статичные (общие в Visual Basic) члены этого типа являются потокобезопасными. Потокобезопасная работа с членами экземпляров типа не гарантируется.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Элементы Есентресаурце](./esentresource-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
