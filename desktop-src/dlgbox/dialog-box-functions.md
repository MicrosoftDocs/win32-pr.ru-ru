---
title: Функции диалоговых окон
description: Функции диалоговых окон
ms.assetid: 7ea6445a-1772-4986-b4b7-27512afa680d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44e63184a75a9bc3bddedc4f8c037719689fced
ms.sourcegitcommit: 57e91b10658c36e28dd8ebe3e77d5b9bec4fbcc2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/15/2021
ms.locfileid: "107509843"
---
# <a name="dialog-box-functions"></a><span data-ttu-id="c0831-103">Функции диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="c0831-103">Dialog box functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c0831-104">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="c0831-104">In this section</span></span>

* [<span data-ttu-id="c0831-105">**креатедиалог**</span><span class="sxs-lookup"><span data-stu-id="c0831-105">**CreateDialog**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialoga)
* [<span data-ttu-id="c0831-106">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="c0831-106">**CreateDialogIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogindirecta)
* [<span data-ttu-id="c0831-107">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="c0831-107">**CreateDialogIndirectParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogindirectparama)
* [<span data-ttu-id="c0831-108">**креатедиалогпарам**</span><span class="sxs-lookup"><span data-stu-id="c0831-108">**CreateDialogParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-createdialogparama)
* [<span data-ttu-id="c0831-109">**дефдлгпрок**</span><span class="sxs-lookup"><span data-stu-id="c0831-109">**DefDlgProc**</span></span>](/windows/win32/api/Winuser/nf-winuser-defdlgprocw)
* [<span data-ttu-id="c0831-110">**диалогбокс**</span><span class="sxs-lookup"><span data-stu-id="c0831-110">**DialogBox**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxa)
* [<span data-ttu-id="c0831-111">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="c0831-111">**DialogBoxIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxindirecta)
* [<span data-ttu-id="c0831-112">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="c0831-112">**DialogBoxIndirectParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxindirectparama)
* [<span data-ttu-id="c0831-113">**диалогбокспарам**</span><span class="sxs-lookup"><span data-stu-id="c0831-113">**DialogBoxParam**</span></span>](/windows/win32/api/Winuser/nf-winuser-dialogboxparama)
* [<span data-ttu-id="c0831-114">**длгпрок**</span><span class="sxs-lookup"><span data-stu-id="c0831-114">**DLGPROC**</span></span>](/windows/win32/api/winuser/nc-winuser-dlgproc)
* [<span data-ttu-id="c0831-115">**EndDialog**</span><span class="sxs-lookup"><span data-stu-id="c0831-115">**EndDialog**</span></span>](/windows/win32/api/Winuser/nf-winuser-enddialog)
* [<span data-ttu-id="c0831-116">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="c0831-116">**GetDialogBaseUnits**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdialogbaseunits)
* [<span data-ttu-id="c0831-117">**жетдлгктрлид**</span><span class="sxs-lookup"><span data-stu-id="c0831-117">**GetDlgCtrlID**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgctrlid)
* [<span data-ttu-id="c0831-118">**жетдлгитем**</span><span class="sxs-lookup"><span data-stu-id="c0831-118">**GetDlgItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitem)
* [<span data-ttu-id="c0831-119">**жетдлгитеминт**</span><span class="sxs-lookup"><span data-stu-id="c0831-119">**GetDlgItemInt**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitemint)
* [<span data-ttu-id="c0831-120">**жетдлгитемтекст**</span><span class="sxs-lookup"><span data-stu-id="c0831-120">**GetDlgItemText**</span></span>](/windows/win32/api/Winuser/nf-winuser-getdlgitemtexta)
* [<span data-ttu-id="c0831-121">**жетнекстдлгграупитем**</span><span class="sxs-lookup"><span data-stu-id="c0831-121">**GetNextDlgGroupItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getnextdlggroupitem)
* [<span data-ttu-id="c0831-122">**жетнекстдлгтабитем**</span><span class="sxs-lookup"><span data-stu-id="c0831-122">**GetNextDlgTabItem**</span></span>](/windows/win32/api/Winuser/nf-winuser-getnextdlgtabitem)
* [<span data-ttu-id="c0831-123">**исдиалогмессаже**</span><span class="sxs-lookup"><span data-stu-id="c0831-123">**IsDialogMessage**</span></span>](/windows/win32/api/Winuser/nf-winuser-isdialogmessagea)
* [<span data-ttu-id="c0831-124">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="c0831-124">**MapDialogRect**</span></span>](/windows/win32/api/Winuser/nf-winuser-mapdialogrect)
* [<span data-ttu-id="c0831-125">**MessageBox**</span><span class="sxs-lookup"><span data-stu-id="c0831-125">**MessageBox**</span></span>](/windows/win32/api/Winuser/nf-winuser-messagebox)
* [<span data-ttu-id="c0831-126">**мессажебоксекс**</span><span class="sxs-lookup"><span data-stu-id="c0831-126">**MessageBoxEx**</span></span>](/windows/win32/api/Winuser/nf-winuser-messageboxexa)
* [<span data-ttu-id="c0831-127">**мессажебоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="c0831-127">**MessageBoxIndirect**</span></span>](/windows/win32/api/Winuser/nf-winuser-messageboxindirecta)
* [<span data-ttu-id="c0831-128">**мсгбокскаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c0831-128">**MSGBOXCALLBACK**</span></span>](/windows/win32/api/winuser/nc-winuser-msgboxcallback)
* [<span data-ttu-id="c0831-129">**сенддлгитеммессаже**</span><span class="sxs-lookup"><span data-stu-id="c0831-129">**SendDlgItemMessage**</span></span>](/windows/win32/api/Winuser/nf-winuser-senddlgitemmessagea)
* [<span data-ttu-id="c0831-130">**сетдлгитеминт**</span><span class="sxs-lookup"><span data-stu-id="c0831-130">**SetDlgItemInt**</span></span>](/windows/win32/api/Winuser/nf-winuser-setdlgitemint)
* [<span data-ttu-id="c0831-131">**сетдлгитемтекст**</span><span class="sxs-lookup"><span data-stu-id="c0831-131">**SetDlgItemText**</span></span>](/windows/win32/api/Winuser/nf-winuser-setdlgitemtexta)
