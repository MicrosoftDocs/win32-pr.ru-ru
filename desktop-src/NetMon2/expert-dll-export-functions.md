---
description: Следующие функции являются точками входа для экспертов-библиотек и вызовов из операционной системы и сетевой монитор.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Функции экспорта DLL эксперта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990917"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="b0a83-103">Функции экспорта DLL эксперта</span><span class="sxs-lookup"><span data-stu-id="b0a83-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="b0a83-104">Следующие функции являются точками входа для экспертов-библиотек и вызовов из операционной системы и сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="b0a83-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="b0a83-105">Функция</span><span class="sxs-lookup"><span data-stu-id="b0a83-105">Function</span></span>                                   | <span data-ttu-id="b0a83-106">Описание</span><span class="sxs-lookup"><span data-stu-id="b0a83-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b0a83-107">**Эксперт по DllMain**</span><span class="sxs-lookup"><span data-stu-id="b0a83-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="b0a83-108">Указывает, что библиотека DLL эксперта загружена или выгружена.</span><span class="sxs-lookup"><span data-stu-id="b0a83-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="b0a83-109">Когда процесс загружает или выгружает библиотеку DLL, операционная система вызывает функцию [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="b0a83-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="b0a83-110">**Регистрация экспертов**</span><span class="sxs-lookup"><span data-stu-id="b0a83-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="b0a83-111">Определяет основные сведения о эксперте в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="b0a83-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="b0a83-112">Сетевой монитор вызывает функцию **Register** .</span><span class="sxs-lookup"><span data-stu-id="b0a83-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="b0a83-113">**Configure**</span><span class="sxs-lookup"><span data-stu-id="b0a83-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="b0a83-114">Настраивает эксперт в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="b0a83-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="b0a83-115">Сетевой монитор вызывает функцию [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a83-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="b0a83-116">**Выполнить**</span><span class="sxs-lookup"><span data-stu-id="b0a83-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="b0a83-117">Запускает эксперт в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="b0a83-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="b0a83-118">Сетевой монитор вызывает функцию [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="b0a83-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="b0a83-119">Сетевой монитор также предоставляет структуры, перечисления и вспомогательные функции, которые могут вызываться экспертом.</span><span class="sxs-lookup"><span data-stu-id="b0a83-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="b0a83-120">Сведения о</span><span class="sxs-lookup"><span data-stu-id="b0a83-120">For information about</span></span>                                      | <span data-ttu-id="b0a83-121">См.</span><span class="sxs-lookup"><span data-stu-id="b0a83-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="b0a83-122">Вспомогательные функции, которые могут вызываться экспертами и анализаторами</span><span class="sxs-lookup"><span data-stu-id="b0a83-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="b0a83-123">Общие функции эксперта и средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="b0a83-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="b0a83-124">Вспомогательные функции, вызываемые только экспертами</span><span class="sxs-lookup"><span data-stu-id="b0a83-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="b0a83-125">Экспертные функции</span><span class="sxs-lookup"><span data-stu-id="b0a83-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="b0a83-126">Структуры, используемые экспертными функциями</span><span class="sxs-lookup"><span data-stu-id="b0a83-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="b0a83-127">Экспертные структуры</span><span class="sxs-lookup"><span data-stu-id="b0a83-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="b0a83-128">Перечисления, используемые экспертными структурами и функциями</span><span class="sxs-lookup"><span data-stu-id="b0a83-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="b0a83-129">Перечисления экспертов</span><span class="sxs-lookup"><span data-stu-id="b0a83-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
