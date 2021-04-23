---
description: 'Дополнительные сведения о свойстве: SystemParameters. Стартфлушсрешолд'
title: SystemParameters. Стартфлушсрешолд, свойство
TOCTitle: 'StartFlushThreshold property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.startflushthreshold(v=EXCHG.10)
ms:contentKeyID: 55104050
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.get_StartFlushThreshold
- Microsoft.Isam.Esent.Interop.SystemParameters.set_StartFlushThreshold
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a0e520682253d7a586c36366d229be59e014c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347972"
---
# <a name="systemparametersstartflushthreshold-property"></a><span data-ttu-id="a959d-103">SystemParameters. Стартфлушсрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="a959d-103">SystemParameters.StartFlushThreshold property</span></span>

<span data-ttu-id="a959d-104">Возвращает или задает пороговое значение, при котором кэш страниц базы данных начинает удалять страницы из кэша, чтобы освободить место для страниц, которые не кэшируются.</span><span class="sxs-lookup"><span data-stu-id="a959d-104">Gets or sets the threshold at which the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="a959d-105">Когда количество буферов страниц в кэше падает ниже этого порога, запускается фоновый процесс для пополнения пула доступных буферов.</span><span class="sxs-lookup"><span data-stu-id="a959d-105">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="a959d-106">Это пороговое значение всегда относительно максимального размера кэша, установленного JET_paramCacheSizeMax.</span><span class="sxs-lookup"><span data-stu-id="a959d-106">This threshold is always relative to the maximum cache size as set by JET_paramCacheSizeMax.</span></span> <span data-ttu-id="a959d-107">Это пороговое значение также должно быть меньше порога окончания, установленного JET_paramStopFlushThreshold.</span><span class="sxs-lookup"><span data-stu-id="a959d-107">This threshold must also always be less than the stop threshold as set by JET_paramStopFlushThreshold.</span></span> <span data-ttu-id="a959d-108">Высота расстояния начального порога определяет время отклика, которое должен иметь кэш страниц базы данных для создания доступных буферов до того, как приложение потребует их.</span><span class="sxs-lookup"><span data-stu-id="a959d-108">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="a959d-109">При высоком пороговом значении запуска фоновому процессу будет больше времени на реагирование.</span><span class="sxs-lookup"><span data-stu-id="a959d-109">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="a959d-110">Тем не менее, при высоком пороговом значении приостанавливается более высокий порог, что уменьшает эффективный размер кэша страниц базы данных.</span><span class="sxs-lookup"><span data-stu-id="a959d-110">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache.</span></span>

<span data-ttu-id="a959d-111">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a959d-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a959d-112">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="a959d-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a959d-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a959d-113">Syntax</span></span>

``` vb
'Declaration
Public Shared Property StartFlushThreshold As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.StartFlushThreshold

SystemParameters.StartFlushThreshold = value
```

``` csharp
public static int StartFlushThreshold { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a959d-114">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a959d-114">Property value</span></span>

<span data-ttu-id="a959d-115">Тип: [System. Int32](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a959d-115">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a959d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a959d-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a959d-117">Справочник</span><span class="sxs-lookup"><span data-stu-id="a959d-117">Reference</span></span>

[<span data-ttu-id="a959d-118">SystemParameters - класс</span><span class="sxs-lookup"><span data-stu-id="a959d-118">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="a959d-119">Элементы SystemParameters</span><span class="sxs-lookup"><span data-stu-id="a959d-119">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="a959d-120">Пространство имен Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="a959d-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
