---
description: 'Дополнительные сведения о: JET_SIGNATURE. Оператор равенства'
title: JET_SIGNATURE. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality(Microsoft.Isam.Esent.Interop.JET_SIGNATURE,Microsoft.Isam.Esent.Interop.JET_SIGNATURE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512803
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.op_Equality
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE.Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011510343f79724c2c529c2b6b18537b43facbef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810499"
---
# <a name="jet_signatureequality-operator"></a><span data-ttu-id="5214c-103">JET_SIGNATURE. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="5214c-103">JET_SIGNATURE.Equality operator</span></span>

<span data-ttu-id="5214c-104">Определяет, равны ли два указанных экземпляра JET_SIGNATURE.</span><span class="sxs-lookup"><span data-stu-id="5214c-104">Determines whether two specified instances of JET_SIGNATURE are equal.</span></span>

<span data-ttu-id="5214c-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5214c-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5214c-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5214c-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5214c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5214c-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SIGNATURE, _
    rhs As JET_SIGNATURE _
) As Boolean
'Usage
Dim lhs As JET_SIGNATURE
Dim rhs As JET_SIGNATURE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SIGNATURE lhs,
    JET_SIGNATURE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="5214c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="5214c-108">Parameters</span></span>

  - <span data-ttu-id="5214c-109">LHS</span><span class="sxs-lookup"><span data-stu-id="5214c-109">lhs</span></span>  
    <span data-ttu-id="5214c-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5214c-110">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="5214c-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5214c-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="5214c-112">rhs</span><span class="sxs-lookup"><span data-stu-id="5214c-112">rhs</span></span>  
    <span data-ttu-id="5214c-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="5214c-113">Type: [Microsoft.Isam.Esent.Interop.JET_SIGNATURE](./jet-signature-structure2.md)</span></span>  
    
    <span data-ttu-id="5214c-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="5214c-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="5214c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5214c-115">Return value</span></span>

<span data-ttu-id="5214c-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5214c-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="5214c-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="5214c-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5214c-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5214c-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5214c-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="5214c-119">Reference</span></span>

[<span data-ttu-id="5214c-120">Структура JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="5214c-120">JET_SIGNATURE structure</span></span>](./jet-signature-structure2.md)

[<span data-ttu-id="5214c-121">Элементы JET_SIGNATURE</span><span class="sxs-lookup"><span data-stu-id="5214c-121">JET_SIGNATURE members</span></span>](./jet-signature-members.md)

[<span data-ttu-id="5214c-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5214c-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
