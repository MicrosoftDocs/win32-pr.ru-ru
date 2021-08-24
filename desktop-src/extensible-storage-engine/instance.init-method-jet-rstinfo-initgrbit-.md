---
description: 'Дополнительные сведения о методе: Instance.Init (JET_RSTINFO, Инитгрбит)'
title: Метод Instance.Init (JET_RSTINFO, Инитгрбит)
TOCTitle: Init method (JET_RSTINFO, InitGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Instance.Init(Microsoft.Isam.Esent.Interop.JET_RSTINFO,Microsoft.Isam.Esent.Interop.InitGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance.init(v=EXCHG.10)
ms:contentKeyID: 55103274
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Instance.Init
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e2a9975c42383c4ba0d58fb1a41dfeb1df07f81cebfd9b028bd54240bfb6b47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834444"
---
# <a name="instanceinit-method-jet_rstinfo-initgrbit"></a>Метод Instance.Init (JET_RSTINFO, Инитгрбит)

Инициализируйте JET_INSTANCE. Для этого API требуется по крайней мере версия ESENT для Vista.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
<SecurityPermissionAttribute(SecurityAction.LinkDemand)> _
Public Sub Init ( _
    recoveryOptions As JET_RSTINFO, _
    grbit As InitGrbit _
)
'Usage
Dim instance As Instance
Dim recoveryOptions As JET_RSTINFO
Dim grbit As InitGrbit

instance.Init(recoveryOptions, grbit)
```

``` csharp
[SecurityPermissionAttribute(SecurityAction.LinkDemand)]
public void Init(
    JET_RSTINFO recoveryOptions,
    InitGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - рековерйоптионс  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_RSTINFO](./jet-rstinfo-class.md)  
    
    Дополнительные параметры восстановления для повторного сопоставления баз данных во время восстановления, расположение для отмены восстановления или состояние восстановления.

<!-- end list -->

  - грбит  
    Тип: [Microsoft.Isam.Esent.Interop.Iniтгрбит](./initgrbit-enumeration.md)  
    
    Параметры инициализации.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс экземпляра](./instance-class.md)

[Члены экземпляра](./instance-members.md)

[Перегрузка init](./instance.init-method2.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
