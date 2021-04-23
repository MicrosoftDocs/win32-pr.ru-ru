---
description: 'Дополнительные сведения о: JET_TABLEID. Метод Equals (JET_TABLEID)'
title: JET_TABLEID. Метод Equals (JET_TABLEID)
TOCTitle: Equals method (JET_TABLEID)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals(Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tableid.equals(v=EXCHG.10)
ms:contentKeyID: 39514708
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLEID.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2eab8bae322c7b19b5aada08801f752ad6bfaa93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265724"
---
# <a name="jet_tableidequals-method-jet_tableid"></a><span data-ttu-id="ff777-103">JET_TABLEID. Метод Equals (JET_TABLEID)</span><span class="sxs-lookup"><span data-stu-id="ff777-103">JET_TABLEID.Equals method (JET_TABLEID)</span></span>

<span data-ttu-id="ff777-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="ff777-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="ff777-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ff777-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ff777-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="ff777-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ff777-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff777-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_TABLEID _
) As Boolean
'Usage
Dim instance As JET_TABLEID
Dim other As JET_TABLEID
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_TABLEID other
)
```

#### <a name="parameters"></a><span data-ttu-id="ff777-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff777-108">Parameters</span></span>

  - <span data-ttu-id="ff777-109">др.</span><span class="sxs-lookup"><span data-stu-id="ff777-109">other</span></span>  
    <span data-ttu-id="ff777-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ff777-110">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ff777-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="ff777-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ff777-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff777-112">Return value</span></span>

<span data-ttu-id="ff777-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="ff777-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="ff777-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="ff777-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="ff777-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="ff777-115">Implements</span></span>

[<span data-ttu-id="ff777-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="ff777-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="ff777-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff777-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ff777-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="ff777-118">Reference</span></span>

[<span data-ttu-id="ff777-119">Структура JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff777-119">JET_TABLEID structure</span></span>](./jet-tableid-structure.md)

[<span data-ttu-id="ff777-120">Элементы JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="ff777-120">JET_TABLEID members</span></span>](./jet-tableid-members.md)

[<span data-ttu-id="ff777-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="ff777-121">Equals overload</span></span>](./jet-tableid.equals-method.md)

[<span data-ttu-id="ff777-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="ff777-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
