---
description: Дополнительные сведения о методе API. JetTerm2
title: API. JetTerm2, метод
TOCTitle: 'JetTerm2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm2(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.TermGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm2(v=EXCHG.10)
ms:contentKeyID: 55100829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f269bc28cf9e8b42b8c0922985cb137b05f1f52b82404320e2277e0e4954733d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983094"
---
# <a name="apijetterm2-method"></a>API. JetTerm2, метод

Завершите работу экземпляра, созданного с помощью [жетинит (JET_INSTANCE)](./api.jetinit-method.md) или [жеткреатеинстанце (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetTerm2 ( _
    instance As JET_INSTANCE, _
    grbit As TermGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim grbit As TermGrbitApi.JetTerm2(instance, grbit)
```

``` csharp
public static void JetTerm2(
    JET_INSTANCE instance,
    TermGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр для завершения.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. термгрбит](./termgrbit-enumeration.md)  
    
    Параметры завершения.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
