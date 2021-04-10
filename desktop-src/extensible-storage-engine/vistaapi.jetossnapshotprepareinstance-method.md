---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшотпрепареинстанце'
title: Вистаапи. Жетосснапшотпрепареинстанце, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotPrepareInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotprepareinstance(v=EXCHG.10)
ms:contentKeyID: 55104304
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotPrepareInstance
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 46151e2b11c669ac9635ce5974757999a8636b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156602"
---
# <a name="vistaapijetossnapshotprepareinstance-method"></a><span data-ttu-id="f514a-103">Вистаапи. Жетосснапшотпрепареинстанце, метод</span><span class="sxs-lookup"><span data-stu-id="f514a-103">VistaApi.JetOSSnapshotPrepareInstance method</span></span>

<span data-ttu-id="f514a-104">Выбирает конкретный экземпляр, который должен быть частью сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f514a-104">Selects a specific instance to be part of the snapshot session.</span></span>

<span data-ttu-id="f514a-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f514a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="f514a-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f514a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f514a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f514a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepareInstance ( _
    snapshot As JET_OSSNAPID, _
    instance As JET_INSTANCE, _
    grbit As SnapshotPrepareInstanceGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim instance As JET_INSTANCE
Dim grbit As SnapshotPrepareInstanceGrbitVistaApi.JetOSSnapshotPrepareInstance(snapshot, _
    instance, grbit)
```

``` csharp
public static void JetOSSnapshotPrepareInstance(
    JET_OSSNAPID snapshot,
    JET_INSTANCE instance,
    SnapshotPrepareInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="f514a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f514a-108">Parameters</span></span>

  - <span data-ttu-id="f514a-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="f514a-109">snapshot</span></span>  
    <span data-ttu-id="f514a-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f514a-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="f514a-111">Идентификатор моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="f514a-111">The snapshot identifier.</span></span>

<!-- end list -->

  - <span data-ttu-id="f514a-112">экземпляр</span><span class="sxs-lookup"><span data-stu-id="f514a-112">instance</span></span>  
    <span data-ttu-id="f514a-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="f514a-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="f514a-114">Экземпляр, добавляемый в моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="f514a-114">The instance to add to the snapshot.</span></span>

<!-- end list -->

  - <span data-ttu-id="f514a-115">грбит</span><span class="sxs-lookup"><span data-stu-id="f514a-115">grbit</span></span>  
    <span data-ttu-id="f514a-116">Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшотпрепареинстанцегрбит](./snapshotprepareinstancegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="f514a-116">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotPrepareInstanceGrbit](./snapshotprepareinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="f514a-117">Параметры для этого вызова.</span><span class="sxs-lookup"><span data-stu-id="f514a-117">Options for this call.</span></span>

## <a name="see-also"></a><span data-ttu-id="f514a-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f514a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f514a-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="f514a-119">Reference</span></span>

[<span data-ttu-id="f514a-120">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="f514a-120">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="f514a-121">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="f514a-121">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="f514a-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="f514a-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
