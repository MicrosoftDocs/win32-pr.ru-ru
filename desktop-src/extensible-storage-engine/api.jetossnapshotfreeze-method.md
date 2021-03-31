---
description: Дополнительные сведения о методе API. Жетосснапшотфризе
title: API. Жетосснапшотфризе, метод
TOCTitle: 'JetOSSnapshotFreeze method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotfreeze(v=EXCHG.10)
ms:contentKeyID: 55100793
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotFreeze
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b7434cb79e90f99ab946c86a97559079352956fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272543"
---
# <a name="apijetossnapshotfreeze-method"></a><span data-ttu-id="0b0a8-103">API. Жетосснапшотфризе, метод</span><span class="sxs-lookup"><span data-stu-id="0b0a8-103">Api.JetOSSnapshotFreeze method</span></span>

<span data-ttu-id="0b0a8-104">Запускает моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-104">Starts a snapshot.</span></span> <span data-ttu-id="0b0a8-105">Во время выполнения моментального снимка подсистема не может выполнить действия записи на диск.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-105">While the snapshot is in progress, no write-to-disk activity by the engine can take place.</span></span>

<span data-ttu-id="0b0a8-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0b0a8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0b0a8-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0b0a8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0b0a8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0b0a8-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotFreeze ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotFreezeGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotFreezeGrbitApi.JetOSSnapshotFreeze(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotFreeze(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotFreezeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="0b0a8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0b0a8-109">Parameters</span></span>

  - <span data-ttu-id="0b0a8-110">snapshot</span><span class="sxs-lookup"><span data-stu-id="0b0a8-110">snapshot</span></span>  
    <span data-ttu-id="0b0a8-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0b0a8-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="0b0a8-112">Сеанс моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-112">The snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b0a8-113">нуминстанцес</span><span class="sxs-lookup"><span data-stu-id="0b0a8-113">numInstances</span></span>  
    <span data-ttu-id="0b0a8-114">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="0b0a8-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="0b0a8-115">Возвращает количество экземпляров, которые являются частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-115">Returns the number of instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b0a8-116">instances</span><span class="sxs-lookup"><span data-stu-id="0b0a8-116">instances</span></span>  
    <span data-ttu-id="0b0a8-117">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="0b0a8-117">Type: \[\]</span></span>  
    
    <span data-ttu-id="0b0a8-118">Возвращает сведения об экземплярах, которые являются частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-118">Returns information about the instances that are part of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="0b0a8-119">грбит</span><span class="sxs-lookup"><span data-stu-id="0b0a8-119">grbit</span></span>  
    <span data-ttu-id="0b0a8-120">Тип: [Microsoft. ISAM. ESENT. Interop. снапшотфризегрбит](./snapshotfreezegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0b0a8-120">Type: [Microsoft.Isam.Esent.Interop.SnapshotFreezeGrbit](./snapshotfreezegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="0b0a8-121">Параметры замораживания моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="0b0a8-121">Snapshot freeze options.</span></span>

## <a name="see-also"></a><span data-ttu-id="0b0a8-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0b0a8-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0b0a8-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="0b0a8-123">Reference</span></span>

[<span data-ttu-id="0b0a8-124">Класс API</span><span class="sxs-lookup"><span data-stu-id="0b0a8-124">Api class</span></span>](./api-class.md)

[<span data-ttu-id="0b0a8-125">Члены API</span><span class="sxs-lookup"><span data-stu-id="0b0a8-125">Api members</span></span>](./api-members.md)

[<span data-ttu-id="0b0a8-126">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0b0a8-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
