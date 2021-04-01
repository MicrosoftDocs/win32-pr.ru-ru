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
ms.openlocfilehash: b0a25e78ca291271a96d06e5c0bf61c691acd4de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072672"
---
# <a name="apijetgetsecondaryindexbookmark-method"></a><span data-ttu-id="0c866-103">API. Жетжетсекондариндексбукмарк, метод</span><span class="sxs-lookup"><span data-stu-id="0c866-103">Api.JetGetSecondaryIndexBookmark method</span></span>

<span data-ttu-id="0c866-104">Извлекает специальную закладку для записи вторичного индекса в текущем положении курсора.</span><span class="sxs-lookup"><span data-stu-id="0c866-104">Retrieves a special bookmark for the secondary index entry at the current position of a cursor.</span></span> <span data-ttu-id="0c866-105">Эту закладку можно использовать для эффективного перемещения курсора обратно к той же записи индекса с помощью Жетготосекондариндексбукмарк.</span><span class="sxs-lookup"><span data-stu-id="0c866-105">This bookmark can then be used to efficiently reposition that cursor back to the same index entry using JetGotoSecondaryIndexBookmark.</span></span> <span data-ttu-id="0c866-106">Это наиболее полезно при изменении расположения вторичного индекса, который содержит дублирующиеся ключи или содержит несколько записей индекса для одной и той же записи.</span><span class="sxs-lookup"><span data-stu-id="0c866-106">This is most useful when repositioning on a secondary index that contains duplicate keys or that contains multiple index entries for the same record.</span></span>

<span data-ttu-id="0c866-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c866-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c866-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c866-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c866-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c866-109">Syntax</span></span>

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

#### <a name="parameters"></a><span data-ttu-id="0c866-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c866-110">Parameters</span></span>

  - <span data-ttu-id="0c866-111">сесид</span><span class="sxs-lookup"><span data-stu-id="0c866-111">sesid</span></span>  
    <span data-ttu-id="0c866-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c866-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="0c866-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="0c866-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-114">TableID</span><span class="sxs-lookup"><span data-stu-id="0c866-114">tableid</span></span>  
    <span data-ttu-id="0c866-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c866-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="0c866-116">Курсор, из которого извлекается закладка.</span><span class="sxs-lookup"><span data-stu-id="0c866-116">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="0c866-117">secondaryKey</span></span>  
    <span data-ttu-id="0c866-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="0c866-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="0c866-119">Выходной буфер для вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-119">Output buffer for the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-120">секондарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="0c866-120">secondaryKeySize</span></span>  
    <span data-ttu-id="0c866-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c866-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0c866-122">Размер буфера вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-122">Size of the secondary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-123">актуалсекондарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="0c866-123">actualSecondaryKeySize</span></span>  
    <span data-ttu-id="0c866-124">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c866-124">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0c866-125">Возвращает размер вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-125">Returns the size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-126">primaryKey</span><span class="sxs-lookup"><span data-stu-id="0c866-126">primaryKey</span></span>  
    <span data-ttu-id="0c866-127">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="0c866-127">Type: \[\]</span></span>  
    
    <span data-ttu-id="0c866-128">Выходной буфер для первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-128">Output buffer for the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-129">примарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="0c866-129">primaryKeySize</span></span>  
    <span data-ttu-id="0c866-130">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c866-130">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0c866-131">Размер буфера первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-131">Size of the primary key buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-132">актуалпримарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="0c866-132">actualPrimaryKeySize</span></span>  
    <span data-ttu-id="0c866-133">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0c866-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0c866-134">Возвращает размер первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="0c866-134">Returns the size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="0c866-135">грбит</span><span class="sxs-lookup"><span data-stu-id="0c866-135">grbit</span></span>  
    <span data-ttu-id="0c866-136">Тип: [Microsoft. ISAM. ESENT. Interop. жетсекондариндексбукмаркгрбит](./getsecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0c866-136">Type: [Microsoft.Isam.Esent.Interop.GetSecondaryIndexBookmarkGrbit](./getsecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0c866-137">Параметры для вызова.</span><span class="sxs-lookup"><span data-stu-id="0c866-137">Options for the call.</span></span>

## <a name="see-also"></a><span data-ttu-id="0c866-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c866-138">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c866-139">Справочник</span><span class="sxs-lookup"><span data-stu-id="0c866-139">Reference</span></span>

[<span data-ttu-id="0c866-140">Класс API</span><span class="sxs-lookup"><span data-stu-id="0c866-140">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0c866-141">Члены API</span><span class="sxs-lookup"><span data-stu-id="0c866-141">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0c866-142">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0c866-142">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
