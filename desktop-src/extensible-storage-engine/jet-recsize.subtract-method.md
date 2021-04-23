---
description: 'Дополнительные сведения о: JET_RECSIZE. Метод Subtract'
title: JET_RECSIZE. Метод Subtract (Microsoft. ISAM. ESENT. Interop. Vista)
TOCTitle: 'Subtract method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract(Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE,Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize.subtract(v=EXCHG.10)
ms:contentKeyID: 39514591
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE.Subtract
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9789dac524e57ea762243ed47d513d262d7ebb0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702699"
---
# <a name="jet_recsizesubtract-method"></a><span data-ttu-id="43bc5-103">JET_RECSIZE. Метод Subtract</span><span class="sxs-lookup"><span data-stu-id="43bc5-103">JET_RECSIZE.Subtract method</span></span>

<span data-ttu-id="43bc5-104">Вычисление разницы между двумя JET_RECSIZEными структурами.</span><span class="sxs-lookup"><span data-stu-id="43bc5-104">Calculate the difference in sizes between two JET_RECSIZE structures.</span></span>

<span data-ttu-id="43bc5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="43bc5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="43bc5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="43bc5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="43bc5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43bc5-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function Subtract ( _
    s1 As JET_RECSIZE, _
    s2 As JET_RECSIZE _
) As JET_RECSIZE
'Usage
Dim s1 As JET_RECSIZE
Dim s2 As JET_RECSIZE
Dim returnValue As JET_RECSIZE

returnValue = JET_RECSIZE.Subtract(s1, s2)
```

``` csharp
public static JET_RECSIZE Subtract(
    JET_RECSIZE s1,
    JET_RECSIZE s2
)
```

#### <a name="parameters"></a><span data-ttu-id="43bc5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="43bc5-108">Parameters</span></span>

  - <span data-ttu-id="43bc5-109">s1</span><span class="sxs-lookup"><span data-stu-id="43bc5-109">s1</span></span>  
    <span data-ttu-id="43bc5-110">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="43bc5-110">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="43bc5-111">Первый JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="43bc5-111">The first JET_RECSIZE.</span></span>

<!-- end list -->

  - <span data-ttu-id="43bc5-112">s2</span><span class="sxs-lookup"><span data-stu-id="43bc5-112">s2</span></span>  
    <span data-ttu-id="43bc5-113">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="43bc5-113">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
    
    <span data-ttu-id="43bc5-114">Второй JET_RECSIZE.</span><span class="sxs-lookup"><span data-stu-id="43bc5-114">The second JET_RECSIZE.</span></span>

#### <a name="return-value"></a><span data-ttu-id="43bc5-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43bc5-115">Return value</span></span>

<span data-ttu-id="43bc5-116">Тип: [Microsoft.ISAM.ESENT.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="43bc5-116">Type: [Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE](./jet-recsize-structure2.md)</span></span>  
<span data-ttu-id="43bc5-117">JET_RECSIZE, содержащий разность размеров между S1 и S2.</span><span class="sxs-lookup"><span data-stu-id="43bc5-117">A JET_RECSIZE containing the difference in sizes between s1 and s2.</span></span>  

## <a name="see-also"></a><span data-ttu-id="43bc5-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43bc5-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="43bc5-119">Справочник</span><span class="sxs-lookup"><span data-stu-id="43bc5-119">Reference</span></span>

[<span data-ttu-id="43bc5-120">Структура JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="43bc5-120">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="43bc5-121">Элементы JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="43bc5-121">JET_RECSIZE members</span></span>](./jet-recsize-members.md)

[<span data-ttu-id="43bc5-122">Пространство имен Microsoft. ISAM. ESENT. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="43bc5-122">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
