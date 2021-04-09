---
title: Функции диалоговых окон
description: .
ms.assetid: 7ea6445a-1772-4986-b4b7-27512afa680d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 789e450e0a6e42157f0036f5d1e805856fcc8b95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070591"
---
# <a name="dialog-box-functions"></a><span data-ttu-id="24936-103">Функции диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="24936-103">Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="24936-104">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="24936-104">In this section</span></span>

-   [<span data-ttu-id="24936-105">**креатедиалог**</span><span class="sxs-lookup"><span data-stu-id="24936-105">**CreateDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialoga)
-   [<span data-ttu-id="24936-106">**креатедиалогиндирект**</span><span class="sxs-lookup"><span data-stu-id="24936-106">**CreateDialogIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
-   [<span data-ttu-id="24936-107">**креатедиалогиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="24936-107">**CreateDialogIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
-   [<span data-ttu-id="24936-108">**креатедиалогпарам**</span><span class="sxs-lookup"><span data-stu-id="24936-108">**CreateDialogParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)
-   [<span data-ttu-id="24936-109">**дефдлгпрок**</span><span class="sxs-lookup"><span data-stu-id="24936-109">**DefDlgProc**</span></span>](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw)
-   [<span data-ttu-id="24936-110">**диалогбокс**</span><span class="sxs-lookup"><span data-stu-id="24936-110">**DialogBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxa)
-   [<span data-ttu-id="24936-111">**диалогбоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="24936-111">**DialogBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
-   [<span data-ttu-id="24936-112">**диалогбоксиндиректпарам**</span><span class="sxs-lookup"><span data-stu-id="24936-112">**DialogBoxIndirectParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
-   [<span data-ttu-id="24936-113">**диалогбокспарам**</span><span class="sxs-lookup"><span data-stu-id="24936-113">**DialogBoxParam**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama)
-   [<span data-ttu-id="24936-114">*DialogProc*</span><span class="sxs-lookup"><span data-stu-id="24936-114">*DialogProc*</span></span>](/windows/win32/api/winuser/nc-winuser-dlgproc)
-   [<span data-ttu-id="24936-115">**EndDialog**</span><span class="sxs-lookup"><span data-stu-id="24936-115">**EndDialog**</span></span>](/windows/desktop/api/Winuser/nf-winuser-enddialog)
-   [<span data-ttu-id="24936-116">**жетдиалогбасеунитс**</span><span class="sxs-lookup"><span data-stu-id="24936-116">**GetDialogBaseUnits**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdialogbaseunits)
-   [<span data-ttu-id="24936-117">**жетдлгктрлид**</span><span class="sxs-lookup"><span data-stu-id="24936-117">**GetDlgCtrlID**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgctrlid)
-   [<span data-ttu-id="24936-118">**жетдлгитем**</span><span class="sxs-lookup"><span data-stu-id="24936-118">**GetDlgItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitem)
-   [<span data-ttu-id="24936-119">**жетдлгитеминт**</span><span class="sxs-lookup"><span data-stu-id="24936-119">**GetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint)
-   [<span data-ttu-id="24936-120">**жетдлгитемтекст**</span><span class="sxs-lookup"><span data-stu-id="24936-120">**GetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta)
-   [<span data-ttu-id="24936-121">**жетнекстдлгграупитем**</span><span class="sxs-lookup"><span data-stu-id="24936-121">**GetNextDlgGroupItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem)
-   [<span data-ttu-id="24936-122">**жетнекстдлгтабитем**</span><span class="sxs-lookup"><span data-stu-id="24936-122">**GetNextDlgTabItem**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem)
-   [<span data-ttu-id="24936-123">**исдиалогмессаже**</span><span class="sxs-lookup"><span data-stu-id="24936-123">**IsDialogMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea)
-   [<span data-ttu-id="24936-124">**мапдиалогрект**</span><span class="sxs-lookup"><span data-stu-id="24936-124">**MapDialogRect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
-   [<span data-ttu-id="24936-125">**MessageBox**</span><span class="sxs-lookup"><span data-stu-id="24936-125">**MessageBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messagebox)
-   [<span data-ttu-id="24936-126">**мессажебоксекс**</span><span class="sxs-lookup"><span data-stu-id="24936-126">**MessageBoxEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxexa)
-   [<span data-ttu-id="24936-127">**мессажебоксиндирект**</span><span class="sxs-lookup"><span data-stu-id="24936-127">**MessageBoxIndirect**</span></span>](/windows/desktop/api/Winuser/nf-winuser-messageboxindirecta)
-   [<span data-ttu-id="24936-128">**сенддлгитеммессаже**</span><span class="sxs-lookup"><span data-stu-id="24936-128">**SendDlgItemMessage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea)
-   [<span data-ttu-id="24936-129">**сетдлгитеминт**</span><span class="sxs-lookup"><span data-stu-id="24936-129">**SetDlgItemInt**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint)
-   [<span data-ttu-id="24936-130">**сетдлгитемтекст**</span><span class="sxs-lookup"><span data-stu-id="24936-130">**SetDlgItemText**</span></span>](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta)

 

 