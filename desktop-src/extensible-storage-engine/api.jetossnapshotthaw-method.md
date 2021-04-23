---
description: Дополнительные сведения о методе API. Жетосснапшотсав
title: API. Жетосснапшотсав, метод
TOCTitle: 'JetOSSnapshotThaw method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.SnapshotThawGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotthaw(v=EXCHG.10)
ms:contentKeyID: 55100780
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotThaw
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f3fe0bc04586dddade7a9723720bbd3c994c516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913184"
---
# <a name="apijetossnapshotthaw-method"></a><span data-ttu-id="a307f-103">API. Жетосснапшотсав, метод</span><span class="sxs-lookup"><span data-stu-id="a307f-103">Api.JetOSSnapshotThaw method</span></span>

<span data-ttu-id="a307f-104">Уведомляет ядро о возможности возобновления обычных операций ввода-вывода после точки фиксации и успешного создания моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a307f-104">Notifies the engine that it can resume normal IO operations after a freeze period and a successful snapshot.</span></span>

<span data-ttu-id="a307f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a307f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a307f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a307f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a307f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a307f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotThaw ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotThawGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotThawGrbitApi.JetOSSnapshotThaw(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotThaw(
    JET_OSSNAPID snapshot,
    SnapshotThawGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="a307f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a307f-108">Parameters</span></span>

  - <span data-ttu-id="a307f-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="a307f-109">snapshot</span></span>  
    <span data-ttu-id="a307f-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a307f-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="a307f-111">Идентификатор моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="a307f-111">The ID of the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="a307f-112">грбит</span><span class="sxs-lookup"><span data-stu-id="a307f-112">grbit</span></span>  
    <span data-ttu-id="a307f-113">Тип: [Microsoft. ISAM. ESENT. Interop. снапшотсавгрбит](./snapshotthawgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a307f-113">Type: [Microsoft.Isam.Esent.Interop.SnapshotThawGrbit](./snapshotthawgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="a307f-114">Параметры разморозки.</span><span class="sxs-lookup"><span data-stu-id="a307f-114">Thaw options.</span></span>

## <a name="see-also"></a><span data-ttu-id="a307f-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a307f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a307f-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="a307f-116">Reference</span></span>

[<span data-ttu-id="a307f-117">Класс API</span><span class="sxs-lookup"><span data-stu-id="a307f-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a307f-118">Члены API</span><span class="sxs-lookup"><span data-stu-id="a307f-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a307f-119">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a307f-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
