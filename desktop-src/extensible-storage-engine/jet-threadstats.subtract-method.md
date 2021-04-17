---
description: 'Дополнительные сведения о: JET_THREADSTATS. Метод Subtract'
title: JET_THREADSTATS. Метод Subtract (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.subtract(v=EXCHG.10)
ms:contentKeyID: 39514465
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf1f47258fe965c41b0a02ccbb32712b0a54c97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693432"
---
# <a name="jet_threadstatssubtract-method"></a><span data-ttu-id="9052f-103">JET_THREADSTATS. Метод Subtract</span><span class="sxs-lookup"><span data-stu-id="9052f-103">JET_THREADSTATS.Subtract method</span></span>

<span data-ttu-id="9052f-104">Вычислите разницу в статистике между двумя JET_THREADSTATSными структурами.</span><span class="sxs-lookup"><span data-stu-id="9052f-104">Calculate the difference in stats between two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="9052f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9052f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="9052f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="9052f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9052f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9052f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = JET_THREADSTATS.Subtract(t1, t2)
```

``` csharp
public static JET_THREADSTATS Subtract(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="9052f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9052f-108">Parameters</span></span>

  - <span data-ttu-id="9052f-109">t1</span><span class="sxs-lookup"><span data-stu-id="9052f-109">t1</span></span>  
    <span data-ttu-id="9052f-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9052f-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="9052f-111">Первый JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="9052f-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="9052f-112">T2</span><span class="sxs-lookup"><span data-stu-id="9052f-112">t2</span></span>  
    <span data-ttu-id="9052f-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9052f-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="9052f-114">Второй JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="9052f-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="9052f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9052f-115">Return value</span></span>

<span data-ttu-id="9052f-116">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="9052f-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="9052f-117">JET_THREADSTATS, содержащий разницу между T1 и T2.</span><span class="sxs-lookup"><span data-stu-id="9052f-117">A JET_THREADSTATS containing the difference in stats between t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="9052f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9052f-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9052f-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="9052f-119">Reference</span></span>

[<span data-ttu-id="9052f-120">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="9052f-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="9052f-121">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="9052f-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="9052f-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="9052f-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
