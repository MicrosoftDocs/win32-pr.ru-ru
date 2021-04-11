---
description: Дополнительные сведения о методе API. Жеттерм
title: API. Жеттерм, метод
TOCTitle: 'JetTerm method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetTerm(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetterm(v=EXCHG.10)
ms:contentKeyID: 55100813
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetTerm
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c8e028ecdc6456521b7aaa671cb4f5199e8751e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272728"
---
# <a name="apijetterm-method"></a>API. Жеттерм, метод

Завершите работу экземпляра, созданного с помощью [жетинит (JET_INSTANCE)](./api.jetinit-method.md) или [жеткреатеинстанце (JET_INSTANCE, String)](./api.jetcreateinstance-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetTerm ( _
    instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetTerm(instance)
```

``` csharp
public static void JetTerm(
    JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Параметры

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр для завершения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
