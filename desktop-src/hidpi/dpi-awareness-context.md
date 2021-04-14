---
title: DPI_AWARENESS_CONTEXTный маркер (виндеф. h)
description: Определяет контекст осведомленности для окна.
ms.assetid: BFD54A9F-642B-4A3A-BBB9-F3A80779251D
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: 1663fad828a2fb29aa0d65ef58ae79616f64edcd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340750"
---
# <a name="dpi_awareness_context-handle"></a><span data-ttu-id="8d88e-103">\_Описатель контекста осведомленности о dpi \_</span><span class="sxs-lookup"><span data-stu-id="8d88e-103">DPI\_AWARENESS\_CONTEXT handle</span></span>

<span data-ttu-id="8d88e-104">Определяет контекст осведомленности для окна.</span><span class="sxs-lookup"><span data-stu-id="8d88e-104">Identifies the awareness context for a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d88e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d88e-105">Syntax</span></span>

``` syntax
#define DPI_AWARENESS_CONTEXT_UNAWARE              ((DPI_AWARENESS_CONTEXT)-1)
#define DPI_AWARENESS_CONTEXT_SYSTEM_AWARE         ((DPI_AWARENESS_CONTEXT)-2)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE    ((DPI_AWARENESS_CONTEXT)-3)
#define DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 ((DPI_AWARENESS_CONTEXT)-4)
#define DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED    ((DPI_AWARENESS_CONTEXT)-5)
```

## <a name="constants"></a><span data-ttu-id="8d88e-106">Константы</span><span class="sxs-lookup"><span data-stu-id="8d88e-106">Constants</span></span>

<span data-ttu-id="8d88e-107">**Независимый \_ контекст осведомленности о dpi \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d88e-107">**DPI\_AWARENESS\_CONTEXT\_UNAWARE**</span></span><dl> <span data-ttu-id="8d88e-108">DPI не расзнается.</span><span class="sxs-lookup"><span data-stu-id="8d88e-108">DPI unaware.</span></span> <span data-ttu-id="8d88e-109">Это окно не масштабируется для изменения DPI и всегда предполагается, что коэффициент масштабирования составляет 100% (96 точек на дюйм).</span><span class="sxs-lookup"><span data-stu-id="8d88e-109">This window does not scale for DPI changes and is always assumed to have a scale factor of 100% (96 DPI).</span></span> <span data-ttu-id="8d88e-110">Она будет автоматически масштабироваться системой при любом другом параметре DPI.</span><span class="sxs-lookup"><span data-stu-id="8d88e-110">It will be automatically scaled by the system on any other DPI setting.</span></span>  
</dl>

<span data-ttu-id="8d88e-111">**\_ \_ система контекста осведомленности \_ \_ об уровне dpi**</span><span class="sxs-lookup"><span data-stu-id="8d88e-111">**DPI\_AWARENESS\_CONTEXT\_SYSTEM\_AWARE**</span></span><dl> <span data-ttu-id="8d88e-112">Учитывать DPI системы.</span><span class="sxs-lookup"><span data-stu-id="8d88e-112">System DPI aware.</span></span> <span data-ttu-id="8d88e-113">Это окно не масштабируется для изменения DPI.</span><span class="sxs-lookup"><span data-stu-id="8d88e-113">This window does not scale for DPI changes.</span></span> <span data-ttu-id="8d88e-114">Он будет запрашивать разрешение DPI один раз и использовать это значение в течение времени существования процесса.</span><span class="sxs-lookup"><span data-stu-id="8d88e-114">It will query for the DPI once and use that value for the lifetime of the process.</span></span> <span data-ttu-id="8d88e-115">Если значение DPI меняется, процесс не будет скорректирован до нового значения DPI.</span><span class="sxs-lookup"><span data-stu-id="8d88e-115">If the DPI changes, the process will not adjust to the new DPI value.</span></span> <span data-ttu-id="8d88e-116">Она будет автоматически масштабироваться по системе, когда значение DPI меняется со значения System.</span><span class="sxs-lookup"><span data-stu-id="8d88e-116">It will be automatically scaled up or down by the system when the DPI changes from the system value.</span></span>  
</dl>

<span data-ttu-id="8d88e-117">**\_ \_ Отслеживание контекста с \_ \_ учетом dpi на монитор \_**</span><span class="sxs-lookup"><span data-stu-id="8d88e-117">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE**</span></span><dl> <span data-ttu-id="8d88e-118">Отслеживание DPI для каждого монитора.</span><span class="sxs-lookup"><span data-stu-id="8d88e-118">Per monitor DPI aware.</span></span> <span data-ttu-id="8d88e-119">Это окно проверяет наличие DPI при его создании и корректирует коэффициент масштабирования при изменении DPI.</span><span class="sxs-lookup"><span data-stu-id="8d88e-119">This window checks for the DPI when it is created and adjusts the scale factor whenever the DPI changes.</span></span> <span data-ttu-id="8d88e-120">Эти процессы не масштабируются автоматически системой.</span><span class="sxs-lookup"><span data-stu-id="8d88e-120">These processes are not automatically scaled by the system.</span></span>  
</dl>

<span data-ttu-id="8d88e-121">**\_ \_ Контекст осведомленности \_ о dpi на \_ монитор \_ \_ версии 2**</span><span class="sxs-lookup"><span data-stu-id="8d88e-121">**DPI\_AWARENESS\_CONTEXT\_PER\_MONITOR\_AWARE\_V2**</span></span><dl> <span data-ttu-id="8d88e-122">Также известен **для каждого монитора версии 2**.</span><span class="sxs-lookup"><span data-stu-id="8d88e-122">Also known as **Per Monitor v2**.</span></span> <span data-ttu-id="8d88e-123">Переносится к исходному режиму поддержки DPI для каждого монитора, который позволяет приложениям получать доступ к новому поведению масштабирования, связанному с DPI, для каждого окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="8d88e-123">An advancement over the original per-monitor DPI awareness mode, which enables applications to access new DPI-related scaling behaviors on a per top-level window basis.</span></span>  
<span data-ttu-id="8d88e-124">На монитор версии 2 был сделан доступным в обновлении для дизайнеров Windows 10 и недоступен в более ранних версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8d88e-124">Per Monitor v2 was made available in the Creators Update of Windows 10, and is not available on earlier versions of the operating system.</span></span>  
<span data-ttu-id="8d88e-125">Ниже представлены дополнительные варианты поведения.</span><span class="sxs-lookup"><span data-stu-id="8d88e-125">The additional behaviors introduced are as follows:</span></span>

-   <span data-ttu-id="8d88e-126">**Уведомления об изменении dpi дочернего окна** . в контексте каждого монитора версии 2 все дерево окна уведомляется о любых произошедших изменениях dpi.</span><span class="sxs-lookup"><span data-stu-id="8d88e-126">**Child window DPI change notifications** - In Per Monitor v2 contexts, the entire window tree is notified of any DPI changes that occur.</span></span>
-   <span data-ttu-id="8d88e-127">**Масштабирование неклиентской области** . все окна автоматически будут иметь неклиентскую область, отрисованную с учетом dpi.</span><span class="sxs-lookup"><span data-stu-id="8d88e-127">**Scaling of non-client area** - All windows will automatically have their non-client area drawn in a DPI sensitive fashion.</span></span> <span data-ttu-id="8d88e-128">Вызовы [**енабленонклиентдпискалинг**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) не нужны.</span><span class="sxs-lookup"><span data-stu-id="8d88e-128">Calls to [**EnableNonClientDpiScaling**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling) are unnecessary.</span></span>
-   <span data-ttu-id="8d88e-129">**Масштабирование меню Win32** . все меню NTuser, созданные в контекстах Monitor 2, будут масштабироваться в соответствии с мониторингом.</span><span class="sxs-lookup"><span data-stu-id="8d88e-129">**Scaling of Win32 menus** - All NTUSER menus created in Per Monitor v2 contexts will be scaling in a per-monitor fashion.</span></span>
-   <span data-ttu-id="8d88e-130">**Масштабирование диалоговых окон** . диалоговые окна Win32, созданные в каждом контексте монитора версии 2, автоматически реагируют на изменения dpi.</span><span class="sxs-lookup"><span data-stu-id="8d88e-130">**Dialog Scaling** - Win32 dialogs created in Per Monitor v2 contexts will automatically respond to DPI changes.</span></span>
-   <span data-ttu-id="8d88e-131">**Улучшенное масштабирование элементов управления Comctl32** . различные элементы управления Comctl32 имеют улучшенное масштабирование DPI в контекстах монитора версии 2.</span><span class="sxs-lookup"><span data-stu-id="8d88e-131">**Improved scaling of comctl32 controls** - Various comctl32 controls have improved DPI scaling behavior in Per Monitor v2 contexts.</span></span>
-   <span data-ttu-id="8d88e-132">**Улучшенное поведение** . дескрипторы укссеме, открытые в контексте каждого окна монитора версии 2, будут действовать с точки зрения dpi, связанного с этим окном.</span><span class="sxs-lookup"><span data-stu-id="8d88e-132">**Improved theming behavior** - UxTheme handles opened in the context of a Per Monitor v2 window will operate in terms of the DPI associated with that window.</span></span>

  
</dl>

<span data-ttu-id="8d88e-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span><span class="sxs-lookup"><span data-stu-id="8d88e-133">**DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED**</span></span>

<span data-ttu-id="8d88e-134">Неосведомленность DPI с улучшенным качеством содержимого на основе GDI.</span><span class="sxs-lookup"><span data-stu-id="8d88e-134">DPI unaware with improved quality of GDI-based content.</span></span> <span data-ttu-id="8d88e-135">Этот режим работает аналогично DPI_AWARENESS_CONTEXT_UNAWARE, но также позволяет системе автоматически улучшать качество отрисовки текста и других примитивов на основе GDI, когда окно отображается на мониторе с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="8d88e-135">This mode behaves similarly to DPI_AWARENESS_CONTEXT_UNAWARE, but also enables the system to automatically improve the rendering quality of text and other GDI-based primitives when the window is displayed on a high-DPI monitor.</span></span>

<span data-ttu-id="8d88e-136">Дополнительные сведения см. в разделе [улучшение возможностей высокого DPI в классических приложениях на основе GDI](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span><span class="sxs-lookup"><span data-stu-id="8d88e-136">For more details, see [Improving the high-DPI experience in GDI-based Desktop apps](https://blogs.windows.com/buildingapps/2017/05/19/improving-high-dpi-experience-gdi-based-desktop-apps/#Uwv9gY1SvpbgQ4dK.97).</span></span>

<span data-ttu-id="8d88e-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED была введена в Октябрь 2018 обновления Windows 10 октября (также известной как версия 1809).</span><span class="sxs-lookup"><span data-stu-id="8d88e-137">DPI_AWARENESS_CONTEXT_UNAWARE_GDISCALED was introduced in the October 2018 update of Windows 10 (also known as version 1809).</span></span>


## <a name="requirements"></a><span data-ttu-id="8d88e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="8d88e-138">Requirements</span></span>

| <span data-ttu-id="8d88e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="8d88e-139">Requirement</span></span> | <span data-ttu-id="8d88e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="8d88e-140">Value</span></span> |
|----|-----------|
| <span data-ttu-id="8d88e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d88e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8d88e-142">\[Только для настольных приложений Windows 10 версии 1607\]</span><span class="sxs-lookup"><span data-stu-id="8d88e-142">Windows 10, version 1607 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d88e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d88e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8d88e-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8d88e-144">None supported</span></span> <br/>  |
| <span data-ttu-id="8d88e-145">Header</span><span class="sxs-lookup"><span data-stu-id="8d88e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d88e-146"><dt>виндеф. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d88e-146"><dt>windef.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="8d88e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d88e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d88e-148">**аредпиаваренессконтекстсекуал**</span><span class="sxs-lookup"><span data-stu-id="8d88e-148">**AreDpiAwarenessContextsEqual**</span></span>](/windows/desktop/api/winuser/nf-winuser-aredpiawarenesscontextsequal)
</dt> <dt>

[<span data-ttu-id="8d88e-149">**жетаваренессфромдпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-149">**GetAwarenessFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getawarenessfromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-150">**жетдпифромдпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-150">**GetDpiFromDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-151">**жетсреаддпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-151">**GetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-152">**жетвиндовдпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-152">**GetWindowDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-153">**исвалиддпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-153">**IsValidDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-isvaliddpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-154">**сетпроцессдпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-154">**SetProcessDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)
</dt> </dl>

[<span data-ttu-id="8d88e-155">**сетсреаддпиаваренессконтекст**</span><span class="sxs-lookup"><span data-stu-id="8d88e-155">**SetThreadDpiAwarenessContext**</span></span>](/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext)
