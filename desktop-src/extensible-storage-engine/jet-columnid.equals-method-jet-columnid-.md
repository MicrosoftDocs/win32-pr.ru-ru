---
description: 'Дополнительные сведения о: JET_COLUMNID. Метод Equals (JET_COLUMNID)'
title: JET_COLUMNID. Метод Equals (JET_COLUMNID)
TOCTitle: Equals method (JET_COLUMNID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals(Microsoft.Isam.Esent.Interop.JET_COLUMNID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_columnid.equals(v=EXCHG.10)
ms:contentKeyID: 39516458
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_COLUMNID.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cb0cc59a465f48474e2fe63f5ef78f1fea85f37c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263379"
---
# <a name="jet_columnidequals-method-jet_columnid"></a><span data-ttu-id="08c59-103">JET_COLUMNID. Метод Equals (JET_COLUMNID)</span><span class="sxs-lookup"><span data-stu-id="08c59-103">JET_COLUMNID.Equals method (JET_COLUMNID)</span></span>

<span data-ttu-id="08c59-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="08c59-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="08c59-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="08c59-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="08c59-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="08c59-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="08c59-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08c59-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_COLUMNID _
) As Boolean
'Usage
Dim instance As JET_COLUMNID
Dim other As JET_COLUMNID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_COLUMNID other
)
```

#### <a name="parameters"></a><span data-ttu-id="08c59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="08c59-108">Parameters</span></span>

  - <span data-ttu-id="08c59-109">др.</span><span class="sxs-lookup"><span data-stu-id="08c59-109">other</span></span>  
    <span data-ttu-id="08c59-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="08c59-110">Type: [Microsoft.Isam.Esent.Interop.JET_COLUMNID](./jet-columnid-structure.md)</span></span>  
    
    <span data-ttu-id="08c59-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="08c59-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="08c59-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="08c59-112">Return value</span></span>

<span data-ttu-id="08c59-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="08c59-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="08c59-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="08c59-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="08c59-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="08c59-115">Implements</span></span>

[<span data-ttu-id="08c59-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="08c59-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="08c59-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08c59-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="08c59-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="08c59-118">Reference</span></span>

[<span data-ttu-id="08c59-119">Структура JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="08c59-119">JET_COLUMNID structure</span></span>](./jet-columnid-structure.md)

[<span data-ttu-id="08c59-120">Элементы JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="08c59-120">JET_COLUMNID members</span></span>](./jet-columnid-members.md)

[<span data-ttu-id="08c59-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="08c59-121">Equals overload</span></span>](./jet-columnid.equals-method.md)

[<span data-ttu-id="08c59-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="08c59-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
