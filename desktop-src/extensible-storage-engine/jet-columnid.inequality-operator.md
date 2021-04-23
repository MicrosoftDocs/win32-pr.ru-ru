---
description: 'Дополнительные сведения о: JET_COLUMNID. Оператор неравенства'
title: JET_COLUMNID. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_COLUMNID,Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516136
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Inequality
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6b0856a5c551be06dd7f4b55f8f144c0e509f1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702425"
---
# <a name="jet_columnidinequality-operator"></a><span data-ttu-id="7bcb9-103">JET_COLUMNID. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="7bcb9-103">JET_COLUMNID.Inequality operator</span></span>

<span data-ttu-id="7bcb9-104">Определяет, являются ли два указанных экземпляра JET_COLUMNID неравными.</span><span class="sxs-lookup"><span data-stu-id="7bcb9-104">Determines whether two specified instances of JET_COLUMNID are not equal.</span></span>

<span data-ttu-id="7bcb9-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7bcb9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7bcb9-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="7bcb9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7bcb9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bcb9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_COLUMNID, _
    rhs As JET_COLUMNID _
) As Boolean
'Usage
Dim lhs As JET_COLUMNID
Dim rhs As JET_COLUMNID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_COLUMNID lhs,
    JET_COLUMNID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="7bcb9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bcb9-108">Parameters</span></span>

  - <span data-ttu-id="7bcb9-109">LHS</span><span class="sxs-lookup"><span data-stu-id="7bcb9-109">lhs</span></span>  
    <span data-ttu-id="7bcb9-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7bcb9-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7bcb9-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7bcb9-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="7bcb9-112">rhs</span><span class="sxs-lookup"><span data-stu-id="7bcb9-112">rhs</span></span>  
    <span data-ttu-id="7bcb9-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7bcb9-113">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="7bcb9-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="7bcb9-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7bcb9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bcb9-115">Return value</span></span>

<span data-ttu-id="7bcb9-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="7bcb9-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="7bcb9-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="7bcb9-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7bcb9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bcb9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7bcb9-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="7bcb9-119">Reference</span></span>

[<span data-ttu-id="7bcb9-120">Структура JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7bcb9-120">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="7bcb9-121">Элементы JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7bcb9-121">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="7bcb9-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="7bcb9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
