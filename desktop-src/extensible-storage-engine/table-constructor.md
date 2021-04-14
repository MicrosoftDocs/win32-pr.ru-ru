---
description: 'Дополнительные сведения: Конструктор таблиц'
title: Конструктор таблиц
TOCTitle: 'Table constructor '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Table.#ctor(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_DBID,System.String,Microsoft.Isam.Esent.Interop.OpenTableGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.table.table(v=EXCHG.10)
ms:contentKeyID: 55104142
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Table.Table
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Table..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8987e643253791e5315dd07b7b20a40dee66cf9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692494"
---
# <a name="table-constructor"></a>Конструктор таблиц

Инициализирует новый экземпляр класса Table. Таблица открывается из заданной базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Sub New ( _
    sesid As JET_SESID, _
    dbid As JET_DBID, _
    name As String, _
    grbit As OpenTableGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim dbid As JET_DBID
Dim name As String
Dim grbit As OpenTableGrbit

Dim instance As New Table(sesid, dbid, _
    name, grbit)
```

``` csharp
public Table(
    JET_SESID sesid,
    JET_DBID dbid,
    string name,
    OpenTableGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - dbid  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)  
    
    База данных, в которой будет открыта таблица.

<!-- end list -->

  - name  
    Тип: [System. String](/dotnet/api/system.string)  
    
    Имя таблицы.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. опентаблегрбит](./opentablegrbit-enumeration.md)  
    
    Параметры Жетопентабле.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Table](./table-class.md)

[Элементы таблицы](./table-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
