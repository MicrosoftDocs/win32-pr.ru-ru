---
description: Дополнительные сведения о методе API. Ескровупдате
title: API. Ескровупдате, метод
TOCTitle: 'EscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.EscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.escrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100668
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.EscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dde632f01bd7ac9cbdf8bc4dc09e1337f32014b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808279"
---
# <a name="apiescrowupdate-method"></a><span data-ttu-id="ee970-103">API. Ескровупдате, метод</span><span class="sxs-lookup"><span data-stu-id="ee970-103">Api.EscrowUpdate method</span></span>

<span data-ttu-id="ee970-104">Выполнить атомарное сложение для одного столбца.</span><span class="sxs-lookup"><span data-stu-id="ee970-104">Perform atomic addition on one column.</span></span> <span data-ttu-id="ee970-105">Столбец должен иметь тип [Long](./jet-coltyp-enumeration.md).</span><span class="sxs-lookup"><span data-stu-id="ee970-105">The column must be of type [Long](./jet-coltyp-enumeration.md).</span></span> <span data-ttu-id="ee970-106">Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="ee970-106">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span>

<span data-ttu-id="ee970-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ee970-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ee970-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ee970-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ee970-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee970-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Function EscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Integer _
) As Integer
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Integer
Dim returnValue As Integer

returnValue = Api.EscrowUpdate(sesid, _
    tableid, columnid, delta)
```

``` csharp
public static int EscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    int delta
)
```

#### <a name="parameters"></a><span data-ttu-id="ee970-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee970-110">Parameters</span></span>

  - <span data-ttu-id="ee970-111">сесид</span><span class="sxs-lookup"><span data-stu-id="ee970-111">sesid</span></span>  
    <span data-ttu-id="ee970-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee970-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ee970-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="ee970-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee970-114">TableID</span><span class="sxs-lookup"><span data-stu-id="ee970-114">tableid</span></span>  
    <span data-ttu-id="ee970-115">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee970-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ee970-116">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="ee970-116">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee970-117">columnid</span><span class="sxs-lookup"><span data-stu-id="ee970-117">columnid</span></span>  
    <span data-ttu-id="ee970-118">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ee970-118">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="ee970-119">Обновляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="ee970-119">The column to update.</span></span> <span data-ttu-id="ee970-120">Это должен быть столбец, который может быть условно обновляемым.</span><span class="sxs-lookup"><span data-stu-id="ee970-120">This must be an escrow-updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="ee970-121">delta</span><span class="sxs-lookup"><span data-stu-id="ee970-121">delta</span></span>  
    <span data-ttu-id="ee970-122">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ee970-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="ee970-123">Дельта, применяемая к столбцу.</span><span class="sxs-lookup"><span data-stu-id="ee970-123">The delta to apply to the column.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ee970-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee970-124">Return value</span></span>

<span data-ttu-id="ee970-125">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ee970-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
<span data-ttu-id="ee970-126">Текущее значение столбца, сохраненное в базе данных (управление версиями игнорируется).</span><span class="sxs-lookup"><span data-stu-id="ee970-126">The current value of the column as stored in the database (versioning is ignored).</span></span>  

## <a name="remarks"></a><span data-ttu-id="ee970-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee970-127">Remarks</span></span>

<span data-ttu-id="ee970-128">Этот метод служит оболочкой для [жетескровупдате (JET_SESID, JET_TABLEID, JET_COLUMNID, \[ \] , Int32, \[ \] , Int32, Int32, ескровупдатегрбит)](./api.jetescrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="ee970-128">This method wraps [JetEscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, \[\], Int32, \[\], Int32, Int32, EscrowUpdateGrbit)](./api.jetescrowupdate-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ee970-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee970-129">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ee970-130">Справочник</span><span class="sxs-lookup"><span data-stu-id="ee970-130">Reference</span></span>

[<span data-ttu-id="ee970-131">Класс API</span><span class="sxs-lookup"><span data-stu-id="ee970-131">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ee970-132">Члены API</span><span class="sxs-lookup"><span data-stu-id="ee970-132">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ee970-133">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ee970-133">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
