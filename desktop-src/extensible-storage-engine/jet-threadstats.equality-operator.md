---
description: 'Дополнительные сведения о: JET_THREADSTATS. Оператор равенства'
title: JET_THREADSTATS. Оператор равенства (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515069
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 076ae2cfa25f446d8d6200fbee7f53ecf0edea5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702799"
---
# <a name="jet_threadstatsequality-operator"></a><span data-ttu-id="670aa-103">JET_THREADSTATS. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="670aa-103">JET_THREADSTATS.Equality operator</span></span>

<span data-ttu-id="670aa-104">Определяет, равны ли два указанных экземпляра JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="670aa-104">Determines whether two specified instances of JET_THREADSTATS are equal.</span></span>

<span data-ttu-id="670aa-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="670aa-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="670aa-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="670aa-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="670aa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="670aa-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_THREADSTATS, _
    rhs As JET_THREADSTATS _
) As Boolean
'Usage
Dim lhs As JET_THREADSTATS
Dim rhs As JET_THREADSTATS
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_THREADSTATS lhs,
    JET_THREADSTATS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="670aa-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="670aa-108">Parameters</span></span>

  - <span data-ttu-id="670aa-109">LHS</span><span class="sxs-lookup"><span data-stu-id="670aa-109">lhs</span></span>  
    <span data-ttu-id="670aa-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="670aa-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="670aa-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="670aa-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="670aa-112">rhs</span><span class="sxs-lookup"><span data-stu-id="670aa-112">rhs</span></span>  
    <span data-ttu-id="670aa-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="670aa-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="670aa-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="670aa-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="670aa-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="670aa-115">Return value</span></span>

<span data-ttu-id="670aa-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="670aa-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="670aa-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="670aa-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="670aa-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="670aa-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="670aa-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="670aa-119">Reference</span></span>

[<span data-ttu-id="670aa-120">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="670aa-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="670aa-121">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="670aa-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="670aa-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="670aa-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
