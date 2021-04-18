---
description: 'Дополнительные сведения о методе: Вистаапи. Жетжетрекордсизе'
title: Вистаапи. Жетжетрекордсизе, метод (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'JetGetRecordSize method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE@,Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetgetrecordsize(v=EXCHG.10)
ms:contentKeyID: 55104285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetGetRecordSize
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37576e39d83270dcac3333e4d1f78fce32bb2669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692490"
---
# <a name="vistaapijetgetrecordsize-method"></a><span data-ttu-id="36406-103">Вистаапи. Жетжетрекордсизе, метод</span><span class="sxs-lookup"><span data-stu-id="36406-103">VistaApi.JetGetRecordSize method</span></span>

<span data-ttu-id="36406-104">Извлекает сведения о размере записи из нужного расположения.</span><span class="sxs-lookup"><span data-stu-id="36406-104">Retrieves record size information from the desired location.</span></span>

<span data-ttu-id="36406-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="36406-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="36406-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="36406-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="36406-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36406-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetRecordSize ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    ByRef recsize As JET_RECSIZE, _
    grbit As GetRecordSizeGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim recsize As JET_RECSIZE
Dim grbit As GetRecordSizeGrbitVistaApi.JetGetRecordSize(sesid, tableid, _
    recsize, grbit)
```

``` csharp
public static void JetGetRecordSize(
    JET_SESID sesid,
    JET_TABLEID tableid,
    ref JET_RECSIZE recsize,
    GetRecordSizeGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="36406-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36406-108">Parameters</span></span>

  - <span data-ttu-id="36406-109">сесид</span><span class="sxs-lookup"><span data-stu-id="36406-109">sesid</span></span>  
    <span data-ttu-id="36406-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36406-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="36406-111">Используемый сеанс.</span><span class="sxs-lookup"><span data-stu-id="36406-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="36406-112">TableID</span><span class="sxs-lookup"><span data-stu-id="36406-112">tableid</span></span>  
    <span data-ttu-id="36406-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="36406-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="36406-114">Курсор, который будет использоваться для вызова API.</span><span class="sxs-lookup"><span data-stu-id="36406-114">The cursor that will be used for the API call.</span></span> <span data-ttu-id="36406-115">Курсор должен быть размещен в записи или иметь подготовленное обновление.</span><span class="sxs-lookup"><span data-stu-id="36406-115">The cursor must be positioned on a record, or have an update prepared.</span></span>

<!-- end list -->

  - <span data-ttu-id="36406-116">рексизе</span><span class="sxs-lookup"><span data-stu-id="36406-116">recsize</span></span>  
    <span data-ttu-id="36406-117">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="36406-117">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="36406-118">Возвращает размер записи.</span><span class="sxs-lookup"><span data-stu-id="36406-118">Returns the size of the record.</span></span>

<!-- end list -->

  - <span data-ttu-id="36406-119">грбит</span><span class="sxs-lookup"><span data-stu-id="36406-119">grbit</span></span>  
    <span data-ttu-id="36406-120">Тип: [Microsoft. ISAM. ESENT. Interop. жетрекордсизегрбит](./getrecordsizegrbit-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="36406-120">Type: [Microsoft.Isam.Esent.Interop.GetRecordSizeGrbit](./getrecordsizegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="36406-121">Параметры вызова.</span><span class="sxs-lookup"><span data-stu-id="36406-121">Call options.</span></span>

## <a name="see-also"></a><span data-ttu-id="36406-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36406-122">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="36406-123">Справочник</span><span class="sxs-lookup"><span data-stu-id="36406-123">Reference</span></span>

[<span data-ttu-id="36406-124">Класс Вистаапи</span><span class="sxs-lookup"><span data-stu-id="36406-124">VistaApi class</span></span>](./vistaapi-class.md)

[<span data-ttu-id="36406-125">Элементы Вистаапи</span><span class="sxs-lookup"><span data-stu-id="36406-125">VistaApi members</span></span>](./vistaapi-members.md)

[<span data-ttu-id="36406-126">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="36406-126">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
