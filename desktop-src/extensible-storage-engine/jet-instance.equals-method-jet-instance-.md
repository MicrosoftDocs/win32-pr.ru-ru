---
description: 'Дополнительные сведения о: JET_INSTANCE. Метод Equals (JET_INSTANCE)'
title: JET_INSTANCE. Метод Equals (JET_INSTANCE)
TOCTitle: Equals method (JET_INSTANCE)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39512490
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be4f2a172da5fc0d7670e7e87464eac04df3cfa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265733"
---
# <a name="jet_instanceequals-method-jet_instance"></a><span data-ttu-id="0c385-103">JET_INSTANCE. Метод Equals (JET_INSTANCE)</span><span class="sxs-lookup"><span data-stu-id="0c385-103">JET_INSTANCE.Equals method (JET_INSTANCE)</span></span>

<span data-ttu-id="0c385-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="0c385-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="0c385-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0c385-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0c385-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="0c385-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0c385-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c385-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim other As JET_INSTANCE
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE other
)
```

#### <a name="parameters"></a><span data-ttu-id="0c385-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c385-108">Parameters</span></span>

  - <span data-ttu-id="0c385-109">др.</span><span class="sxs-lookup"><span data-stu-id="0c385-109">other</span></span>  
    <span data-ttu-id="0c385-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="0c385-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="0c385-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="0c385-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="0c385-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c385-112">Return value</span></span>

<span data-ttu-id="0c385-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="0c385-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="0c385-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="0c385-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="0c385-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="0c385-115">Implements</span></span>

[<span data-ttu-id="0c385-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="0c385-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="0c385-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c385-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0c385-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="0c385-118">Reference</span></span>

[<span data-ttu-id="0c385-119">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0c385-119">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="0c385-120">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="0c385-120">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="0c385-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="0c385-121">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="0c385-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="0c385-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
