---
description: 'Дополнительные сведения о: JET_INDEXID. Метод Equals (JET_INDEXID)'
title: JET_INDEXID. Метод Equals (JET_INDEXID)
TOCTitle: Equals method (JET_INDEXID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INDEXID.Equals(Microsoft.Isam.Esent.Interop.JET_INDEXID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexid.equals(v=EXCHG.10)
ms:contentKeyID: 39515277
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INDEXID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10877a283e10d6126c46fa1c5687b23814aa2ac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656695"
---
# <a name="jet_indexidequals-method-jet_indexid"></a><span data-ttu-id="56634-103">JET_INDEXID. Метод Equals (JET_INDEXID)</span><span class="sxs-lookup"><span data-stu-id="56634-103">JET_INDEXID.Equals method (JET_INDEXID)</span></span>

<span data-ttu-id="56634-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="56634-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="56634-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="56634-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="56634-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="56634-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="56634-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56634-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INDEXID _
) As Boolean
'Usage
Dim instance As JET_INDEXID
Dim other As JET_INDEXID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INDEXID other
)
```

#### <a name="parameters"></a><span data-ttu-id="56634-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56634-108">Parameters</span></span>

  - <span data-ttu-id="56634-109">др.</span><span class="sxs-lookup"><span data-stu-id="56634-109">other</span></span>  
    <span data-ttu-id="56634-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="56634-110">Type: [Microsoft.Isam.Esent.Interop.JET_INDEXID](./jet-indexid-structure2.md)</span></span>  
    
    <span data-ttu-id="56634-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="56634-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="56634-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56634-112">Return value</span></span>

<span data-ttu-id="56634-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="56634-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="56634-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="56634-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="56634-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="56634-115">Implements</span></span>

[<span data-ttu-id="56634-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="56634-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="56634-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56634-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="56634-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="56634-118">Reference</span></span>

[<span data-ttu-id="56634-119">Структура JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="56634-119">JET_INDEXID structure</span></span>](./jet-indexid-structure2.md)

[<span data-ttu-id="56634-120">Элементы JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="56634-120">JET_INDEXID members</span></span>](./jet-indexid-members.md)

[<span data-ttu-id="56634-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="56634-121">Equals overload</span></span>](./jet-indexid.equals-method.md)

[<span data-ttu-id="56634-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="56634-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
