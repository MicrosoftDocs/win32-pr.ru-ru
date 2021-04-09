---
description: 'Дополнительные сведения о: JET_RECSIZE. Оператор равенства'
title: JET_RECSIZE. Оператор равенства (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_equality(v=EXCHG.10)
ms:contentKeyID: 39515439
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Equality
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f95ee6975a71e40d702b1f68c47ad6831881ffa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143576"
---
# <a name="jet_recsizeequality-operator"></a><span data-ttu-id="11566-103">JET_RECSIZE. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="11566-103">JET_RECSIZE.Equality operator</span></span>

<span data-ttu-id="11566-104">Определяет, равны ли два указанных экземпляра JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="11566-104">Determines whether two specified instances of JET_RECSIZE are equal.</span></span>

<span data-ttu-id="11566-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="11566-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="11566-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="11566-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="11566-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11566-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_RECSIZE, _
    rhs As JET_RECSIZE _
) As Boolean
'Usage
Dim lhs As JET_RECSIZE
Dim rhs As JET_RECSIZE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_RECSIZE lhs,
    JET_RECSIZE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="11566-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11566-108">Parameters</span></span>

  - <span data-ttu-id="11566-109">LHS</span><span class="sxs-lookup"><span data-stu-id="11566-109">lhs</span></span>  
    <span data-ttu-id="11566-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="11566-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="11566-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="11566-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="11566-112">rhs</span><span class="sxs-lookup"><span data-stu-id="11566-112">rhs</span></span>  
    <span data-ttu-id="11566-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="11566-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="11566-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="11566-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="11566-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11566-115">Return value</span></span>

<span data-ttu-id="11566-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="11566-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="11566-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="11566-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="11566-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11566-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="11566-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="11566-119">Reference</span></span>

[<span data-ttu-id="11566-120">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="11566-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="11566-121">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="11566-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="11566-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="11566-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
