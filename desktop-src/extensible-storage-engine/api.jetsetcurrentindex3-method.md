---
description: Дополнительные сведения о методе API. JetSetCurrentIndex3
title: API. JetSetCurrentIndex3, метод
TOCTitle: 'JetSetCurrentIndex3 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex3(v=EXCHG.10)
ms:contentKeyID: 55100805
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex3
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c56f259a35026bb47a5e58b7b364b52d9bedbc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647461"
---
# <a name="apijetsetcurrentindex3-method"></a><span data-ttu-id="12c79-103">API. JetSetCurrentIndex3, метод</span><span class="sxs-lookup"><span data-stu-id="12c79-103">Api.JetSetCurrentIndex3 method</span></span>

<span data-ttu-id="12c79-104">Задает текущий индекс курсора.</span><span class="sxs-lookup"><span data-stu-id="12c79-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="12c79-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="12c79-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="12c79-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="12c79-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12c79-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex3 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit, _
    itagSequence As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbit
Dim itagSequence As IntegerApi.JetSetCurrentIndex3(sesid, _
    tableid, index, grbit, itagSequence)
```

``` csharp
public static void JetSetCurrentIndex3(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit,
    int itagSequence
)
```

#### <a name="parameters"></a><span data-ttu-id="12c79-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="12c79-108">Parameters</span></span>

  - <span data-ttu-id="12c79-109">сесид</span><span class="sxs-lookup"><span data-stu-id="12c79-109">sesid</span></span>  
    <span data-ttu-id="12c79-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="12c79-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="12c79-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="12c79-112">TableID</span><span class="sxs-lookup"><span data-stu-id="12c79-112">tableid</span></span>  
    <span data-ttu-id="12c79-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="12c79-114">Курсор, для которого задается индекс.</span><span class="sxs-lookup"><span data-stu-id="12c79-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="12c79-115">index</span><span class="sxs-lookup"><span data-stu-id="12c79-115">index</span></span>  
    <span data-ttu-id="12c79-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="12c79-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="12c79-117">Имя выбранного индекса.</span><span class="sxs-lookup"><span data-stu-id="12c79-117">The name of the index to be selected.</span></span> <span data-ttu-id="12c79-118">Если это значение равно null или пуст, первичный индекс будет выбран.</span><span class="sxs-lookup"><span data-stu-id="12c79-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="12c79-119">грбит</span><span class="sxs-lookup"><span data-stu-id="12c79-119">grbit</span></span>  
    <span data-ttu-id="12c79-120">Тип: [Microsoft. ISAM. ESENT. Interop. сеткуррентиндексгрбит](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="12c79-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="12c79-121">Задайте параметры индекса.</span><span class="sxs-lookup"><span data-stu-id="12c79-121">Set index options.</span></span>

<!-- end list -->

  - <span data-ttu-id="12c79-122">итагсекуенце</span><span class="sxs-lookup"><span data-stu-id="12c79-122">itagSequence</span></span>  
    <span data-ttu-id="12c79-123">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="12c79-123">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="12c79-124">Порядковый номер значения столбца с несколькими значениями, который будет использоваться для позиционирования курсора на новом индексе.</span><span class="sxs-lookup"><span data-stu-id="12c79-124">Sequence number of the multi-valued column value which will be used to position the cursor on the new index.</span></span> <span data-ttu-id="12c79-125">Этот параметр используется только в сочетании с параметром [OnMove](./setcurrentindexgrbit-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="12c79-125">This parameter is only used in conjunction with [NoMove](./setcurrentindexgrbit-enumeration.md).</span></span> <span data-ttu-id="12c79-126">Если этот параметр отсутствует или имеет значение 0, предполагается, что оно равно 1.</span><span class="sxs-lookup"><span data-stu-id="12c79-126">When this parameter is not present or is set to zero, its value is presumed to be 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="12c79-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12c79-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="12c79-128">Справочник</span><span class="sxs-lookup"><span data-stu-id="12c79-128">Reference</span></span>

[<span data-ttu-id="12c79-129">Класс API</span><span class="sxs-lookup"><span data-stu-id="12c79-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="12c79-130">Члены API</span><span class="sxs-lookup"><span data-stu-id="12c79-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="12c79-131">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="12c79-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
