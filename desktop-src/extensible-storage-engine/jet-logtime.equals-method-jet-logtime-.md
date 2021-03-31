---
description: 'Дополнительные сведения о: JET_LOGTIME. Метод Equals (JET_LOGTIME)'
title: JET_LOGTIME. Метод Equals (JET_LOGTIME)
TOCTitle: Equals method (JET_LOGTIME)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equals(Microsoft.Isam.Esent.Interop.JET_LOGTIME)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.equals(v=EXCHG.10)
ms:contentKeyID: 39512684
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f0f678d5528eaf57c63af5cdd28d0c101870ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818656"
---
# <a name="jet_logtimeequals-method-jet_logtime"></a><span data-ttu-id="427c1-103">JET_LOGTIME. Метод Equals (JET_LOGTIME)</span><span class="sxs-lookup"><span data-stu-id="427c1-103">JET_LOGTIME.Equals method (JET_LOGTIME)</span></span>

<span data-ttu-id="427c1-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="427c1-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="427c1-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="427c1-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="427c1-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="427c1-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="427c1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="427c1-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_LOGTIME _
) As Boolean
'Usage
Dim instance As JET_LOGTIME
Dim other As JET_LOGTIME
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_LOGTIME other
)
```

#### <a name="parameters"></a><span data-ttu-id="427c1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="427c1-108">Parameters</span></span>

  - <span data-ttu-id="427c1-109">др.</span><span class="sxs-lookup"><span data-stu-id="427c1-109">other</span></span>  
    <span data-ttu-id="427c1-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span><span class="sxs-lookup"><span data-stu-id="427c1-110">Type: [Microsoft.Isam.Esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)</span></span>  
    
    <span data-ttu-id="427c1-111">Экземпляр, сравниваемый с этим экземпляром.</span><span class="sxs-lookup"><span data-stu-id="427c1-111">An instance to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="427c1-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="427c1-112">Return value</span></span>

<span data-ttu-id="427c1-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="427c1-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="427c1-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="427c1-114">True if the two instances are equal.</span></span>  

#### <a name="implements"></a><span data-ttu-id="427c1-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="427c1-115">Implements</span></span>

[<span data-ttu-id="427c1-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="427c1-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="427c1-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="427c1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="427c1-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="427c1-118">Reference</span></span>

[<span data-ttu-id="427c1-119">Структура JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="427c1-119">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="427c1-120">Элементы JET_LOGTIME</span><span class="sxs-lookup"><span data-stu-id="427c1-120">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="427c1-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="427c1-121">Equals overload</span></span>](./jet-logtime.equals-method.md)

[<span data-ttu-id="427c1-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="427c1-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
