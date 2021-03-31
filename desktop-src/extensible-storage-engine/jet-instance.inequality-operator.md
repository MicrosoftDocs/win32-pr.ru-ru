---
description: 'Дополнительные сведения о: JET_INSTANCE. Оператор неравенства'
title: JET_INSTANCE. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Inequality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d537b01d3485e7f5e2d1d629c005a228eac92306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156899"
---
# <a name="jet_instanceinequality-operator"></a><span data-ttu-id="95628-103">JET_INSTANCE. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="95628-103">JET_INSTANCE.Inequality operator</span></span>

<span data-ttu-id="95628-104">Определяет, являются ли два указанных экземпляра JET_INSTANCE неравными.</span><span class="sxs-lookup"><span data-stu-id="95628-104">Determines whether two specified instances of JET_INSTANCE are not equal.</span></span>

<span data-ttu-id="95628-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="95628-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="95628-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="95628-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="95628-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95628-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="95628-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="95628-108">Parameters</span></span>

  - <span data-ttu-id="95628-109">LHS</span><span class="sxs-lookup"><span data-stu-id="95628-109">lhs</span></span>  
    <span data-ttu-id="95628-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95628-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="95628-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="95628-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="95628-112">rhs</span><span class="sxs-lookup"><span data-stu-id="95628-112">rhs</span></span>  
    <span data-ttu-id="95628-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="95628-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="95628-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="95628-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="95628-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95628-115">Return value</span></span>

<span data-ttu-id="95628-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="95628-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="95628-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="95628-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="95628-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95628-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="95628-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="95628-119">Reference</span></span>

[<span data-ttu-id="95628-120">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="95628-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="95628-121">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="95628-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="95628-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="95628-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
