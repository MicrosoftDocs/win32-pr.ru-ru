---
description: 'Дополнительные сведения о свойстве: JET_RSTINFO. Пфнстатус'
title: Свойство JET_RSTINFO. Пфнстатус
TOCTitle: 'pfnStatus property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_rstinfo.pfnstatus(v=EXCHG.10)
ms:contentKeyID: 55103829
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.set_pfnStatus
- Microsoft.Isam.Esent.Interop.JET_RSTINFO.get_pfnStatus
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57b400e91867d4408fcdb93b979d1a39d8e7eb76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692206"
---
# <a name="jet_rstinfopfnstatus-property"></a>Свойство JET_RSTINFO. Пфнстатус

Возвращает или задает обратный вызов для получения или установки функции Status.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Property pfnStatus As JET_PFNSTATUS
    Get
    Set
'Usage
Dim instance As JET_RSTINFO
Dim value As JET_PFNSTATUS

value = instance.pfnStatus

instance.pfnStatus = value
```

``` csharp
public JET_PFNSTATUS pfnStatus { get; set; }
```

#### <a name="property-value"></a>Значение свойства

Тип: [Microsoft.ISAM.ESENT.Interop.JET_PFNSTATUS](./jet-pfnstatus-delegate.md)  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс JET_RSTINFO](./jet-rstinfo-class.md)

[Элементы JET_RSTINFO](./jet-rstinfo-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
