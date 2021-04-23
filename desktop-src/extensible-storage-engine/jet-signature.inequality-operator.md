---
description: 'Дополнительные сведения о: JET_SIGNATURE. Оператор неравенства'
title: JET_SIGNATURE. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39516073
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Inequality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 646b97f37aea55ee3e9d1aa24e80b9d26ea82469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702695"
---
# <a name="jet_signatureinequality-operator"></a><span data-ttu-id="227b5-103">JET_SIGNATURE. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="227b5-103">JET_SIGNATURE.Inequality operator</span></span>

<span data-ttu-id="227b5-104">Определяет, являются ли два указанных экземпляра JET_SIGNATURE неравными.</span><span class="sxs-lookup"><span data-stu-id="227b5-104">Determines whether two specified instances of JET_SIGNATURE are not equal.</span></span>

<span data-ttu-id="227b5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="227b5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="227b5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="227b5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="227b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="227b5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="227b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="227b5-108">Parameters</span></span>

  - <span data-ttu-id="227b5-109">LHS</span><span class="sxs-lookup"><span data-stu-id="227b5-109">lhs</span></span>  
    <span data-ttu-id="227b5-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="227b5-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="227b5-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="227b5-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="227b5-112">rhs</span><span class="sxs-lookup"><span data-stu-id="227b5-112">rhs</span></span>  
    <span data-ttu-id="227b5-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="227b5-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="227b5-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="227b5-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="227b5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="227b5-115">Return value</span></span>

<span data-ttu-id="227b5-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="227b5-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="227b5-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="227b5-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="227b5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="227b5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="227b5-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="227b5-119">Reference</span></span>

[<span data-ttu-id="227b5-120">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="227b5-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="227b5-121">Элементы JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="227b5-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="227b5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="227b5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
