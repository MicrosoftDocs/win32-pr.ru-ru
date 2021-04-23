---
description: 'Дополнительные сведения: метод API. Макекэй (JET_SESID, JET_TABLEID, Double, Макекэйгрбит)'
title: Метод API. Макекэй (JET_SESID, JET_TABLEID, Double, Макекэйгрбит)
TOCTitle: MakeKey method (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.MakeKey(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Double,Microsoft.Isam.Esent.Interop.MakeKeyGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.makekey(v=EXCHG.10)
ms:contentKeyID: 55100839
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.MakeKey
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b0e78b2828ae8727fea7b7909c903bbc7381505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897982"
---
# <a name="apimakekey-method-jet_sesid-jet_tableid-double-makekeygrbit"></a><span data-ttu-id="1bfaa-103">Метод API. Макекэй (JET_SESID, JET_TABLEID, Double, Макекэйгрбит)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-103">Api.MakeKey method (JET_SESID, JET_TABLEID, Double, MakeKeyGrbit)</span></span>

<span data-ttu-id="1bfaa-104">Конструирует ключ поиска, который затем может использоваться [жетсик (JET_SESID, JET_TABLEID, сикгрбит)](./api.jetseek-method.md) и [жетсетиндексранже (JET_SESID, JET_TABLEID, сетиндексранжегрбит)](./api.jetsetindexrange-method.md).</span><span class="sxs-lookup"><span data-stu-id="1bfaa-104">Constructs a search key that may then be used by [JetSeek(JET_SESID, JET_TABLEID, SeekGrbit)](./api.jetseek-method.md) and [JetSetIndexRange(JET_SESID, JET_TABLEID, SetIndexRangeGrbit)](./api.jetsetindexrange-method.md).</span></span>

<span data-ttu-id="1bfaa-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1bfaa-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1bfaa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1bfaa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub MakeKey ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    data As Double, _
    grbit As MakeKeyGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim data As Double
Dim grbit As MakeKeyGrbitApi.MakeKey(sesid, tableid, data, _
    grbit)
```

``` csharp
public static void MakeKey(
    JET_SESID sesid,
    JET_TABLEID tableid,
    double data,
    MakeKeyGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1bfaa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1bfaa-108">Parameters</span></span>

  - <span data-ttu-id="1bfaa-109">сесид</span><span class="sxs-lookup"><span data-stu-id="1bfaa-109">sesid</span></span>  
    <span data-ttu-id="1bfaa-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1bfaa-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="1bfaa-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1bfaa-112">TableID</span><span class="sxs-lookup"><span data-stu-id="1bfaa-112">tableid</span></span>  
    <span data-ttu-id="1bfaa-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1bfaa-114">Курсор, на котором создается ключ.</span><span class="sxs-lookup"><span data-stu-id="1bfaa-114">The cursor to create the key on.</span></span>

<!-- end list -->

  - <span data-ttu-id="1bfaa-115">.</span><span class="sxs-lookup"><span data-stu-id="1bfaa-115">data</span></span>  
    <span data-ttu-id="1bfaa-116">Тип: [System. Double](/dotnet/api/system.double)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-116">Type: [System.Double](/dotnet/api/system.double)</span></span>  
    
    <span data-ttu-id="1bfaa-117">Данные столбца для текущего ключевого столбца текущего индекса.</span><span class="sxs-lookup"><span data-stu-id="1bfaa-117">Column data for the current key column of the current index.</span></span>

<!-- end list -->

  - <span data-ttu-id="1bfaa-118">грбит</span><span class="sxs-lookup"><span data-stu-id="1bfaa-118">grbit</span></span>  
    <span data-ttu-id="1bfaa-119">Тип: [Microsoft. ISAM. ESENT. Interop. макекэйгрбит](./makekeygrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1bfaa-119">Type: [Microsoft.Isam.Esent.Interop.MakeKeyGrbit](./makekeygrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1bfaa-120">Ключевые параметры.</span><span class="sxs-lookup"><span data-stu-id="1bfaa-120">Key options.</span></span>

## <a name="see-also"></a><span data-ttu-id="1bfaa-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1bfaa-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1bfaa-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="1bfaa-122">Reference</span></span>

[<span data-ttu-id="1bfaa-123">Класс API</span><span class="sxs-lookup"><span data-stu-id="1bfaa-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1bfaa-124">Члены API</span><span class="sxs-lookup"><span data-stu-id="1bfaa-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1bfaa-125">Перегрузка Макекэй</span><span class="sxs-lookup"><span data-stu-id="1bfaa-125">MakeKey overload</span></span>](./api.makekey-method.md)

[<span data-ttu-id="1bfaa-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1bfaa-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
