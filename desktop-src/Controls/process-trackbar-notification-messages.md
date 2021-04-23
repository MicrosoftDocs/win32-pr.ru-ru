---
title: Обработка сообщений с уведомлениями TrackBar
description: Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское \_ сообщение WM HSCROLL или WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774543"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="44f92-103">Обработка сообщений с уведомлениями TrackBar</span><span class="sxs-lookup"><span data-stu-id="44f92-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="44f92-104">Значения TrackBar уведомляют свое родительское окно действий пользователя, отправляя родительское сообщение [**WM \_ HSCROLL**](wm-hscroll.md) или [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="44f92-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="44f92-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="44f92-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="44f92-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="44f92-106">Technologies</span></span>

-   [<span data-ttu-id="44f92-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="44f92-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="44f92-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="44f92-108">Prerequisites</span></span>

-   <span data-ttu-id="44f92-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="44f92-109">C/C++</span></span>
-   <span data-ttu-id="44f92-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="44f92-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="44f92-111">Инструкции</span><span class="sxs-lookup"><span data-stu-id="44f92-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="44f92-112">Обработка сообщений с уведомлениями линейки</span><span class="sxs-lookup"><span data-stu-id="44f92-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="44f92-113">В следующем примере кода показана функция, которая вызывается, когда родительское окно TrackBar получает [**сообщение \_ HSCROLL WM**](wm-hscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="44f92-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="44f92-114">Значение TrackBar в этом примере имеет стиль [**TBS \_ енаблеселранже**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="44f92-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="44f92-115">Положение ползунка сравнивается с диапазоном выбора, а ползунок перемещается на начальную или конечную точку диапазона выбора при необходимости.</span><span class="sxs-lookup"><span data-stu-id="44f92-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="44f92-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44f92-116">Remarks</span></span>

<span data-ttu-id="44f92-117">В диалоговом окне, содержащем линейку с [**\_ вертикальным**](trackbar-control-styles.md) стилем TBS, эта функция может использоваться при получении сообщения [**\_ VSCROLL WM**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="44f92-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="44f92-118">См. также</span><span class="sxs-lookup"><span data-stu-id="44f92-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f92-119">Использование элементов управления TrackBar</span><span class="sxs-lookup"><span data-stu-id="44f92-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




