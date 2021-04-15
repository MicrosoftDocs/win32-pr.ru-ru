---
title: ЛИБМАИН. CPP
description: В примере компонента поставщика пример кода стандартной точки входа библиотеки DLL для Adssmp.dll находится в Либмаин. cpp. Поддерживаемые подпрограммы перечислены в следующей таблице.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654120"
---
# <a name="libmaincpp"></a><span data-ttu-id="80f30-104">ЛИБМАИН. CPP</span><span class="sxs-lookup"><span data-stu-id="80f30-104">LIBMAIN.CPP</span></span>

<span data-ttu-id="80f30-105">В примере компонента поставщика пример кода стандартной точки входа библиотеки DLL для Adssmp.dll находится в Либмаин. cpp.</span><span class="sxs-lookup"><span data-stu-id="80f30-105">In the example provider component, a code example of the standard DLL entry point for Adssmp.dll is in Libmain.cpp.</span></span> <span data-ttu-id="80f30-106">Поддерживаемые подпрограммы перечислены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="80f30-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="80f30-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="80f30-107">Item</span></span>                                  | <span data-ttu-id="80f30-108">Описание</span><span class="sxs-lookup"><span data-stu-id="80f30-108">Description</span></span>                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| <span data-ttu-id="80f30-109">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="80f30-109">**DllGetClassObject**</span></span><br/>      | <span data-ttu-id="80f30-110">Стандартная точка входа библиотеки DLL для поиска фабрик классов.</span><span class="sxs-lookup"><span data-stu-id="80f30-110">Standard DLL entry point for locating class factories.</span></span><br/>        |
| <span data-ttu-id="80f30-111">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="80f30-111">**DllCanUnloadNow**</span></span><br/>        | <span data-ttu-id="80f30-112">Стандартная точка входа DLL для определения возможности выгрузки библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="80f30-112">Standard DLL entry point to determine if DLL can be unloaded.</span></span><br/> |
| <span data-ttu-id="80f30-113">**либмаин**</span><span class="sxs-lookup"><span data-stu-id="80f30-113">**LibMain**</span></span><br/>                | <span data-ttu-id="80f30-114">Точка входа инициализации стандартной библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="80f30-114">Standard DLL initialization entry point.</span></span><br/>                      |
| <span data-ttu-id="80f30-115">**искомпатиблеолеверсион**</span><span class="sxs-lookup"><span data-stu-id="80f30-115">**IsCompatibleOleVersion**</span></span><br/> | <span data-ttu-id="80f30-116">Проверьте совместимость со временем выполнения OLE.</span><span class="sxs-lookup"><span data-stu-id="80f30-116">Verify compatibility with the OLE run time.</span></span><br/>                   |
| <span data-ttu-id="80f30-117">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="80f30-117">**DllMain**</span></span><br/>                | <span data-ttu-id="80f30-118">Точка входа для большинства версий Windows 2000 или Windows NT.</span><span class="sxs-lookup"><span data-stu-id="80f30-118">Entry point for most Windows 2000 or Windows NT versions.</span></span><br/>     |



 

 

 





