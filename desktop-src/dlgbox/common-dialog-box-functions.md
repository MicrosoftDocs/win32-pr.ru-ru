---
title: Общие функции диалоговых окон
description: . | Общие функции диалоговых окон
ms.assetid: 4a94330b-e0d5-48d7-80f3-86ba6ca1f0f9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f0ca24f319bb27955ba117a8035df3042fb44
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674663"
---
# <a name="common-dialog-box-functions"></a><span data-ttu-id="4d0c3-104">Общие функции диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="4d0c3-104">Common Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4d0c3-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="4d0c3-105">In this section</span></span>

-   [<span data-ttu-id="4d0c3-106">*кчукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-106">*CCHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)
-   [<span data-ttu-id="4d0c3-107">*кфхукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-107">*CFHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
-   <span data-ttu-id="4d0c3-108">[**чусеколор**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d0c3-108">[**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span></span>
-   [<span data-ttu-id="4d0c3-109">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-109">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="4d0c3-110">**коммдлжекстендедеррор**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-110">**CommDlgExtendedError**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror)
-   [<span data-ttu-id="4d0c3-111">**Строки FindText**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-111">**FindText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)
-   [<span data-ttu-id="4d0c3-112">*фрхукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-112">*FRHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)
-   [<span data-ttu-id="4d0c3-113">**жетфилетитле**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-113">**GetFileTitle**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)
-   [<span data-ttu-id="4d0c3-114">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-114">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
-   [<span data-ttu-id="4d0c3-115">**жетсавефиленаме**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-115">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
-   [<span data-ttu-id="4d0c3-116">*офнхукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-116">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
-   <span data-ttu-id="4d0c3-117">[*офнхукпроколдстиле*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d0c3-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span></span>
-   [<span data-ttu-id="4d0c3-118">**пажепаинсук**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-118">**PagePaintHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
-   <span data-ttu-id="4d0c3-119">[**пажесетупдлг**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d0c3-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
-   [<span data-ttu-id="4d0c3-120">**пажесетуфук**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-120">**PageSetupHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)
-   <span data-ttu-id="4d0c3-121">[**принтдлг**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d0c3-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span></span>
-   <span data-ttu-id="4d0c3-122">[**принтдлжекс**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4d0c3-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span></span>
-   [<span data-ttu-id="4d0c3-123">*принсукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-123">*PrintHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)
-   [<span data-ttu-id="4d0c3-124">**реплацетекст**</span><span class="sxs-lookup"><span data-stu-id="4d0c3-124">**ReplaceText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)
-   [<span data-ttu-id="4d0c3-125">*сетуфукпрок*</span><span class="sxs-lookup"><span data-stu-id="4d0c3-125">*SetupHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)

 

 
