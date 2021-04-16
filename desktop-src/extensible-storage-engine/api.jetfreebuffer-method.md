---
description: Дополнительные сведения о методе API. Жетфрибуффер
title: API. Жетфрибуффер, метод
TOCTitle: 'JetFreeBuffer method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer(System.IntPtr)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetfreebuffer(v=EXCHG.10)
ms:contentKeyID: 55100694
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetFreeBuffer
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a584caf0f7c59c77e7d3c4a058a03780043e0f87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719324"
---
# <a name="apijetfreebuffer-method"></a>API. Жетфрибуффер, метод

Освобождает память, выделенную при вызове ядра СУБД.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetFreeBuffer ( _
    buffer As IntPtr _
)
'Usage
Dim buffer As IntPtrApi.JetFreeBuffer(buffer)
```

``` csharp
public static void JetFreeBuffer(
    IntPtr buffer
)
```

#### <a name="parameters"></a>Параметры

  - buffer  
    Тип: [System. IntPtr](/dotnet/api/system.intptr)  
    
    Буфер, выделенный при вызове ядра СУБД. [Ноль](/dotnet/api/system.intptr.zero) является допустимым и будет игнорироваться.

## <a name="remarks"></a>Комментарии

Этот метод является внутренним, поскольку мы никогда не предоставляем память, выделенную функцией ESENT вызывающим объектам.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
