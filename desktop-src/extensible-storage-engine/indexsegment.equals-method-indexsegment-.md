---
description: 'Дополнительные сведения о методе: Индекссегмент. Equals (Индекссегмент)'
title: Метод Индекссегмент. Equals (Индекссегмент)
TOCTitle: Equals method (IndexSegment)
ms:assetid: M:Microsoft.Isam.Esent.Interop.IndexSegment.Equals(Microsoft.Isam.Esent.Interop.IndexSegment)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.indexsegment.equals(v=EXCHG.10)
ms:contentKeyID: 55103276
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.IndexSegment.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad14e8a22ab3e64f9df870f1e0a218e83f30a0aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263385"
---
# <a name="indexsegmentequals-method-indexsegment"></a><span data-ttu-id="87ab5-103">Метод Индекссегмент. Equals (Индекссегмент)</span><span class="sxs-lookup"><span data-stu-id="87ab5-103">IndexSegment.Equals method (IndexSegment)</span></span>

<span data-ttu-id="87ab5-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="87ab5-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="87ab5-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="87ab5-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="87ab5-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="87ab5-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="87ab5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87ab5-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As IndexSegment _
) As Boolean
'Usage
Dim instance As IndexSegment
Dim other As IndexSegment
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    IndexSegment other
)
```

#### <a name="parameters"></a><span data-ttu-id="87ab5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="87ab5-108">Parameters</span></span>

  - <span data-ttu-id="87ab5-109">др.</span><span class="sxs-lookup"><span data-stu-id="87ab5-109">other</span></span>  
    <span data-ttu-id="87ab5-110">Тип: [Microsoft. ISAM. ESENT. Interop. индекссегмент](./indexsegment-class.md)</span><span class="sxs-lookup"><span data-stu-id="87ab5-110">Type: [Microsoft.Isam.Esent.Interop.IndexSegment](./indexsegment-class.md)</span></span>  
    
    <span data-ttu-id="87ab5-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="87ab5-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="87ab5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87ab5-112">Return value</span></span>

<span data-ttu-id="87ab5-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="87ab5-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="87ab5-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="87ab5-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="87ab5-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="87ab5-115">Implements</span></span>

[<span data-ttu-id="87ab5-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="87ab5-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="87ab5-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87ab5-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="87ab5-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="87ab5-118">Reference</span></span>

[<span data-ttu-id="87ab5-119">Класс Индекссегмент</span><span class="sxs-lookup"><span data-stu-id="87ab5-119">IndexSegment class</span></span>](./indexsegment-class.md)

[<span data-ttu-id="87ab5-120">Элементы Индекссегмент</span><span class="sxs-lookup"><span data-stu-id="87ab5-120">IndexSegment members</span></span>](./indexsegment-members.md)

[<span data-ttu-id="87ab5-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="87ab5-121">Equals overload</span></span>](./indexsegment.equals-method.md)

[<span data-ttu-id="87ab5-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="87ab5-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
