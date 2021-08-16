---
description: Дополнительные сведения о методе Instance.Init (Инитгрбит)
title: Метод Instance.Init (Инитгрбит)
TOCTitle: Init method (InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103295
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b2ce0ba3edd115802c07a0df2a3cc454f9953f7548692bce7aab7734da2a17fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112553"
---
# <a name="instanceinit-method-initgrbit"></a>Метод Instance.Init (Инитгрбит)

Инициализируйте JET_INSTANCE.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim grbit As InitGrbit

instance.Init(grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - грбит  
    Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)  
    
    Параметры инициализации.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Члены экземпляра](./instance-members.md)

[Перегрузка init](./instance.init-method2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
