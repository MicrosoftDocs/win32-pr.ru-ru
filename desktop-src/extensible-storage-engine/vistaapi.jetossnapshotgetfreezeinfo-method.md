---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшотжетфризеинфо'
title: Вистаапи. Жетосснапшотжетфризеинфо, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotGetFreezeInfo method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,System.Int32@,Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO[]@,Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotgetfreezeinfo(v=EXCHG.10)
ms:contentKeyID: 55104199
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotGetFreezeInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84b8f33f1fcac280e8fee65c1092c8fccdec3b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683136"
---
# <a name="vistaapijetossnapshotgetfreezeinfo-method"></a><span data-ttu-id="1febc-103">Вистаапи. Жетосснапшотжетфризеинфо, метод</span><span class="sxs-lookup"><span data-stu-id="1febc-103">VistaApi.JetOSSnapshotGetFreezeInfo method</span></span>

<span data-ttu-id="1febc-104">Возвращает список экземпляров и баз данных, которые являются частью сеанса моментального снимка в любой момент.</span><span class="sxs-lookup"><span data-stu-id="1febc-104">Retrieves the list of instances and databases that are part of the snapshot session at any given moment.</span></span>

<span data-ttu-id="1febc-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1febc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="1febc-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1febc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1febc-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1febc-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotGetFreezeInfo ( _
    snapshot As JET_OSSNAPID, _
    <OutAttribute> ByRef numInstances As Integer, _
    <OutAttribute> ByRef instances As JET_INSTANCE_INFO(), _
    grbit As SnapshotGetFreezeInfoGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim numInstances As Integer
Dim instances As JET_INSTANCE_INFO()
Dim grbit As SnapshotGetFreezeInfoGrbitVistaApi.JetOSSnapshotGetFreezeInfo(snapshot, _
    numInstances, instances, grbit)
```

``` csharp
public static void JetOSSnapshotGetFreezeInfo(
    JET_OSSNAPID snapshot,
    out int numInstances,
    out JET_INSTANCE_INFO[] instances,
    SnapshotGetFreezeInfoGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="1febc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1febc-108">Parameters</span></span>

  - <span data-ttu-id="1febc-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="1febc-109">snapshot</span></span>  
    <span data-ttu-id="1febc-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1febc-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="1febc-111">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="1febc-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="1febc-112">нуминстанцес</span><span class="sxs-lookup"><span data-stu-id="1febc-112">numInstances</span></span>  
    <span data-ttu-id="1febc-113">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1febc-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="1febc-114">Возвращает количество экземпляров.</span><span class="sxs-lookup"><span data-stu-id="1febc-114">Returns the number of instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="1febc-115">instances</span><span class="sxs-lookup"><span data-stu-id="1febc-115">instances</span></span>  
    <span data-ttu-id="1febc-116">Тип \[\]</span><span class="sxs-lookup"><span data-stu-id="1febc-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="1febc-117">Возвращает сведения об экземплярах.</span><span class="sxs-lookup"><span data-stu-id="1febc-117">Returns information about the instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="1febc-118">грбит</span><span class="sxs-lookup"><span data-stu-id="1febc-118">grbit</span></span>  
    <span data-ttu-id="1febc-119">Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшотжетфризеинфогрбит](./snapshotgetfreezeinfogrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1febc-119">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotGetFreezeInfoGrbit](./snapshotgetfreezeinfogrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="1febc-120">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="1febc-120">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="1febc-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1febc-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1febc-122">Справочник</span><span class="sxs-lookup"><span data-stu-id="1febc-122">Reference</span></span>

[<span data-ttu-id="1febc-123">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="1febc-123">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="1febc-124">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="1febc-124">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="1febc-125">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="1febc-125">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
