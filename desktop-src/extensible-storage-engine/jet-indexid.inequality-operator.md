---
description: 'Дополнительные сведения о: JET_INDEXID. Оператор неравенства'
title: JET_INDEXID. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_INDEXID,Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39510422
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f08dc8d80a9d62a0cb837e4d4d1fd5e60e025c5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999627"
---
# <a name="jet_indexidinequality-operator"></a><span data-ttu-id="f6a96-103">JET_INDEXID. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="f6a96-103">JET_INDEXID.Inequality operator</span></span>

<span data-ttu-id="f6a96-104">Определяет, являются ли два указанных экземпляра JET_INDEXID неравными.</span><span class="sxs-lookup"><span data-stu-id="f6a96-104">Determines whether two specified instances of JET_INDEXID are not equal.</span></span>

<span data-ttu-id="f6a96-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6a96-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6a96-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6a96-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6a96-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6a96-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_INDEXID, _
    rhs As JET_INDEXID _
) As Boolean
'Usage
Dim lhs As JET_INDEXID
Dim rhs As JET_INDEXID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_INDEXID lhs,
    JET_INDEXID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f6a96-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6a96-108">Parameters</span></span>

  - <span data-ttu-id="f6a96-109">LHS</span><span class="sxs-lookup"><span data-stu-id="f6a96-109">lhs</span></span>  
    <span data-ttu-id="f6a96-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6a96-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="f6a96-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f6a96-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6a96-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f6a96-112">rhs</span></span>  
    <span data-ttu-id="f6a96-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6a96-113">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="f6a96-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f6a96-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6a96-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6a96-115">Return value</span></span>

<span data-ttu-id="f6a96-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f6a96-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f6a96-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="f6a96-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6a96-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6a96-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6a96-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="f6a96-119">Reference</span></span>

[<span data-ttu-id="f6a96-120">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f6a96-120">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="f6a96-121">Элементы JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="f6a96-121">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="f6a96-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6a96-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
