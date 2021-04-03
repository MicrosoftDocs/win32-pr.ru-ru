---
description: 'Дополнительные сведения о: JET_HANDLE. Оператор равенства'
title: JET_HANDLE. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_equality(v=EXCHG.10)
ms:contentKeyID: 39512271
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37f0a7f10dd757a51dcdd450db2d2f0e863ab043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817824"
---
# <a name="jet_handleequality-operator"></a><span data-ttu-id="ce59d-103">JET_HANDLE. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="ce59d-103">JET_HANDLE.Equality operator</span></span>

<span data-ttu-id="ce59d-104">Определяет, равны ли два указанных экземпляра JET_HANDLE.</span><span class="sxs-lookup"><span data-stu-id="ce59d-104">Determines whether two specified instances of JET_HANDLE are equal.</span></span>

<span data-ttu-id="ce59d-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ce59d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ce59d-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ce59d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ce59d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce59d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="ce59d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ce59d-108">Parameters</span></span>

  - <span data-ttu-id="ce59d-109">LHS</span><span class="sxs-lookup"><span data-stu-id="ce59d-109">lhs</span></span>  
    <span data-ttu-id="ce59d-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce59d-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="ce59d-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="ce59d-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="ce59d-112">rhs</span><span class="sxs-lookup"><span data-stu-id="ce59d-112">rhs</span></span>  
    <span data-ttu-id="ce59d-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ce59d-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="ce59d-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="ce59d-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ce59d-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ce59d-115">Return value</span></span>

<span data-ttu-id="ce59d-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ce59d-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ce59d-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="ce59d-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce59d-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce59d-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ce59d-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ce59d-119">Reference</span></span>

[<span data-ttu-id="ce59d-120">Структура JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="ce59d-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="ce59d-121">Элементы JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="ce59d-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="ce59d-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ce59d-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
