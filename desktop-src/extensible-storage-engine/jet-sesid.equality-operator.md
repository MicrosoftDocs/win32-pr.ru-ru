---
description: 'Дополнительные сведения о: JET_SESID. Оператор равенства'
title: JET_SESID. Оператор равенства
TOCTitle: 'Equality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_equality(v=EXCHG.10)
ms:contentKeyID: 39511173
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Equality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Equality
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 19e0550452fb0053978cabcdb393222c814c85f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497121"
---
# <a name="jet_sesidequality-operator"></a><span data-ttu-id="b0015-103">JET_SESID. Оператор равенства</span><span class="sxs-lookup"><span data-stu-id="b0015-103">JET_SESID.Equality operator</span></span>

<span data-ttu-id="b0015-104">Определяет, равны ли два указанных экземпляра JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="b0015-104">Determines whether two specified instances of JET_SESID are equal.</span></span>

<span data-ttu-id="b0015-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b0015-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b0015-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="b0015-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b0015-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b0015-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator = ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs = rhs)
```

``` csharp
public static bool operator ==(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="b0015-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b0015-108">Parameters</span></span>

  - <span data-ttu-id="b0015-109">LHS</span><span class="sxs-lookup"><span data-stu-id="b0015-109">lhs</span></span>  
    <span data-ttu-id="b0015-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0015-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b0015-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b0015-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="b0015-112">rhs</span><span class="sxs-lookup"><span data-stu-id="b0015-112">rhs</span></span>  
    <span data-ttu-id="b0015-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="b0015-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="b0015-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="b0015-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="b0015-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0015-115">Return value</span></span>

<span data-ttu-id="b0015-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="b0015-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="b0015-117">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="b0015-117">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="b0015-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b0015-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b0015-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="b0015-119">Reference</span></span>

[<span data-ttu-id="b0015-120">Структура JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b0015-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="b0015-121">Элементы JET_SESID</span><span class="sxs-lookup"><span data-stu-id="b0015-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="b0015-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="b0015-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
