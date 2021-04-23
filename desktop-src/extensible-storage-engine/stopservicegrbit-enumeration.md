---
description: Дополнительные сведения о перечислении Стопсервицегрбит
title: Перечисление Стопсервицегрбит (Microsoft. ISAM. ESENT. Interop. Windows8)
TOCTitle: StopServiceGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.stopservicegrbit(v=EXCHG.10)
ms:contentKeyID: 55104330
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.BackgroundUserTasks
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.All
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.QuiesceCaches
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit.Resume
- Microsoft.Isam.Esent.Interop.Windows8.StopServiceGrbit
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 54e54576dfb1023ec4e3bc55ddd198a77f0ddf25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692514"
---
# <a name="stopservicegrbit-enumeration"></a><span data-ttu-id="40c62-103">Перечисление Стопсервицегрбит</span><span class="sxs-lookup"><span data-stu-id="40c62-103">StopServiceGrbit enumeration</span></span>

<span data-ttu-id="40c62-104">Параметры для [JetStopServiceInstance2 (JET_INSTANCE, стопсервицегрбит)](./windows8api.jetstopserviceinstance2-method.md).</span><span class="sxs-lookup"><span data-stu-id="40c62-104">Options for [JetStopServiceInstance2(JET_INSTANCE, StopServiceGrbit)](./windows8api.jetstopserviceinstance2-method.md).</span></span>

<span data-ttu-id="40c62-105">Это перечисление имеет атрибут [FlagsAttribute](/dotnet/api/system.flagsattribute), который разрешает побитовое сочетание значений его элементов.</span><span class="sxs-lookup"><span data-stu-id="40c62-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="40c62-106">**Пространство имен:**  [Microsoft. ISAM. ESENT. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40c62-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="40c62-107">**Сборка:**  Microsoft. ISAM. ESENT. Interop (в Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="40c62-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40c62-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40c62-108">Syntax</span></span>

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration StopServiceGrbit
'Usage
Dim instance As StopServiceGrbit
```

``` csharp
[FlagsAttribute]
public enum StopServiceGrbit
```

## <a name="members"></a><span data-ttu-id="40c62-109">Члены</span><span class="sxs-lookup"><span data-stu-id="40c62-109">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="40c62-110">Имя участника</span><span class="sxs-lookup"><span data-stu-id="40c62-110">Member name</span></span></th>
<th><span data-ttu-id="40c62-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40c62-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40c62-112">Все</span><span class="sxs-lookup"><span data-stu-id="40c62-112">All</span></span></td>
<td><span data-ttu-id="40c62-113">Останавливает все службы ESE для указанного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="40c62-113">Stops all ESE services for the specified instance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40c62-114">баккграундусертаскс</span><span class="sxs-lookup"><span data-stu-id="40c62-114">BackgroundUserTasks</span></span></td>
<td><span data-ttu-id="40c62-115">Останавливает Перезапускаемые клиентские задачи фонового обслуживания (дефрагментацию B + Tree).</span><span class="sxs-lookup"><span data-stu-id="40c62-115">Stops restartable client specificed background maintenance tasks (B+ Tree Defrag).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="40c62-116">куиесцекачес</span><span class="sxs-lookup"><span data-stu-id="40c62-116">QuiesceCaches</span></span></td>
<td><span data-ttu-id="40c62-117">Куиесцес все "грязные" кэши на диск.</span><span class="sxs-lookup"><span data-stu-id="40c62-117">Quiesces all dirty caches to disk.</span></span> <span data-ttu-id="40c62-118">Асинхронная.</span><span class="sxs-lookup"><span data-stu-id="40c62-118">Asynchronous.</span></span> <span data-ttu-id="40c62-119">Замораживание отменяется, если впоследствии вызывается бит возобновления.</span><span class="sxs-lookup"><span data-stu-id="40c62-119">Quiescing is cancelled if the Resume bit is called subsequently.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="40c62-120">Возобновить</span><span class="sxs-lookup"><span data-stu-id="40c62-120">Resume</span></span></td>
<td><span data-ttu-id="40c62-121">Возобновляет ранее выданные операции выхода, т. е. &quot; перезапускает службу &quot; .</span><span class="sxs-lookup"><span data-stu-id="40c62-121">Resumes previously issued StopService operations, i.e. &quot;restarts service&quot;.</span></span> <span data-ttu-id="40c62-122">Можно сочетать с грбитс, чтобы возобновить работу конкретных служб, или с параметром 0x0 возобновляет работу всех предыдущих остановленных служб.</span><span class="sxs-lookup"><span data-stu-id="40c62-122">Can be combined with above grbits to Resume specific services, or with 0x0 Resumes all previous stopped services.</span></span>
<p><span data-ttu-id="40c62-123">Предупреждение. Этот бит можно использовать только для возобновления JET_bitStopServiceBackground и JET_bitStopServiceQuiesceCaches, если вы выполняли JET_bitStopServiceAll или JET_bitStopServiceAPI, попытка использовать JET_bitStopServiceResume завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="40c62-123">Warning: This bit can only be used to resume JET_bitStopServiceBackground and JET_bitStopServiceQuiesceCaches, if you did a JET_bitStopServiceAll or JET_bitStopServiceAPI, attempting to use JET_bitStopServiceResume will fail.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="40c62-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40c62-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40c62-125">Справочник</span><span class="sxs-lookup"><span data-stu-id="40c62-125">Reference</span></span>

[<span data-ttu-id="40c62-126">Пространство имен Microsoft. ISAM. ESENT. Interop. Windows8</span><span class="sxs-lookup"><span data-stu-id="40c62-126">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
