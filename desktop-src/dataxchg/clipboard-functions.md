---
title: Функции буфера обмена
description: . | Функции буфера обмена
ms.assetid: 54addf54-921d-4246-b21e-ae993f8bcb02
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a6a0304c55e4c97f2243599909decd997758e9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273543"
---
# <a name="clipboard-functions"></a><span data-ttu-id="90ce3-104">Функции буфера обмена</span><span class="sxs-lookup"><span data-stu-id="90ce3-104">Clipboard Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="90ce3-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="90ce3-105">In this section</span></span>

-   [<span data-ttu-id="90ce3-106">**аддклипбоардформатлистенер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-106">**AddClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-addclipboardformatlistener)
-   [<span data-ttu-id="90ce3-107">**чанжеклипбоардчаин**</span><span class="sxs-lookup"><span data-stu-id="90ce3-107">**ChangeClipboardChain**</span></span>](/windows/desktop/api/Winuser/nf-winuser-changeclipboardchain)
-   [<span data-ttu-id="90ce3-108">**клосеклипбоард**</span><span class="sxs-lookup"><span data-stu-id="90ce3-108">**CloseClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-closeclipboard)
-   [<span data-ttu-id="90ce3-109">**каунтклипбоардформатс**</span><span class="sxs-lookup"><span data-stu-id="90ce3-109">**CountClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-countclipboardformats)
-   [<span data-ttu-id="90ce3-110">**емптиклипбоард**</span><span class="sxs-lookup"><span data-stu-id="90ce3-110">**EmptyClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
-   [<span data-ttu-id="90ce3-111">**енумклипбоардформатс**</span><span class="sxs-lookup"><span data-stu-id="90ce3-111">**EnumClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enumclipboardformats)
-   [<span data-ttu-id="90ce3-112">**жетклипбоарддата**</span><span class="sxs-lookup"><span data-stu-id="90ce3-112">**GetClipboardData**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboarddata)
-   [<span data-ttu-id="90ce3-113">**жетклипбоардформатнаме**</span><span class="sxs-lookup"><span data-stu-id="90ce3-113">**GetClipboardFormatName**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardformatnamea)
-   [<span data-ttu-id="90ce3-114">**жетклипбоардовнер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-114">**GetClipboardOwner**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardowner)
-   [<span data-ttu-id="90ce3-115">**жетклипбоардсекуенценумбер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-115">**GetClipboardSequenceNumber**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardsequencenumber)
-   [<span data-ttu-id="90ce3-116">**жетклипбоардвиевер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-116">**GetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getclipboardviewer)
-   [<span data-ttu-id="90ce3-117">**жетопенклипбоардвиндов**</span><span class="sxs-lookup"><span data-stu-id="90ce3-117">**GetOpenClipboardWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getopenclipboardwindow)
-   [<span data-ttu-id="90ce3-118">**жетприоритиклипбоардформат**</span><span class="sxs-lookup"><span data-stu-id="90ce3-118">**GetPriorityClipboardFormat**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getpriorityclipboardformat)
-   [<span data-ttu-id="90ce3-119">**жетупдатедклипбоардформатс**</span><span class="sxs-lookup"><span data-stu-id="90ce3-119">**GetUpdatedClipboardFormats**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getupdatedclipboardformats)
-   [<span data-ttu-id="90ce3-120">**исклипбоардформатаваилабле**</span><span class="sxs-lookup"><span data-stu-id="90ce3-120">**IsClipboardFormatAvailable**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isclipboardformatavailable)
-   [<span data-ttu-id="90ce3-121">**опенклипбоард**</span><span class="sxs-lookup"><span data-stu-id="90ce3-121">**OpenClipboard**</span></span>](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
-   [<span data-ttu-id="90ce3-122">**регистерклипбоардформат**</span><span class="sxs-lookup"><span data-stu-id="90ce3-122">**RegisterClipboardFormat**</span></span>](/windows/desktop/api/Winuser/nf-winuser-registerclipboardformata)
-   [<span data-ttu-id="90ce3-123">**ремовеклипбоардформатлистенер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-123">**RemoveClipboardFormatListener**</span></span>](/windows/desktop/api/Winuser/nf-winuser-removeclipboardformatlistener)
-   [<span data-ttu-id="90ce3-124">**сетклипбоарддата**</span><span class="sxs-lookup"><span data-stu-id="90ce3-124">**SetClipboardData**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboarddata)
-   [<span data-ttu-id="90ce3-125">**сетклипбоардвиевер**</span><span class="sxs-lookup"><span data-stu-id="90ce3-125">**SetClipboardViewer**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)

 

 




