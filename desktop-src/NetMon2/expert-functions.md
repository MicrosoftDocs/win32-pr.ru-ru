---
description: Следующие вспомогательные функции могут вызываться только экспертами, которые экспортируют функцию Run или configure.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Экспертные функции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896794"
---
# <a name="expert-functions"></a><span data-ttu-id="d4f52-103">Экспертные функции</span><span class="sxs-lookup"><span data-stu-id="d4f52-103">Expert Functions</span></span>

<span data-ttu-id="d4f52-104">Следующие вспомогательные функции могут вызываться только экспертами, которые экспортируют функцию [Run](run.md) или [Configure](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="d4f52-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="d4f52-105">Функция</span><span class="sxs-lookup"><span data-stu-id="d4f52-105">Function</span></span>                                         | <span data-ttu-id="d4f52-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d4f52-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4f52-107">експертжетфраме</span><span class="sxs-lookup"><span data-stu-id="d4f52-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="d4f52-108">Извлекает заданный кадр из записи.</span><span class="sxs-lookup"><span data-stu-id="d4f52-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="d4f52-109">експертиндикатестатус</span><span class="sxs-lookup"><span data-stu-id="d4f52-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="d4f52-110">Указывает процент завершения анализа записи экспертом.</span><span class="sxs-lookup"><span data-stu-id="d4f52-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="d4f52-111">експертжетстартупинфо</span><span class="sxs-lookup"><span data-stu-id="d4f52-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="d4f52-112">Извлекает сведения о запуске эксперта.</span><span class="sxs-lookup"><span data-stu-id="d4f52-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="d4f52-113">експертмеморисизе</span><span class="sxs-lookup"><span data-stu-id="d4f52-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="d4f52-114">Возвращает размер памяти, выделенной при вызове функции **експерталлокмемори** .</span><span class="sxs-lookup"><span data-stu-id="d4f52-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="d4f52-115">експертсубмитевент</span><span class="sxs-lookup"><span data-stu-id="d4f52-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="d4f52-116">Указывает на проблему и получает сведения о проблеме, если она существует.</span><span class="sxs-lookup"><span data-stu-id="d4f52-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="d4f52-117">експерталлокмемори</span><span class="sxs-lookup"><span data-stu-id="d4f52-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="d4f52-118">Выделяет память для эксперта.</span><span class="sxs-lookup"><span data-stu-id="d4f52-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="d4f52-119">експертреаллокмемори</span><span class="sxs-lookup"><span data-stu-id="d4f52-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="d4f52-120">Изменяет размер памяти, выделенной функцией **експерталлокмемори** .</span><span class="sxs-lookup"><span data-stu-id="d4f52-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="d4f52-121">експертфримемори</span><span class="sxs-lookup"><span data-stu-id="d4f52-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="d4f52-122">Освобождает память, выделенную экспертом.</span><span class="sxs-lookup"><span data-stu-id="d4f52-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="d4f52-123">Дополнительные сведения о функциях экспорта, вспомогательных функциях, которые могут вызываться экспертами и анализаторами, структурами и перечислениями, см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d4f52-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="d4f52-124">Сведения о</span><span class="sxs-lookup"><span data-stu-id="d4f52-124">For information about</span></span>                                             | <span data-ttu-id="d4f52-125">См.</span><span class="sxs-lookup"><span data-stu-id="d4f52-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="d4f52-126">Функции, экспортированные экспертами</span><span class="sxs-lookup"><span data-stu-id="d4f52-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="d4f52-127">Функции экспорта DLL эксперта</span><span class="sxs-lookup"><span data-stu-id="d4f52-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="d4f52-128">Структуры, используемые экспертными функциями</span><span class="sxs-lookup"><span data-stu-id="d4f52-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="d4f52-129">Экспертные структуры</span><span class="sxs-lookup"><span data-stu-id="d4f52-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="d4f52-130">Перечисления, используемые экспертными структурами и функциями</span><span class="sxs-lookup"><span data-stu-id="d4f52-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="d4f52-131">Перечисления экспертов</span><span class="sxs-lookup"><span data-stu-id="d4f52-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="d4f52-132">Общие вспомогательные функции, которые могут вызываться экспертами и анализаторами</span><span class="sxs-lookup"><span data-stu-id="d4f52-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="d4f52-133">Общие функции эксперта и средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="d4f52-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



