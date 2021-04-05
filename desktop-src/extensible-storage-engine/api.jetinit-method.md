---
description: Дополнительные сведения о методе API. Жетинит
title: API. Жетинит, метод
TOCTitle: 'JetInit method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetInit(Microsoft.Isam.Esent.Interop.JET_INSTANCE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetinit(v=EXCHG.10)
ms:contentKeyID: 55100760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetInit
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetInit
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27b0ad5fa640b853b46cd39ae595a1f486812adb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913356"
---
# <a name="apijetinit-method"></a>API. Жетинит, метод

Инициализируйте ядро СУБД ESENT.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetInit ( _
    ByRef instance As JET_INSTANCE _
)
'Usage
Dim instance As JET_INSTANCEApi.JetInit(instance)
```

``` csharp
public static void JetInit(
    ref JET_INSTANCE instance
)
```

#### <a name="parameters"></a>Параметры

  - экземпляр  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)  
    
    Экземпляр для инициализации. Если экземпляр не был выделен, создается новый, а ядро работает в режиме с одним экземпляром.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
