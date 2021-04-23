---
description: 'Дополнительные сведения о: JET_LOGTIME. Оператор равенства'
title: JET_LOGTIME. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality(Microsoft.Isam.Esent.Interop.JET_LOGTIME,Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.op_equality(v=EXCHG.10)
ms:contentKeyID: 39514101
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equality
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d7f346a1331200b18c2fc9e51d8eebc1ddaef105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693786"
---
# <a name="jet_logtimeequality-operator"></a><span data-ttu-id="f6df9-103">JET_LOGTIME. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="f6df9-103">JET_LOGTIME.Equality operator</span></span>

<span data-ttu-id="f6df9-104">Определяет, равны ли два указанных экземпляра JET_LOGTIME.</span><span class="sxs-lookup"><span data-stu-id="f6df9-104">Determines whether two specified instances of JET_LOGTIME are equal.</span></span>

<span data-ttu-id="f6df9-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f6df9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f6df9-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f6df9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f6df9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f6df9-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_LOGTIME, _
    rhs As JET_LOGTIME _
) As Boolean
'Usage
Dim lhs As JET_LOGTIME
Dim rhs As JET_LOGTIME
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_LOGTIME lhs,
    JET_LOGTIME rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="f6df9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f6df9-108">Parameters</span></span>

  - <span data-ttu-id="f6df9-109">LHS</span><span class="sxs-lookup"><span data-stu-id="f6df9-109">lhs</span></span>  
    <span data-ttu-id="f6df9-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6df9-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f6df9-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f6df9-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="f6df9-112">rhs</span><span class="sxs-lookup"><span data-stu-id="f6df9-112">rhs</span></span>  
    <span data-ttu-id="f6df9-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="f6df9-113">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="f6df9-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="f6df9-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f6df9-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f6df9-115">Return value</span></span>

<span data-ttu-id="f6df9-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f6df9-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f6df9-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="f6df9-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f6df9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f6df9-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f6df9-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="f6df9-119">Reference</span></span>

[<span data-ttu-id="f6df9-120">Структура JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="f6df9-120">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="f6df9-121">Элементы JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="f6df9-121">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="f6df9-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f6df9-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
