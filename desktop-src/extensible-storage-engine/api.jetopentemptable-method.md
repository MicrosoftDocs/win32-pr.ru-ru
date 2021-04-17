---
description: Дополнительные сведения о методе API. Жетопентемптабле
title: API. Жетопентемптабле, метод
TOCTitle: 'JetOpenTempTable method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable(v=EXCHG.10)
ms:contentKeyID: 55100773
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa41ce62b8bc2d7f2429acb5de809ad0be44a609
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693631"
---
# <a name="apijetopentemptable-method"></a><span data-ttu-id="25fe0-103">API. Жетопентемптабле, метод</span><span class="sxs-lookup"><span data-stu-id="25fe0-103">Api.JetOpenTempTable method</span></span>

<span data-ttu-id="25fe0-104">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="25fe0-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="25fe0-105">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="25fe0-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="25fe0-106">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="25fe0-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="25fe0-107">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="25fe0-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="25fe0-108">См. также [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="25fe0-108">Also see [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="25fe0-109">[Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="25fe0-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="25fe0-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="25fe0-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="25fe0-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="25fe0-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="25fe0-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25fe0-112">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable(sesid, columns, _
    numColumns, grbit, tableid, columnids)
```

``` csharp
public static void JetOpenTempTable(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="25fe0-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="25fe0-113">Parameters</span></span>

  - <span data-ttu-id="25fe0-114">сесид</span><span class="sxs-lookup"><span data-stu-id="25fe0-114">sesid</span></span>  
    <span data-ttu-id="25fe0-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25fe0-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="25fe0-116">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="25fe0-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="25fe0-117">столбцы</span><span class="sxs-lookup"><span data-stu-id="25fe0-117">columns</span></span>  
    <span data-ttu-id="25fe0-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="25fe0-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="25fe0-119">Определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="25fe0-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="25fe0-120">нумколумнс</span><span class="sxs-lookup"><span data-stu-id="25fe0-120">numColumns</span></span>  
    <span data-ttu-id="25fe0-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="25fe0-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="25fe0-122">Число определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="25fe0-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="25fe0-123">грбит</span><span class="sxs-lookup"><span data-stu-id="25fe0-123">grbit</span></span>  
    <span data-ttu-id="25fe0-124">Тип: [Microsoft. ISAM. ESENT. Interop. темптаблегрбит](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="25fe0-124">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="25fe0-125">Параметры создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="25fe0-125">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="25fe0-126">TableID</span><span class="sxs-lookup"><span data-stu-id="25fe0-126">tableid</span></span>  
    <span data-ttu-id="25fe0-127">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="25fe0-127">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="25fe0-128">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="25fe0-128">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="25fe0-129">Закрытие этого TableID с помощью [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) освобождает ресурсы, связанные с временной таблицей.</span><span class="sxs-lookup"><span data-stu-id="25fe0-129">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="25fe0-130">колумнидс</span><span class="sxs-lookup"><span data-stu-id="25fe0-130">columnids</span></span>  
    <span data-ttu-id="25fe0-131">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="25fe0-131">Type: \[\]</span></span>  
    
    <span data-ttu-id="25fe0-132">Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="25fe0-132">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="25fe0-133">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="25fe0-133">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="25fe0-134">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="25fe0-134">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="25fe0-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25fe0-135">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="25fe0-136">Справочник</span><span class="sxs-lookup"><span data-stu-id="25fe0-136">Reference</span></span>

[<span data-ttu-id="25fe0-137">Класс API</span><span class="sxs-lookup"><span data-stu-id="25fe0-137">Api class</span></span>](./api-class.md)

[<span data-ttu-id="25fe0-138">Члены API</span><span class="sxs-lookup"><span data-stu-id="25fe0-138">Api members</span></span>](./api-members.md)

[<span data-ttu-id="25fe0-139">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="25fe0-139">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
