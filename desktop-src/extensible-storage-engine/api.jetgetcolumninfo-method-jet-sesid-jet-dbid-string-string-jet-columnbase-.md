---
description: 'Дополнительные сведения: метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)'
title: Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)
TOCTitle: JetGetColumnInfo method (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,System.String,Microsoft.Isam.Esent.Interop.JET_COLUMNBASE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetcolumninfo(v=EXCHG.10)
ms:contentKeyID: 55100705
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetColumnInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8bd0dd2872ac22b2ab8c7d7e5b98857d223e38abd286e0d9554ecbea1f621855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983434"
---
# <a name="apijetgetcolumninfo-method-jet_sesid-jet_dbid-string-string-jet_columnbase"></a>Метод API. Жетжетколумнинфо (JET_SESID, JET_DBID, строка, строка, JET_COLUMNBASE)

Извлекает сведения о столбце в таблице.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetColumnInfo ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    tablename As String, _
    columnName As String, _
    <OutAttribute> ByRef columnbase As JET_COLUMNBASE _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim tablename As String
Dim columnName As String
Dim columnbase As JET_COLUMNBASEApi.JetGetColumnInfo(sesid, dbid, _
    tablename, columnName, columnbase)
```

``` csharp
public static void JetGetColumnInfo(
    JET_SESID sesid,
    JET_DBID dbid,
    string tablename,
    string columnName,
    out JET_COLUMNBASE columnbase
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
    
    Имя таблицы, содержащей столбец.

<!-- end list -->

  - columnName  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя столбца.

<!-- end list -->

  - колумнбасе  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)  
    
    Заполняется сведениями о столбцах в таблице.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Перегрузка Жетжетколумнинфо](./api.jetgetcolumninfo-method.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
