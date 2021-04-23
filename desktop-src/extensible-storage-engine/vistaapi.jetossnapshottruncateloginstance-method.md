---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшоттрункателогинстанце'
title: Вистаапи. Жетосснапшоттрункателогинстанце, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotTruncateLogInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshottruncateloginstance(v=EXCHG.10)
ms:contentKeyID: 55104197
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotTruncateLogInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 75d694629585a730f5c1c7b9b08bb7b06e735cb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913747"
---
# <a name="vistaapijetossnapshottruncateloginstance-method"></a><span data-ttu-id="1b932-103">Вистаапи. Жетосснапшоттрункателогинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="1b932-103">VistaApi.JetOSSnapshotTruncateLogInstance method</span></span>

<span data-ttu-id="1b932-104">Усекает журнал для указанного экземпляра во время сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="1b932-104">Truncates the log for a specified instance during a snapshot session.</span></span>

<span data-ttu-id="1b932-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b932-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1b932-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1b932-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b932-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b932-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotTruncateLogInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotTruncateLogGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotTruncateLogGrbitVistaApi.JetOSSnapshotTruncateLogInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotTruncateLogInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotTruncateLogGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1b932-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1b932-108">Parameters</span></span>

  - <span data-ttu-id="1b932-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="1b932-109">snapshot</span></span>  
    <span data-ttu-id="1b932-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b932-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="1b932-111">Идентификатор моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="1b932-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b932-112">экземпляр</span><span class="sxs-lookup"><span data-stu-id="1b932-112">instance</span></span>  
    <span data-ttu-id="1b932-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b932-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1b932-114">Экземпляр, для которого необходимо усечь журнал.</span><span class="sxs-lookup"><span data-stu-id="1b932-114">The instance to truncat the log for.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b932-115">грбит</span><span class="sxs-lookup"><span data-stu-id="1b932-115">grbit</span></span>  
    <span data-ttu-id="1b932-116">Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшоттрункателоггрбит](./snapshottruncateloggrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1b932-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotTruncateLogGrbit](./snapshottruncateloggrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1b932-117">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1b932-117">Options for this call.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b932-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b932-118">Remarks</span></span>

<span data-ttu-id="1b932-119">Эта функция должна вызываться только в том случае, если моментальный снимок был создан с помощью параметра [континуеафтерсав](./vistagrbits.continueafterthaw-field.md) .</span><span class="sxs-lookup"><span data-stu-id="1b932-119">This function should be called only if the snapshot was created with the [ContinueAfterThaw](./vistagrbits.continueafterthaw-field.md) option.</span></span> <span data-ttu-id="1b932-120">В противном случае сеанс моментального снимка заканчивается после вызова [жетосснапшотсав (JET_OSSNAPID, снапшотсавгрбит)](./api.jetossnapshotthaw-method.md).</span><span class="sxs-lookup"><span data-stu-id="1b932-120">Otherwise, the snapshot session ends after the call to [JetOSSnapshotThaw(JET_OSSNAPID, SnapshotThawGrbit)](./api.jetossnapshotthaw-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1b932-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1b932-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b932-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="1b932-122">Reference</span></span>

[<span data-ttu-id="1b932-123">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="1b932-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="1b932-124">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="1b932-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="1b932-125">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="1b932-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
