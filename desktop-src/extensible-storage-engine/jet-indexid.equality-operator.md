---
description: 'Дополнительные сведения о: JET_INDEXID. Оператор равенства'
title: JET_INDEXID. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39516722
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9fa7574aeed52377b516f63549a6f690dc168d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999725"
---
# <a name="jet_indexidequality-operator"></a><span data-ttu-id="0abab-103">JET_INDEXID. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="0abab-103">JET_INDEXID.Equality operator</span></span>

<span data-ttu-id="0abab-104">Определяет, равны ли два указанных экземпляра JET_INDEXID.</span><span class="sxs-lookup"><span data-stu-id="0abab-104">Determines whether two specified instances of JET_INDEXID are equal.</span></span>

<span data-ttu-id="0abab-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0abab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0abab-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0abab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0abab-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0abab-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="0abab-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0abab-108">Parameters</span></span>

  - <span data-ttu-id="0abab-109">LHS</span><span class="sxs-lookup"><span data-stu-id="0abab-109">lhs</span></span>  
    <span data-ttu-id="0abab-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="0abab-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="0abab-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="0abab-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="0abab-112">rhs</span><span class="sxs-lookup"><span data-stu-id="0abab-112">rhs</span></span>  
    <span data-ttu-id="0abab-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="0abab-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="0abab-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="0abab-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0abab-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0abab-115">Return value</span></span>

<span data-ttu-id="0abab-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0abab-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0abab-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="0abab-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0abab-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0abab-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0abab-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="0abab-119">Reference</span></span>

[<span data-ttu-id="0abab-120">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0abab-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="0abab-121">Элементы JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="0abab-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="0abab-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0abab-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
