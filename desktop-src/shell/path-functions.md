---
description: Функции пути
ms.assetid: 0105FC65-332B-4F99-9629-F3DFEAD97535
title: Функции пути (оболочка Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12265e9b1dd51f8e2ea5bc0cc384bf227b8cd041
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985641"
---
# <a name="path-functions-the-windows-shell"></a><span data-ttu-id="632af-103">Функции пути (оболочка Windows)</span><span class="sxs-lookup"><span data-stu-id="632af-103">Path Functions (The Windows Shell)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="632af-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="632af-104">In this section</span></span>

-   [<span data-ttu-id="632af-105">**пасаллокканоникализе**</span><span class="sxs-lookup"><span data-stu-id="632af-105">**PathAllocCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccanonicalize)
-   [<span data-ttu-id="632af-106">**пасаллоккомбине**</span><span class="sxs-lookup"><span data-stu-id="632af-106">**PathAllocCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathalloccombine)
-   [<span data-ttu-id="632af-107">**паскчаддбаккслаш**</span><span class="sxs-lookup"><span data-stu-id="632af-107">**PathCchAddBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslash)
-   [<span data-ttu-id="632af-108">**паскчаддбаккслашекс**</span><span class="sxs-lookup"><span data-stu-id="632af-108">**PathCchAddBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddbackslashex)
-   [<span data-ttu-id="632af-109">**паскчаддекстенсион**</span><span class="sxs-lookup"><span data-stu-id="632af-109">**PathCchAddExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchaddextension)
-   [<span data-ttu-id="632af-110">**паскчаппенд**</span><span class="sxs-lookup"><span data-stu-id="632af-110">**PathCchAppend**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappend)
-   [<span data-ttu-id="632af-111">**паскчаппендекс**</span><span class="sxs-lookup"><span data-stu-id="632af-111">**PathCchAppendEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchappendex)
-   [<span data-ttu-id="632af-112">**паскчканоникализе**</span><span class="sxs-lookup"><span data-stu-id="632af-112">**PathCchCanonicalize**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalize)
-   [<span data-ttu-id="632af-113">**паскчканоникализикс**</span><span class="sxs-lookup"><span data-stu-id="632af-113">**PathCchCanonicalizeEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcanonicalizeex)
-   [<span data-ttu-id="632af-114">**паскчкомбине**</span><span class="sxs-lookup"><span data-stu-id="632af-114">**PathCchCombine**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombine)
-   [<span data-ttu-id="632af-115">**паскчкомбиникс**</span><span class="sxs-lookup"><span data-stu-id="632af-115">**PathCchCombineEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchcombineex)
-   [<span data-ttu-id="632af-116">**паскчфиндекстенсион**</span><span class="sxs-lookup"><span data-stu-id="632af-116">**PathCchFindExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchfindextension)
-   [<span data-ttu-id="632af-117">**паскчисрут**</span><span class="sxs-lookup"><span data-stu-id="632af-117">**PathCchIsRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchisroot)
-   [<span data-ttu-id="632af-118">**паскчремовебаккслаш**</span><span class="sxs-lookup"><span data-stu-id="632af-118">**PathCchRemoveBackslash**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslash)
-   [<span data-ttu-id="632af-119">**паскчремовебаккслашекс**</span><span class="sxs-lookup"><span data-stu-id="632af-119">**PathCchRemoveBackslashEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovebackslashex)
-   [<span data-ttu-id="632af-120">**паскчремовикстенсион**</span><span class="sxs-lookup"><span data-stu-id="632af-120">**PathCchRemoveExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremoveextension)
-   [<span data-ttu-id="632af-121">**паскчремовефилеспек**</span><span class="sxs-lookup"><span data-stu-id="632af-121">**PathCchRemoveFileSpec**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchremovefilespec)
-   [<span data-ttu-id="632af-122">**паскчренамикстенсион**</span><span class="sxs-lookup"><span data-stu-id="632af-122">**PathCchRenameExtension**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchrenameextension)
-   [<span data-ttu-id="632af-123">**паскчскипрут**</span><span class="sxs-lookup"><span data-stu-id="632af-123">**PathCchSkipRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchskiproot)
-   [<span data-ttu-id="632af-124">**паскчстриппрефикс**</span><span class="sxs-lookup"><span data-stu-id="632af-124">**PathCchStripPrefix**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstripprefix)
-   [<span data-ttu-id="632af-125">**паскчстрипторут**</span><span class="sxs-lookup"><span data-stu-id="632af-125">**PathCchStripToRoot**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathcchstriptoroot)
-   [<span data-ttu-id="632af-126">**пасисунцекс**</span><span class="sxs-lookup"><span data-stu-id="632af-126">**PathIsUNCEx**</span></span>](/windows/desktop/api/pathcch/nf-pathcch-pathisuncex)

 

 



