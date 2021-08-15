---
description: 'Дополнительные сведения: метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)'
title: Метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)
TOCTitle: GetTableIndexes method (JET_SESID, JET_DBID, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetTableIndexes(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.gettableindexes(v=EXCHG.10)
ms:contentKeyID: 55100648
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
ms.openlocfilehash: 22390c3c38638d62060671475b60dbaf48495803de21b941a17eb2a275ccda17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983834"
---
# <a name="apigettableindexes-method-jet_sesid-jet_dbid-string"></a>Метод API. Жеттаблеиндексес (JET_SESID, JET_DBID, String)

Выполняет перебор всех индексов в таблице, возвращая сведения о каждой из них.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function GetTableIndexes ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String _
) As IEnumerable(Of IndexInfo)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim returnValue As IEnumerable(Of IndexInfo)

returnValue = Api.GetTableIndexes(sesid, _
    dbid, tablename)
```

``` csharp
public static IEnumerable<IndexInfo> GetTableIndexes(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - dbid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    База данных, содержащая таблицу.

<!-- end list -->

  - tablename  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя таблицы.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1)\<[IndexInfo](./indexinfo-class.md)\>  
Итератор по Индексинфо для каждого индекса в таблице.  

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жеттаблеиндексес](./api.gettableindexes-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
