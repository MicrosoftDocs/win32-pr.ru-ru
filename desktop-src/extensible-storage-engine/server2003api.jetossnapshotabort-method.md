---
description: 'Дополнительные сведения о методе: Server2003Api. Жетосснапшотаборт'
title: Server2003Api. Жетосснапшотаборт, метод (Microsoft. ISAM. ESENT. Interop. server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 44ee61a7c6cff7fe90a77fdaced786532457c132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692548"
---
# <a name="server2003apijetossnapshotabort-method"></a><span data-ttu-id="c06f3-103">Server2003Api. Жетосснапшотаборт, метод</span><span class="sxs-lookup"><span data-stu-id="c06f3-103">Server2003Api.JetOSSnapshotAbort method</span></span>

<span data-ttu-id="c06f3-104">Уведомляет ядро о возможности возобновления обычных операций ввода-вывода после завершения периода фиксации с неудачным снимком.</span><span class="sxs-lookup"><span data-stu-id="c06f3-104">Notifies the engine that it can resume normal IO operations after a freeze period ended with a failed snapshot.</span></span>

<span data-ttu-id="c06f3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c06f3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)</span></span>  
<span data-ttu-id="c06f3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c06f3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c06f3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c06f3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c06f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c06f3-108">Parameters</span></span>

  - <span data-ttu-id="c06f3-109">снапид</span><span class="sxs-lookup"><span data-stu-id="c06f3-109">snapid</span></span>  
    <span data-ttu-id="c06f3-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c06f3-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="c06f3-111">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="c06f3-111">Identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="c06f3-112">грбит</span><span class="sxs-lookup"><span data-stu-id="c06f3-112">grbit</span></span>  
    <span data-ttu-id="c06f3-113">Тип: [Microsoft. ISAM. ESENT. Interop. server2003. снапшотабортгрбит](./snapshotabortgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c06f3-113">Type: [Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c06f3-114">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="c06f3-114">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="c06f3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c06f3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c06f3-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="c06f3-116">Reference</span></span>

[<span data-ttu-id="c06f3-117">Класс Server2003Api</span><span class="sxs-lookup"><span data-stu-id="c06f3-117">Server2003Api class</span></span>](./server2003api-class.md)

[<span data-ttu-id="c06f3-118">Элементы Server2003Api</span><span class="sxs-lookup"><span data-stu-id="c06f3-118">Server2003Api members</span></span>](./server2003api-members.md)

[<span data-ttu-id="c06f3-119">Пространство имен Microsoft. ISAM. ESENT. Interop. server2003</span><span class="sxs-lookup"><span data-stu-id="c06f3-119">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
