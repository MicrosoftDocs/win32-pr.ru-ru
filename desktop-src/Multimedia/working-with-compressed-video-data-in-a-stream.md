---
title: Работа с сжатыми данными видео в потоке
description: Работа с сжатыми данными видео в потоке
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069898"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a><span data-ttu-id="fd753-103">Работа с сжатыми данными видео в потоке</span><span class="sxs-lookup"><span data-stu-id="fd753-103">Working with Compressed Video Data in a Stream</span></span>

<span data-ttu-id="fd753-104">Авифиле предоставляет несколько способов доступа к сжатым видеопотокам.</span><span class="sxs-lookup"><span data-stu-id="fd753-104">AVIFile provides several ways for you to access compressed video streams.</span></span>

<span data-ttu-id="fd753-105">Если вы хотите отобразить один или несколько кадров сжатого видеопотока, можно извлечь кадры с помощью функции [**авистреамреад**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) и переслать данные сжатых кадров в функции дравдиб, чтобы отобразить их.</span><span class="sxs-lookup"><span data-stu-id="fd753-105">If you want to display one or more frames of a compressed video stream, you can retrieve the frames by using the [**AVIStreamRead**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) function and forwarding the compressed frame data to DrawDib functions to display them.</span></span> <span data-ttu-id="fd753-106">Функции Дравдиб могут отображать изображения нескольких глубин изображения и автоматически расдизеринг изображений для дисплеев, которые не могут работать с определенными типами изображений, не зависящими от устройства (DIB).</span><span class="sxs-lookup"><span data-stu-id="fd753-106">DrawDib functions can display images of several image depths and automatically dither images for displays that cannot handle certain types of device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="fd753-107">Эти функции работают с несжатыми и сжатыми изображениями.</span><span class="sxs-lookup"><span data-stu-id="fd753-107">These functions work with uncompressed and compressed images.</span></span> <span data-ttu-id="fd753-108">Дополнительные сведения о функциях Дравдиб см. в разделе [функции дравдиб](drawdib-functions.md).</span><span class="sxs-lookup"><span data-stu-id="fd753-108">For more information about DrawDib functions, see [DrawDib Functions](drawdib-functions.md).</span></span>

<span data-ttu-id="fd753-109">Авифиле предоставляет функции для распаковки одного кадра видео.</span><span class="sxs-lookup"><span data-stu-id="fd753-109">AVIFile provides functions for decompressing a single video frame.</span></span> <span data-ttu-id="fd753-110">Чтобы выделить ресурсы, используйте функцию [**авистреамжетфрамеопен**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) .</span><span class="sxs-lookup"><span data-stu-id="fd753-110">To allocate resources, use the [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) function.</span></span> <span data-ttu-id="fd753-111">Эта функция создает буфер для распакованных данных.</span><span class="sxs-lookup"><span data-stu-id="fd753-111">This function creates a buffer for the decompressed data.</span></span>

<span data-ttu-id="fd753-112">Вы можете распаковать один кадр видео с помощью функции [**авистреамжетфраме**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) .</span><span class="sxs-lookup"><span data-stu-id="fd753-112">You can decompress a single video frame by using the [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) function.</span></span> <span data-ttu-id="fd753-113">Эта функция распаковывает кадр и извлекает полный кадр данных изображения, возвращая адрес DIB в структуре [битмапинфохеадер](/previous-versions//ms532290(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fd753-113">This function decompresses the frame and retrieves a complete frame of image data, returning the address of the DIB in the [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) structure.</span></span> <span data-ttu-id="fd753-114">Приложение может отображать DIB с помощью стандартных функций рисования или с помощью функций Дравдиб.</span><span class="sxs-lookup"><span data-stu-id="fd753-114">Your application can display the DIB by using standard drawing functions or by using the DrawDib functions.</span></span>

<span data-ttu-id="fd753-115">Если приложение выполняет последовательные вызовы **авистреамжетфраме**, функция перезаписывает свой буфер в каждый полученный кадр.</span><span class="sxs-lookup"><span data-stu-id="fd753-115">If your application makes successive calls to **AVIStreamGetFrame**, the function overwrites its buffer with each retrieved frame.</span></span>

<span data-ttu-id="fd753-116">После завершения использования **авистреамжетфраме** и распакованного DIB-рисунка в буфер можно освободить выделенные ресурсы с помощью функции [**авистреамжетфрамеклосе**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) .</span><span class="sxs-lookup"><span data-stu-id="fd753-116">When you finish using **AVIStreamGetFrame** and the decompressed DIB is in its buffer, you can release the allocated resources by using the [**AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) function.</span></span>

<span data-ttu-id="fd753-117">Дополнительные сведения о распаковке изображений см. в разделе [Диспетчер сжатия видео](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="fd753-117">For more information about decompressing images, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 