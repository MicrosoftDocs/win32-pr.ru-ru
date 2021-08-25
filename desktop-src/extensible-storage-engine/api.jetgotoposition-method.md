---
description: Дополнительные сведения о методе API. Жетготопоситион
title: API. Жетготопоситион, метод
TOCTitle: 'JetGotoPosition method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoPosition(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RECPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotoposition(v=EXCHG.10)
ms:contentKeyID: 55100756
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoPosition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea8601220ba33538cdf53c90bea48f28d22886ae01c0e43692cd0e4b3a94b206
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978214"
---
# <a name="apijetgotoposition-method"></a>API. Жетготопоситион, метод

Перемещает курсор на новое место, которое представляет собой часть пути с помощью текущего индекса. См. также раздел [жетжетрекордпоситион (JET_SESID, JET_TABLEID, JET_RECPOS)](./api.jetgetrecordposition-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGotoPosition ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    recpos As JET_RECPOS _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recpos As JET_RECPOSApi.JetGotoPosition(sesid, tableid, _
    recpos)
```

``` csharp
public static void JetGotoPosition(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RECPOS recpos
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор для позиции.

<!-- end list -->

  - рекпос  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_RECPOS](./jet-recpos-class.md)  
    
    Приближенное положение для перемещения.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
