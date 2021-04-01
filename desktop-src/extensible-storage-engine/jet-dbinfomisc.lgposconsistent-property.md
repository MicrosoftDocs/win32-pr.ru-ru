---
description: 'Дополнительные сведения о свойстве: JET_DBINFOMISC. Лгпосконсистент'
title: Свойство JET_DBINFOMISC. Лгпосконсистент
TOCTitle: 'lgposConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.lgposconsistent(v=EXCHG.10)
ms:contentKeyID: 39516221
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.lgposConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_lgposConsistent
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3549e02b99b70f0704cd716410123dd732b1e518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143630"
---
# <a name="jet_dbinfomisclgposconsistent-property"></a>Свойство JET_DBINFOMISC. Лгпосконсистент

Возвращает лгпос, когда база данных была сделана целостной. Если база данных не согласуется, это значение равно null.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property lgposConsistent As JET_LGPOS
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LGPOS

value = instance.lgposConsistent
```

``` csharp
public JET_LGPOS lgposConsistent { get; internal set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Элементы JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
