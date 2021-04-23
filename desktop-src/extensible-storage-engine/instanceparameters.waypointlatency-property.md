---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Вайпоинтлатенци'
title: Инстанцепараметерс. Вайпоинтлатенци, свойство
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d7d837d7fff804926529ec67780e319d85031f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703286"
---
# <a name="instanceparameterswaypointlatency-property"></a><span data-ttu-id="fdc39-103">Инстанцепараметерс. Вайпоинтлатенци, свойство</span><span class="sxs-lookup"><span data-stu-id="fdc39-103">InstanceParameters.WaypointLatency property</span></span>

<span data-ttu-id="fdc39-104">Возвращает или задает число журналов, в которых ESENT будет откладывать сбросы базы данных для.</span><span class="sxs-lookup"><span data-stu-id="fdc39-104">Gets or sets a the number of logs that esent will defer database flushes for.</span></span> <span data-ttu-id="fdc39-105">Это можно использовать для повышения возможности восстановления базы данных, если ошибки приводят к потере файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="fdc39-105">This can be used to increase database recoverability if failures cause logfiles to be lost.</span></span> <span data-ttu-id="fdc39-106">Поддерживается в Windows 7 и выше.</span><span class="sxs-lookup"><span data-stu-id="fdc39-106">Supported on Windows 7 and up.</span></span> <span data-ttu-id="fdc39-107">Игнорируется в Windows XP, Windows Server 2003, Windows Vista и Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="fdc39-107">Ignored on Windows XP, Windows Server 2003, Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="fdc39-108">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fdc39-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fdc39-109">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="fdc39-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fdc39-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fdc39-110">Syntax</span></span>

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fdc39-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fdc39-111">Property value</span></span>

<span data-ttu-id="fdc39-112">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fdc39-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fdc39-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdc39-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fdc39-114">Справочник</span><span class="sxs-lookup"><span data-stu-id="fdc39-114">Reference</span></span>

[<span data-ttu-id="fdc39-115">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="fdc39-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="fdc39-116">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="fdc39-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="fdc39-117">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="fdc39-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
