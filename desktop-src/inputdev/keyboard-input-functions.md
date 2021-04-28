---
title: Функции ввода с клавиатуры
description: Функции ввода с клавиатуры
ms.assetid: 731b8209-1ca8-4667-bd39-7bd0cef45380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b690a93c2813eca7c7b4487e42bfc8664bd894
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112952"
---
# <a name="keyboard-input-functions"></a><span data-ttu-id="4d024-103">Функции ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="4d024-103">Keyboard Input Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4d024-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="4d024-104">In This Section</span></span>

-   [<span data-ttu-id="4d024-105">**активатекэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="4d024-105">**ActivateKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout)
-   [<span data-ttu-id="4d024-106">**блоккинпут**</span><span class="sxs-lookup"><span data-stu-id="4d024-106">**BlockInput**</span></span>](/windows/win32/api/winuser/nf-winuser-blockinput)
-   [<span data-ttu-id="4d024-107">**енаблевиндов**</span><span class="sxs-lookup"><span data-stu-id="4d024-107">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
-   [<span data-ttu-id="4d024-108">**жетактивевиндов**</span><span class="sxs-lookup"><span data-stu-id="4d024-108">**GetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-getactivewindow)
-   [<span data-ttu-id="4d024-109">**жетасинккэйстате**</span><span class="sxs-lookup"><span data-stu-id="4d024-109">**GetAsyncKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getasynckeystate)
-   [<span data-ttu-id="4d024-110">**Фокус ввода**</span><span class="sxs-lookup"><span data-stu-id="4d024-110">**GetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-getfocus)
-   [<span data-ttu-id="4d024-111">**жеткбкодепаже**</span><span class="sxs-lookup"><span data-stu-id="4d024-111">**GetKBCodePage**</span></span>](/windows/win32/api/winuser/nf-winuser-getkbcodepage)
-   [<span data-ttu-id="4d024-112">**жеткэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="4d024-112">**GetKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)
-   [<span data-ttu-id="4d024-113">**жеткэйбоардлайаутлист**</span><span class="sxs-lookup"><span data-stu-id="4d024-113">**GetKeyboardLayoutList**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist)
-   [<span data-ttu-id="4d024-114">**жеткэйбоардлайаутнаме**</span><span class="sxs-lookup"><span data-stu-id="4d024-114">**GetKeyboardLayoutName**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)
-   [<span data-ttu-id="4d024-115">**жеткэйбоардстате**</span><span class="sxs-lookup"><span data-stu-id="4d024-115">**GetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardstate)
-   [<span data-ttu-id="4d024-116">**жеткэйбоардтипе**</span><span class="sxs-lookup"><span data-stu-id="4d024-116">**GetKeyboardType**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardtype)
-   [<span data-ttu-id="4d024-117">**жеткэйнаметекст**</span><span class="sxs-lookup"><span data-stu-id="4d024-117">**GetKeyNameText**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeynametexta)
-   [<span data-ttu-id="4d024-118">**жеткэйстате**</span><span class="sxs-lookup"><span data-stu-id="4d024-118">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
-   [<span data-ttu-id="4d024-119">**жетластинпутинфо**</span><span class="sxs-lookup"><span data-stu-id="4d024-119">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
-   [<span data-ttu-id="4d024-120">**исвиндовенаблед**</span><span class="sxs-lookup"><span data-stu-id="4d024-120">**IsWindowEnabled**</span></span>](/windows/win32/api/winuser/nf-winuser-iswindowenabled)
-   [<span data-ttu-id="4d024-121">**\_событие кэйбд**</span><span class="sxs-lookup"><span data-stu-id="4d024-121">**keybd\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-keybd_event)
-   [<span data-ttu-id="4d024-122">**лоадкэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="4d024-122">**LoadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)
-   [<span data-ttu-id="4d024-123">**мапвиртуалкэй**</span><span class="sxs-lookup"><span data-stu-id="4d024-123">**MapVirtualKey**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)
-   [<span data-ttu-id="4d024-124">**мапвиртуалкэйекс**</span><span class="sxs-lookup"><span data-stu-id="4d024-124">**MapVirtualKeyEx**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa)
-   [<span data-ttu-id="4d024-125">**оемкэйскан**</span><span class="sxs-lookup"><span data-stu-id="4d024-125">**OemKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-oemkeyscan)
-   [<span data-ttu-id="4d024-126">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="4d024-126">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
-   [<span data-ttu-id="4d024-127">**SendInput**</span><span class="sxs-lookup"><span data-stu-id="4d024-127">**SendInput**</span></span>](/windows/win32/api/winuser/nf-winuser-sendinput)
-   [<span data-ttu-id="4d024-128">**сетактивевиндов**</span><span class="sxs-lookup"><span data-stu-id="4d024-128">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
-   [<span data-ttu-id="4d024-129">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="4d024-129">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
-   [<span data-ttu-id="4d024-130">**сеткэйбоардстате**</span><span class="sxs-lookup"><span data-stu-id="4d024-130">**SetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-setkeyboardstate)
-   [<span data-ttu-id="4d024-131">**ToAscii**</span><span class="sxs-lookup"><span data-stu-id="4d024-131">**ToAscii**</span></span>](/windows/win32/api/winuser/nf-winuser-toascii)
-   [<span data-ttu-id="4d024-132">**тоасЦииекс**</span><span class="sxs-lookup"><span data-stu-id="4d024-132">**ToAsciiEx**</span></span>](/windows/win32/api/winuser/nf-winuser-toasciiex)
-   [<span data-ttu-id="4d024-133">**тауникоде**</span><span class="sxs-lookup"><span data-stu-id="4d024-133">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)
-   [<span data-ttu-id="4d024-134">**тауникодикс**</span><span class="sxs-lookup"><span data-stu-id="4d024-134">**ToUnicodeEx**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicodeex)
-   [<span data-ttu-id="4d024-135">**унлоадкэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="4d024-135">**UnloadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)
-   [<span data-ttu-id="4d024-136">**унрегистерхоткэй**</span><span class="sxs-lookup"><span data-stu-id="4d024-136">**UnregisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-unregisterhotkey)
-   [<span data-ttu-id="4d024-137">**вккэйскан**</span><span class="sxs-lookup"><span data-stu-id="4d024-137">**VkKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscana)
-   [<span data-ttu-id="4d024-138">**вккэйсканекс**</span><span class="sxs-lookup"><span data-stu-id="4d024-138">**VkKeyScanEx**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscanexa)

 

 
