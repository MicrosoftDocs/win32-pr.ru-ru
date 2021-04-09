---
title: Запись видео с минимальным подходом
description: Запись видео с минимальным подходом
ms.assetid: e39ff590-69c0-4927-90c2-786c6082068f
keywords:
- Видео для Windows (VFW), запись видео
- VFW (видео для Windows), запись видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a65d5d5bbdc00dfd947c5d917e514d72e3ac069
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103890524"
---
# <a name="video-capture-a-minimal-approach"></a><span data-ttu-id="fdd21-105">Видеозапись: минимальный подход</span><span class="sxs-lookup"><span data-stu-id="fdd21-105">Video Capture: A Minimal Approach</span></span>

<span data-ttu-id="fdd21-106">Видеозапись помещает поток видео и звуковых данных и сохраняет их на жестком диске или на любом другом типе постоянного запоминающего устройства.</span><span class="sxs-lookup"><span data-stu-id="fdd21-106">Video capture digitizes a stream of video and audio data, and stores it on a hard disk or some other type of persistent storage device.</span></span> <span data-ttu-id="fdd21-107">В этом разделе описывается добавление простой формы видеозаписи в приложение с помощью трех инструкций кода.</span><span class="sxs-lookup"><span data-stu-id="fdd21-107">This section describes how to add a simple form of video capture to an application using three statements of code.</span></span> <span data-ttu-id="fdd21-108">В нем также описывается завершение или прерывание сеанса записи путем отправки сообщений в окно Capture (захват).</span><span class="sxs-lookup"><span data-stu-id="fdd21-108">It also describes how to end or abort a capture session by sending messages to the capture window.</span></span>

<span data-ttu-id="fdd21-109">Окно записи Авикап обрабатывает сведения о потоковой передаче аудио и видео в файлы AVI.</span><span class="sxs-lookup"><span data-stu-id="fdd21-109">An AVICap capture window handles the details of streaming audio and video capture to AVI files.</span></span> <span data-ttu-id="fdd21-110">Это освобождает ваше приложение от участия в формате AVI, управлении видео-и аудио-буферами, а также на низком уровне доступа к видео и драйверам звуковых устройств.</span><span class="sxs-lookup"><span data-stu-id="fdd21-110">This frees your application from involvement in the AVI file format, video and audio buffer management, and the low-level access of video and audio device drivers.</span></span> <span data-ttu-id="fdd21-111">Авикап предоставляет гибкий интерфейс для приложений.</span><span class="sxs-lookup"><span data-stu-id="fdd21-111">AVICap provides a flexible interface for applications.</span></span> <span data-ttu-id="fdd21-112">Вы можете добавить запись видео в приложение, используя только следующие строки кода:</span><span class="sxs-lookup"><span data-stu-id="fdd21-112">You can add video capture to your application, using only the following lines of code:</span></span>


```C++
hWndC = capCreateCaptureWindow ( "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE , 0, 0, 160, 120, hwndParent, nID);

SendMessage (hWndC, WM_CAP_DRIVER_CONNECT, 0 /* wIndex */, 0L);

SendMessage (hWndC, WM_CAP_SEQUENCE, 0, 0L);
 
```



<span data-ttu-id="fdd21-113">Также доступен интерфейс макросов, который предоставляет альтернативу использованию функции [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) и повышает удобочитаемость приложения.</span><span class="sxs-lookup"><span data-stu-id="fdd21-113">A macro interface is also available that provides an alternative to using the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function and improves the readability of an application.</span></span> <span data-ttu-id="fdd21-114">В следующем примере для добавления видеозаписи в приложение используется интерфейс макросов.</span><span class="sxs-lookup"><span data-stu-id="fdd21-114">The following example uses the macro interface to add video capture to an application.</span></span>


```C++
hWndC = capCreateCaptureWindow (   "My Own Capture Window", 
    WS_CHILD | WS_VISIBLE ,   0, 0, 160, 120, hwndParent, nID);

capDriverConnect (hWndC, 0);

capCaptureSequence (hWndC); 
 
```



<span data-ttu-id="fdd21-115">После того как приложение создаст окно записи класса Авикап и подключится к видеодрайверу, окно записи готово к записи данных.</span><span class="sxs-lookup"><span data-stu-id="fdd21-115">After your application creates a capture window of the AVICap window class and connects it to a video driver, the capture window is ready to capture data.</span></span> <span data-ttu-id="fdd21-116">На этом этапе приложение может просто отправить сообщение [**\_ \_ последовательности авторизации WM**](wm-cap-sequence.md) (или макрос [**капкаптуресекуенце**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) ) для начала записи.</span><span class="sxs-lookup"><span data-stu-id="fdd21-116">At this point, your application can simply send the [**WM\_CAP\_SEQUENCE**](wm-cap-sequence.md) message (or the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro) to begin capturing.</span></span>

<span data-ttu-id="fdd21-117">С помощью параметров по умолчанию \_ последовательность закрепления WM \_ инициирует запись видео-и звукового ввода в файл с именем CAPTURE.AVI.</span><span class="sxs-lookup"><span data-stu-id="fdd21-117">Using default settings, WM\_CAP\_SEQUENCE initiates the capture of video and audio input to a file named CAPTURE.AVI.</span></span> <span data-ttu-id="fdd21-118">Запись сохраняется до тех пор, пока не произойдет одно из следующих событий:</span><span class="sxs-lookup"><span data-stu-id="fdd21-118">Capture continues until one of the following events occurs:</span></span>

-   <span data-ttu-id="fdd21-119">Пользователь нажимает клавишу ESC или кнопку мыши.</span><span class="sxs-lookup"><span data-stu-id="fdd21-119">The user presses the ESC key or a mouse button.</span></span>
-   <span data-ttu-id="fdd21-120">Приложение останавливает или прерывает операцию записи.</span><span class="sxs-lookup"><span data-stu-id="fdd21-120">Your application stops or aborts capture operation.</span></span>
-   <span data-ttu-id="fdd21-121">Диск заполнен.</span><span class="sxs-lookup"><span data-stu-id="fdd21-121">The disk becomes full.</span></span>

<span data-ttu-id="fdd21-122">В приложении можно запретить потоковую передачу записанных данных в файл, отправив сообщение [**об \_ \_ окончании крепления WM**](wm-cap-stop.md) (или макрос [**капкаптурестоп**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="fdd21-122">In an application, you can stop streaming captured data to a file by sending the [**WM\_CAP\_STOP**](wm-cap-stop.md) (or the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro) message to a capture window.</span></span> <span data-ttu-id="fdd21-123">Можно также прервать операцию записи, отправив сообщение [**об \_ \_ отмене крепления WM**](wm-cap-abort.md) (или макрос [**капкаптуреаборт**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="fdd21-123">You can also abort the capture operation by sending the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message (or the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro) to a capture window.</span></span>

 

 