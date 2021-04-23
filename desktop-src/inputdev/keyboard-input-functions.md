---
title: Функции ввода с клавиатуры
description: .
ms.assetid: 731b8209-1ca8-4667-bd39-7bd0cef45380
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d034ef3f9c20591200247c312fb3c45521d086
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337428"
---
# <a name="keyboard-input-functions"></a><span data-ttu-id="2f5d4-103">Функции ввода с клавиатуры</span><span class="sxs-lookup"><span data-stu-id="2f5d4-103">Keyboard Input Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2f5d4-104">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="2f5d4-104">In This Section</span></span>

-   [<span data-ttu-id="2f5d4-105">**активатекэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-105">**ActivateKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-activatekeyboardlayout)
-   [<span data-ttu-id="2f5d4-106">**блоккинпут**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-106">**BlockInput**</span></span>](/windows/win32/api/winuser/nf-winuser-blockinput)
-   [<span data-ttu-id="2f5d4-107">**енаблевиндов**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-107">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
-   [<span data-ttu-id="2f5d4-108">**жетактивевиндов**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-108">**GetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-getactivewindow)
-   [<span data-ttu-id="2f5d4-109">**жетасинккэйстате**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-109">**GetAsyncKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getasynckeystate)
-   [<span data-ttu-id="2f5d4-110">**Фокус ввода**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-110">**GetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-getfocus)
-   [<span data-ttu-id="2f5d4-111">**жеткбкодепаже**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-111">**GetKBCodePage**</span></span>](/windows/win32/api/winuser/nf-winuser-getkbcodepage)
-   [<span data-ttu-id="2f5d4-112">**жеткэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-112">**GetKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)
-   [<span data-ttu-id="2f5d4-113">**жеткэйбоардлайаутлист**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-113">**GetKeyboardLayoutList**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutlist)
-   [<span data-ttu-id="2f5d4-114">**жеткэйбоардлайаутнаме**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-114">**GetKeyboardLayoutName**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardlayoutnamea)
-   [<span data-ttu-id="2f5d4-115">**жеткэйбоардстате**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-115">**GetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardstate)
-   [<span data-ttu-id="2f5d4-116">**жеткэйбоардтипе**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-116">**GetKeyboardType**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeyboardtype)
-   [<span data-ttu-id="2f5d4-117">**жеткэйнаметекст**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-117">**GetKeyNameText**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeynametexta)
-   [<span data-ttu-id="2f5d4-118">**жеткэйстате**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-118">**GetKeyState**</span></span>](/windows/win32/api/winuser/nf-winuser-getkeystate)
-   [<span data-ttu-id="2f5d4-119">**жетластинпутинфо**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-119">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
-   [<span data-ttu-id="2f5d4-120">**исвиндовенаблед**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-120">**IsWindowEnabled**</span></span>](/windows/win32/api/winuser/nf-winuser-iswindowenabled)
-   [<span data-ttu-id="2f5d4-121">**\_событие кэйбд**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-121">**keybd\_event**</span></span>](/windows/win32/api/winuser/nf-winuser-keybd_event)
-   [<span data-ttu-id="2f5d4-122">**лоадкэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-122">**LoadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta)
-   [<span data-ttu-id="2f5d4-123">**мапвиртуалкэй**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-123">**MapVirtualKey**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeya)
-   [<span data-ttu-id="2f5d4-124">**мапвиртуалкэйекс**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-124">**MapVirtualKeyEx**</span></span>](/windows/win32/api/winuser/nf-winuser-mapvirtualkeyexa)
-   [<span data-ttu-id="2f5d4-125">**оемкэйскан**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-125">**OemKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-oemkeyscan)
-   [<span data-ttu-id="2f5d4-126">**RegisterHotKey**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-126">**RegisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-registerhotkey)
-   [<span data-ttu-id="2f5d4-127">**SendInput**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-127">**SendInput**</span></span>](/windows/win32/api/winuser/nf-winuser-sendinput)
-   [<span data-ttu-id="2f5d4-128">**сетактивевиндов**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-128">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
-   [<span data-ttu-id="2f5d4-129">**SetFocus**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-129">**SetFocus**</span></span>](/windows/win32/api/winuser/nf-winuser-setfocus)
-   [<span data-ttu-id="2f5d4-130">**сеткэйбоардстате**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-130">**SetKeyboardState**</span></span>](/windows/win32/api/winuser/nf-winuser-setkeyboardstate)
-   [<span data-ttu-id="2f5d4-131">**ToAscii**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-131">**ToAscii**</span></span>](/windows/win32/api/winuser/nf-winuser-toascii)
-   [<span data-ttu-id="2f5d4-132">**тоасЦииекс**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-132">**ToAsciiEx**</span></span>](/windows/win32/api/winuser/nf-winuser-toasciiex)
-   [<span data-ttu-id="2f5d4-133">**тауникоде**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-133">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)
-   [<span data-ttu-id="2f5d4-134">**тауникодикс**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-134">**ToUnicodeEx**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicodeex)
-   [<span data-ttu-id="2f5d4-135">**унлоадкэйбоардлайаут**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-135">**UnloadKeyboardLayout**</span></span>](/windows/win32/api/winuser/nf-winuser-unloadkeyboardlayout)
-   [<span data-ttu-id="2f5d4-136">**унрегистерхоткэй**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-136">**UnregisterHotKey**</span></span>](/windows/win32/api/winuser/nf-winuser-unregisterhotkey)
-   [<span data-ttu-id="2f5d4-137">**вккэйскан**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-137">**VkKeyScan**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscana)
-   [<span data-ttu-id="2f5d4-138">**вккэйсканекс**</span><span class="sxs-lookup"><span data-stu-id="2f5d4-138">**VkKeyScanEx**</span></span>](/windows/win32/api/winuser/nf-winuser-vkkeyscanexa)

 

 