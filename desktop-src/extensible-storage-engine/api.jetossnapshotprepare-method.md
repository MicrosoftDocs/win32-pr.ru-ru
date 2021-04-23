---
description: Дополнительные сведения о методе API. Жетосснапшотпрепаре
title: API. Жетосснапшотпрепаре, метод
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0ac304cf522e7c99a2495925da8571b2139c0a69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272542"
---
# <a name="apijetossnapshotprepare-method"></a><span data-ttu-id="fdc83-103">API. Жетосснапшотпрепаре, метод</span><span class="sxs-lookup"><span data-stu-id="fdc83-103">Api.JetOSSnapshotPrepare method</span></span>

<span data-ttu-id="fdc83-104">Начинает подготовку сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="fdc83-104">Begins the preparations for a snapshot session.</span></span> <span data-ttu-id="fdc83-105">Сеанс моментальных снимков — это короткий интервал времени, в течение которого модуль не выполняет никаких операций записи с диска IOs на диск, чтобы подсистема могла участвовать в сеансе моментальных снимков тома (при использовании модуля записи моментальных снимков).</span><span class="sxs-lookup"><span data-stu-id="fdc83-105">A snapshot session is a short time interval in which the engine does not issue any write IOs to disk, so that the engine can participate in a volume snapshot session (when driven by a snapshot writer).</span></span>

<span data-ttu-id="fdc83-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fdc83-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fdc83-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fdc83-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc83-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdc83-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="fdc83-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdc83-109">Parameters</span></span>

  - <span data-ttu-id="fdc83-110">snapshot</span><span class="sxs-lookup"><span data-stu-id="fdc83-110">snapshot</span></span>  
    <span data-ttu-id="fdc83-111">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="fdc83-111">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="fdc83-112">Возвращает идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="fdc83-112">Returns the ID of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="fdc83-113">грбит</span><span class="sxs-lookup"><span data-stu-id="fdc83-113">grbit</span></span>  
    <span data-ttu-id="fdc83-114">Тип: [Microsoft. ISAM. ESENT. Interop. снапшотпрепарегрбит](./snapshotpreparegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fdc83-114">Type: [Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="fdc83-115">Параметры моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="fdc83-115">Snapshot options.</span></span>

## <a name="see-also"></a><span data-ttu-id="fdc83-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdc83-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fdc83-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="fdc83-117">Reference</span></span>

[<span data-ttu-id="fdc83-118">Класс API</span><span class="sxs-lookup"><span data-stu-id="fdc83-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fdc83-119">Члены API</span><span class="sxs-lookup"><span data-stu-id="fdc83-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fdc83-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fdc83-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
