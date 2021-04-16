---
description: 'Дополнительные сведения о: JET_RECSIZE. Оператор вычитания'
title: JET_RECSIZE. Оператор вычитания (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtraction operator '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.op_subtraction(v=EXCHG.10)
ms:contentKeyID: 39516016
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.op_Subtraction
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtraction
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be60da4aeeab78794f087e9c7095a16dd39eb378
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702698"
---
# <a name="jet_recsizesubtraction-operator"></a><span data-ttu-id="cfffe-103">JET_RECSIZE. Оператор вычитания</span><span class="sxs-lookup"><span data-stu-id="cfffe-103">JET_RECSIZE.Subtraction operator</span></span>

<span data-ttu-id="cfffe-104">Вычисление разницы между двумя JET_RECSIZEными структурами.</span><span class="sxs-lookup"><span data-stu-id="cfffe-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="cfffe-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cfffe-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="cfffe-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cfffe-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cfffe-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfffe-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Operator - ( _
    left As JET_RECSIZE, _
    right As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim left As JET_RECSIZE
Dim right As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = (left - right)
```

``` csharp
public static JET_RECSIZE operator -(
    JET_RECSIZE left,
    JET_RECSIZE right
)
```

#### <a name="parameters"></a><span data-ttu-id="cfffe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfffe-108">Parameters</span></span>

  - <span data-ttu-id="cfffe-109">Левое</span><span class="sxs-lookup"><span data-stu-id="cfffe-109">left</span></span>  
    <span data-ttu-id="cfffe-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="cfffe-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="cfffe-111">Первый JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="cfffe-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="cfffe-112">right</span><span class="sxs-lookup"><span data-stu-id="cfffe-112">right</span></span>  
    <span data-ttu-id="cfffe-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="cfffe-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="cfffe-114">Второй JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="cfffe-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="cfffe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfffe-115">Return value</span></span>

<span data-ttu-id="cfffe-116">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="cfffe-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="cfffe-117">JET_RECSIZE, содержащая разность между левым и правым размером.</span><span class="sxs-lookup"><span data-stu-id="cfffe-117">A JET_RECSIZE containing the difference in sizes between left and right.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cfffe-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfffe-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cfffe-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="cfffe-119">Reference</span></span>

[<span data-ttu-id="cfffe-120">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="cfffe-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="cfffe-121">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="cfffe-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="cfffe-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="cfffe-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
