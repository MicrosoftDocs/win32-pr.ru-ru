---
description: 'Дополнительные сведения о: JET_INSTANCE. Метод Equals (Object)'
title: JET_INSTANCE. Метод Equals (Object)
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_INSTANCE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance.equals(v=EXCHG.10)
ms:contentKeyID: 39515717
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
ms.openlocfilehash: 2b13393b487abb4de65360f5199ae1123d3f076e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081195"
---
# <a name="jet_instanceequals-method-object"></a><span data-ttu-id="20f2f-103">JET_INSTANCE. Метод Equals (Object)</span><span class="sxs-lookup"><span data-stu-id="20f2f-103">JET_INSTANCE.Equals method (Object)</span></span>

<span data-ttu-id="20f2f-104">Возвращает значение, указывающее, равен ли данный экземпляр другому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="20f2f-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="20f2f-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="20f2f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="20f2f-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="20f2f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="20f2f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20f2f-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_INSTANCE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="20f2f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="20f2f-108">Parameters</span></span>

  - <span data-ttu-id="20f2f-109">obj</span><span class="sxs-lookup"><span data-stu-id="20f2f-109">obj</span></span>  
    <span data-ttu-id="20f2f-110">Тип: [System. Object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="20f2f-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="20f2f-111">Объект для сравнения с данным экземпляром.</span><span class="sxs-lookup"><span data-stu-id="20f2f-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="20f2f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20f2f-112">Return value</span></span>

<span data-ttu-id="20f2f-113">Тип: [System. Boolean](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="20f2f-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="20f2f-114">Значение true, если два экземпляра равны.</span><span class="sxs-lookup"><span data-stu-id="20f2f-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="20f2f-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20f2f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="20f2f-116">Справочник</span><span class="sxs-lookup"><span data-stu-id="20f2f-116">Reference</span></span>

[<span data-ttu-id="20f2f-117">Структура JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="20f2f-117">JET_INSTANCE structure</span></span>](./jet-instance-structure.md)

[<span data-ttu-id="20f2f-118">Элементы JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="20f2f-118">JET_INSTANCE members</span></span>](./jet-instance-members.md)

[<span data-ttu-id="20f2f-119">Перегрузка Equals</span><span class="sxs-lookup"><span data-stu-id="20f2f-119">Equals overload</span></span>](./jet-instance.equals-method.md)

[<span data-ttu-id="20f2f-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="20f2f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
