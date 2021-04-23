---
description: 'Дополнительные сведения о свойстве: SystemParameters. Стопфлушсрешолд'
title: SystemParameters. Стопфлушсрешолд, свойство
TOCTitle: 'StopFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.stopflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104130
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StopFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.StopFlushThreshold
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0b79a9e5894de6539e8ab7dc0db4218b5f6cb3bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347965"
---
# <a name="systemparametersstopflushthreshold-property"></a><span data-ttu-id="41482-103">SystemParameters. Стопфлушсрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="41482-103">SystemParameters.StopFlushThreshold property</span></span>

<span data-ttu-id="41482-104">Возвращает или задает пороговое значение, при котором кэш страниц базы данных завершает исключение страниц из кэша, освобождая пространство для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="41482-104">Gets or sets the threshold at which the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="41482-105">Когда количество буферов страниц в кэше превышает это пороговое значение, фоновый процесс, который был запущен для пополнения пула доступных буферов, останавливается.</span><span class="sxs-lookup"><span data-stu-id="41482-105">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="41482-106">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="41482-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="41482-107">Это пороговое значение также должно быть больше, чем пороговое значение начала, заданное JET_paramStartFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="41482-107">This threshold must also always be greater than the start threshold as set by JET_paramStartFlushThreshold.</span></span> <span data-ttu-id="41482-108">Расстояние между пороговым значением начала и порогом окончания влияет на эффективность, с которой страницы базы данных сбрасываются фоновым процессом.</span><span class="sxs-lookup"><span data-stu-id="41482-108">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="41482-109">Чем больше промежуток, тем больше вероятность, что записи на соседние страницы могут быть объединены.</span><span class="sxs-lookup"><span data-stu-id="41482-109">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="41482-110">Однако при высоком пороговом значении будет уменьшен эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="41482-110">However, a high stop threshold will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="41482-111">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="41482-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="41482-112">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="41482-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="41482-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41482-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StopFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StopFlushThreshold

SystemParameters.StopFlushThreshold = value
```

``` csharp
public static int StopFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="41482-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="41482-114">Property value</span></span>

<span data-ttu-id="41482-115">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="41482-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="41482-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41482-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="41482-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="41482-117">Reference</span></span>

[<span data-ttu-id="41482-118">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="41482-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="41482-119">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="41482-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="41482-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="41482-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
