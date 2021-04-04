---
description: Дополнительные сведения о методе API. Жетмакекэй
title: API. Жетмакекэй, метод
TOCTitle: 'JetMakeKey method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetMakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetmakekey(v=EXCHG.10)
ms:contentKeyID: 55100764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetMakeKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 13db6e7106f5312e03ffa5acfbd86c72d38c6edb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999369"
---
# <a name="apijetmakekey-method"></a><span data-ttu-id="3ae34-103">API. Жетмакекэй, метод</span><span class="sxs-lookup"><span data-stu-id="3ae34-103">Api.JetMakeKey method</span></span>

<span data-ttu-id="3ae34-104">Конструирует ключи поиска, которые затем могут использоваться [жетсик (JET_SESID, JET_TABLEID, сикгрбит)](./api.jetseek-method.md) и [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="3ae34-104">Constructs search keys that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="3ae34-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3ae34-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3ae34-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3ae34-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae34-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ae34-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetMakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Byte(), _
    dataSize As Integer, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Byte()
Dim dataSize As Integer
Dim grbit As MakeKeyGrbitApi.JetMakeKey(sesid, tableid, data, _
    dataSize, grbit)
```

``` csharp
public static void JetMakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] data,
    int dataSize,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="3ae34-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ae34-108">Parameters</span></span>

  - <span data-ttu-id="3ae34-109">сесид</span><span class="sxs-lookup"><span data-stu-id="3ae34-109">sesid</span></span>  
    <span data-ttu-id="3ae34-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3ae34-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="3ae34-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="3ae34-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="3ae34-112">TableID</span><span class="sxs-lookup"><span data-stu-id="3ae34-112">tableid</span></span>  
    <span data-ttu-id="3ae34-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="3ae34-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="3ae34-114">Курсор, на котором создается ключ.</span><span class="sxs-lookup"><span data-stu-id="3ae34-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="3ae34-115">.</span><span class="sxs-lookup"><span data-stu-id="3ae34-115">data</span></span>  
    <span data-ttu-id="3ae34-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae34-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="3ae34-117">Данные столбца для текущего ключевого столбца текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="3ae34-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="3ae34-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="3ae34-118">dataSize</span></span>  
    <span data-ttu-id="3ae34-119">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="3ae34-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="3ae34-120">Размер данных.</span><span class="sxs-lookup"><span data-stu-id="3ae34-120">Size of the data.</span></span>

<!-- end list -->

  - <span data-ttu-id="3ae34-121">грбит</span><span class="sxs-lookup"><span data-stu-id="3ae34-121">grbit</span></span>  
    <span data-ttu-id="3ae34-122">Тип: [Microsoft. ISAM. ESENT. Interop. макекэйгрбит](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="3ae34-122">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="3ae34-123">Ключевые параметры.</span><span class="sxs-lookup"><span data-stu-id="3ae34-123">Key options.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae34-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ae34-124">Remarks</span></span>

<span data-ttu-id="3ae34-125">Функции Макекэй предоставляют ключевые функции, относящиеся к типу данных.</span><span class="sxs-lookup"><span data-stu-id="3ae34-125">The MakeKey functions provide datatype-specific make key functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ae34-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ae34-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3ae34-127">Справочник</span><span class="sxs-lookup"><span data-stu-id="3ae34-127">Reference</span></span>

[<span data-ttu-id="3ae34-128">Класс API</span><span class="sxs-lookup"><span data-stu-id="3ae34-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="3ae34-129">Члены API</span><span class="sxs-lookup"><span data-stu-id="3ae34-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="3ae34-130">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="3ae34-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
