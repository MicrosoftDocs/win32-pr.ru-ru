---
description: 'Дополнительные сведения о методе: Windows8Api. Пререадкэйранжес'
title: Windows8Api. Пререадкэйранжес, метод (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'PrereadKeyRanges method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[][],System.Int32[],System.Byte[][],System.Int32[],System.Int32,System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[],Microsoft.Isam.Esent.Interop.Windows8.PrereadIndexRangesGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.prereadkeyranges(v=EXCHG.10)
ms:contentKeyID: 55104465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.PrereadKeyRanges
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 02328ddc47daec4fbd98f88222dd7519053ed92aa64d2a0048782340d626b03c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119452694"
---
# <a name="windows8apiprereadkeyranges-method"></a>Windows8Api. Пререадкэйранжес, метод

Если записи с указанными диапазонами ключей отсутствуют в буферном кэше, запустите асинхронные операции чтения, чтобы перенести записи в буферный кэш базы данных.

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub PrereadKeyRanges ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    keysStart As Byte()(), _
    keyStartLengths As Integer(), _
    keysEnd As Byte()(), _
    keyEndLengths As Integer(), _
    rangeIndex As Integer, _
    rangeCount As Integer, _
    <OutAttribute> ByRef rangesPreread As Integer, _
    columnsPreread As JET_COLUMNID(), _
    grbit As PrereadIndexRangesGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim keysStart As Byte()()
Dim keyStartLengths As Integer()
Dim keysEnd As Byte()()
Dim keyEndLengths As Integer()
Dim rangeIndex As Integer
Dim rangeCount As Integer
Dim rangesPreread As Integer
Dim columnsPreread As JET_COLUMNID()
Dim grbit As PrereadIndexRangesGrbitWindows8Api.PrereadKeyRanges(sesid, tableid, _
    keysStart, keyStartLengths, keysEnd, _
    keyEndLengths, rangeIndex, rangeCount, _
    rangesPreread, columnsPreread, grbit)
```

``` csharp
public static void PrereadKeyRanges(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[][] keysStart,
    int[] keyStartLengths,
    byte[][] keysEnd,
    int[] keyEndLengths,
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

  - кэйсстарт  
    Тип \[\]  
    
    Начало диапазона ключевых диапазонов для чтения.

<!-- end list -->

  - кэйстартленгсс  
    Тип \[\]  
    
    Длина начальных клавиш для чтения.

<!-- end list -->

  - кэйсенд  
    Тип \[\]  
    
    Конец диапазона ключей для чтения.

<!-- end list -->

  - кэйендленгсс  
    Тип \[\]  
    
    Длина конечных клавиш для чтения.

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

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс Windows8Api](./windows8api-class.md)

[Элементы Windows8Api](./windows8api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
