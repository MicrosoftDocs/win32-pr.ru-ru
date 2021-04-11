---
description: 'Дополнительные сведения о: JET_PFNREALLOC делегата'
title: JET_PFNREALLOC делегат
TOCTitle: JET_PFNREALLOC delegate
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_pfnrealloc(v=EXCHG.10)
ms:contentKeyID: 39515764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC..ctor
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.BeginInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.EndInvoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC.Invoke
- Microsoft.Isam.Esent.Interop.JET_PFNREALLOC
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7aab9fef2d7a449c877f88d2ed77aa19cbb2409d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999625"
---
# <a name="jet_pfnrealloc-delegate"></a>JET_PFNREALLOC делегат

Обратный вызов, используемый Жетенумератеколумнс для выделения памяти для буферов вывода.

Этот API несовместим с CLS. 

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Delegate Function JET_PFNREALLOC ( _
    context As IntPtr, _
    memory As IntPtr, _
    requestedSize As UInteger _
) As IntPtr
'Usage
Dim instance As New JET_PFNREALLOC(AddressOf HandlerMethod)
```

``` csharp
[CLSCompliantAttribute(false)]
public delegate IntPtr JET_PFNREALLOC(
    IntPtr context,
    IntPtr memory,
    uint requestedSize
)
```

#### <a name="parameters"></a>Параметры

  - контекст  
    Тип: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Контекст, заданный для Жетенумератеколумнс.

<!-- end list -->

  - Память  
    Тип: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Если ненулевое значение, указатель на блок памяти, ранее выделенный этим обратным вызовом.

<!-- end list -->

  - requestedSize  
    Тип: [System. UInt32](/dotnet/api/system.uint32)  
    
    Новый размер блока памяти (в байтах). Если это значение равно 0 и указан блок памяти, то этот блок памяти будет освобожден.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. IntPtr](/dotnet/api/system.intptr)  
Указатель на только что выделенную память. Если память не может быть выделена, возвращается [нуль](/dotnet/api/system.intptr.zero) .  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
