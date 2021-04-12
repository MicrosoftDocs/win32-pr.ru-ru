---
description: 'Дополнительные сведения о: JET_DBID. Оператор равенства'
title: JET_DBID. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality(Microsoft.Isam.Esent.Interop.JET_DBID,Microsoft.Isam.Esent.Interop.JET_DBID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511764
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID.Equality
- Microsoft.Isam.Esent.Interop.JET_DBID.op_Equality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f9e99de78665d07e1e5a800f5520a39eb05e74e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543287"
---
# <a name="jet_dbidequality-operator"></a><span data-ttu-id="be4ef-103">JET_DBID. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="be4ef-103">JET_DBID.Equality operator</span></span>

<span data-ttu-id="be4ef-104">Определяет, равны ли два указанных экземпляра JET_DBID.</span><span class="sxs-lookup"><span data-stu-id="be4ef-104">Determines whether two specified instances of JET_DBID are equal.</span></span>

<span data-ttu-id="be4ef-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="be4ef-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="be4ef-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="be4ef-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="be4ef-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be4ef-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_DBID, _
    rhs As JET_DBID _
) As Boolean
'Usage
Dim lhs As JET_DBID
Dim rhs As JET_DBID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_DBID lhs,
    JET_DBID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="be4ef-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="be4ef-108">Parameters</span></span>

  - <span data-ttu-id="be4ef-109">LHS</span><span class="sxs-lookup"><span data-stu-id="be4ef-109">lhs</span></span>  
    <span data-ttu-id="be4ef-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="be4ef-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="be4ef-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="be4ef-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="be4ef-112">rhs</span><span class="sxs-lookup"><span data-stu-id="be4ef-112">rhs</span></span>  
    <span data-ttu-id="be4ef-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBID](./jet-dbid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="be4ef-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBID](./jet-dbid-structure.md)</span></span>  
    
    <span data-ttu-id="be4ef-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="be4ef-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="be4ef-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be4ef-115">Return value</span></span>

<span data-ttu-id="be4ef-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="be4ef-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="be4ef-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="be4ef-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="be4ef-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be4ef-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be4ef-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="be4ef-119">Reference</span></span>

[<span data-ttu-id="be4ef-120">Структура JET_DBID</span><span class="sxs-lookup"><span data-stu-id="be4ef-120">JET_DBID structure</span></span>](./jet-dbid-structure.md)

[<span data-ttu-id="be4ef-121">Элементы JET_DBID</span><span class="sxs-lookup"><span data-stu-id="be4ef-121">JET_DBID members</span></span>](./jet-dbid-members.md)

[<span data-ttu-id="be4ef-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="be4ef-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
