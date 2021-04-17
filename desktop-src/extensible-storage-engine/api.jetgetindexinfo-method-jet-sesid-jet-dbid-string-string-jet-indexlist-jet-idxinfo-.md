---
description: 'Дополнительные сведения: метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)'
title: Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)
TOCTitle: JetGetIndexInfo method (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXLIST@,Microsoft.Isam.Esent.Interop.JET_IdxInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetindexinfo(v=EXCHG.10)
ms:contentKeyID: 55107227
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetIndexInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0cc7c110c139c66fdd5d8baee4ebb102922adf7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673220"
---
# <a name="apijetgetindexinfo-method-jet_sesid-jet_dbid-string-string-jet_indexlist-jet_idxinfo"></a>Метод API. Жетжетиндексинфо (JET_SESID, JET_DBID, строка, строка, JET_INDEXLIST, JET_IdxInfo)

Извлекает сведения о индексах в таблице.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetIndexInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    indexname As String, _
    <OutAttribute> ByRef result As JET_INDEXLIST, _
    infoLevel As JET_IdxInfo _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim indexname As String
Dim result As JET_INDEXLIST
Dim infoLevel As JET_IdxInfoApi.JetGetIndexInfo(sesid, dbid, _
    tablename, indexname, result, infoLevel)
```

``` csharp
public static void JetGetIndexInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string indexname,
    out JET_INDEXLIST result,
    JET_IdxInfo infoLevel
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - dbid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    Используемая база данных.

<!-- end list -->

  - tablename  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя таблицы, о которой необходимо получить сведения об индексе.

<!-- end list -->

  - IndexName  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя индекса, сведения о котором необходимо получить.

<!-- end list -->

  - result  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXLIST](./jet-indexlist-class.md)  
    
    Заполняется сведениями о индексах в таблице.

<!-- end list -->

  - инфолевел  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_IdxInfo](./jet-idxinfo-enumeration.md)  
    
    Тип извлекаемых данных.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жетжетиндексинфо](./api.jetgetindexinfo-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
