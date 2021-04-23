---
description: 'Дополнительные сведения о: JET_HANDLE. Оператор неравенства'
title: JET_HANDLE. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality(Microsoft.Isam.Esent.Interop.JET_HANDLE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39511285
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.op_Inequality
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5feee9739ad57103b71786ae7d1cdbf5f7e858ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348815"
---
# <a name="jet_handleinequality-operator"></a><span data-ttu-id="08dec-103">JET_HANDLE. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="08dec-103">JET_HANDLE.Inequality operator</span></span>

<span data-ttu-id="08dec-104">Определяет, являются ли два указанных экземпляра JET_HANDLE неравными.</span><span class="sxs-lookup"><span data-stu-id="08dec-104">Determines whether two specified instances of JET_HANDLE are not equal.</span></span>

<span data-ttu-id="08dec-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08dec-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08dec-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08dec-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08dec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08dec-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_HANDLE, _
    rhs As JET_HANDLE _
) As Boolean
'Usage
Dim lhs As JET_HANDLE
Dim rhs As JET_HANDLE
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_HANDLE lhs,
    JET_HANDLE rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="08dec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08dec-108">Parameters</span></span>

  - <span data-ttu-id="08dec-109">LHS</span><span class="sxs-lookup"><span data-stu-id="08dec-109">lhs</span></span>  
    <span data-ttu-id="08dec-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08dec-110">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="08dec-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="08dec-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="08dec-112">rhs</span><span class="sxs-lookup"><span data-stu-id="08dec-112">rhs</span></span>  
    <span data-ttu-id="08dec-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08dec-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="08dec-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="08dec-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="08dec-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08dec-115">Return value</span></span>

<span data-ttu-id="08dec-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="08dec-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="08dec-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="08dec-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="08dec-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08dec-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08dec-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="08dec-119">Reference</span></span>

[<span data-ttu-id="08dec-120">Структура JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="08dec-120">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="08dec-121">Элементы JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="08dec-121">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="08dec-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="08dec-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
