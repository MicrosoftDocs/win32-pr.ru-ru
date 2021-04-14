---
title: Диалоговые окна видео
description: Диалоговые окна видео
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Сообщение WM_CAP_DLG_VIDEOSOURCE
- макрос Капдлгвидеосаурце
- Сообщение WM_CAP_DLG_VIDEOFORMAT
- макрос Капдлгвидеоформат
- Сообщение WM_CAP_DLG_VIDEODISPLAY
- макрос Капдлгвидеодисплай
- Сообщение WM_CAP_DLG_VIDEOCOMPRESSION
- макрос Капдлгвидеокомпрессион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661517"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="b4c41-111">Диалоговые окна видео</span><span class="sxs-lookup"><span data-stu-id="b4c41-111">Video Dialog Boxes</span></span>

<span data-ttu-id="b4c41-112">Каждый драйвер записи может предоставить до четырех диалоговых окон для управления аспектами обработки разрядов и отслеживания видео, а также для определения атрибутов сжатия, используемых при уменьшении размера данных видео.</span><span class="sxs-lookup"><span data-stu-id="b4c41-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="b4c41-113">Содержимое этих диалоговых окон определяется драйвером видеозаписи.</span><span class="sxs-lookup"><span data-stu-id="b4c41-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="b4c41-114">Диалоговое окно Источник видео управляет выбором каналов входного видео и параметрами, влияющими на видеоизображение, которое следует расформатировать в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="b4c41-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="b4c41-115">В этом диалоговом окне перечисляются типы сигналов, соединяющие источник видео с картой захвата (обычно СВХС и составные входные данные), и предоставляет элементы управления для изменения оттенка, контраста или насыщенности.</span><span class="sxs-lookup"><span data-stu-id="b4c41-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="b4c41-116">Если диалоговое окно поддерживается драйвером видеозаписи, его можно отобразить и обновить с помощью сообщения [**WM \_ \_ \_ видеосаурце DLG**](wm-cap-dlg-videosource.md) (или макроса [**капдлгвидеосаурце**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).</span><span class="sxs-lookup"><span data-stu-id="b4c41-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="b4c41-117">Диалоговое окно Формат видео управляет выделением цифровых размеров видеокадра, а также параметров сжатия для захваченного видео.</span><span class="sxs-lookup"><span data-stu-id="b4c41-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="b4c41-118">Если диалоговое окно поддерживается драйвером видеозаписи, его можно отобразить и обновить с помощью сообщения [**WM \_ \_ \_ видеоформат DLG**](wm-cap-dlg-videoformat.md) (или макроса [**капдлгвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).</span><span class="sxs-lookup"><span data-stu-id="b4c41-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="b4c41-119">Диалоговое окно отображения видео управляет отображением видео на мониторе во время записи.</span><span class="sxs-lookup"><span data-stu-id="b4c41-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="b4c41-120">Элементы управления в этом диалоговом окне не влияют на Оцифрованные видеоданные, но могут повлиять на представление оцифрованного сигнала.</span><span class="sxs-lookup"><span data-stu-id="b4c41-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="b4c41-121">Например, устройства записи, поддерживающие наложение, могут допускать изменение тона и насыщенности, цвет ключа или выравнивание наложения.</span><span class="sxs-lookup"><span data-stu-id="b4c41-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="b4c41-122">Если диалоговое окно поддерживается драйвером видеозаписи, его можно отобразить и обновить с помощью сообщения [**WM \_ \_ \_ видеодисплай DLG**](wm-cap-dlg-videodisplay.md) (или макроса [**капдлгвидеодисплай**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).</span><span class="sxs-lookup"><span data-stu-id="b4c41-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="b4c41-123">Диалоговое окно «сжатие видео» управляет атрибутами сжатия видео после записи.</span><span class="sxs-lookup"><span data-stu-id="b4c41-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="b4c41-124">Если диалоговое окно поддерживается драйвером видеозаписи, его можно отобразить и обновить с помощью сообщения [**WM \_ \_ \_ видеокомпрессион DLG**](wm-cap-dlg-videocompression.md) (или макроса [**капдлгвидеокомпрессион**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).</span><span class="sxs-lookup"><span data-stu-id="b4c41-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




