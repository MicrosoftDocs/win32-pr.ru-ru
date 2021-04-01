---
description: 'Дополнительные сведения о: JET_LS. Оператор неравенства'
title: JET_LS. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality(Microsoft.Isam.Esent.Interop.JET_LS,Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39512483
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_LS.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: da167f0deda8254d279e7d81c7219b6e9920673f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081191"
---
# <a name="jet_lsinequality-operator"></a><span data-ttu-id="107e0-103">JET_LS. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="107e0-103">JET_LS.Inequality operator</span></span>

<span data-ttu-id="107e0-104">Определяет, являются ли два указанных экземпляра JET_LS неравными.</span><span class="sxs-lookup"><span data-stu-id="107e0-104">Determines whether two specified instances of JET_LS are not equal.</span></span>

<span data-ttu-id="107e0-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="107e0-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="107e0-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="107e0-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="107e0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="107e0-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_LS, _
    rhs As JET_LS _
) As Boolean
'Usage
Dim lhs As JET_LS
Dim rhs As JET_LS
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_LS lhs,
    JET_LS rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="107e0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="107e0-108">Parameters</span></span>

  - <span data-ttu-id="107e0-109">LHS</span><span class="sxs-lookup"><span data-stu-id="107e0-109">lhs</span></span>  
    <span data-ttu-id="107e0-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="107e0-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="107e0-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="107e0-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="107e0-112">rhs</span><span class="sxs-lookup"><span data-stu-id="107e0-112">rhs</span></span>  
    <span data-ttu-id="107e0-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="107e0-113">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="107e0-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="107e0-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="107e0-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="107e0-115">Return value</span></span>

<span data-ttu-id="107e0-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="107e0-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="107e0-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="107e0-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="107e0-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="107e0-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="107e0-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="107e0-119">Reference</span></span>

[<span data-ttu-id="107e0-120">Структура JET_LS</span><span class="sxs-lookup"><span data-stu-id="107e0-120">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="107e0-121">Элементы JET_LS</span><span class="sxs-lookup"><span data-stu-id="107e0-121">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="107e0-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="107e0-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
