---
title: Стили элементов управления анимацией (Коммктрл. h)
description: В этом разделе перечислены стили окон, используемые с элементами управления "анимация".
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d779b92c51420bc6bd9ad238bcff538dbc85841f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657261"
---
# <a name="animation-control-styles"></a><span data-ttu-id="72b47-103">Стили элементов управления анимацией</span><span class="sxs-lookup"><span data-stu-id="72b47-103">Animation Control Styles</span></span>

<span data-ttu-id="72b47-104">В этом разделе перечислены стили окон, используемые с элементами управления "анимация".</span><span class="sxs-lookup"><span data-stu-id="72b47-104">This section lists the window styles used with animation controls.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="72b47-105">Константа</span><span class="sxs-lookup"><span data-stu-id="72b47-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="72b47-106">Описание</span><span class="sxs-lookup"><span data-stu-id="72b47-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <span data-ttu-id="72b47-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="72b47-107"><dt><strong>ACS_AUTOPLAY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="72b47-108">Запускает воспроизведение анимации сразу после открытия AVI-файла.</span><span class="sxs-lookup"><span data-stu-id="72b47-108">Starts playing the animation as soon as the AVI clip is opened.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <span data-ttu-id="72b47-109"><dt><strong>ACS_CENTER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="72b47-109"><dt><strong>ACS_CENTER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="72b47-110">Центрирование анимации в окне анимированного элемента управления.</span><span class="sxs-lookup"><span data-stu-id="72b47-110">Centers the animation in the animation control's window.</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <span data-ttu-id="72b47-111"><dt><strong>ACS_TIMER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="72b47-111"><dt><strong>ACS_TIMER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="72b47-112">По умолчанию элемент управления создает поток для воспроизведения фрагмента AVI.</span><span class="sxs-lookup"><span data-stu-id="72b47-112">By default, the control creates a thread to play the AVI clip.</span></span> <span data-ttu-id="72b47-113">Если установить этот флаг, элемент управления воспроизводит клип, не создавая поток; на внутреннем уровне элемент управления использует таймер Win32 для синхронизации воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="72b47-113">If you set this flag, the control plays the clip without creating a thread; internally the control uses a Win32 timer to synchronize playback.</span></span> <br/> <span data-ttu-id="72b47-114"><strong>Comctl32.dll версии 6 и более поздних версий:</strong> Этот стиль не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="72b47-114"><strong>Comctl32.dll version 6 and later:</strong> This style is not supported.</span></span> <span data-ttu-id="72b47-115">По умолчанию элемент управления воспроизводит ролик AVI без создания потока.</span><span class="sxs-lookup"><span data-stu-id="72b47-115">By default, the control plays the AVI clip without creating a thread.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="72b47-116">Версия Comctl32.dll 6 не является распространяемой.</span><span class="sxs-lookup"><span data-stu-id="72b47-116">Comctl32.dll version 6 is not redistributable.</span></span> <span data-ttu-id="72b47-117">Чтобы использовать Comctl32.dll версии 6, укажите ее в манифесте.</span><span class="sxs-lookup"><span data-stu-id="72b47-117">To use Comctl32.dll version 6, specify it in a manifest.</span></span> <span data-ttu-id="72b47-118">Дополнительные сведения о манифестах см. в разделе <a href="cookbook-overview.md">Включение визуальных стилей</a>.</span><span class="sxs-lookup"><span data-stu-id="72b47-118">For more information on manifests, see <a href="cookbook-overview.md">Enabling Visual Styles</a>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <span data-ttu-id="72b47-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="72b47-119"><dt><strong>ACS_TRANSPARENT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="72b47-120">Позволяет сопоставить цвет фона анимации с основным окном, создавая &quot; прозрачный &quot; фон.</span><span class="sxs-lookup"><span data-stu-id="72b47-120">Allows you to match an animation's background color to that of the underlying window, creating a &quot;transparent&quot; background.</span></span> <span data-ttu-id="72b47-121">У родителя элемента управления анимации не должно быть стиля WS_CLIPCHILDREN (см. раздел <a href="/windows/desktop/winmsg/window-styles">стили окна</a>).</span><span class="sxs-lookup"><span data-stu-id="72b47-121">The parent of the animation control must not have the WS_CLIPCHILDREN style (see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>).</span></span> <span data-ttu-id="72b47-122">Элемент управления отправляет <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> сообщение родительскому объекту.</span><span class="sxs-lookup"><span data-stu-id="72b47-122">The control sends a <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> message to its parent.</span></span> <span data-ttu-id="72b47-123">Используйте <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>сетбкколор</strong></a> , чтобы задать в качестве цвета фона для контекста устройства соответствующее значение.</span><span class="sxs-lookup"><span data-stu-id="72b47-123">Use <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> to set the background color for the device context to an appropriate value.</span></span> <span data-ttu-id="72b47-124">Элемент управления интерпретирует верхний левый пиксел первого кадра как цвет фона анимации по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="72b47-124">The control interprets the upper-left pixel of the first frame as the animation's default background color.</span></span> <span data-ttu-id="72b47-125">Он выполнит сопоставление всех пикселей с этим цветом и значением, которое вы указали в ответе на WM_CTLCOLORSTATIC.</span><span class="sxs-lookup"><span data-stu-id="72b47-125">It will remap all pixels with that color to the value you supplied in response to WM_CTLCOLORSTATIC.</span></span> <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="72b47-126">Требования</span><span class="sxs-lookup"><span data-stu-id="72b47-126">Requirements</span></span>



| <span data-ttu-id="72b47-127">Требование</span><span class="sxs-lookup"><span data-stu-id="72b47-127">Requirement</span></span> | <span data-ttu-id="72b47-128">Значение</span><span class="sxs-lookup"><span data-stu-id="72b47-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72b47-129">Header</span><span class="sxs-lookup"><span data-stu-id="72b47-129">Header</span></span><br/> | <dl> <span data-ttu-id="72b47-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b47-130"><dt>CommCtrl.h</dt></span></span> </dl> |



