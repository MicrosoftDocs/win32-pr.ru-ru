---
title: Ограничение перемещения ползунка
description: Как описано в разделе о элементах управления TrackBar, можно отключить часть диапазона TrackBar в качестве диапазона выбора. Одной из целей диапазона выбора может быть ограничение перемещения ползунка, что делает некоторые части ограничений полного диапазона.
ms.assetid: 9DD8BB11-EC6F-4695-BA56-5061F6EA5436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5414ddf72c44dcaed85afde349f0b9f813ed0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887943"
---
# <a name="how-to-limit-slider-movement"></a><span data-ttu-id="a2cbb-104">Ограничение перемещения ползунка</span><span class="sxs-lookup"><span data-stu-id="a2cbb-104">How to Limit Slider Movement</span></span>

<span data-ttu-id="a2cbb-105">Как описано в разделе [о элементах управления TrackBar](trackbar-controls.md), можно отключить часть диапазона TrackBar в качестве диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="a2cbb-105">As described in [About Trackbar Controls](trackbar-controls.md), it is possible to set off part of the trackbar range as a selection range.</span></span> <span data-ttu-id="a2cbb-106">Одной из целей диапазона выбора может быть ограничение перемещения ползунка, что делает некоторые части ограничений полного диапазона.</span><span class="sxs-lookup"><span data-stu-id="a2cbb-106">One purpose of a selection range might be to limit movement of the slider, making some parts of the full range off limits.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a2cbb-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="a2cbb-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a2cbb-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="a2cbb-108">Technologies</span></span>

-   [<span data-ttu-id="a2cbb-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="a2cbb-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a2cbb-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="a2cbb-110">Prerequisites</span></span>

-   <span data-ttu-id="a2cbb-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="a2cbb-111">C/C++</span></span>
-   <span data-ttu-id="a2cbb-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="a2cbb-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a2cbb-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="a2cbb-113">Instructions</span></span>

### <a name="limit-slider-movement"></a><span data-ttu-id="a2cbb-114">Ограничение перемещения ползунка</span><span class="sxs-lookup"><span data-stu-id="a2cbb-114">Limit Slider Movement</span></span>

<span data-ttu-id="a2cbb-115">В следующем примере кода ограничивается перемещение ползунка путем сброса положения ползунка при перемещении за пределы диапазона выбора.</span><span class="sxs-lookup"><span data-stu-id="a2cbb-115">The following example code limits movement of the slider by resetting the slider's position whenever it is moved outside the selection range.</span></span>


```
case WM_HSCROLL:
    {
        HWND hTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);
        
        if (hTrackbar == (HWND)lParam)
        {
            int newPos    = SendMessage(hTrackbar, TBM_GETPOS, 0, 0);
            int selStart  = SendMessage(hTrackbar, TBM_GETSELSTART, 0, 0);
            int selEnd    = SendMessage(hTrackbar, TBM_GETSELEND, 0, 0);
            
            if (newPos > selEnd)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selEnd);
            }
            
            else if (newPos < selStart)
            {
                SendMessage(hTrackbar, TBM_SETPOS, (WPARAM)TRUE, (LPARAM)selStart);
            }
        }
        
        break;
    }
```



## <a name="remarks"></a><span data-ttu-id="a2cbb-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2cbb-116">Remarks</span></span>

<span data-ttu-id="a2cbb-117">Этот фрагмент кода был бы частью процедуры окна диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a2cbb-117">This code snippet would be part of a dialog box's Window Procedure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2cbb-118">См. также</span><span class="sxs-lookup"><span data-stu-id="a2cbb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2cbb-119">Использование элементов управления TrackBar</span><span class="sxs-lookup"><span data-stu-id="a2cbb-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




