---
description: Дополнительные сведения о методе API. JetSetCurrentIndex2
title: API. JetSetCurrentIndex2, метод
TOCTitle: 'JetSetCurrentIndex2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String,Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetcurrentindex2(v=EXCHG.10)
ms:contentKeyID: 55100798
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetCurrentIndex2
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e08e1fe5027641348259381d74b34ce16b034e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423753"
---
# <a name="apijetsetcurrentindex2-method"></a><span data-ttu-id="e8a33-103">API. JetSetCurrentIndex2, метод</span><span class="sxs-lookup"><span data-stu-id="e8a33-103">Api.JetSetCurrentIndex2 method</span></span>

<span data-ttu-id="e8a33-104">Задает текущий индекс курсора.</span><span class="sxs-lookup"><span data-stu-id="e8a33-104">Set the current index of a cursor.</span></span>

<span data-ttu-id="e8a33-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8a33-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8a33-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8a33-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8a33-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetCurrentIndex2 ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    index As String, _
    grbit As SetCurrentIndexGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim index As String
Dim grbit As SetCurrentIndexGrbitApi.JetSetCurrentIndex2(sesid, _
    tableid, index, grbit)
```

``` csharp
public static void JetSetCurrentIndex2(
    JET_SESID sesid,
    JET_TABLEID tableid,
    string index,
    SetCurrentIndexGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e8a33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8a33-108">Parameters</span></span>

  - <span data-ttu-id="e8a33-109">сесид</span><span class="sxs-lookup"><span data-stu-id="e8a33-109">sesid</span></span>  
    <span data-ttu-id="e8a33-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8a33-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e8a33-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="e8a33-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8a33-112">TableID</span><span class="sxs-lookup"><span data-stu-id="e8a33-112">tableid</span></span>  
    <span data-ttu-id="e8a33-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8a33-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e8a33-114">Курсор, для которого задается индекс.</span><span class="sxs-lookup"><span data-stu-id="e8a33-114">The cursor to set the index on.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8a33-115">index</span><span class="sxs-lookup"><span data-stu-id="e8a33-115">index</span></span>  
    <span data-ttu-id="e8a33-116">Тип: [System. String](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e8a33-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e8a33-117">Имя выбранного индекса.</span><span class="sxs-lookup"><span data-stu-id="e8a33-117">The name of the index to be selected.</span></span> <span data-ttu-id="e8a33-118">Если это значение равно null или пуст, первичный индекс будет выбран.</span><span class="sxs-lookup"><span data-stu-id="e8a33-118">If this is null or empty the primary index will be selected.</span></span>

<!-- end list -->

  - <span data-ttu-id="e8a33-119">грбит</span><span class="sxs-lookup"><span data-stu-id="e8a33-119">grbit</span></span>  
    <span data-ttu-id="e8a33-120">Тип: [Microsoft. ISAM. ESENT. Interop. сеткуррентиндексгрбит](./setcurrentindexgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e8a33-120">Type: [Microsoft.Isam.Esent.Interop.SetCurrentIndexGrbit](./setcurrentindexgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e8a33-121">Задайте параметры индекса.</span><span class="sxs-lookup"><span data-stu-id="e8a33-121">Set index options.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8a33-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8a33-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8a33-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="e8a33-123">Reference</span></span>

[<span data-ttu-id="e8a33-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="e8a33-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e8a33-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="e8a33-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e8a33-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e8a33-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
