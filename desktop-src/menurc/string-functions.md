---
title: Строковые функции
description: .
ms.assetid: 0249ea7a-84f1-4e25-9e80-0be5eb6c04ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b2f6c3f75e98de2f951f56aa2891eab72401a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411196"
---
# <a name="string-functions"></a><span data-ttu-id="f7afb-103">Строковые функции</span><span class="sxs-lookup"><span data-stu-id="f7afb-103">String Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f7afb-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="f7afb-104">In This Section</span></span>

-   [<span data-ttu-id="f7afb-105">**чарловер**</span><span class="sxs-lookup"><span data-stu-id="f7afb-105">**CharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowera)
-   [<span data-ttu-id="f7afb-106">**чарловербуфф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-106">**CharLowerBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa)
-   [<span data-ttu-id="f7afb-107">**чарнекст**</span><span class="sxs-lookup"><span data-stu-id="f7afb-107">**CharNext**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnexta)
-   [<span data-ttu-id="f7afb-108">**чарнекстекса**</span><span class="sxs-lookup"><span data-stu-id="f7afb-108">**CharNextExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charnextexa)
-   [<span data-ttu-id="f7afb-109">**чарпрев**</span><span class="sxs-lookup"><span data-stu-id="f7afb-109">**CharPrev**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charpreva)
-   [<span data-ttu-id="f7afb-110">**чарпревекса**</span><span class="sxs-lookup"><span data-stu-id="f7afb-110">**CharPrevExA**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charprevexa)
-   [<span data-ttu-id="f7afb-111">**чартуем**</span><span class="sxs-lookup"><span data-stu-id="f7afb-111">**CharToOem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooema)
-   [<span data-ttu-id="f7afb-112">**чартуембуфф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-112">**CharToOemBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-chartooembuffa)
-   [<span data-ttu-id="f7afb-113">**чаруппер**</span><span class="sxs-lookup"><span data-stu-id="f7afb-113">**CharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charuppera)
-   [<span data-ttu-id="f7afb-114">**чаруппербуфф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-114">**CharUpperBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa)
-   [<span data-ttu-id="f7afb-115">**исчаралфа**</span><span class="sxs-lookup"><span data-stu-id="f7afb-115">**IsCharAlpha**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)
-   [<span data-ttu-id="f7afb-116">**исчаралфанумерик**</span><span class="sxs-lookup"><span data-stu-id="f7afb-116">**IsCharAlphaNumeric**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica)
-   [<span data-ttu-id="f7afb-117">**исчарловер**</span><span class="sxs-lookup"><span data-stu-id="f7afb-117">**IsCharLower**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)
-   [<span data-ttu-id="f7afb-118">**исчаруппер**</span><span class="sxs-lookup"><span data-stu-id="f7afb-118">**IsCharUpper**</span></span>](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)
-   [<span data-ttu-id="f7afb-119">**лоадстринг**</span><span class="sxs-lookup"><span data-stu-id="f7afb-119">**LoadString**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadstringa)
-   [<span data-ttu-id="f7afb-120">**лстркат**</span><span class="sxs-lookup"><span data-stu-id="f7afb-120">**lstrcat**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcata)
-   [<span data-ttu-id="f7afb-121">**лстркмп**</span><span class="sxs-lookup"><span data-stu-id="f7afb-121">**lstrcmp**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa)
-   [<span data-ttu-id="f7afb-122">**лстркмпи**</span><span class="sxs-lookup"><span data-stu-id="f7afb-122">**lstrcmpi**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcmpia)
-   [<span data-ttu-id="f7afb-123">**лстркпи**</span><span class="sxs-lookup"><span data-stu-id="f7afb-123">**lstrcpy**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpya)
-   [<span data-ttu-id="f7afb-124">**лстркпин**</span><span class="sxs-lookup"><span data-stu-id="f7afb-124">**lstrcpyn**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrcpyna)
-   [<span data-ttu-id="f7afb-125">**lstrlen**</span><span class="sxs-lookup"><span data-stu-id="f7afb-125">**lstrlen**</span></span>](/windows/desktop/api/Winbase/nf-winbase-lstrlena)
-   [<span data-ttu-id="f7afb-126">**оемточар**</span><span class="sxs-lookup"><span data-stu-id="f7afb-126">**OemToChar**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtochara)
-   [<span data-ttu-id="f7afb-127">**оемточарбуфф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-127">**OemToCharBuff**</span></span>](/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa)
-   [<span data-ttu-id="f7afb-128">**вспринтф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-128">**wsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)
-   [<span data-ttu-id="f7afb-129">**ввспринтф**</span><span class="sxs-lookup"><span data-stu-id="f7afb-129">**wvsprintf**</span></span>](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa)

 

 




