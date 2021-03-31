---
description: Дополнительные сведения о методе API. JetOpenTempTable2
title: API. JetOpenTempTable2, метод
TOCTitle: 'JetOpenTempTable2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable2(v=EXCHG.10)
ms:contentKeyID: 55100777
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8fd3f0e04db6519fbcaa1c2d2fa9060d2d993d27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272544"
---
# <a name="apijetopentemptable2-method"></a>API. JetOpenTempTable2, метод

Создает временную таблицу с одним индексом. Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс. Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером. Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно. См. также [жетопентемптабле (JET_SESID, \[ \] , Int32, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md). [Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).

**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Синтаксис

``` vb
'Declaration
Public Shared Sub JetOpenTempTable2 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    lcid As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim lcid As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable2(sesid, columns, _
    numColumns, lcid, grbit, tableid, _
    columnids)
```

``` csharp
public static void JetOpenTempTable2(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    int lcid,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a>Параметры

  - сесид  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)  
    
    Используемый сеанс.

<!-- end list -->

  - столбцы  
    Тип \[\]  
    
    Определения столбцов для столбцов, созданных во временной таблице.

<!-- end list -->

  - нумколумнс  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    Число определений столбцов.

<!-- end list -->

  - lcid  
    Тип: [System. Int32](/dotnet/api/system.int32)  
    
    КОД локали, используемый для сравнения данных любого ключевого столбца Юникода во временной таблице. Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет.

<!-- end list -->

  - грбит  
    Тип: [Microsoft. ISAM. ESENT. Interop. темптаблегрбит](./temptablegrbit-enumeration.md)  
    
    Параметры создания таблицы.

<!-- end list -->

  - TableID  
    Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)  
    
    Возвращает TableID временной таблицы. Закрытие этого TableID с помощью [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) освобождает ресурсы, связанные с временной таблицей.

<!-- end list -->

  - колумнидс  
    Тип \[\]  
    
    Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы. Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов. В результате размер этого буфера должен соответствовать размеру входного массива.

## <a name="see-also"></a>См. также раздел

#### <a name="reference"></a>Справочник

[Класс API](./api-class.md)

[Члены API](./api-members.md)

[Пространство имен Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)
