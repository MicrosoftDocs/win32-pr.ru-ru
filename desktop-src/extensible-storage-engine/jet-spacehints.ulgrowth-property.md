---
description: 'Дополнительные сведения о свойстве: JET_SPACEHINTS. Улгровс'
title: Свойство JET_SPACEHINTS. Улгровс
TOCTitle: 'ulGrowth property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints.ulgrowth(v=EXCHG.10)
ms:contentKeyID: 55103929
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.set_ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.ulGrowth
- Microsoft.Isam.Esent.Interop.JET_SPACEHINTS.get_ulGrowth
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 946975a1777778871ecb8ae66c8e567e7c2ffcd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808471"
---
# <a name="jet_spacehintsulgrowth-property"></a><span data-ttu-id="5ae02-103">Свойство JET_SPACEHINTS. Улгровс</span><span class="sxs-lookup"><span data-stu-id="5ae02-103">JET_SPACEHINTS.ulGrowth property</span></span>

<span data-ttu-id="5ae02-104">Возвращает или задает процент роста по отношению к последнему или исходному размеру (возможно, округленному до ближайшего размера выделенной памяти JET).</span><span class="sxs-lookup"><span data-stu-id="5ae02-104">Gets or sets the percent growth from last growth or initial size (possibly rounded to nearest native JET allocation size).</span></span> <span data-ttu-id="5ae02-105">Допустимые значения: 0, \[ 100, 50000).</span><span class="sxs-lookup"><span data-stu-id="5ae02-105">Valid values are 0, and \[100, 50000).</span></span>

<span data-ttu-id="5ae02-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5ae02-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5ae02-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="5ae02-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5ae02-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ae02-108">Syntax</span></span>

``` vb
'Declaration
Public Property ulGrowth As Integer
    Get
    Set
'Usage
Dim instance As JET_SPACEHINTS
Dim value As Integer

value = instance.ulGrowth

instance.ulGrowth = value
```

``` csharp
public int ulGrowth { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="5ae02-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5ae02-109">Property value</span></span>

<span data-ttu-id="5ae02-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="5ae02-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="5ae02-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ae02-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5ae02-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="5ae02-112">Reference</span></span>

[<span data-ttu-id="5ae02-113">Класс JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5ae02-113">JET_SPACEHINTS class</span></span>](./jet-spacehints-class.md)

[<span data-ttu-id="5ae02-114">Элементы JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5ae02-114">JET_SPACEHINTS members</span></span>](./jet-spacehints-members.md)

[<span data-ttu-id="5ae02-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="5ae02-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
