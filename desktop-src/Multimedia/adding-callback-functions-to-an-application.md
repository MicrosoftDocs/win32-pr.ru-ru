---
title: Добавление функций обратного вызова в приложение
description: Добавление функций обратного вызова в приложение
ms.assetid: b7bde1be-b229-4e00-8906-22d7dcf9ea04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d4f5f3dc43227f92305032decaf917bf521d95b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532177"
---
# <a name="adding-callback-functions-to-an-application"></a><span data-ttu-id="ba1b9-103">Добавление функций обратного вызова в приложение</span><span class="sxs-lookup"><span data-stu-id="ba1b9-103">Adding Callback Functions to an Application</span></span>

<span data-ttu-id="ba1b9-104">Приложение может регистрировать функции обратного вызова с помощью окна Capture, чтобы оно уведомляет приложение в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="ba1b9-104">An application can register callback functions with the capture window so that it notifies the application in the following circumstances:</span></span>

-   <span data-ttu-id="ba1b9-105">Состояние изменится</span><span class="sxs-lookup"><span data-stu-id="ba1b9-105">The status changes</span></span>
-   <span data-ttu-id="ba1b9-106">Ошибки происходят</span><span class="sxs-lookup"><span data-stu-id="ba1b9-106">Errors occur</span></span>
-   <span data-ttu-id="ba1b9-107">Станут доступны видеокадры и буферы аудио</span><span class="sxs-lookup"><span data-stu-id="ba1b9-107">Video frame and audio buffers become available</span></span>
-   <span data-ttu-id="ba1b9-108">Приложение должно передаваться во время потоковой записи</span><span class="sxs-lookup"><span data-stu-id="ba1b9-108">The application should yield during streaming capture</span></span>

<span data-ttu-id="ba1b9-109">В следующем примере создается окно записи, а в цикле обработки сообщений приложения регистрируется состояние, ошибка, поток видео и функции обратного вызова кадра.</span><span class="sxs-lookup"><span data-stu-id="ba1b9-109">The following example creates a capture window and registers status, error, video stream, and frame callback functions in the message-processing loop of an application.</span></span> <span data-ttu-id="ba1b9-110">Он также включает образец инструкции для отключения функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ba1b9-110">It also includes a sample statement for disabling a callback function.</span></span> <span data-ttu-id="ba1b9-111">В последующих примерах показаны простые функции состояния, ошибки и кадра обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="ba1b9-111">Subsequent examples show simple status, error, and frame callback functions.</span></span>


```C++
case WM_CREATE: 
{ 
    char    achDeviceName[80] ; 
    char    achDeviceVersion[100] ; 
    char    achBuffer[100] ; 
    WORD    wDriverCount = 0 ; 
    WORD    wIndex ; 
    WORD    wError ; 
    HMENU   hMenu ; 
 
    // Create a capture window using the capCreateCaptureWindow macro.
    ghWndCap = capCreateCaptureWindow((LPSTR)"Capture Window", 
        WS_CHILD | WS_VISIBLE, 0, 0, 160, 120, (HWND) hWnd, (int) 0); 
 
    // Register the error callback function using the 
    // capSetCallbackOnError macro. 
    capSetCallbackOnError(ghWndCap, fpErrorCallback); 
 
    // Register the status callback function using the 
    // capSetCallbackOnStatus macro. 
    capSetCallbackOnStatus(ghWndCap, fpStatusCallback); 
 
    // Register the video-stream callback function using the
    // capSetCallbackOnVideoStream macro. 
    capSetCallbackOnVideoStream(ghWndCap, fpVideoCallback); 
 
    // Register the frame callback function using the
    // capSetCallbackOnFrame macro. 
    capSetCallbackOnFrame(ghWndCap, fpFrameCallback); 
 
    // Connect to a capture driver 

    break; 
} 
case WM_CLOSE: 
{ 
// Use the capSetCallbackOnFrame macro to 
// disable the frame callback. Similar calls exist for the other 
// callback functions.

    capSetCallbackOnFrame(ghWndCap, NULL); 

    break; 
} 
 
```



## <a name="related-topics"></a><span data-ttu-id="ba1b9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="ba1b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba1b9-113">Использование видеозаписи</span><span class="sxs-lookup"><span data-stu-id="ba1b9-113">Using Video Capture</span></span>](using-video-capture.md)
</dt> </dl>

 

 




