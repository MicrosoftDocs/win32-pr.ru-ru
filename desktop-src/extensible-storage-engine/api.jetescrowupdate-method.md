---
description: Дополнительные сведения о методе API. Жетескровупдате
title: API. Жетескровупдате, метод
TOCTitle: 'JetEscrowUpdate method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_COLUMNID,System.Byte[],System.Int32,System.Byte[],System.Int32,System.Int32@,Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetescrowupdate(v=EXCHG.10)
ms:contentKeyID: 55100740
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetEscrowUpdate
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 09e74f964fd6018248a3cfc594621bed96f92e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719325"
---
# <a name="apijetescrowupdate-method"></a><span data-ttu-id="14f6a-103">API. Жетескровупдате, метод</span><span class="sxs-lookup"><span data-stu-id="14f6a-103">Api.JetEscrowUpdate method</span></span>

<span data-ttu-id="14f6a-104">Выполняет атомарную операцию сложения для одного столбца.</span><span class="sxs-lookup"><span data-stu-id="14f6a-104">Performs an atomic addition operation on one column.</span></span> <span data-ttu-id="14f6a-105">Эта функция позволяет нескольким сеансам одновременно обновлять одну и ту же запись без конфликтов.</span><span class="sxs-lookup"><span data-stu-id="14f6a-105">This function allows multiple sessions to update the same record concurrently without conflicts.</span></span> <span data-ttu-id="14f6a-106">См. также [ескровупдате (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span><span class="sxs-lookup"><span data-stu-id="14f6a-106">Also see [EscrowUpdate(JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)](./api.escrowupdate-method.md).</span></span>

<span data-ttu-id="14f6a-107">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="14f6a-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="14f6a-108">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="14f6a-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="14f6a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14f6a-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetEscrowUpdate ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    columnid As JET_COLUMNID, _
    delta As Byte(), _
    deltaSize As Integer, _
    previousValue As Byte(), _
    previousValueLength As Integer, _
    <OutAttribute> ByRef actualPreviousValueLength As Integer, _
    grbit As EscrowUpdateGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim columnid As JET_COLUMNID
Dim delta As Byte()
Dim deltaSize As Integer
Dim previousValue As Byte()
Dim previousValueLength As Integer
Dim actualPreviousValueLength As Integer
Dim grbit As EscrowUpdateGrbitApi.JetEscrowUpdate(sesid, tableid, _
    columnid, delta, deltaSize, previousValue, _
    previousValueLength, actualPreviousValueLength, _
    grbit)
```

``` csharp
public static void JetEscrowUpdate(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_COLUMNID columnid,
    byte[] delta,
    int deltaSize,
    byte[] previousValue,
    int previousValueLength,
    out int actualPreviousValueLength,
    EscrowUpdateGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="14f6a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="14f6a-110">Parameters</span></span>

  - <span data-ttu-id="14f6a-111">сесид</span><span class="sxs-lookup"><span data-stu-id="14f6a-111">sesid</span></span>  
    <span data-ttu-id="14f6a-112">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14f6a-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="14f6a-113">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="14f6a-113">The session to use.</span></span> <span data-ttu-id="14f6a-114">Сеанс должен быть в транзакции.</span><span class="sxs-lookup"><span data-stu-id="14f6a-114">The session must be in a transaction.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-115">TableID</span><span class="sxs-lookup"><span data-stu-id="14f6a-115">tableid</span></span>  
    <span data-ttu-id="14f6a-116">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14f6a-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="14f6a-117">Обновляемый курсор.</span><span class="sxs-lookup"><span data-stu-id="14f6a-117">The cursor to update.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-118">columnid</span><span class="sxs-lookup"><span data-stu-id="14f6a-118">columnid</span></span>  
    <span data-ttu-id="14f6a-119">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="14f6a-119">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="14f6a-120">Обновляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="14f6a-120">The column to update.</span></span> <span data-ttu-id="14f6a-121">Это должен быть условно обновляемый столбец.</span><span class="sxs-lookup"><span data-stu-id="14f6a-121">This must be an escrow updatable column.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-122">delta</span><span class="sxs-lookup"><span data-stu-id="14f6a-122">delta</span></span>  
    <span data-ttu-id="14f6a-123">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="14f6a-123">Type: \[\]</span></span>  
    
    <span data-ttu-id="14f6a-124">Буфер, содержащий слагаемое.</span><span class="sxs-lookup"><span data-stu-id="14f6a-124">The buffer containing the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-125">делтасизе</span><span class="sxs-lookup"><span data-stu-id="14f6a-125">deltaSize</span></span>  
    <span data-ttu-id="14f6a-126">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="14f6a-126">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="14f6a-127">Размер слагаемое.</span><span class="sxs-lookup"><span data-stu-id="14f6a-127">The size of the addend.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-128">превиаусвалуе</span><span class="sxs-lookup"><span data-stu-id="14f6a-128">previousValue</span></span>  
    <span data-ttu-id="14f6a-129">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="14f6a-129">Type: \[\]</span></span>  
    
    <span data-ttu-id="14f6a-130">Выходной буфер, который получит текущее значение столбца.</span><span class="sxs-lookup"><span data-stu-id="14f6a-130">An output buffer that will recieve the current value of the column.</span></span> <span data-ttu-id="14f6a-131">Этот буфер может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="14f6a-131">This buffer can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-132">превиаусвалуеленгс</span><span class="sxs-lookup"><span data-stu-id="14f6a-132">previousValueLength</span></span>  
    <span data-ttu-id="14f6a-133">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="14f6a-133">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="14f6a-134">Размер буфера Превиаусвалуе.</span><span class="sxs-lookup"><span data-stu-id="14f6a-134">The size of the previousValue buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-135">актуалпревиаусвалуеленгс</span><span class="sxs-lookup"><span data-stu-id="14f6a-135">actualPreviousValueLength</span></span>  
    <span data-ttu-id="14f6a-136">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="14f6a-136">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="14f6a-137">Возвращает фактический размер Превиаусвалуе.</span><span class="sxs-lookup"><span data-stu-id="14f6a-137">Returns the actual size of the previousValue.</span></span>

<!-- end list -->

  - <span data-ttu-id="14f6a-138">грбит</span><span class="sxs-lookup"><span data-stu-id="14f6a-138">grbit</span></span>  
    <span data-ttu-id="14f6a-139">Тип: [Microsoft. ISAM. ESENT. Interop. ескровупдатегрбит](./escrowupdategrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="14f6a-139">Type: [Microsoft.Isam.Esent.Interop.EscrowUpdateGrbit](./escrowupdategrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="14f6a-140">Параметры депонирования обновлений.</span><span class="sxs-lookup"><span data-stu-id="14f6a-140">Escrow update options.</span></span>

## <a name="see-also"></a><span data-ttu-id="14f6a-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14f6a-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="14f6a-142">Справочник</span><span class="sxs-lookup"><span data-stu-id="14f6a-142">Reference</span></span>

[<span data-ttu-id="14f6a-143">Класс API</span><span class="sxs-lookup"><span data-stu-id="14f6a-143">Api class</span></span>](./api-class.md)

[<span data-ttu-id="14f6a-144">Члены API</span><span class="sxs-lookup"><span data-stu-id="14f6a-144">Api members</span></span>](./api-members.md)

[<span data-ttu-id="14f6a-145">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="14f6a-145">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
