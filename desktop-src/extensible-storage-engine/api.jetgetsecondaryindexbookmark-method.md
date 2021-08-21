---
description: Дополнительные сведения о методе API. Жетжетсекондариндексбукмарк
title: API. Жетжетсекондариндексбукмарк, метод
TOCTitle: 'JetGetSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100725
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSecondaryIndexBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9a1ca2430ae188b256fb1c6d026db7b6d78e45fdbfeaec158242019b7795d910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042532"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a>API. Жетжетсекондариндексбукмарк, метод

Извлекает специальную закладку для записи вторичного индекса в текущем положении курсора. Эту закладку можно использовать для эффективного перемещения курсора обратно к той же записи индекса с помощью Жетготосекондариндексбукмарк. Это наиболее полезно при изменении расположения вторичного индекса, который содержит дублирующиеся ключи или содержит несколько записей индекса для одной и той же записи.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetGetSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    <OutAttribute> ByRef actualSecondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    <OutAttribute> ByRef actualPrimaryKeySize As Integer, _
    grbit As GetSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim actualSecondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim actualPrimaryKeySize As Integer
Dim grbit As GetSecondaryIndexBookmarkGrbitApi.JetGetSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    actualSecondaryKeySize, primaryKey, _
    primaryKeySize, actualPrimaryKeySize, _
    grbit)
```

``` csharp
public static void JetGetSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    out int actualSecondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    out int actualPrimaryKeySize,
    GetSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Курсор, из которого извлекается закладка.

<!-- end list -->

  - secondaryKey  
    Тип \[\]  
    
    Выходной буфер для вторичного ключа.

<!-- end list -->

  - секондарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер буфера вторичного ключа.

<!-- end list -->

  - актуалсекондарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает размер вторичного ключа.

<!-- end list -->

  - primaryKey  
    Тип \[\]  
    
    Выходной буфер для первичного ключа.

<!-- end list -->

  - примарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Размер буфера первичного ключа.

<!-- end list -->

  - актуалпримарикэйсизе  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает размер первичного ключа.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. жетсекондариндексбукмаркгрбит](./getsecondaryindexbookmarkgrbit-enumeration.md)  
    
    Параметры для вызова.

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
