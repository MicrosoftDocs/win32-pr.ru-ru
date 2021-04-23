---
title: Имена Version-Independent WFP и нацелены на конкретные версии Windows
description: Во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661499"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a><span data-ttu-id="7a8fd-103">Имена Version-Independent WFP и нацелены на конкретные версии Windows</span><span class="sxs-lookup"><span data-stu-id="7a8fd-103">WFP Version-Independent Names and Targeting Specific Versions of Windows</span></span>

<span data-ttu-id="7a8fd-104">Во многих случаях API платформы фильтрации Windows (WFP) предоставляет более одной версии функции или структуры.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-104">In many cases, the Windows Filtering Platform (WFP) API provides more than one version of a function or structure.</span></span>

<span data-ttu-id="7a8fd-105">Большинство имен данных и функций в API WFP заканчиваются номером версии, например "0" или "1", даже если имеется только одна версия.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-105">Most data and function names in the WFP API end with a version number, such as "0" or "1", even if there is only one version.</span></span>

## <a name="version-mapping-in-fwpvih"></a><span data-ttu-id="7a8fd-106">Сопоставление версий в фвпви. h</span><span class="sxs-lookup"><span data-stu-id="7a8fd-106">Version Mapping in fwpvi.h</span></span>

<span data-ttu-id="7a8fd-107">Файл заголовка фвпви. h включается начиная с пакета SDK для Windows 7 и WDK.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-107">The fwpvi.h header file is included starting with the Windows 7 SDK and WDK.</span></span> <span data-ttu-id="7a8fd-108">Этот заголовочный файл сопоставляет имя API без версий с версией, которая подходит для использования с данной операционной системой.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-108">This header file maps the versionless API name to the version that is appropriate for use with a given operating system.</span></span>

<span data-ttu-id="7a8fd-109">Например, ниже приведен краткий фрагмент из версии фвпви. h, включенной в пакет SDK для Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-109">For example, here is a brief excerpt from the version of fwpvi.h included in the Windows 8 SDK.</span></span>


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



<span data-ttu-id="7a8fd-110">Как показано выше, существует только одна версия **фвпмнетевенткреатинумхандле** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) — поэтому любой вызов **фвпмнетевенткреатинумхандле** всегда будет вызывать **FwpmNetEventCreateEnumHandle0**, независимо от целевой операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-110">As shown above, there is only one version of **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) – so any call to **FwpmNetEventCreateEnumHandle** will always call **FwpmNetEventCreateEnumHandle0**, regardless of the operating system targeted.</span></span>

<span data-ttu-id="7a8fd-111">Однако существуют три версии **фвпмнетевентенум**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)и [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span><span class="sxs-lookup"><span data-stu-id="7a8fd-111">However, there are three versions of of **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1), and [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2).</span></span> <span data-ttu-id="7a8fd-112">Файл заголовка фвпви. h гарантирует, что вызов **фвпмнетевентенум** будет вызывать версию, наиболее подходящую для целевой операционной системы:</span><span class="sxs-lookup"><span data-stu-id="7a8fd-112">The fwpvi.h header file ensures that a call to **FwpmNetEventEnum** will call the version most appropriate to the targeted operating system:</span></span>

-   <span data-ttu-id="7a8fd-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) для Windows 8 (или более поздней версии)</span><span class="sxs-lookup"><span data-stu-id="7a8fd-113">[**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) for Windows 8 (or later)</span></span>
-   <span data-ttu-id="7a8fd-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) для Windows 7 нацелена</span><span class="sxs-lookup"><span data-stu-id="7a8fd-114">[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) for Windows 7 is targeted</span></span>
-   <span data-ttu-id="7a8fd-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) для более ранних операционных систем (например, Windows Vista или Windows Vista с пакетом обновления 1 (SP1))</span><span class="sxs-lookup"><span data-stu-id="7a8fd-115">[**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) for earlier operating systems (such as Windows Vista or Windows Vista with Service Pack 1 (SP1))</span></span>

## <a name="calling-version-independent-functions-and-structures"></a><span data-ttu-id="7a8fd-116">Вызов функций и структур Version-Independent</span><span class="sxs-lookup"><span data-stu-id="7a8fd-116">Calling Version-Independent Functions and Structures</span></span>

<span data-ttu-id="7a8fd-117">Разработчикам WFP, предназначенным для конкретной операционной системы или версии WDK, рекомендуется всегда программироваться с помощью макросов, не зависящих от версии.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-117">WFP developers targeting a particular operating system or WDK version are encouraged to always program against the version-independent macros.</span></span> <span data-ttu-id="7a8fd-118">При этом будет автоматически выбрана последняя версия, поддерживаемая в целевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-118">This will automatically select the latest version supported in the operating system you are targeting.</span></span> <span data-ttu-id="7a8fd-119">Рекомендуется использовать самые последние файлы заголовков, даже при использовании более ранней операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-119">Use of the most recent header files is recommended, even when targeting an earlier operating system.</span></span> <span data-ttu-id="7a8fd-120">Это позволит обеспечить использование последней поддерживаемой версии, а также упростить обслуживание и обновление кода.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-120">Doing this consistently will ensure the latest supported version is used, and can also make it easier to maintain and update your code.</span></span>

<span data-ttu-id="7a8fd-121">В [справочной документации по API WFP](fwp-reference.md) описывается каждая версия нумерованного API.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-121">The [WFP API reference documentation](fwp-reference.md) describes each version of a numbered API.</span></span> <span data-ttu-id="7a8fd-122">Если существует более одной версии, задается Целевая операционная система.</span><span class="sxs-lookup"><span data-stu-id="7a8fd-122">If more than one version exists, the targeted operating system is noted.</span></span> <span data-ttu-id="7a8fd-123">Однако разработчики, как правило, хотят вызывать ненезависимые от версии интерфейсы API (не имеющие номера) и указывать целевую операционную систему (например, **нтдди \_ WIN6** для Windows Vista или **нтдди \_ WIN8** для Windows 8).</span><span class="sxs-lookup"><span data-stu-id="7a8fd-123">However, developers will generally want to call the version-independent (numberless) APIs, and indicate the targeted operating system (such as **NTDDI\_WIN6** for Windows Vista or **NTDDI\_WIN8** for Windows 8).</span></span>

<span data-ttu-id="7a8fd-124">Чтобы обеспечить правильную обработку функций, которые принимают разные параметры в разных версиях, можно включить условные блоки, такие как `#if (NTDDI_VERSION >= NTDDI_WIN7)` .</span><span class="sxs-lookup"><span data-stu-id="7a8fd-124">To ensure proper handling of functions that take different parameters in different versions, you can include conditional blocks such as `#if (NTDDI_VERSION >= NTDDI_WIN7)`.</span></span>

 

 




