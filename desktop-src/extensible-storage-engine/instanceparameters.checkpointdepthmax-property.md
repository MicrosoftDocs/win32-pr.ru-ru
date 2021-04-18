---
description: 'Дополнительные сведения о свойстве: Инстанцепараметерс. Чеккпоинтдепсмакс'
title: Инстанцепараметерс. Чеккпоинтдепсмакс, свойство
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711448"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a><span data-ttu-id="539de-103">Инстанцепараметерс. Чеккпоинтдепсмакс, свойство</span><span class="sxs-lookup"><span data-stu-id="539de-103">InstanceParameters.CheckpointDepthMax property</span></span>

<span data-ttu-id="539de-104">Возвращает или задает пороговое значение в байтах для того, сколько файлов журнала транзакций потребуется воспроизвести после сбоя.</span><span class="sxs-lookup"><span data-stu-id="539de-104">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="539de-105">Если циклическое ведение журнала включено с помощью Циркуларлог, этот параметр также управляет приблизительным объемом файлов журнала транзакций, которые будут храниться на диске.</span><span class="sxs-lookup"><span data-stu-id="539de-105">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="539de-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="539de-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="539de-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="539de-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="539de-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="539de-108">Syntax</span></span>

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="539de-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="539de-109">Property value</span></span>

<span data-ttu-id="539de-110">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="539de-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="539de-111">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="539de-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="539de-112">Справочник</span><span class="sxs-lookup"><span data-stu-id="539de-112">Reference</span></span>

[<span data-ttu-id="539de-113">Класс Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="539de-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="539de-114">Элементы Инстанцепараметерс</span><span class="sxs-lookup"><span data-stu-id="539de-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="539de-115">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="539de-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
