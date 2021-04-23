---
description: 'Дополнительные сведения о: JET_COLUMNID. Оператор GreaterThanOrEqual'
title: JET_COLUMNID. Оператор GreaterThanOrEqual
TOCTitle: 'GreaterThanOrEqual operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_greaterthanorequal(v=EXCHG.10)
ms:contentKeyID: 39509674
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_GreaterThanOrEqual
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.GreaterThanOrEqual
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 344d1ed95ebc6a4a79d17f8b664f3f8a76740367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692140"
---
# <a name="jet_columnidgreaterthanorequal-operator"></a><span data-ttu-id="abce5-103">JET_COLUMNID. Оператор GreaterThanOrEqual</span><span class="sxs-lookup"><span data-stu-id="abce5-103">JET_COLUMNID.GreaterThanOrEqual operator</span></span>

<span data-ttu-id="abce5-104">Определить, является ли одно значение columnid более переданного или равным другому columnid.</span><span class="sxs-lookup"><span data-stu-id="abce5-104">Determine whether one columnid is after or equal to another columnid.</span></span>

<span data-ttu-id="abce5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="abce5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="abce5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="abce5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="abce5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abce5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator >= ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs >= rhs)
```

``` csharp
public static bool operator >=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="abce5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="abce5-108">Parameters</span></span>

  - <span data-ttu-id="abce5-109">LHS</span><span class="sxs-lookup"><span data-stu-id="abce5-109">lhs</span></span>  
    <span data-ttu-id="abce5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="abce5-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="abce5-111">Первое значение columnid для сравнения.</span><span class="sxs-lookup"><span data-stu-id="abce5-111">The first columnid to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="abce5-112">rhs</span><span class="sxs-lookup"><span data-stu-id="abce5-112">rhs</span></span>  
    <span data-ttu-id="abce5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="abce5-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="abce5-114">Второе значение columnid для сравнения.</span><span class="sxs-lookup"><span data-stu-id="abce5-114">The second columnid to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="abce5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abce5-115">Return value</span></span>

<span data-ttu-id="abce5-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="abce5-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="abce5-117">Значение true, если LHS предшествует или равен RHS.</span><span class="sxs-lookup"><span data-stu-id="abce5-117">True if lhs comes after or is equal to rhs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="abce5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abce5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="abce5-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="abce5-119">Reference</span></span>

[<span data-ttu-id="abce5-120">Структура JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="abce5-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="abce5-121">Элементы JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="abce5-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="abce5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="abce5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
