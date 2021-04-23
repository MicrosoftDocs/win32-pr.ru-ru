---
description: Приложения, использующие функции API Юникода и кодировки символов, обычно используют один и тот же класс окна. Операционная система прозрачно преобразует сообщения между окнами различных классов.
ms.assetid: 68e9839b-39f8-411a-8ae4-4a627c667cae
title: Автоматическое преобразование сообщений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b02a5c5a4951189333608aa448f09ba9c6866d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809526"
---
# <a name="automatic-message-translation"></a><span data-ttu-id="1e123-104">Автоматическое преобразование сообщений</span><span class="sxs-lookup"><span data-stu-id="1e123-104">Automatic Message Translation</span></span>

<span data-ttu-id="1e123-105">Приложения, использующие функции API Юникода и кодировки символов, обычно используют один и тот же класс окна.</span><span class="sxs-lookup"><span data-stu-id="1e123-105">Applications using the Unicode and character set API functions generally use the same window class.</span></span> <span data-ttu-id="1e123-106">Операционная система прозрачно преобразует сообщения между окнами различных классов.</span><span class="sxs-lookup"><span data-stu-id="1e123-106">The operating system transparently translates messages between windows of different classes.</span></span>

<span data-ttu-id="1e123-107">Функция Window реализована для получения сообщений в формате Юникод или кодовой страницы Windows.</span><span class="sxs-lookup"><span data-stu-id="1e123-107">A window function is implemented to receive messages in Unicode or Windows code page format.</span></span> <span data-ttu-id="1e123-108">Оконная функция может передавать сообщения или вызывать функции любого из этих типов.</span><span class="sxs-lookup"><span data-stu-id="1e123-108">The window function can send messages or call functions of either type.</span></span>

<span data-ttu-id="1e123-109">Следующие сообщения содержат текстовые аргументы и подчиняются автоматическому преобразованию текста.</span><span class="sxs-lookup"><span data-stu-id="1e123-109">The following messages have text arguments and are subject to automatic text translation.</span></span> <span data-ttu-id="1e123-110">Сведения об автоматическом переводе см. в разделе [подклассировать и автоматическое преобразование сообщений](subclassing-and-automatic-message-translation.md).</span><span class="sxs-lookup"><span data-stu-id="1e123-110">For information about automatic translation, see [Subclassing and Automatic Message Translation](subclassing-and-automatic-message-translation.md).</span></span>

<dl>

[<span data-ttu-id="1e123-111">\_ADDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="1e123-111">CB\_ADDSTRING</span></span>](../controls/cb-addstring.md)  
[<span data-ttu-id="1e123-112">\_Каталог CB</span><span class="sxs-lookup"><span data-stu-id="1e123-112">CB\_DIR</span></span>](../controls/cb-dir.md)  
[<span data-ttu-id="1e123-113">\_FINDSTRING CB</span><span class="sxs-lookup"><span data-stu-id="1e123-113">CB\_FINDSTRING</span></span>](../controls/cb-findstring.md)  
[<span data-ttu-id="1e123-114">\_ЖЕТЛБТЕКСТ CB</span><span class="sxs-lookup"><span data-stu-id="1e123-114">CB\_GETLBTEXT</span></span>](../controls/cb-getlbtext.md)  
[<span data-ttu-id="1e123-115">\_ИНСЕРТСТРИНГ CB</span><span class="sxs-lookup"><span data-stu-id="1e123-115">CB\_INSERTSTRING</span></span>](../controls/cb-insertstring.md)  
[<span data-ttu-id="1e123-116">\_СЕЛЕКТСТРИНГ CB</span><span class="sxs-lookup"><span data-stu-id="1e123-116">CB\_SELECTSTRING</span></span>](../controls/cb-selectstring.md)  
[<span data-ttu-id="1e123-117">EM, \_ строка</span><span class="sxs-lookup"><span data-stu-id="1e123-117">EM\_GETLINE</span></span>](../controls/em-getline.md)  
[<span data-ttu-id="1e123-118">EM \_ реплацесел</span><span class="sxs-lookup"><span data-stu-id="1e123-118">EM\_REPLACESEL</span></span>](../controls/em-replacesel.md)  
[<span data-ttu-id="1e123-119">EM \_ сетпассвордчар</span><span class="sxs-lookup"><span data-stu-id="1e123-119">EM\_SETPASSWORDCHAR</span></span>](../controls/em-setpasswordchar.md)  
[<span data-ttu-id="1e123-120">ADDFILE балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-120">LB\_ADDFILE</span></span>](../controls/lb-addfile.md)  
[<span data-ttu-id="1e123-121">ADDSTRING балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-121">LB\_ADDSTRING</span></span>](../controls/lb-addstring.md)  
[<span data-ttu-id="1e123-122">Каталог балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-122">LB\_DIR</span></span>](../controls/lb-dir.md)  
[<span data-ttu-id="1e123-123">FINDSTRING балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-123">LB\_FINDSTRING</span></span>](../controls/lb-findstring.md)  
[<span data-ttu-id="1e123-124">\_Балансировка нагрузки</span><span class="sxs-lookup"><span data-stu-id="1e123-124">LB\_GETTEXT</span></span>](../controls/lb-gettext.md)  
[<span data-ttu-id="1e123-125">инсертстринг балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-125">LB\_INSERTSTRING</span></span>](../controls/lb-insertstring.md)  
[<span data-ttu-id="1e123-126">селектстринг балансировки нагрузки \_</span><span class="sxs-lookup"><span data-stu-id="1e123-126">LB\_SELECTSTRING</span></span>](../controls/lb-selectstring.md)  
[<span data-ttu-id="1e123-127">WM \_ асккбформатнаме</span><span class="sxs-lookup"><span data-stu-id="1e123-127">WM\_ASKCBFORMATNAME</span></span>](../dataxchg/wm-askcbformatname.md)  
[<span data-ttu-id="1e123-128">WM \_ char</span><span class="sxs-lookup"><span data-stu-id="1e123-128">WM\_CHAR</span></span>](../inputdev/wm-char.md)  
[<span data-ttu-id="1e123-129">WM \_ чартоитем</span><span class="sxs-lookup"><span data-stu-id="1e123-129">WM\_CHARTOITEM</span></span>](../controls/wm-chartoitem.md)  
[<span data-ttu-id="1e123-130">\_Создание WM</span><span class="sxs-lookup"><span data-stu-id="1e123-130">WM\_CREATE</span></span>](../winmsg/wm-create.md)  
[<span data-ttu-id="1e123-131">WM \_ деадчар</span><span class="sxs-lookup"><span data-stu-id="1e123-131">WM\_DEADCHAR</span></span>](../inputdev/wm-deadchar.md)  
[<span data-ttu-id="1e123-132">WM \_ девмодечанже</span><span class="sxs-lookup"><span data-stu-id="1e123-132">WM\_DEVMODECHANGE</span></span>](../gdi/wm-devmodechange.md)  
[<span data-ttu-id="1e123-133">WM \_ gettext</span><span class="sxs-lookup"><span data-stu-id="1e123-133">WM\_GETTEXT</span></span>](../winmsg/wm-gettext.md)  
[<span data-ttu-id="1e123-134">WM \_ мдикреате</span><span class="sxs-lookup"><span data-stu-id="1e123-134">WM\_MDICREATE</span></span>](../winmsg/wm-mdicreate.md)  
[<span data-ttu-id="1e123-135">WM \_ менучар</span><span class="sxs-lookup"><span data-stu-id="1e123-135">WM\_MENUCHAR</span></span>](../menurc/wm-menuchar.md)  
[<span data-ttu-id="1e123-136">WM \_ нккреате</span><span class="sxs-lookup"><span data-stu-id="1e123-136">WM\_NCCREATE</span></span>](../winmsg/wm-nccreate.md)  
[<span data-ttu-id="1e123-137">WM \_ SETTEXT</span><span class="sxs-lookup"><span data-stu-id="1e123-137">WM\_SETTEXT</span></span>](../winmsg/wm-settext.md)  
[<span data-ttu-id="1e123-138">WM \_ сисчар</span><span class="sxs-lookup"><span data-stu-id="1e123-138">WM\_SYSCHAR</span></span>](../menurc/wm-syschar.md)  
[<span data-ttu-id="1e123-139">WM \_ сисдеадчар</span><span class="sxs-lookup"><span data-stu-id="1e123-139">WM\_SYSDEADCHAR</span></span>](../inputdev/wm-sysdeadchar.md)  
[<span data-ttu-id="1e123-140">WM \_ вининичанже</span><span class="sxs-lookup"><span data-stu-id="1e123-140">WM\_WININICHANGE</span></span>](../winmsg/wm-wininichange.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="1e123-141">См. также</span><span class="sxs-lookup"><span data-stu-id="1e123-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e123-142">Юникод в Windows API</span><span class="sxs-lookup"><span data-stu-id="1e123-142">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
