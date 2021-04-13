---
title: Предоставление обновлений состояния
description: Предоставление обновлений состояния
ms.assetid: 0f22c5d5-c85b-411e-a4dd-b7ad768be975
keywords:
- Макрос МЦивндсетактиветимер
- Макрос МЦивндсетинактиветимер
- Макрос МЦивнджетактиветимер
- Макрос МЦивнджетинактиветимер
- Макрос МЦивндсеттимерс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd53c9580f3ae9be09817979178d10e60765ea3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410871"
---
# <a name="providing-status-updates"></a><span data-ttu-id="1cbe5-108">Предоставление обновлений состояния</span><span class="sxs-lookup"><span data-stu-id="1cbe5-108">Providing Status Updates</span></span>

<span data-ttu-id="1cbe5-109">МЦивнд использует таймеры для периодического обновления сведений в заголовке окна и полосе прокрутки, а также для отправки сообщений уведомления родительскому окну.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-109">MCIWnd uses timers to periodically update information in the window title bar and scroll bar, and to send notification messages to the parent window.</span></span> <span data-ttu-id="1cbe5-110">Один таймер управляет периодом обновления активного окна МЦивнд, а второй таймер управляет периодом обновления неактивных окон МЦивнд.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-110">One timer controls the update period of the active MCIWnd window, and a second timer controls the update period for MCIWnd windows that are inactive.</span></span> <span data-ttu-id="1cbe5-111">Приложение может использовать макросы таймера МЦивнд для получения текущих параметров таймера и настройки периодов обновления.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-111">Your application can use the MCIWnd timer macros to retrieve the current timer settings and to adjust the update periods.</span></span>

<span data-ttu-id="1cbe5-112">Период обновления, используемый таймером активного окна, можно задать с помощью макроса [**мЦивндсетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="1cbe5-112">You can set the update period used by the active window timer by using the [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) macro.</span></span> <span data-ttu-id="1cbe5-113">Этот макрос задает период, используемый МЦивнд для обновления TrackBar, обновления расположения воспроизведения, указанного в заголовке окна, и уведомления родительского окна о том, что носитель был изменен.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-113">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window title bar, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="1cbe5-114">Текущий период обновления, используемый таймером активного окна, можно получить с помощью макроса [**мЦивнджетактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="1cbe5-114">You can retrieve the current update period used by the active window timer by using the [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) macro.</span></span> <span data-ttu-id="1cbe5-115">По умолчанию период обновления для таймера активного окна составляет 500 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-115">The default update period for the active window timer is 500 milliseconds.</span></span>

<span data-ttu-id="1cbe5-116">Период обновления, используемый таймером неактивного окна, можно задать с помощью макроса [**мЦивндсетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="1cbe5-116">You can set the update period used by the inactive window timer by using the [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) macro.</span></span> <span data-ttu-id="1cbe5-117">Этот макрос задает период, используемый параметром МЦивнд для обновления TrackBar, обновления расположения воспроизведения, указанного в заголовке окна, и уведомления родительского окна о том, что носитель был изменен.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-117">This macro sets the period used by MCIWnd to update the trackbar, to update the playback position reported in the window caption, and to notify the parent window that the media has changed.</span></span> <span data-ttu-id="1cbe5-118">Текущий период обновления, используемый таймером неактивного окна, можно получить с помощью макроса [**мЦивнджетинактиветимер**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .</span><span class="sxs-lookup"><span data-stu-id="1cbe5-118">You can retrieve the current update period used by the inactive window timer by using the [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) macro.</span></span> <span data-ttu-id="1cbe5-119">По умолчанию период обновления таймера неактивного окна составляет 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-119">The default update period for the inactive window timer is 2000 milliseconds.</span></span>

<span data-ttu-id="1cbe5-120">В приложении можно одновременно задать период обновления для обоих таймеров с помощью макроса [**мЦивндсеттимерс**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .</span><span class="sxs-lookup"><span data-stu-id="1cbe5-120">Your application can simultaneously set the update period for both timers by using the [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) macro.</span></span> <span data-ttu-id="1cbe5-121">Размер хранилища для значения периода обновления ограничен 16 битами.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-121">The storage for the value of the update period is limited to 16 bits.</span></span> <span data-ttu-id="1cbe5-122">Если требуется большее количество для любого периода обновления, установите таймеры по отдельности.</span><span class="sxs-lookup"><span data-stu-id="1cbe5-122">If a larger quantity for either update period is needed, set the timers individually.</span></span>

 

 




