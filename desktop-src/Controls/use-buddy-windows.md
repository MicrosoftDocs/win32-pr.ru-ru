---
title: Использование дружественных окон
description: Настроив другие элементы управления как дружественные окна для TrackBar, можно автоматически размещать эти элементы управления на концах TrackBar в виде меток.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067808"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="fc9ba-103">Использование дружественных окон</span><span class="sxs-lookup"><span data-stu-id="fc9ba-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="fc9ba-104">Настроив другие элементы управления как дружественные окна для TrackBar, можно автоматически размещать эти элементы управления на концах TrackBar в виде меток.</span><span class="sxs-lookup"><span data-stu-id="fc9ba-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="fc9ba-105">На следующем рисунке показана горизонтальная и вертикальная линейка, как со статическими элементами управления в качестве дружественных окон.</span><span class="sxs-lookup"><span data-stu-id="fc9ba-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![снимок экрана, показывающий диалоговое окно с горизонтальной и вертикальной TrackBar](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="fc9ba-107">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="fc9ba-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="fc9ba-108">Технологии</span><span class="sxs-lookup"><span data-stu-id="fc9ba-108">Technologies</span></span>

-   [<span data-ttu-id="fc9ba-109">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="fc9ba-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="fc9ba-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="fc9ba-110">Prerequisites</span></span>

-   <span data-ttu-id="fc9ba-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="fc9ba-111">C/C++</span></span>
-   <span data-ttu-id="fc9ba-112">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="fc9ba-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="fc9ba-113">Инструкции</span><span class="sxs-lookup"><span data-stu-id="fc9ba-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="fc9ba-114">Использование дружественных окон</span><span class="sxs-lookup"><span data-stu-id="fc9ba-114">Use Buddy Windows</span></span>

<span data-ttu-id="fc9ba-115">В следующем примере кода создаются дружественные окна, показанные на рисунке.</span><span class="sxs-lookup"><span data-stu-id="fc9ba-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="fc9ba-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc9ba-116">Remarks</span></span>

<span data-ttu-id="fc9ba-117">**IDC \_ SLIDER1** и **IDC \_ SLIDER2** — это ползунки, созданные в редакторе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc9ba-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc9ba-118">См. также</span><span class="sxs-lookup"><span data-stu-id="fc9ba-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc9ba-119">Использование элементов управления TrackBar</span><span class="sxs-lookup"><span data-stu-id="fc9ba-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




