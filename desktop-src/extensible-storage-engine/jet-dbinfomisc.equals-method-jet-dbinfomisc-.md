---
description: 'Дополнительные сведения о: JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)'
title: JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)
TOCTitle: Equals method (JET_DBINFOMISC)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(Microsoft.Isam.Esent.Interop.JET_DBINFOMISC)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39514332
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bbe29fe112b82b5c88673d9301b3feb4b0c94536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143645"
---
# <a name="jet_dbinfomiscequals-method-jet_dbinfomisc"></a><span data-ttu-id="f3473-103">JET_DBINFOMISC. Метод Equals (JET_DBINFOMISC)</span><span class="sxs-lookup"><span data-stu-id="f3473-103">JET_DBINFOMISC.Equals method (JET_DBINFOMISC)</span></span>

<span data-ttu-id="f3473-104">Указывает, равен ли текущий объект другому объекту того же типа.</span><span class="sxs-lookup"><span data-stu-id="f3473-104">Indicates whether the current object is equal to another object of the same type.</span></span>

<span data-ttu-id="f3473-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f3473-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f3473-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="f3473-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f3473-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3473-107">Syntax</span></span>

``` vb
'Declaration
Public Function Equals ( _
    other As JET_DBINFOMISC _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim other As JET_DBINFOMISC
Dim returnValue As Boolean

returnValue = instance.Equals(other)
```

``` csharp
public bool Equals(
    JET_DBINFOMISC other
)
```

#### <a name="parameters"></a><span data-ttu-id="f3473-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3473-108">Parameters</span></span>

  - <span data-ttu-id="f3473-109">др.</span><span class="sxs-lookup"><span data-stu-id="f3473-109">other</span></span>  
    <span data-ttu-id="f3473-110">Тип: [Microsoft.ISAM.ESENT.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="f3473-110">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="f3473-111">Объект, который требуется сравнить с данным объектом.</span><span class="sxs-lookup"><span data-stu-id="f3473-111">An object to compare with this object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f3473-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3473-112">Return value</span></span>

<span data-ttu-id="f3473-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="f3473-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="f3473-114">Значение true, если текущий объект равен другому параметру; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="f3473-114">True if the current object is equal to the other parameter; otherwise, false.</span></span>  

#### <a name="implements"></a><span data-ttu-id="f3473-115">Реализации</span><span class="sxs-lookup"><span data-stu-id="f3473-115">Implements</span></span>

[<span data-ttu-id="f3473-116">IEquatable \<T\> . Equals (T)</span><span class="sxs-lookup"><span data-stu-id="f3473-116">IEquatable\<T\>.Equals(T)</span></span>](/dotnet/api/system.iequatable-1.equals#System_IEquatable_1_Equals__0_)  

## <a name="see-also"></a><span data-ttu-id="f3473-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3473-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f3473-118">Справочник</span><span class="sxs-lookup"><span data-stu-id="f3473-118">Reference</span></span>

[<span data-ttu-id="f3473-119">Класс JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f3473-119">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="f3473-120">Элементы JET_DBINFOMISC</span><span class="sxs-lookup"><span data-stu-id="f3473-120">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="f3473-121">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="f3473-121">Equals overload</span></span>](./jet-dbinfomisc.equals-method.md)

[<span data-ttu-id="f3473-122">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="f3473-122">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
