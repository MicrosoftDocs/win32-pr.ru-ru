---
title: Плоские полосы прокрутки
description: В Microsoft Internet Explorer 4,0 появилась новая визуальная технология, называемая плоскими полосами прокрутки.
ms.assetid: f7e00e71-bf12-4db9-bb84-6d413b967049
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fbbdb64aa9815cb56f5dc3bf55ffb17390db38
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793993"
---
# <a name="flat-scroll-bars"></a><span data-ttu-id="bde2d-103">Плоские полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="bde2d-103">Flat Scroll Bars</span></span>

<span data-ttu-id="bde2d-104">В Microsoft Internet Explorer 4,0 появилась новая визуальная технология, называемая плоскими полосами прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-104">Microsoft Internet Explorer 4.0 introduced a new visual technology called flat scroll bars.</span></span> <span data-ttu-id="bde2d-105">Функционально плоские полосы прокрутки ведут себя так же, как стандартные полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-105">Functionally, flat scroll bars behave just like standard scroll bars.</span></span> <span data-ttu-id="bde2d-106">Разница заключается в том, что их внешний вид можно изменить на более высокий, чем стандартные полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-106">The difference is that you can customize their appearance to a greater extent than standard scroll bars.</span></span>

<span data-ttu-id="bde2d-107">На следующем рисунке показано окно, содержащее плоскую полосу прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-107">The following illustration shows a window that contains a flat scroll bar.</span></span>

![снимок экрана окна, содержащего плоскую полосу прокрутки](images/flatsb.jpg)

> [!Note]  
> <span data-ttu-id="bde2d-109">Неструктурированные полосы прокрутки поддерживаются Comctl32.dll версиями 4,71 – 5,82.</span><span class="sxs-lookup"><span data-stu-id="bde2d-109">Flat scroll bars are supported by Comctl32.dll versions 4.71 through 5.82.</span></span> <span data-ttu-id="bde2d-110">Comctl32.dll версии 6,00 и более поздних не поддерживают плоские полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-110">Comctl32.dll versions 6.00 and later do not support flat scroll bars.</span></span>

 

## <a name="using-flat-scroll-bars"></a><span data-ttu-id="bde2d-111">Использование плоских полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="bde2d-111">Using Flat Scroll Bars</span></span>

<span data-ttu-id="bde2d-112">В этом разделе описывается, как реализовать плоские полосы прокрутки в приложении.</span><span class="sxs-lookup"><span data-stu-id="bde2d-112">This section describes how to implement flat scroll bars in your application.</span></span>

### <a name="before-you-begin"></a><span data-ttu-id="bde2d-113">Перед началом</span><span class="sxs-lookup"><span data-stu-id="bde2d-113">Before You Begin</span></span>

<span data-ttu-id="bde2d-114">Чтобы использовать функции плоской полосы прокрутки, необходимо включить Коммктрл. h в исходные файлы и связать с Comctl32. lib.</span><span class="sxs-lookup"><span data-stu-id="bde2d-114">To use the flat scroll bar functions, you must include Commctrl.h in your source files and link with Comctl32.lib.</span></span>

### <a name="adding-flat-scroll-bars-to-a-window"></a><span data-ttu-id="bde2d-115">Добавление плоских полос прокрутки в окно</span><span class="sxs-lookup"><span data-stu-id="bde2d-115">Adding Flat Scroll Bars to a Window</span></span>

<span data-ttu-id="bde2d-116">Чтобы добавить плоские полосы прокрутки в окно, вызовите [**инитиализефлатсб**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), передав в окно маркер.</span><span class="sxs-lookup"><span data-stu-id="bde2d-116">To add flat scroll bars to a window, call [**InitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb), passing the handle to the window.</span></span> <span data-ttu-id="bde2d-117">Вместо использования стандартных функций полосы прокрутки для работы с полосами прокрутки необходимо использовать эквивалентную \_ функцию флатсб XXX.</span><span class="sxs-lookup"><span data-stu-id="bde2d-117">Instead of using the standard scroll bar functions to manipulate your scroll bars, you must use the equivalent FlatSB\_XXX function.</span></span> <span data-ttu-id="bde2d-118">Существуют плоские функции полосы прокрутки для установки и получения данных прокрутки, диапазона и расположения.</span><span class="sxs-lookup"><span data-stu-id="bde2d-118">There are flat scroll bar functions for setting and retrieving the scroll information, range, and position.</span></span> <span data-ttu-id="bde2d-119">Если для окна не инициализированы плоские полосы прокрутки, API плоской полосы прокрутки будет откладываться на соответствующие стандартные функции, если они используются.</span><span class="sxs-lookup"><span data-stu-id="bde2d-119">If flat scroll bars haven't been initialized for your window, the flat scroll bar API will defer to the corresponding standard functions, if any are used.</span></span> <span data-ttu-id="bde2d-120">Это позволяет включать и отключать плоские полосы прокрутки без написания условного кода.</span><span class="sxs-lookup"><span data-stu-id="bde2d-120">This allows you to turn flat scroll bars on and off without having to write conditional code.</span></span>

<span data-ttu-id="bde2d-121">Так как приложение может установить пользовательские метрики для плоских полос прокрутки, они не обновляются автоматически при изменении системных метрик.</span><span class="sxs-lookup"><span data-stu-id="bde2d-121">Because an application may have set custom metrics for its flat scroll bars, they are not automatically updated when system metrics change.</span></span> <span data-ttu-id="bde2d-122">При изменении метрик полосы прокрутки системы сообщение [**WM \_ сеттингчанже**](/windows/desktop/winmsg/wm-settingchange) пересылается с параметром *wParam* , установленным в значение [**SPI \_ сетнонклиентметрикс**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="bde2d-122">When the system scroll bar metrics change, a [**WM\_SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) message is broadcast, with its *wParam* set to [**SPI\_SETNONCLIENTMETRICS**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span> <span data-ttu-id="bde2d-123">Чтобы обновить плоские полосы прокрутки до новых системных метрик, приложения должны выполнить обработку этого сообщения и явно изменить свойства, зависящие от метрики плоской полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-123">To update flat scroll bars to the new system metrics, applications must handle this message and change the flat scroll bar's metric-dependent properties explicitly.</span></span>

<span data-ttu-id="bde2d-124">Чтобы обновить свойства полосы прокрутки, используйте [**флатсб \_ сетскроллпроп**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span><span class="sxs-lookup"><span data-stu-id="bde2d-124">To update your scroll bar properties, use [**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop).</span></span> <span data-ttu-id="bde2d-125">Следующий фрагмент кода изменяет свойства, зависящие от метрики плоской полосы прокрутки, на текущие системные значения.</span><span class="sxs-lookup"><span data-stu-id="bde2d-125">The following code fragment changes a flat scroll bar's metric dependent properties to the current system values.</span></span>


```
void FlatSB_UpdateMetrics(HWND hWnd)
{
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXVSCROLL, GetSystemMetrics(SM_CXVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHSCROLL, GetSystemMetrics(SM_CXHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVSCROLL, GetSystemMetrics(SM_CYVSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYHSCROLL, GetSystemMetrics(SM_CYHSCROLL), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CXHTHUMB, GetSystemMetrics(SM_CXHTHUMB), FALSE);
FlatSB_SetScrollProp(hWnd, WSB_PROP_CYVTHUMB, GetSystemMetrics(SM_CYVTHUMB), TRUE);
}
```



### <a name="enhancing-flat-scroll-bars"></a><span data-ttu-id="bde2d-126">Улучшение плоских полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="bde2d-126">Enhancing Flat Scroll Bars</span></span>

<span data-ttu-id="bde2d-127">[**Флатсб \_ Сетскроллпроп**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) позволяет изменять плоские полосы прокрутки для настройки вида окна.</span><span class="sxs-lookup"><span data-stu-id="bde2d-127">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) allows you to modify the flat scroll bars to customize the look of your window.</span></span> <span data-ttu-id="bde2d-128">Для вертикальных полос прокрутки можно изменить ширину полосы и высоту стрелок направления.</span><span class="sxs-lookup"><span data-stu-id="bde2d-128">For vertical scroll bars, you can change the width of the bar and the height of the direction arrows.</span></span> <span data-ttu-id="bde2d-129">Для горизонтальных полос прокрутки можно изменить высоту линейки и ширину стрелок направления.</span><span class="sxs-lookup"><span data-stu-id="bde2d-129">For horizontal scroll bars, you can change the height of the bar and the width of the direction arrows.</span></span> <span data-ttu-id="bde2d-130">Также можно изменить цвет фона как для горизонтальной, так и для вертикальной полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-130">You can also change the background color of both the horizontal and vertical scroll bars.</span></span>

<span data-ttu-id="bde2d-131">[**Флатсб \_ Сетскроллпроп**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) также позволяет настроить отображение плоских полос прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-131">[**FlatSB\_SetScrollProp**](/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop) also allows you to customize how the flat scroll bars are displayed.</span></span> <span data-ttu-id="bde2d-132">Изменив свойства WSB \_ prop \_ ВСТИЛЕ и WSB \_ prop \_ хстиле, можно задать тип полосы прокрутки, который будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="bde2d-132">By changing the WSB\_PROP\_VSTYLE and WSB\_PROP\_HSTYLE properties, you can set the type of scroll bar that you want to use.</span></span> <span data-ttu-id="bde2d-133">Доступны три стиля.</span><span class="sxs-lookup"><span data-stu-id="bde2d-133">Three styles are available.</span></span>



|                    |                                                                                                                                                                          |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde2d-134">\_режим ENCARTA для шины \_</span><span class="sxs-lookup"><span data-stu-id="bde2d-134">FSB\_ENCARTA\_MODE</span></span> | <span data-ttu-id="bde2d-135">Отображается стандартная плоская полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-135">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="bde2d-136">Когда указатель мыши перемещается над кнопкой направления или бегунком, эта часть полосы прокрутки будет отображаться в трехмерном виде.</span><span class="sxs-lookup"><span data-stu-id="bde2d-136">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in 3-D.</span></span>             |
| <span data-ttu-id="bde2d-137">\_плоский \_ режим системной шины</span><span class="sxs-lookup"><span data-stu-id="bde2d-137">FSB\_FLAT\_MODE</span></span>    | <span data-ttu-id="bde2d-138">Отображается стандартная плоская полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-138">A standard flat scroll bar is displayed.</span></span> <span data-ttu-id="bde2d-139">Когда указатель мыши перемещается над кнопкой направления или бегунком, эта часть полосы прокрутки будет отображаться в инвертированных цветах.</span><span class="sxs-lookup"><span data-stu-id="bde2d-139">When the mouse moves over a direction button or the thumb, that portion of the scroll bar will be displayed in inverted colors.</span></span> |
| <span data-ttu-id="bde2d-140">\_обычный \_ режим системной шины</span><span class="sxs-lookup"><span data-stu-id="bde2d-140">FSB\_REGULAR\_MODE</span></span> | <span data-ttu-id="bde2d-141">Отображается обычная, неплоская полоса прокрутки.</span><span class="sxs-lookup"><span data-stu-id="bde2d-141">A normal, nonflat scroll bar is displayed.</span></span> <span data-ttu-id="bde2d-142">Специальные визуальные эффекты не применяются.</span><span class="sxs-lookup"><span data-stu-id="bde2d-142">No special visual effects will be applied.</span></span>                                                                                    |



 

### <a name="removing-flat-scroll-bars"></a><span data-ttu-id="bde2d-143">Удаление плоских полос прокрутки</span><span class="sxs-lookup"><span data-stu-id="bde2d-143">Removing Flat Scroll Bars</span></span>

<span data-ttu-id="bde2d-144">Если вы хотите удалить плоские полосы прокрутки из окна, вызовите функцию [**унинитиализефлатсб**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) , передав маркер в окно.</span><span class="sxs-lookup"><span data-stu-id="bde2d-144">If you want to remove flat scroll bars from your window, call the [**UninitializeFlatSB**](/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb) function, passing the handle to the window.</span></span> <span data-ttu-id="bde2d-145">Эта функция удаляет плоские полосы прокрутки из окна во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="bde2d-145">This function only removes flat scroll bars from your window at run time.</span></span> <span data-ttu-id="bde2d-146">Вам не нужно вызывать эту функцию при уничтожении окна.</span><span class="sxs-lookup"><span data-stu-id="bde2d-146">You do not need to call this function when your window is destroyed.</span></span>

 

 