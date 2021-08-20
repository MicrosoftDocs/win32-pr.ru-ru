---
description: 'Дополнительные сведения о методе: Windows8Api. Жеттрипререадиндексранжес'
title: Windows8Api. Жеттрипререадиндексранжес, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'JetTryPrereadIndexRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Windows8.JET_INDEX_RANGE[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jettryprereadindexranges(v=EXCHG.10)
ms:contentKeyID: 55104421
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetTryPrereadIndexRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4c36b5e7ba99f5e8ff1099b0df75ef424ff2554bcb06a1e126be51b43f3192e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117700557"
---
# <a name="windows8apijettryprereadindexranges-method"></a>Windows8Api. Жеттрипререадиндексранжес, метод

Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Function JetTryPrereadIndexRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    indexRanges As JET_INDEX_RANGE(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim indexRanges As JET_INDEX_RANGE()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbit
Dim returnValue As Boolean

returnValue = Windows8Api.JetTryPrereadIndexRanges(sesid, _
    tableid, indexRanges, rangeIndex, _
    rangeCount, rangesPreread, columnsPreread, _
    grbit)
```

``` csharp
public static bool JetTryPrereadIndexRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_INDEX_RANGE[] indexRanges,
    int rangeIndex,
    int rangeCount,
    out int rangesPreread,
    JET_COLUMNID[] columnsPreread,
    PrereadIndexRangesGrbit grbit
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Таблица, для которой выдаются сведения о предчтении.

<!-- end list -->

  - индексранжес  
    Тип \[\]  
    
    Диапазоны ключей для чтения.

<!-- end list -->

  - rangeIndex  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Индекс первого диапазона ключей в массиве для чтения.

<!-- end list -->

  - ранжекаунт  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Максимальное число диапазонов ключей для чтения.

<!-- end list -->

  - ранжеспререад  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Возвращает количество ключей, фактически прочитанных в данный период.

<!-- end list -->

  - колумнспререад  
    Тип \[\]  
    
    Список идентификаторов столбцов для столбцов с длинными значениями для чтения.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. Windows8. пререадиндексранжесгрбит](./prereadindexrangesgrbit-enumeration.md)  
    
    Параметры для чтения. Используется для указания направления выполнения перед чтением.

#### <a name="return-value"></a>Возвращаемое значение

Тип: [System. Boolean](/dotnet/api/system.boolean)  
**\[ значение \] true** , если выполнено некоторое предсчитывание, и **\[ false \]** в противном случае.  

## <a name="see-also"></a>См. также

#### <a name="reference"></a>Справочник

[Класс Windows8Api](./windows8api-class.md)

[Элементы Windows8Api](./windows8api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
