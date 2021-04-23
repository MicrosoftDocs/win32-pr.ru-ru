---
description: 'Дополнительные сведения: метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, Ретриевеколумнгрбит)'
title: Метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, Ретриевеколумнгрбит)
TOCTitle: RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Text.Encoding,Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumnasstring(v=EXCHG.10)
ms:contentKeyID: 55100862
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumnAsString
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2008726577bac37e129a887af2d8b1747323c81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693796"
---
# <a name="apiretrievecolumnasstring-method-jet_sesid-jet_tableid-jet_columnid-encoding-retrievecolumngrbit"></a><span data-ttu-id="79643-103">Метод API. Ретриевеколумнасстринг (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, Ретриевеколумнгрбит)</span><span class="sxs-lookup"><span data-stu-id="79643-103">Api.RetrieveColumnAsString method (JET_SESID, JET_TABLEID, JET_COLUMNID, Encoding, RetrieveColumnGrbit)</span></span>

<span data-ttu-id="79643-104">Извлекает значение строкового столбца из текущей записи.</span><span class="sxs-lookup"><span data-stu-id="79643-104">Retrieves a string column value from the current record.</span></span> <span data-ttu-id="79643-105">Запись — это запись, связанная с записью индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="79643-105">The record is that record associated with the index entry at the current position of the cursor.</span></span>

<span data-ttu-id="79643-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="79643-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="79643-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="79643-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="79643-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79643-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function RetrieveColumnAsString ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    encoding As Encoding, _
    grbit As RetrieveColumnGrbit _
) As String
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim encoding As Encoding
Dim grbit As RetrieveColumnGrbit
Dim returnValue As String

returnValue = Api.RetrieveColumnAsString(sesid, _
    tableid, columnid, encoding, grbit)
```

``` csharp
public static string RetrieveColumnAsString(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    Encoding encoding,
    RetrieveColumnGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="79643-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="79643-109">Parameters</span></span>

  - <span data-ttu-id="79643-110">сесид</span><span class="sxs-lookup"><span data-stu-id="79643-110">sesid</span></span>  
    <span data-ttu-id="79643-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79643-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="79643-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="79643-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="79643-113">TableID</span><span class="sxs-lookup"><span data-stu-id="79643-113">tableid</span></span>  
    <span data-ttu-id="79643-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79643-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="79643-115">Курсор, из которого извлекается столбец.</span><span class="sxs-lookup"><span data-stu-id="79643-115">The cursor to retrieve the column from.</span></span>

<!-- end list -->

  - <span data-ttu-id="79643-116">columnid</span><span class="sxs-lookup"><span data-stu-id="79643-116">columnid</span></span>  
    <span data-ttu-id="79643-117">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="79643-117">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="79643-118">Значение columnid, которое необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="79643-118">The columnid to retrieve.</span></span>

<!-- end list -->

  - <span data-ttu-id="79643-119">encoding</span><span class="sxs-lookup"><span data-stu-id="79643-119">encoding</span></span>  
    <span data-ttu-id="79643-120">Тип: [System. Text. Encoding](/dotnet/api/system.text.encoding)</span><span class="sxs-lookup"><span data-stu-id="79643-120">Type: [System.Text.Encoding](/dotnet/api/system.text.encoding)</span></span>  
    
    <span data-ttu-id="79643-121">Кодировка строки, используемая при преобразовании данных.</span><span class="sxs-lookup"><span data-stu-id="79643-121">The string encoding to use when converting data.</span></span>

<!-- end list -->

  - <span data-ttu-id="79643-122">грбит</span><span class="sxs-lookup"><span data-stu-id="79643-122">grbit</span></span>  
    <span data-ttu-id="79643-123">Тип: [Microsoft. ISAM. ESENT. Interop. ретриевеколумнгрбит](./retrievecolumngrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="79643-123">Type: [Microsoft.Isam.Esent.Interop.RetrieveColumnGrbit](./retrievecolumngrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="79643-124">Параметры извлечения.</span><span class="sxs-lookup"><span data-stu-id="79643-124">Retrieval options.</span></span>

#### <a name="return-value"></a><span data-ttu-id="79643-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79643-125">Return value</span></span>

<span data-ttu-id="79643-126">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="79643-126">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="79643-127">Данные, полученные из столбца в виде строки.</span><span class="sxs-lookup"><span data-stu-id="79643-127">The data retrieved from the column as a string.</span></span> <span data-ttu-id="79643-128">Значение null, если столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="79643-128">Null if the column is null.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79643-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79643-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="79643-130">Справочник</span><span class="sxs-lookup"><span data-stu-id="79643-130">Reference</span></span>

[<span data-ttu-id="79643-131">Класс API</span><span class="sxs-lookup"><span data-stu-id="79643-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="79643-132">Члены API</span><span class="sxs-lookup"><span data-stu-id="79643-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="79643-133">Перегрузка Ретриевеколумнасстринг</span><span class="sxs-lookup"><span data-stu-id="79643-133">RetrieveColumnAsString overload</span></span>](./api.retrievecolumnasstring-method.md)

[<span data-ttu-id="79643-134">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="79643-134">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
