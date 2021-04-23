---
description: 'Дополнительные сведения о: JET_THREADSTATS. Оператор сложения'
title: JET_THREADSTATS. Оператор сложения (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Addition operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition(Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS,Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_threadstats.op_addition(v=EXCHG.10)
ms:contentKeyID: 39516195
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.Addition
- Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS.op_Addition
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 829bf96b3c7095b95644db220a5d18c7e987e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703343"
---
# <a name="jet_threadstatsaddition-operator"></a><span data-ttu-id="ba2c2-103">JET_THREADSTATS. Оператор сложения</span><span class="sxs-lookup"><span data-stu-id="ba2c2-103">JET_THREADSTATS.Addition operator</span></span>

<span data-ttu-id="ba2c2-104">Добавьте статистику в две структуры JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="ba2c2-104">Add the stats in two JET_THREADSTATS structures.</span></span>

<span data-ttu-id="ba2c2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ba2c2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ba2c2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ba2c2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ba2c2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba2c2-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator + ( _
    t1 As JET_THREADSTATS, _
    t2 As JET_THREADSTATS _
) As JET_THREADSTATS
'Usage
Dim t1 As JET_THREADSTATS
Dim t2 As JET_THREADSTATS
Dim returnValue As JET_THREADSTATS

returnValue = (t1 + t2)
```

``` csharp
public static JET_THREADSTATS operator +(
    JET_THREADSTATS t1,
    JET_THREADSTATS t2
)
```

#### <a name="parameters"></a><span data-ttu-id="ba2c2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba2c2-108">Parameters</span></span>

  - <span data-ttu-id="ba2c2-109">t1</span><span class="sxs-lookup"><span data-stu-id="ba2c2-109">t1</span></span>  
    <span data-ttu-id="ba2c2-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ba2c2-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="ba2c2-111">Первый JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="ba2c2-111">The first JET_THREADSTATS.</span></span>

<!-- end list -->

  - <span data-ttu-id="ba2c2-112">T2</span><span class="sxs-lookup"><span data-stu-id="ba2c2-112">t2</span></span>  
    <span data-ttu-id="ba2c2-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ba2c2-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
    
    <span data-ttu-id="ba2c2-114">Второй JET_THREADSTATS.</span><span class="sxs-lookup"><span data-stu-id="ba2c2-114">The second JET_THREADSTATS.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ba2c2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba2c2-115">Return value</span></span>

<span data-ttu-id="ba2c2-116">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="ba2c2-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_THREADSTATS](./jet-threadstats-structure2.md)</span></span>  
<span data-ttu-id="ba2c2-117">JET_THREADSTATS, содержащий результат добавления статистики в T1 и T2.</span><span class="sxs-lookup"><span data-stu-id="ba2c2-117">A JET_THREADSTATS containing the result of adding the stats in t1 and t2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ba2c2-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba2c2-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ba2c2-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="ba2c2-119">Reference</span></span>

[<span data-ttu-id="ba2c2-120">Структура JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="ba2c2-120">JET_THREADSTATS structure</span></span>](./jet-threadstats-structure2.md)

[<span data-ttu-id="ba2c2-121">Элементы JET_THREADSTATS</span><span class="sxs-lookup"><span data-stu-id="ba2c2-121">JET_THREADSTATS members</span></span>](./jet-threadstats-members.md)

[<span data-ttu-id="ba2c2-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="ba2c2-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
