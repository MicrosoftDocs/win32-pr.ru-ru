---
description: 'Дополнительные сведения о: JET_DBID. Оператор неравенства'
title: JET_DBID. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511214
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_DBID.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10dc41be66e687f7cba277dcbd7486e08ae2ad74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711005"
---
# <a name="jet_dbidinequality-operator"></a><span data-ttu-id="a33f6-103">JET_DBID. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="a33f6-103">JET_DBID.Inequality operator</span></span>

<span data-ttu-id="a33f6-104">Определяет, являются ли два указанных экземпляра JET_DBID неравными.</span><span class="sxs-lookup"><span data-stu-id="a33f6-104">Determines whether two specified instances of JET_DBID are not equal.</span></span>

<span data-ttu-id="a33f6-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a33f6-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a33f6-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a33f6-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a33f6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a33f6-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="a33f6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a33f6-108">Parameters</span></span>

  - <span data-ttu-id="a33f6-109">LHS</span><span class="sxs-lookup"><span data-stu-id="a33f6-109">lhs</span></span>  
    <span data-ttu-id="a33f6-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a33f6-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a33f6-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a33f6-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="a33f6-112">rhs</span><span class="sxs-lookup"><span data-stu-id="a33f6-112">rhs</span></span>  
    <span data-ttu-id="a33f6-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a33f6-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="a33f6-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a33f6-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="a33f6-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a33f6-115">Return value</span></span>

<span data-ttu-id="a33f6-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="a33f6-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="a33f6-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="a33f6-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a33f6-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a33f6-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a33f6-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="a33f6-119">Reference</span></span>

[<span data-ttu-id="a33f6-120">Структура JET_DBID</span><span class="sxs-lookup"><span data-stu-id="a33f6-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="a33f6-121">Элементы JET_DBID</span><span class="sxs-lookup"><span data-stu-id="a33f6-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="a33f6-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a33f6-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
