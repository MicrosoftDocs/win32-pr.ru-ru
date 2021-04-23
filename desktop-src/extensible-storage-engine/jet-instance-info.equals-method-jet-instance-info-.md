---
description: 'Дополнительные сведения о: JET_INSTANCE_INFO. Метод Equals (JET_INSTANCE_INFO)'
title: JET_INSTANCE_INFO. Метод Equals (JET_INSTANCE_INFO)
TOCTitle: Equals method (JET_INSTANCE_INFO)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals(Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.equals(v=EXCHG.10)
ms:contentKeyID: 55103697
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b601e018b51e6e95162478ff6c5fe12e77f7b469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998661"
---
# <a name="jet_instance_infoequals-method-jet_instance_info"></a><span data-ttu-id="d13b2-103">JET_INSTANCE_INFO. Метод Equals (JET_INSTANCE_INFO)</span><span class="sxs-lookup"><span data-stu-id="d13b2-103">JET_INSTANCE_INFO.Equals method (JET_INSTANCE_INFO)</span></span>

<span data-ttu-id="d13b2-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="d13b2-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="d13b2-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d13b2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d13b2-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="d13b2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d13b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d13b2-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_INSTANCE_INFO _
) As Boolean
'Usage
Dim instance As JET_INSTANCE_INFO
Dim other As JET_INSTANCE_INFO
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_INSTANCE_INFO other
)
```

#### <a name="parameters"></a><span data-ttu-id="d13b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d13b2-108">Parameters</span></span>

  - <span data-ttu-id="d13b2-109">др.</span><span class="sxs-lookup"><span data-stu-id="d13b2-109">other</span></span>  
    <span data-ttu-id="d13b2-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span><span class="sxs-lookup"><span data-stu-id="d13b2-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO](./jet-instance-info-class.md)</span></span>  
    
    <span data-ttu-id="d13b2-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="d13b2-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="d13b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d13b2-112">Return value</span></span>

<span data-ttu-id="d13b2-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="d13b2-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="d13b2-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="d13b2-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="d13b2-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="d13b2-115">Implements</span></span>

[<span data-ttu-id="d13b2-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="d13b2-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="d13b2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d13b2-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d13b2-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="d13b2-118">Reference</span></span>

[<span data-ttu-id="d13b2-119">Класс JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="d13b2-119">JET_INSTANCE_INFO class</span></span>](./jet-instance-info-class.md)

[<span data-ttu-id="d13b2-120">Элементы JET_INSTANCE_INFO</span><span class="sxs-lookup"><span data-stu-id="d13b2-120">JET_INSTANCE_INFO members</span></span>](./jet-instance-info-members.md)

[<span data-ttu-id="d13b2-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="d13b2-121">Equals overload</span></span>](./jet-instance-info.equals-method.md)

[<span data-ttu-id="d13b2-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="d13b2-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
