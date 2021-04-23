---
description: Дополнительные сведения о методе API. Трисик
title: API. Трисик, метод
TOCTitle: 'TrySeek method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.TrySeek(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.SeekGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.tryseek(v=EXCHG.10)
ms:contentKeyID: 55100941
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.TrySeek
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46472c59c14bd515e744a7ccfa908752783d27fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896990"
---
# <a name="apitryseek-method"></a><span data-ttu-id="e947f-103">API. Трисик, метод</span><span class="sxs-lookup"><span data-stu-id="e947f-103">Api.TrySeek method</span></span>

<span data-ttu-id="e947f-104">Эффективно позиционирует курсор на запись индекса, которая соответствует условиям поиска, заданным в ключе поиска в этом курсоре, и заданному неравенству.</span><span class="sxs-lookup"><span data-stu-id="e947f-104">Efficiently positions a cursor to an index entry that matches the search criteria specified by the search key in that cursor and the specified inequality.</span></span> <span data-ttu-id="e947f-105">Ключ поиска должен быть ранее создан с помощью Жетмакекэй.</span><span class="sxs-lookup"><span data-stu-id="e947f-105">A search key must have been previously constructed using JetMakeKey.</span></span>

<span data-ttu-id="e947f-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e947f-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e947f-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e947f-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e947f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e947f-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function TrySeek ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    grbit As SeekGrbit _
) As Boolean
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim grbit As SeekGrbit
Dim returnValue As Boolean

returnValue = Api.TrySeek(sesid, _
    tableid, grbit)
```

``` csharp
public static bool TrySeek(
    JET_SESID sesid,
    JET_TABLEID tableid,
    SeekGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="e947f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e947f-109">Parameters</span></span>

  - <span data-ttu-id="e947f-110">сесид</span><span class="sxs-lookup"><span data-stu-id="e947f-110">sesid</span></span>  
    <span data-ttu-id="e947f-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e947f-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e947f-112">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="e947f-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e947f-113">TableID</span><span class="sxs-lookup"><span data-stu-id="e947f-113">tableid</span></span>  
    <span data-ttu-id="e947f-114">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e947f-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="e947f-115">Курсор для позиции.</span><span class="sxs-lookup"><span data-stu-id="e947f-115">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="e947f-116">грбит</span><span class="sxs-lookup"><span data-stu-id="e947f-116">grbit</span></span>  
    <span data-ttu-id="e947f-117">Тип: [Microsoft. ISAM. ESENT. Interop. сикгрбит](./seekgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e947f-117">Type: [Microsoft.Isam.Esent.Interop.SeekGrbit](./seekgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="e947f-118">Параметр поиска.</span><span class="sxs-lookup"><span data-stu-id="e947f-118">Seek option.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e947f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e947f-119">Return value</span></span>

<span data-ttu-id="e947f-120">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e947f-120">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e947f-121">Значение true, если найдена запись, соответствующая критериям.</span><span class="sxs-lookup"><span data-stu-id="e947f-121">True if a record matching the criteria was found.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e947f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e947f-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e947f-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="e947f-123">Reference</span></span>

[<span data-ttu-id="e947f-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="e947f-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e947f-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="e947f-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e947f-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e947f-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
