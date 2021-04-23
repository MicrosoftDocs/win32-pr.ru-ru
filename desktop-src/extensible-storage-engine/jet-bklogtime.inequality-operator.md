---
description: 'Дополнительные сведения о: JET_BKLOGTIME. Оператор неравенства'
title: JET_BKLOGTIME. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality(Microsoft.Isam.Esent.Interop.JET_BKLOGTIME,Microsoft.Isam.Esent.Interop.JET_BKLOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512908
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.Inequality
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.op_Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42f13a1068543caaa590015151b523c1a441c806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702951"
---
# <a name="jet_bklogtimeinequality-operator"></a><span data-ttu-id="c84bf-103">JET_BKLOGTIME. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="c84bf-103">JET_BKLOGTIME.Inequality operator</span></span>

<span data-ttu-id="c84bf-104">Определяет, являются ли два указанных экземпляра JET_BKLOGTIME неравными.</span><span class="sxs-lookup"><span data-stu-id="c84bf-104">Determines whether two specified instances of JET_BKLOGTIME are not equal.</span></span>

<span data-ttu-id="c84bf-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c84bf-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c84bf-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="c84bf-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c84bf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c84bf-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_BKLOGTIME, _
    rhs As JET_BKLOGTIME _
) As Boolean
'Usage
Dim lhs As JET_BKLOGTIME
Dim rhs As JET_BKLOGTIME
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_BKLOGTIME lhs,
    JET_BKLOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="c84bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c84bf-108">Parameters</span></span>

  - <span data-ttu-id="c84bf-109">LHS</span><span class="sxs-lookup"><span data-stu-id="c84bf-109">lhs</span></span>  
    <span data-ttu-id="c84bf-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c84bf-110">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="c84bf-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c84bf-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="c84bf-112">rhs</span><span class="sxs-lookup"><span data-stu-id="c84bf-112">rhs</span></span>  
    <span data-ttu-id="c84bf-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="c84bf-113">Type: [Microsoft.Isam.Esent.Interop.JET_BKLOGTIME](./jet-bklogtime-structure2.md)</span></span>  
    
    <span data-ttu-id="c84bf-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="c84bf-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c84bf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c84bf-115">Return value</span></span>

<span data-ttu-id="c84bf-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="c84bf-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="c84bf-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="c84bf-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="c84bf-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c84bf-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c84bf-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="c84bf-119">Reference</span></span>

[<span data-ttu-id="c84bf-120">Структура JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="c84bf-120">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="c84bf-121">Элементы JET_BKLOGTIME</span><span class="sxs-lookup"><span data-stu-id="c84bf-121">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="c84bf-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="c84bf-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
