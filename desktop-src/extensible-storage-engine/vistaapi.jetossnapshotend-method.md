---
description: 'Дополнительные сведения о методе: Вистаапи. Жетосснапшотенд'
title: Вистаапи. Жетосснапшотенд, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 291d83929940a9f66f4e16c5088e6ec08187f908
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810342"
---
# <a name="vistaapijetossnapshotend-method"></a><span data-ttu-id="c7ef3-103">Вистаапи. Жетосснапшотенд, метод</span><span class="sxs-lookup"><span data-stu-id="c7ef3-103">VistaApi.JetOSSnapshotEnd method</span></span>

<span data-ttu-id="c7ef3-104">Уведомляет обработчик о завершении сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-104">Notifies the engine that the snapshot session finished.</span></span>

<span data-ttu-id="c7ef3-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c7ef3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c7ef3-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c7ef3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c7ef3-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7ef3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c7ef3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7ef3-108">Parameters</span></span>

  - <span data-ttu-id="c7ef3-109">snapshot</span><span class="sxs-lookup"><span data-stu-id="c7ef3-109">snapshot</span></span>  
    <span data-ttu-id="c7ef3-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c7ef3-110">Type: [Microsoft.Isam.Esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)</span></span>  
    
    <span data-ttu-id="c7ef3-111">Идентификатор сеанса моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-111">The identifier of the snapshot session.</span></span>

<!-- end list -->

  - <span data-ttu-id="c7ef3-112">грбит</span><span class="sxs-lookup"><span data-stu-id="c7ef3-112">grbit</span></span>  
    <span data-ttu-id="c7ef3-113">Тип: [Microsoft. ISAM. ESENT. Interop. Vista. снапшотендгрбит](./snapshotendgrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c7ef3-113">Type: [Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c7ef3-114">Параметры конца моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-114">Snapshot end options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7ef3-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7ef3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c7ef3-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="c7ef3-116">Reference</span></span>

[<span data-ttu-id="c7ef3-117">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="c7ef3-117">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="c7ef3-118">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="c7ef3-118">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="c7ef3-119">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="c7ef3-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
