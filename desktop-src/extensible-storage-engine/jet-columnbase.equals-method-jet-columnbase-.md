---
description: 'Дополнительные сведения о: JET_COLUMNBASE. Метод Equals (JET_COLUMNBASE)'
title: JET_COLUMNBASE. Метод Equals (JET_COLUMNBASE)
TOCTitle: Equals method (JET_COLUMNBASE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNBASE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnbase.equals(v=EXCHG.10)
ms:contentKeyID: 55103355
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNBASE.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ada65f03966ebd5f0bf7142d3953117734c2f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913580"
---
# <a name="jet_columnbaseequals-method-jet_columnbase"></a><span data-ttu-id="27775-103">JET_COLUMNBASE. Метод Equals (JET_COLUMNBASE)</span><span class="sxs-lookup"><span data-stu-id="27775-103">JET_COLUMNBASE.Equals method (JET_COLUMNBASE)</span></span>

<span data-ttu-id="27775-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="27775-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="27775-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="27775-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="27775-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="27775-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="27775-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27775-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNBASE _
) As Boolean
'Usage
Dim instance As JET_COLUMNBASE
Dim other As JET_COLUMNBASE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNBASE other
)
```

#### <a name="parameters"></a><span data-ttu-id="27775-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="27775-108">Parameters</span></span>

  - <span data-ttu-id="27775-109">др.</span><span class="sxs-lookup"><span data-stu-id="27775-109">other</span></span>  
    <span data-ttu-id="27775-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span><span class="sxs-lookup"><span data-stu-id="27775-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNBASE](./jet-columnbase-class.md)</span></span>  
    
    <span data-ttu-id="27775-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="27775-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="27775-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27775-112">Return value</span></span>

<span data-ttu-id="27775-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="27775-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="27775-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="27775-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="27775-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="27775-115">Implements</span></span>

[<span data-ttu-id="27775-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="27775-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="27775-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27775-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="27775-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="27775-118">Reference</span></span>

[<span data-ttu-id="27775-119">Класс JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="27775-119">JET_COLUMNBASE class</span></span>](./jet-columnbase-class.md)

[<span data-ttu-id="27775-120">Элементы JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="27775-120">JET_COLUMNBASE members</span></span>](./jet-columnbase-members.md)

[<span data-ttu-id="27775-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="27775-121">Equals overload</span></span>](./jet-columnbase.equals-method.md)

[<span data-ttu-id="27775-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="27775-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
