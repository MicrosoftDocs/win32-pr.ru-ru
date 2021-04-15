---
description: 'Дополнительные сведения: оператор JET_COMMIT_ID. GreaterThanOrEqual'
title: Оператор JET_COMMIT_ID. GreaterThanOrEqual (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID,Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.jet_commit_id.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 55104298
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID.op_GreaterThanOrEqual
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e531168d2c0656c465d8eace46d00181375bc4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701718"
---
# <a name="jet_commit_idgreaterthanorequal-operator"></a><span data-ttu-id="f606b-103">JET_COMMIT_ID. GreaterThanOrEqual, оператор</span><span class="sxs-lookup"><span data-stu-id="f606b-103">JET_COMMIT_ID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="f606b-104">Определите, находится ли один коммитид перед другой коммитид.</span><span class="sxs-lookup"><span data-stu-id="f606b-104">Determine whether one commitid is before another commitid.</span></span>

<span data-ttu-id="f606b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f606b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="f606b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f606b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f606b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f606b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COMMIT_ID, _
    rhs As JET_COMMIT_ID _
) As Boolean
'Usage
Dim lhs As JET_COMMIT_ID
Dim rhs As JET_COMMIT_ID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COMMIT_ID lhs,
    JET_COMMIT_ID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f606b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f606b-108">Parameters</span></span>

  - <span data-ttu-id="f606b-109">LHS</span><span class="sxs-lookup"><span data-stu-id="f606b-109">lhs</span></span>  
    <span data-ttu-id="f606b-110">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="f606b-110">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="f606b-111">Первый коммитид для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f606b-111">The first commitid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f606b-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f606b-112">rhs</span></span>  
    <span data-ttu-id="f606b-113">Тип: [Microsoft.ISAM.ESENT.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span><span class="sxs-lookup"><span data-stu-id="f606b-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_COMMIT_ID](./jet-commit-id-class.md)</span></span>  
    
    <span data-ttu-id="f606b-114">Второй коммитид для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f606b-114">The second commitid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f606b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f606b-115">Return value</span></span>

<span data-ttu-id="f606b-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f606b-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f606b-117">Значение true, если LHS предшествует или равен RHS.</span><span class="sxs-lookup"><span data-stu-id="f606b-117">True if lhs comes after or equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f606b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f606b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f606b-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="f606b-119">Reference</span></span>

[<span data-ttu-id="f606b-120">Класс JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="f606b-120">JET_COMMIT_ID class</span></span>](./jet-commit-id-class.md)

[<span data-ttu-id="f606b-121">Элементы JET_COMMIT_ID</span><span class="sxs-lookup"><span data-stu-id="f606b-121">JET_COMMIT_ID members</span></span>](./jet-commit-id-members.md)

[<span data-ttu-id="f606b-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="f606b-122">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
