---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Макссессионс'
title: Инстанцепараметерс. Макссессионс, свойство
TOCTitle: 'MaxSessions property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxsessions(v=EXCHG.10)
ms:contentKeyID: 55103557
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxSessions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2294a8de2e3603a638607efad5baaa6af6c1ec17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712593"
---
# <a name="instanceparametersmaxsessions-property"></a><span data-ttu-id="4623c-103">Инстанцепараметерс. Макссессионс, свойство</span><span class="sxs-lookup"><span data-stu-id="4623c-103">InstanceParameters.MaxSessions property</span></span>

<span data-ttu-id="4623c-104">Возвращает или задает количество ресурсов сеансов, зарезервированных для данного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="4623c-104">Gets or sets the number of sessions resources reserved for this instance.</span></span> <span data-ttu-id="4623c-105">Ресурс сеанса непосредственно соответствует JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="4623c-105">A session resource directly corresponds to a JET_SESID.</span></span>

<span data-ttu-id="4623c-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4623c-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4623c-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="4623c-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4623c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4623c-108">Syntax</span></span>

``` vb
'Declaration
Public Property MaxSessions As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxSessions

instance.MaxSessions = value
```

``` csharp
public int MaxSessions { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="4623c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4623c-109">Property value</span></span>

<span data-ttu-id="4623c-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="4623c-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="4623c-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4623c-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4623c-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="4623c-112">Reference</span></span>

[<span data-ttu-id="4623c-113">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="4623c-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="4623c-114">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="4623c-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="4623c-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="4623c-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
