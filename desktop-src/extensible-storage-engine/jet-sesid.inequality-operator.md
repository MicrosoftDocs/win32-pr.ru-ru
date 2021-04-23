---
description: 'Дополнительные сведения о: JET_SESID. Оператор неравенства'
title: JET_SESID. Оператор неравенства
TOCTitle: 'Inequality operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_SESID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_sesid.op_inequality(v=EXCHG.10)
ms:contentKeyID: 39514305
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SESID.Inequality
- Microsoft.Isam.Esent.Interop.JET_SESID.op_Inequality
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e42b5e21937ae8af4ccd04708520ece40558c5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144263"
---
# <a name="jet_sesidinequality-operator"></a><span data-ttu-id="473c7-103">JET_SESID. Оператор неравенства</span><span class="sxs-lookup"><span data-stu-id="473c7-103">JET_SESID.Inequality operator</span></span>

<span data-ttu-id="473c7-104">Определяет, являются ли два указанных экземпляра JET_SESID неравными.</span><span class="sxs-lookup"><span data-stu-id="473c7-104">Determines whether two specified instances of JET_SESID are not equal.</span></span>

<span data-ttu-id="473c7-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="473c7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="473c7-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="473c7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="473c7-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="473c7-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator <> ( _
    lhs As JET_SESID, _
    rhs As JET_SESID _
) As Boolean
'Usage
Dim lhs As JET_SESID
Dim rhs As JET_SESID
Dim returnValue As Boolean

returnValue = (lhs <> rhs)
```

``` csharp
public static bool operator !=(
    JET_SESID lhs,
    JET_SESID rhs
)
```

#### <a name="parameters"></a><span data-ttu-id="473c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="473c7-108">Parameters</span></span>

  - <span data-ttu-id="473c7-109">LHS</span><span class="sxs-lookup"><span data-stu-id="473c7-109">lhs</span></span>  
    <span data-ttu-id="473c7-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="473c7-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="473c7-111">Первый экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="473c7-111">The first instance to compare.</span></span>

<!-- end list -->

  - <span data-ttu-id="473c7-112">rhs</span><span class="sxs-lookup"><span data-stu-id="473c7-112">rhs</span></span>  
    <span data-ttu-id="473c7-113">Тип: [Microsoft.ISAM.ESENT.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="473c7-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="473c7-114">Второй экземпляр для сравнения.</span><span class="sxs-lookup"><span data-stu-id="473c7-114">The second instance to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="473c7-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="473c7-115">Return value</span></span>

<span data-ttu-id="473c7-116">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="473c7-116">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="473c7-117">Значение true, если два экземпляра не равны.</span><span class="sxs-lookup"><span data-stu-id="473c7-117">True if the two instances are not equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="473c7-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="473c7-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="473c7-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="473c7-119">Reference</span></span>

[<span data-ttu-id="473c7-120">Структура JET_SESID</span><span class="sxs-lookup"><span data-stu-id="473c7-120">JET_SESID structure</span></span>](./jet-sesid-structure.md)

[<span data-ttu-id="473c7-121">Элементы JET_SESID</span><span class="sxs-lookup"><span data-stu-id="473c7-121">JET_SESID members</span></span>](./jet-sesid-members.md)

[<span data-ttu-id="473c7-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="473c7-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
