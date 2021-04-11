---
title: Запись Still-Image
description: Запись Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Сообщение WM_CAP_GRAB_FRAME_NOSTOP
- Сообщение WM_CAP_GRAB_FRAME
- макрос Капграбфраменостоп
- макрос Капграбфраме
- Сообщение WM_CAP_EDIT_COPY
- макрос Капедиткопи
- Сообщение WM_CAP_FILE_SAVEDIB
- макрос Капфилесаведиб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132902"
---
# <a name="still-image-capture"></a><span data-ttu-id="5d787-111">Запись Still-Image</span><span class="sxs-lookup"><span data-stu-id="5d787-111">Still-Image Capture</span></span>

<span data-ttu-id="5d787-112">Если вы хотите записать один кадр как изображение по-прежнему, вы можете использовать для записи изображения с цифрами во внутреннем буфере фрейма, а также сообщение об ошибке [**\_ \_ захвата \_ \_**](wm-cap-grab-frame-nostop.md) или маркер [**\_ \_ захвата \_ WM**](wm-cap-grab-frame.md) Cap (или макрос [**капграбфраменостоп**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) или [**капграбфраме**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ).</span><span class="sxs-lookup"><span data-stu-id="5d787-112">If you want to capture a single frame as a still image, you can use the [**WM\_CAP\_GRAB\_FRAME\_NOSTOP**](wm-cap-grab-frame-nostop.md) or [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message (or the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) or [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro) to capture the digitized image in an internal frame buffer.</span></span> <span data-ttu-id="5d787-113">Можно закрепить изображение на захваченном образе с помощью \_ \_ кадра захвата WM Cap \_ .</span><span class="sxs-lookup"><span data-stu-id="5d787-113">You can freeze the display on the captured image by using WM\_CAP\_GRAB\_FRAME.</span></span> <span data-ttu-id="5d787-114">В противном случае \_ Используйте \_ \_ неостанавливаться в кадре захвата WM Cap \_ .</span><span class="sxs-lookup"><span data-stu-id="5d787-114">Otherwise, use WM\_CAP\_GRAB\_FRAME\_NOSTOP.</span></span>

<span data-ttu-id="5d787-115">После записи образ можно скопировать для использования другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="5d787-115">Once captured, you can copy the image for use by other applications.</span></span> <span data-ttu-id="5d787-116">Вы можете скопировать изображение из буфера фрейма в буфер обмена с помощью сообщения об [**\_ \_ изменении \_ размера WM Cap**](wm-cap-edit-copy.md) (или макроса [**капедиткопи**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ).</span><span class="sxs-lookup"><span data-stu-id="5d787-116">You can copy an image from the frame buffer to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="5d787-117">Вы также можете скопировать изображение из буфера кадров в растровое изображение, не зависящее от устройства (DIB), с помощью сообщения [](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) саведиб (или макроса капфилесаведиб) с [**\_ закреплениями \_ \_ WM**](wm-cap-file-savedib.md) .</span><span class="sxs-lookup"><span data-stu-id="5d787-117">You can also copy the image from the frame buffer to a device-independent bitmap (DIB) by using the [**WM\_CAP\_FILE\_SAVEDIB**](wm-cap-file-savedib.md) message (or the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro).</span></span>

<span data-ttu-id="5d787-118">Приложение также может использовать два сообщения однокадрового захвата для изменения последовательности кадров или для создания последовательности фотографий со временем длительности.</span><span class="sxs-lookup"><span data-stu-id="5d787-118">Your application can also use the two single-frame capture messages to edit a sequence frame by frame, or to create a time-lapse photography sequence.</span></span>

 

 




