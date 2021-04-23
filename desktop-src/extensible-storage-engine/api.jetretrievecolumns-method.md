---
description: Дополнительные сведения о методе API. Жетретриевеколумнс
title: API. Жетретриевеколумнс, метод
TOCTitle: 'JetRetrieveColumns method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumns(v=EXCHG.10)
ms:contentKeyID: 55100797
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumns
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d3fd4db2ce8cbcad5f74db7d4c95363aa68e9b38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701420"
---
# <a name="apijetretrievecolumns-method"></a><span data-ttu-id="603cc-103">API. Жетретриевеколумнс, метод</span><span class="sxs-lookup"><span data-stu-id="603cc-103">Api.JetRetrieveColumns method</span></span>

<span data-ttu-id="603cc-104">Получает несколько значений столбцов из текущей записи в одной операции.</span><span class="sxs-lookup"><span data-stu-id="603cc-104">Retrieves multiple column values from the current record in a single operation.</span></span> <span data-ttu-id="603cc-105">Массив структур JET_RETRIEVECOLUMN используется для описания набора значений столбцов для извлечения, а также для описания выходных буферов для каждого извлекаемого значения столбца.</span><span class="sxs-lookup"><span data-stu-id="603cc-105">An array of JET_RETRIEVECOLUMN structures is used to describe the set of column values to be retrieved, and to describe output buffers for each column value to be retrieved.</span></span>

<span data-ttu-id="603cc-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="603cc-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="603cc-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="603cc-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="603cc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="603cc-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetRetrieveColumns ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    retrievecolumns As JET_RETRIEVECOLUMN(), _
    numColumns As Integer _
) As JET_wrn
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim retrievecolumns As JET_RETRIEVECOLUMN()
Dim numColumns As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetRetrieveColumns(sesid, _
    tableid, retrievecolumns, numColumns)
```

``` csharp
public static JET_wrn JetRetrieveColumns(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_RETRIEVECOLUMN[] retrievecolumns,
    int numColumns
)
```

#### <a name="parameters"></a><span data-ttu-id="603cc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="603cc-109">Parameters</span></span>

  - <span data-ttu-id="603cc-110">сесид</span><span class="sxs-lookup"><span data-stu-id="603cc-110">sesid</span></span>  
    <span data-ttu-id="603cc-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="603cc-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="603cc-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="603cc-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="603cc-113">TableID</span><span class="sxs-lookup"><span data-stu-id="603cc-113">tableid</span></span>  
    <span data-ttu-id="603cc-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="603cc-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="603cc-115">Курсор, из которого извлекаются данные.</span><span class="sxs-lookup"><span data-stu-id="603cc-115">The cursor to retrieve the data from.</span></span>

<!-- end list -->

  - <span data-ttu-id="603cc-116">ретриевеколумнс</span><span class="sxs-lookup"><span data-stu-id="603cc-116">retrievecolumns</span></span>  
    <span data-ttu-id="603cc-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="603cc-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="603cc-118">Массив из одного или нескольких объектов [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) , описывающих извлекаемые данные.</span><span class="sxs-lookup"><span data-stu-id="603cc-118">An array of one or more [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) objects describing the data to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="603cc-119">нумколумнс</span><span class="sxs-lookup"><span data-stu-id="603cc-119">numColumns</span></span>  
    <span data-ttu-id="603cc-120">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="603cc-120">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="603cc-121">Число записей в массиве Columns.</span><span class="sxs-lookup"><span data-stu-id="603cc-121">The number of entries in the columns array.</span></span>

#### <a name="return-value"></a><span data-ttu-id="603cc-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="603cc-122">Return value</span></span>

<span data-ttu-id="603cc-123">Тип: [Microsoft.ISAM.ESENT.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="603cc-123">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="603cc-124">Если любой полученный столбец усекается из-за недостаточного размера буфера, API возвратит [буффертрункатед](./jet-wrn-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="603cc-124">If any column retrieved is truncated due to an insufficient length buffer, then the API will return [BufferTruncated](./jet-wrn-enumeration.md).</span></span> <span data-ttu-id="603cc-125">Однако другие ошибки JET_wrnColumnNull возвращаются только в поле ошибки объекта [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) .</span><span class="sxs-lookup"><span data-stu-id="603cc-125">However other errors JET_wrnColumnNull are returned only in the error field of the [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) object.</span></span>  

## <a name="see-also"></a><span data-ttu-id="603cc-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="603cc-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="603cc-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="603cc-127">Reference</span></span>

[<span data-ttu-id="603cc-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="603cc-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="603cc-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="603cc-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="603cc-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="603cc-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
