---
description: Для работы с данными производительности в Visual Basic можно использовать следующие функции.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Функции счетчиков производительности для Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909720"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="75d15-103">Функции счетчиков производительности для Visual Basic</span><span class="sxs-lookup"><span data-stu-id="75d15-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="75d15-104">Функции, описанные в этом разделе, могут быть изменены или недоступны в будущем.</span><span class="sxs-lookup"><span data-stu-id="75d15-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="75d15-105">Вместо этого корпорация Майкрософт рекомендует использовать функции, описанные в разделе [функции счетчиков производительности](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="75d15-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="75d15-106">Для работы с данными производительности в Visual Basic можно использовать следующие функции.</span><span class="sxs-lookup"><span data-stu-id="75d15-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="75d15-107">**пдхклосекуери**</span><span class="sxs-lookup"><span data-stu-id="75d15-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="75d15-108">**пдхколлекткуеридата**</span><span class="sxs-lookup"><span data-stu-id="75d15-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="75d15-109">**пдхремовекаунтер**</span><span class="sxs-lookup"><span data-stu-id="75d15-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="75d15-110">**пдхвбаддкаунтер**</span><span class="sxs-lookup"><span data-stu-id="75d15-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="75d15-111">**пдхвбкреатекаунтерпаслист**</span><span class="sxs-lookup"><span data-stu-id="75d15-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="75d15-112">**пдхвбжеткаунтерпаселементс**</span><span class="sxs-lookup"><span data-stu-id="75d15-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="75d15-113">**пдхвбжеткаунтерпасфромлист**</span><span class="sxs-lookup"><span data-stu-id="75d15-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="75d15-114">**пдхвбжетдаублекаунтервалуе**</span><span class="sxs-lookup"><span data-stu-id="75d15-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="75d15-115">**пдхвбжетлогфилесизе**</span><span class="sxs-lookup"><span data-stu-id="75d15-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="75d15-116">**пдхвбжетонекаунтерпас**</span><span class="sxs-lookup"><span data-stu-id="75d15-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="75d15-117">**пдхвбисгудстатус**</span><span class="sxs-lookup"><span data-stu-id="75d15-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="75d15-118">**пдхвбопенлог**</span><span class="sxs-lookup"><span data-stu-id="75d15-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="75d15-119">**пдхвбопенкуери**</span><span class="sxs-lookup"><span data-stu-id="75d15-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="75d15-120">**пдхвбупдателог**</span><span class="sxs-lookup"><span data-stu-id="75d15-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="75d15-121">`PdhVb***`Функции работают с сеансом на уровне процесса и не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="75d15-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="75d15-122">Эти функции следует использовать только из простых однопотоковых приложений.</span><span class="sxs-lookup"><span data-stu-id="75d15-122">These functions should only be used from simple single-threaded applications.</span></span>
