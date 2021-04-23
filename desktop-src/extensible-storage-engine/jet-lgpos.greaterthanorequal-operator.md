---
description: 'Дополнительные сведения о: JET_LGPOS. Оператор GreaterThanOrEqual'
title: JET_LGPOS. Оператор GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_LGPOS,Microsoft.Isam.Esent.Interop.JET_LGPOS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_lgpos.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39510730
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LGPOS.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_LGPOS.op_GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a932ea983b3044d1db8395fbf87962cd3b733ae8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674446"
---
# <a name="jet_lgposgreaterthanorequal-operator"></a><span data-ttu-id="cae63-103">JET_LGPOS. Оператор GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="cae63-103">JET_LGPOS.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="cae63-104">Определить, находится ли одна запись журнала после или равна другому положению в журнале.</span><span class="sxs-lookup"><span data-stu-id="cae63-104">Determine whether one log position is after or equal to another log position.</span></span>

<span data-ttu-id="cae63-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cae63-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cae63-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cae63-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cae63-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cae63-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_LGPOS, _
    rhs As JET_LGPOS _
) As Boolean
'Usage
Dim lhs As JET_LGPOS
Dim rhs As JET_LGPOS
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_LGPOS lhs,
    JET_LGPOS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="cae63-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cae63-108">Parameters</span></span>

  - <span data-ttu-id="cae63-109">LHS</span><span class="sxs-lookup"><span data-stu-id="cae63-109">lhs</span></span>  
    <span data-ttu-id="cae63-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="cae63-110">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="cae63-111">Первое сравниваемое расположение журнала.</span><span class="sxs-lookup"><span data-stu-id="cae63-111">The first log position to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="cae63-112">rhs</span><span class="sxs-lookup"><span data-stu-id="cae63-112">rhs</span></span>  
    <span data-ttu-id="cae63-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="cae63-113">Type: [Microsoft.Isam.Esent.Interop.JET_LGPOS](./jet-lgpos-structure2.md)</span></span>  
    
    <span data-ttu-id="cae63-114">Второе сравниваемое расположение журнала.</span><span class="sxs-lookup"><span data-stu-id="cae63-114">The second log position to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cae63-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cae63-115">Return value</span></span>

<span data-ttu-id="cae63-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="cae63-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="cae63-117">Значение true, если LHS предшествует или равен RHS.</span><span class="sxs-lookup"><span data-stu-id="cae63-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cae63-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cae63-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cae63-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="cae63-119">Reference</span></span>

[<span data-ttu-id="cae63-120">Структура JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="cae63-120">JET_LGPOS structure</span></span>](./jet-lgpos-structure2.md)

[<span data-ttu-id="cae63-121">Элементы JET_LGPOS</span><span class="sxs-lookup"><span data-stu-id="cae63-121">JET_LGPOS members</span></span>](./jet-lgpos-members.md)

[<span data-ttu-id="cae63-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cae63-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
