---
description: Дополнительные сведения о методе API. JetOpenTempTable3
title: Метод Api.JetOpenTempTable3
TOCTitle: 'JetOpenTempTable3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_COLUMNDEF[],System.Int32,Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX,Microsoft.Isam.Esent.Interop.TempTableGrbit,Microsoft.Isam.Esent.Interop.JET_TABLEID@,Microsoft.Isam.Esent.Interop.JET_COLUMNID[])
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetopentemptable3(v=EXCHG.10)
ms:contentKeyID: 55100774
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOpenTempTable3
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e88b5413492c0ae00ed41e569afb49ca6c18e51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693630"
---
# <a name="apijetopentemptable3-method"></a><span data-ttu-id="7a1ec-103">Метод Api.JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="7a1ec-103">Api.JetOpenTempTable3 method</span></span>

<span data-ttu-id="7a1ec-104">Создает временную таблицу с одним индексом.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-104">Creates a temporary table with a single index.</span></span> <span data-ttu-id="7a1ec-105">Временная таблица хранит и извлекает записи так же, как обычная таблица, созданная с помощью Жеткреатетаблеколумниндекс.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-105">A temporary table stores and retrieves records just like an ordinary table created using JetCreateTableColumnIndex.</span></span> <span data-ttu-id="7a1ec-106">Однако временные таблицы выполняются гораздо быстрее, чем обычные таблицы, в связи с их постоянным характером.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-106">However, temporary tables are much faster than ordinary tables due to their volatile nature.</span></span> <span data-ttu-id="7a1ec-107">Они также могут использоваться для очень быстрой сортировки и удаления дубликатов наборов записей при обращении к ним только последовательно.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-107">They can also be used to very quickly sort and perform duplicate removal on record sets when accessed in a purely sequential manner.</span></span> <span data-ttu-id="7a1ec-108">См. также [жетопентемптабле (JET_SESID, \[ \] , Int32, темптаблегрбит, JET_TABLEID, \[ \] )](./api.jetopentemptable-method.md), [жетопентемпораритабле (JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span><span class="sxs-lookup"><span data-stu-id="7a1ec-108">Also see [JetOpenTempTable(JET_SESID, \[\], Int32, TempTableGrbit, JET_TABLEID, \[\])](./api.jetopentemptable-method.md), [JetOpenTemporaryTable(JET_SESID, JET_OPENTEMPORARYTABLE)](./vistaapi.jetopentemporarytable-method.md).</span></span>

<span data-ttu-id="7a1ec-109">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7a1ec-110">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1ec-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a1ec-111">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOpenTempTable3 ( _
    sesid As JET_SESID, _
    columns As JET_COLUMNDEF(), _
    numColumns As Integer, _
    unicodeindex As JET_UNICODEINDEX, _
    grbit As TempTableGrbit, _
    <OutAttribute> ByRef tableid As JET_TABLEID, _
    columnids As JET_COLUMNID() _
)
'Usage
Dim sesid As JET_SESID
Dim columns As JET_COLUMNDEF()
Dim numColumns As Integer
Dim unicodeindex As JET_UNICODEINDEX
Dim grbit As TempTableGrbit
Dim tableid As JET_TABLEID
Dim columnids As JET_COLUMNID()

Api.JetOpenTempTable3(sesid, columns, _
    numColumns, unicodeindex, grbit, _
    tableid, columnids)
```

``` csharp
public static void JetOpenTempTable3(
    JET_SESID sesid,
    JET_COLUMNDEF[] columns,
    int numColumns,
    JET_UNICODEINDEX unicodeindex,
    TempTableGrbit grbit,
    out JET_TABLEID tableid,
    JET_COLUMNID[] columnids
)
```

#### <a name="parameters"></a><span data-ttu-id="7a1ec-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a1ec-112">Parameters</span></span>

  - <span data-ttu-id="7a1ec-113">сесид</span><span class="sxs-lookup"><span data-stu-id="7a1ec-113">sesid</span></span>  
    <span data-ttu-id="7a1ec-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-114">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7a1ec-115">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-115">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-116">столбцы</span><span class="sxs-lookup"><span data-stu-id="7a1ec-116">columns</span></span>  
    <span data-ttu-id="7a1ec-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="7a1ec-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="7a1ec-118">Определения столбцов для столбцов, созданных во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-118">Column definitions for the columns created in the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-119">нумколумнс</span><span class="sxs-lookup"><span data-stu-id="7a1ec-119">numColumns</span></span>  
    <span data-ttu-id="7a1ec-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7a1ec-121">Число определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-121">Number of column definitions.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-122">уникодеиндекс</span><span class="sxs-lookup"><span data-stu-id="7a1ec-122">unicodeindex</span></span>  
    <span data-ttu-id="7a1ec-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-123">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  
    
    <span data-ttu-id="7a1ec-124">КОД локали и флаги нормализации, которые будут использоваться для сравнения данных любого ключевого столбца Юникода во временной таблице.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-124">The Locale ID and normalization flags that will be used to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="7a1ec-125">Если этот параметр отсутствует, используются параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-125">When this is not present then the default options are used.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-126">грбит</span><span class="sxs-lookup"><span data-stu-id="7a1ec-126">grbit</span></span>  
    <span data-ttu-id="7a1ec-127">Тип: [Microsoft. ISAM. ESENT. Interop. темптаблегрбит](./temptablegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-127">Type: [Microsoft.Isam.Esent.Interop.TempTableGrbit](./temptablegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7a1ec-128">Параметры создания таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-128">Table creation options.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-129">TableID</span><span class="sxs-lookup"><span data-stu-id="7a1ec-129">tableid</span></span>  
    <span data-ttu-id="7a1ec-130">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7a1ec-130">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="7a1ec-131">Возвращает TableID временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-131">Returns the tableid of the temporary table.</span></span> <span data-ttu-id="7a1ec-132">Закрытие этого TableID с помощью [жетклосетабле (JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) освобождает ресурсы, связанные с временной таблицей.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-132">Closing this tableid with [JetCloseTable(JET_SESID, JET_TABLEID)](./api.jetclosetable-method.md) frees the resources associated with the temporary table.</span></span>

<!-- end list -->

  - <span data-ttu-id="7a1ec-133">колумнидс</span><span class="sxs-lookup"><span data-stu-id="7a1ec-133">columnids</span></span>  
    <span data-ttu-id="7a1ec-134">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="7a1ec-134">Type: \[\]</span></span>  
    
    <span data-ttu-id="7a1ec-135">Выходной буфер, который получает массив идентификаторов столбцов, созданных во время создания временной таблицы.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-135">The output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="7a1ec-136">Идентификаторы столбцов в этом массиве будут точно соответствовать входному массиву определений столбцов.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-136">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="7a1ec-137">В результате размер этого буфера должен соответствовать размеру входного массива.</span><span class="sxs-lookup"><span data-stu-id="7a1ec-137">As a result, the size of this buffer must correspond to the size of the input array.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a1ec-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a1ec-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7a1ec-139">Справочник</span><span class="sxs-lookup"><span data-stu-id="7a1ec-139">Reference</span></span>

[<span data-ttu-id="7a1ec-140">Класс API</span><span class="sxs-lookup"><span data-stu-id="7a1ec-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7a1ec-141">Члены API</span><span class="sxs-lookup"><span data-stu-id="7a1ec-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7a1ec-142">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7a1ec-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
