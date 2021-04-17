---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Версионсторетасккуеуемакс'
title: Инстанцепараметерс. Версионсторетасккуеуемакс, свойство
TOCTitle: 'VersionStoreTaskQueueMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.versionstoretaskqueuemax(v=EXCHG.10)
ms:contentKeyID: 55103554
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.VersionStoreTaskQueueMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_VersionStoreTaskQueueMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd522fa46df40182b6dfe638e7663df8e9e56c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498153"
---
# <a name="instanceparametersversionstoretaskqueuemax-property"></a><span data-ttu-id="cde51-103">Инстанцепараметерс. Версионсторетасккуеуемакс, свойство</span><span class="sxs-lookup"><span data-stu-id="cde51-103">InstanceParameters.VersionStoreTaskQueueMax property</span></span>

<span data-ttu-id="cde51-104">Возвращает или задает количество рабочих элементов фоновой очистки, которые могут быть поставлены в очередь пула потоков компонента Database Engine в любой момент времени.</span><span class="sxs-lookup"><span data-stu-id="cde51-104">Gets or sets the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<span data-ttu-id="cde51-105">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cde51-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cde51-106">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="cde51-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cde51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cde51-107">Syntax</span></span>

``` vb
'Declaration
Public Property VersionStoreTaskQueueMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.VersionStoreTaskQueueMax

instance.VersionStoreTaskQueueMax = value
```

``` csharp
public int VersionStoreTaskQueueMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="cde51-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cde51-108">Property value</span></span>

<span data-ttu-id="cde51-109">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="cde51-109">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cde51-110">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cde51-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cde51-111">Справочник</span><span class="sxs-lookup"><span data-stu-id="cde51-111">Reference</span></span>

[<span data-ttu-id="cde51-112">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="cde51-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="cde51-113">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="cde51-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="cde51-114">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="cde51-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
