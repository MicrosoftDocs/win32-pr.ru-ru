---
description: 'Дополнительные сведения о: JET_INSTANCE. Оператор равенства'
title: JET_INSTANCE. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512671
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equality
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41a3ffe2eebeb7566d431c655a27360c9380413c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656623"
---
# <a name="jet_instanceequality-operator"></a><span data-ttu-id="1dd2b-103">JET_INSTANCE. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="1dd2b-103">JET_INSTANCE.Equality operator</span></span>

<span data-ttu-id="1dd2b-104">Определяет, равны ли два указанных экземпляра JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-104">Determines whether two specified instances of JET_INSTANCE are equal.</span></span>

<span data-ttu-id="1dd2b-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1dd2b-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd2b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1dd2b-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INSTANCE, _
    rhs As JET_INSTANCE _
) As Boolean
'Usage
Dim lhs As JET_INSTANCE
Dim rhs As JET_INSTANCE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INSTANCE lhs,
    JET_INSTANCE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="1dd2b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1dd2b-108">Parameters</span></span>

  - <span data-ttu-id="1dd2b-109">LHS</span><span class="sxs-lookup"><span data-stu-id="1dd2b-109">lhs</span></span>  
    <span data-ttu-id="1dd2b-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1dd2b-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="1dd2b-112">rhs</span><span class="sxs-lookup"><span data-stu-id="1dd2b-112">rhs</span></span>  
    <span data-ttu-id="1dd2b-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-113">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="1dd2b-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="1dd2b-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1dd2b-115">Return value</span></span>

<span data-ttu-id="1dd2b-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="1dd2b-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="1dd2b-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="1dd2b-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1dd2b-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1dd2b-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1dd2b-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="1dd2b-119">Reference</span></span>

[<span data-ttu-id="1dd2b-120">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1dd2b-120">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="1dd2b-121">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="1dd2b-121">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="1dd2b-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="1dd2b-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
