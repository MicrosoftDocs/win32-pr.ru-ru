---
description: Дополнительные сведения о методе API. JetSetCurrentIndex4
title: API. JetSetCurrentIndex4, метод
TOCTitle: 'JetSetCurrentIndex4 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex4(v=EXCHG.10)
ms:contentKeyID: 55100806
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex4
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d2b9319554b998175b3f533c6cd5f4c2d05ba02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673217"
---
# <a name="apijetsetcurrentindex4-method"></a><span data-ttu-id="4ddab-103">API. JetSetCurrentIndex4, метод</span><span class="sxs-lookup"><span data-stu-id="4ddab-103">Api.JetSetCurrentIndex4 method</span></span>

<span data-ttu-id="4ddab-104">Задает текущий индекс курсора.</span><span class="sxs-lookup"><span data-stu-id="4ddab-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="4ddab-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4ddab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4ddab-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4ddab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4ddab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4ddab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex4 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    indexid As JET_INDEXID, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim indexid As JET_INDEXID
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex4(sesid, _
    tableid, index, indexid, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex4(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    JET_INDEXID indexid,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="4ddab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4ddab-108">Parameters</span></span>

  - <span data-ttu-id="4ddab-109">сесид</span><span class="sxs-lookup"><span data-stu-id="4ddab-109">sesid</span></span>  
    <span data-ttu-id="4ddab-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ddab-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="4ddab-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="4ddab-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddab-112">TableID</span><span class="sxs-lookup"><span data-stu-id="4ddab-112">tableid</span></span>  
    <span data-ttu-id="4ddab-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="4ddab-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="4ddab-114">Курсор, для которого задается индекс.</span><span class="sxs-lookup"><span data-stu-id="4ddab-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddab-115">index</span><span class="sxs-lookup"><span data-stu-id="4ddab-115">index</span></span>  
    <span data-ttu-id="4ddab-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4ddab-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="4ddab-117">Имя выбранного индекса.</span><span class="sxs-lookup"><span data-stu-id="4ddab-117">The name of the index to be selected.</span></span> <span data-ttu-id="4ddab-118">Если это значение равно null или пуст, первичный индекс будет выбран.</span><span class="sxs-lookup"><span data-stu-id="4ddab-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddab-119">indexid</span><span class="sxs-lookup"><span data-stu-id="4ddab-119">indexid</span></span>  
    <span data-ttu-id="4ddab-120">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="4ddab-120">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="4ddab-121">Идентификатор выбираемого индекса.</span><span class="sxs-lookup"><span data-stu-id="4ddab-121">The id of the index to select.</span></span> <span data-ttu-id="4ddab-122">Этот идентификатор можно получить с помощью Жетжетиндексинфо или Жетжеттаблеиндексинфо с параметром [индексид](./jet-idxinfo-enumeration.md) .</span><span class="sxs-lookup"><span data-stu-id="4ddab-122">This id can be obtained using JetGetIndexInfo or JetGetTableIndexInfo with the [IndexId](./jet-idxinfo-enumeration.md) option.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddab-123">грбит</span><span class="sxs-lookup"><span data-stu-id="4ddab-123">grbit</span></span>  
    <span data-ttu-id="4ddab-124">Тип: [Microsoft. ISAM. ESENT. Interop. сеткуррентиндексгрбит](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="4ddab-124">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="4ddab-125">Задайте параметры индекса.</span><span class="sxs-lookup"><span data-stu-id="4ddab-125">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="4ddab-126">итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="4ddab-126">itagSequence</span></span>  
    <span data-ttu-id="4ddab-127">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4ddab-127">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="4ddab-128">Порядковый номер значения столбца с несколькими значениями, который будет использоваться для позиционирования курсора на новом индексе.</span><span class="sxs-lookup"><span data-stu-id="4ddab-128">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="4ddab-129">Этот параметр используется только в сочетании с параметром [OnMove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="4ddab-129">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="4ddab-130">Если этот параметр отсутствует или имеет значение 0, предполагается, что оно равно 1.</span><span class="sxs-lookup"><span data-stu-id="4ddab-130">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ddab-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4ddab-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4ddab-132">Справочник</span><span class="sxs-lookup"><span data-stu-id="4ddab-132">Reference</span></span>

[<span data-ttu-id="4ddab-133">Класс API</span><span class="sxs-lookup"><span data-stu-id="4ddab-133">Api class</span></span>](./api-class.md)

[<span data-ttu-id="4ddab-134">Члены API</span><span class="sxs-lookup"><span data-stu-id="4ddab-134">Api members</span></span>](./api-members.md)

[<span data-ttu-id="4ddab-135">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4ddab-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
