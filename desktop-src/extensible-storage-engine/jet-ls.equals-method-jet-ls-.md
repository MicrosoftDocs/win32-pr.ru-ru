---
description: 'Дополнительные сведения о: JET_LS. Метод Equals (JET_LS)'
title: JET_LS. Метод Equals (JET_LS)
TOCTitle: Equals method (JET_LS)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LS.Equals(Microsoft.Isam.Esent.Interop.JET_LS)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls.equals(v=EXCHG.10)
ms:contentKeyID: 39510488
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c8a571f97fcf5abc5ff9a69ff476d48adfd8015c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712441"
---
# <a name="jet_lsequals-method-jet_ls"></a><span data-ttu-id="e8aec-103">JET_LS. Метод Equals (JET_LS)</span><span class="sxs-lookup"><span data-stu-id="e8aec-103">JET_LS.Equals method (JET_LS)</span></span>

<span data-ttu-id="e8aec-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="e8aec-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="e8aec-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e8aec-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e8aec-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="e8aec-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e8aec-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8aec-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_LS _
) As Boolean
'Usage
Dim instance As JET_LS
Dim other As JET_LS
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_LS other
)
```

#### <a name="parameters"></a><span data-ttu-id="e8aec-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8aec-108">Parameters</span></span>

  - <span data-ttu-id="e8aec-109">др.</span><span class="sxs-lookup"><span data-stu-id="e8aec-109">other</span></span>  
    <span data-ttu-id="e8aec-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e8aec-110">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="e8aec-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="e8aec-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e8aec-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8aec-112">Return value</span></span>

<span data-ttu-id="e8aec-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="e8aec-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="e8aec-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="e8aec-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="e8aec-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="e8aec-115">Implements</span></span>

[<span data-ttu-id="e8aec-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="e8aec-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="e8aec-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8aec-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e8aec-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="e8aec-118">Reference</span></span>

[<span data-ttu-id="e8aec-119">Структура JET_LS</span><span class="sxs-lookup"><span data-stu-id="e8aec-119">JET_LS structure</span></span>](./jet-ls-structure.md)

[<span data-ttu-id="e8aec-120">Элементы JET_LS</span><span class="sxs-lookup"><span data-stu-id="e8aec-120">JET_LS members</span></span>](./jet-ls-members.md)

[<span data-ttu-id="e8aec-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="e8aec-121">Equals overload</span></span>](./jet-ls.equals-method.md)

[<span data-ttu-id="e8aec-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="e8aec-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
