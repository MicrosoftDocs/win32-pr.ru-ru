---
description: Дополнительные сведения о методе API. Трисетиндексранже
title: API. Трисетиндексранже, метод
TOCTitle: 'TrySetIndexRange method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SetIndexRangeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.trysetindexrange(v=EXCHG.10)
ms:contentKeyID: 55100893
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySetIndexRange
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cbc04a7fe79f14976e509928e243030b641e8a89703e638861e95d60653fc081
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275294"
---
# <a name="apitrysetindexrange-method"></a>API. Трисетиндексранже, метод

Временно ограничивает набор записей индекса, которые курсор может проанализировать с помощью Жетмове, начиная с текущего элемента индекса и заканчивая элементом индекса, который соответствует критериям поиска, заданным в этом курсоре, и указанным критериям. Ключ поиска должен быть ранее создан с помощью Жетмакекэй. Возвращает значение true, если диапазон индекса не является пустым, и false в противном случае.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function TrySetIndexRange ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SetIndexRangeGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SetIndexRangeGrbit
Dim returnValue As Boolean

returnValue = Api.TrySetIndexRange(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySetIndexRange(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SetIndexRangeGrbit grbit
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

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. сетиндексранжегрбит](./setindexrangegrbit-enumeration.md)  
    
    Параметр поиска.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
Значение true, если поиск выполнен успешно.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
