---
description: Дополнительные сведения о методе API. Жетготосекондариндексбукмарк
title: API. Жетготосекондариндексбукмарк, метод
TOCTitle: 'JetGotoSecondaryIndexBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotosecondaryindexbookmark(v=EXCHG.10)
ms:contentKeyID: 55100755
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoSecondaryIndexBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: af146236a2a5398dfb0b7b81f42dcfc6227a6de9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693680"
---
# <a name="apijetgotosecondaryindexbookmark-method"></a><span data-ttu-id="112b4-103">API. Жетготосекондариндексбукмарк, метод</span><span class="sxs-lookup"><span data-stu-id="112b4-103">Api.JetGotoSecondaryIndexBookmark method</span></span>

<span data-ttu-id="112b4-104">Позиционирует курсор на запись индекса, связанную с закладкой дополнительного индекса.</span><span class="sxs-lookup"><span data-stu-id="112b4-104">Positions a cursor to an index entry that is associated with the specified secondary index bookmark.</span></span> <span data-ttu-id="112b4-105">Закладку вторичного индекса необходимо использовать с тем же индексом для той же таблицы, из которой она была первоначально извлечена.</span><span class="sxs-lookup"><span data-stu-id="112b4-105">The secondary index bookmark must be used with the same index over the same table from which it was originally retrieved.</span></span> <span data-ttu-id="112b4-106">Закладку вторичного индекса для записи индекса можно получить с помощью Жетготосекондариндексбукмарк (JET_SESID, JET_TABLEID, \[ \] , Int32, \[ \] , Int32, готосекондариндексбукмаркгрбит).</span><span class="sxs-lookup"><span data-stu-id="112b4-106">The secondary index bookmark for an index entry can be retrieved using JetGotoSecondaryIndexBookmark(JET_SESID, JET_TABLEID, \[\], Int32, \[\], Int32, GotoSecondaryIndexBookmarkGrbit).</span></span>

<span data-ttu-id="112b4-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="112b4-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="112b4-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="112b4-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="112b4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="112b4-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoSecondaryIndexBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    secondaryKey As Byte(), _
    secondaryKeySize As Integer, _
    primaryKey As Byte(), _
    primaryKeySize As Integer, _
    grbit As GotoSecondaryIndexBookmarkGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim secondaryKey As Byte()
Dim secondaryKeySize As Integer
Dim primaryKey As Byte()
Dim primaryKeySize As Integer
Dim grbit As GotoSecondaryIndexBookmarkGrbitApi.JetGotoSecondaryIndexBookmark(sesid, _
    tableid, secondaryKey, secondaryKeySize, _
    primaryKey, primaryKeySize, grbit)
```

``` csharp
public static void JetGotoSecondaryIndexBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] secondaryKey,
    int secondaryKeySize,
    byte[] primaryKey,
    int primaryKeySize,
    GotoSecondaryIndexBookmarkGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="112b4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="112b4-110">Parameters</span></span>

  - <span data-ttu-id="112b4-111">сесид</span><span class="sxs-lookup"><span data-stu-id="112b4-111">sesid</span></span>  
    <span data-ttu-id="112b4-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="112b4-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="112b4-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="112b4-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-114">TableID</span><span class="sxs-lookup"><span data-stu-id="112b4-114">tableid</span></span>  
    <span data-ttu-id="112b4-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="112b4-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="112b4-116">Курсор таблицы для позиционирования.</span><span class="sxs-lookup"><span data-stu-id="112b4-116">The table cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-117">secondaryKey</span><span class="sxs-lookup"><span data-stu-id="112b4-117">secondaryKey</span></span>  
    <span data-ttu-id="112b4-118">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="112b4-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="112b4-119">Буфер, содержащий вторичный ключ.</span><span class="sxs-lookup"><span data-stu-id="112b4-119">The buffer that contains the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-120">секондарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="112b4-120">secondaryKeySize</span></span>  
    <span data-ttu-id="112b4-121">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="112b4-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="112b4-122">Размер вторичного ключа.</span><span class="sxs-lookup"><span data-stu-id="112b4-122">The size of the secondary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-123">primaryKey</span><span class="sxs-lookup"><span data-stu-id="112b4-123">primaryKey</span></span>  
    <span data-ttu-id="112b4-124">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="112b4-124">Type: \[\]</span></span>  
    
    <span data-ttu-id="112b4-125">Буфер, содержащий первичный ключ.</span><span class="sxs-lookup"><span data-stu-id="112b4-125">The buffer that contains the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-126">примарикэйсизе</span><span class="sxs-lookup"><span data-stu-id="112b4-126">primaryKeySize</span></span>  
    <span data-ttu-id="112b4-127">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="112b4-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="112b4-128">Размер первичного ключа.</span><span class="sxs-lookup"><span data-stu-id="112b4-128">The size of the primary key.</span></span>

<!-- end list -->

  - <span data-ttu-id="112b4-129">грбит</span><span class="sxs-lookup"><span data-stu-id="112b4-129">grbit</span></span>  
    <span data-ttu-id="112b4-130">Тип: [Microsoft. ISAM. ESENT. Interop. готосекондариндексбукмаркгрбит](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="112b4-130">Type: [Microsoft.Isam.Esent.Interop.GotoSecondaryIndexBookmarkGrbit](./gotosecondaryindexbookmarkgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="112b4-131">Параметры для размещения закладки.</span><span class="sxs-lookup"><span data-stu-id="112b4-131">Options for positioning the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="112b4-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="112b4-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="112b4-133">Справочник</span><span class="sxs-lookup"><span data-stu-id="112b4-133">Reference</span></span>

[<span data-ttu-id="112b4-134">Класс API</span><span class="sxs-lookup"><span data-stu-id="112b4-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="112b4-135">Члены API</span><span class="sxs-lookup"><span data-stu-id="112b4-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="112b4-136">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="112b4-136">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
