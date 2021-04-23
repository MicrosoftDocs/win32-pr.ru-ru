---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшоттрункателог'
title: Вистаапи. Жетосснапшоттрункателог, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLog method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncatelog(v=EXCHG.10)
ms:contentKeyID: 55104308
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLog
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0af8054bc414ea5dbd6c7225fa9e2cd7117c74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682380"
---
# <a name="vistaapijetossnapshottruncatelog-method"></a><span data-ttu-id="7116b-103">Вистаапи. Жетосснапшоттрункателог, метод</span><span class="sxs-lookup"><span data-stu-id="7116b-103">VistaApi.JetOSSnapshotTruncateLog method</span></span>

<span data-ttu-id="7116b-104">Включает усечение журнала для всех экземпляров, которые являются частью сеанса моментальных снимков.</span><span class="sxs-lookup"><span data-stu-id="7116b-104">Enables log truncation for all instances that are part of the snapshot session.</span></span>

<span data-ttu-id="7116b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7116b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="7116b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7116b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7116b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7116b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLog ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLog(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLog(
    JET_OSSNAPID snapshot,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="7116b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7116b-108">Parameters</span></span>

  - <span data-ttu-id="7116b-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="7116b-109">snapshot</span></span>  
    <span data-ttu-id="7116b-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7116b-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="7116b-111">Идентификатор моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7116b-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="7116b-112">грбит</span><span class="sxs-lookup"><span data-stu-id="7116b-112">grbit</span></span>  
    <span data-ttu-id="7116b-113">Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшоттрункателоггрбит](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7116b-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="7116b-114">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="7116b-114">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="7116b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7116b-115">Remarks</span></span>

<span data-ttu-id="7116b-116">Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра [континуеафтерсав](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="7116b-116">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="7116b-117">В противном случае сеанс моментального снимка заканчивается после вызова [жетосснапшотсав (JET_OSSNAPID, снапшотсавгрбит)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="7116b-117">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7116b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7116b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7116b-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="7116b-119">Reference</span></span>

[<span data-ttu-id="7116b-120">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="7116b-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="7116b-121">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="7116b-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="7116b-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="7116b-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
