---
description: 'Дополнительные сведения: метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)'
title: Метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)
TOCTitle: GetTableIndexes method (JET_SESID, JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55107219
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetTableIndexes
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8708f285445b13ecb1c9d2cb306ec14c7976905b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701428"
---
# <a name="apigettableindexes-method-jet_sesid-jet_tableid"></a>Метод API. Жеттаблеиндексес (JET_SESID, JET_TABLEID)

Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    tableid)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Таблица, для которой необходимо получить сведения об индексе.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\>  
Итератор по Индексинфо для каждого индекса в таблице.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жеттаблеиндексес](./api.gettableindexes-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
