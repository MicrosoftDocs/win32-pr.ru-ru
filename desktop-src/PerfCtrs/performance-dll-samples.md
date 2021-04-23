---
description: Windows SDK (WSDK) содержит три полных примера библиотек DLL производительности.
ms.assetid: 862be53a-3d58-42b9-adf0-2f913dc6fb06
title: Примеры библиотек DLL производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e2210899651a065218474eb49175553a05aa8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663169"
---
# <a name="performance-dll-samples"></a><span data-ttu-id="c41b4-103">Примеры библиотек DLL производительности</span><span class="sxs-lookup"><span data-stu-id="c41b4-103">Performance DLL Samples</span></span>

<span data-ttu-id="c41b4-104">Windows SDK (WSDK) содержит три полных примера библиотек DLL производительности.</span><span class="sxs-lookup"><span data-stu-id="c41b4-104">The Windows SDK (WSDK) contains three complete sample performance DLLs.</span></span> <span data-ttu-id="c41b4-105">Эти примеры находятся в каталоге Samples \\ винбасе \\ WinNT \\ перфтул \\ перфдллс.</span><span class="sxs-lookup"><span data-stu-id="c41b4-105">These samples are located in the Samples\\WinBase\\WinNT\\PerfTool\\PerfDlls directory.</span></span> <span data-ttu-id="c41b4-106">Корень этого пути является базовым каталогом установки WSDK.</span><span class="sxs-lookup"><span data-stu-id="c41b4-106">The root of this path is the base installation directory of the WSDK.</span></span> <span data-ttu-id="c41b4-107">Вы можете скачать WSDK из пакета средств [разработки программного обеспечения (SDK) для Microsoft Windows](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (выполните поиск по Windows SDK и выберите загрузку последней выпущенной операционной системы).</span><span class="sxs-lookup"><span data-stu-id="c41b4-107">You can download the WSDK from the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) (search for Windows SDK and select the download for the latest released operating system).</span></span>

<span data-ttu-id="c41b4-108">Ниже приведены примеры, содержащиеся в этом каталоге.</span><span class="sxs-lookup"><span data-stu-id="c41b4-108">The samples contained in this directory are:</span></span>

-   <span data-ttu-id="c41b4-109">**Аппмем**— предоставляет аналоги функций [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-globalrealloc)и [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) , которые сообщают сведения о производительности.</span><span class="sxs-lookup"><span data-stu-id="c41b4-109">**AppMem**—Provides counterparts of the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc), [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc), and [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) functions that report performance information.</span></span> <span data-ttu-id="c41b4-110">Счетчики производительности в реестре и средстве производительности могут считывать сведения о производительности.</span><span class="sxs-lookup"><span data-stu-id="c41b4-110">Performance counters in the registry and the Performance tool can read the performance information.</span></span>
-   <span data-ttu-id="c41b4-111">**Леакибин**— демонстрируется использование счетчиков производительности приложений.</span><span class="sxs-lookup"><span data-stu-id="c41b4-111">**LeakyBin**—Demonstrates the use of application performance counters.</span></span>
-   <span data-ttu-id="c41b4-112">**Перфжен**— предоставляет три волны в пять различных периодов для использования с средством производительности для предоставления данных с известным показателем и значением.</span><span class="sxs-lookup"><span data-stu-id="c41b4-112">**PerfGen**—Provides three waveforms at five different periods for use with the Performance tool to provide data at a known rate and value.</span></span> <span data-ttu-id="c41b4-113">Это может быть полезно при тестировании приложений, использующих данные о производительности и требующих для тестирования прогнозируемых значений.</span><span class="sxs-lookup"><span data-stu-id="c41b4-113">This can be useful in testing applications that use performance data and need predictable values to test against.</span></span>

 

 
