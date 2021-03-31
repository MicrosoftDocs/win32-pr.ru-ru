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
# <a name="apijetopentemptable2-method"></a><span data-ttu-id="637ae-103">API. JetOpenTempTable2, метод</span><span class="sxs-lookup"><span data-stu-id="637ae-103">Api.JetOpenTempTable2 method</span></span>

<span data-ttu-id="637ae-104">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="637ae-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="637ae-105">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="637ae-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="637ae-106">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="637ae-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="637ae-107">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="637ae-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="637ae-108">См. также [жетопентемптабле (JET_SESID, \[ \] , Int32, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [JetOpenTempTable3 (JET_SESID, \[ \] , Int32, JET_UNICODEINDEX, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable3-method.md).</span><span class="sxs-lookup"><span data-stu-id="637ae-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTempTable3(JET_SESID, \[\], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable3-method.md).</span></span> <span data-ttu-id="637ae-109">[Жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="637ae-109">[JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="637ae-110">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="637ae-110">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="637ae-111">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="637ae-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="637ae-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="637ae-112">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="637ae-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="637ae-113">Parameters</span></span>

  - <span data-ttu-id="637ae-114">сесид</span><span class="sxs-lookup"><span data-stu-id="637ae-114">sesid</span></span>  
    <span data-ttu-id="637ae-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="637ae-115">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="637ae-116">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="637ae-116">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-117">столбцы</span><span class="sxs-lookup"><span data-stu-id="637ae-117">columns</span></span>  
    <span data-ttu-id="637ae-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="637ae-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="637ae-119">Определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="637ae-119">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-120">нумколумнс</span><span class="sxs-lookup"><span data-stu-id="637ae-120">numColumns</span></span>  
    <span data-ttu-id="637ae-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="637ae-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="637ae-122">Число определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="637ae-122">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-123">lcid</span><span class="sxs-lookup"><span data-stu-id="637ae-123">lcid</span></span>  
    <span data-ttu-id="637ae-124">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="637ae-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="637ae-125">КОД локали, используемый для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="637ae-125">The locale ID to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="637ae-126">Любой языковой стандарт может использоваться при условии, что на компьютере установлен соответствующий языковой пакет.</span><span class="sxs-lookup"><span data-stu-id="637ae-126">Any locale may be used as long as the appropriate language pack has been installed on the machine.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-127">грбит</span><span class="sxs-lookup"><span data-stu-id="637ae-127">grbit</span></span>  
    <span data-ttu-id="637ae-128">Тип: [Microsoft. ISAM. ESENT. Interop. темптаблегрбит](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="637ae-128">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="637ae-129">Параметры создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="637ae-129">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-130">TableID</span><span class="sxs-lookup"><span data-stu-id="637ae-130">tableid</span></span>  
    <span data-ttu-id="637ae-131">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="637ae-131">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="637ae-132">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="637ae-132">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="637ae-133">Закрытие этого TableID с помощью [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) освобождает ресурсы, связанные с временной таблицей.</span><span class="sxs-lookup"><span data-stu-id="637ae-133">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="637ae-134">колумнидс</span><span class="sxs-lookup"><span data-stu-id="637ae-134">columnids</span></span>  
    <span data-ttu-id="637ae-135">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="637ae-135">Type: \[\]</span></span>  
    
    <span data-ttu-id="637ae-136">Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="637ae-136">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="637ae-137">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="637ae-137">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="637ae-138">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="637ae-138">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="637ae-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="637ae-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="637ae-140">Справочник</span><span class="sxs-lookup"><span data-stu-id="637ae-140">Reference</span></span>

[<span data-ttu-id="637ae-141">Класс API</span><span class="sxs-lookup"><span data-stu-id="637ae-141">Api class</span></span>](./api-class.md)

[<span data-ttu-id="637ae-142">Члены API</span><span class="sxs-lookup"><span data-stu-id="637ae-142">Api members</span></span>](./api-members.md)

[<span data-ttu-id="637ae-143">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="637ae-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
