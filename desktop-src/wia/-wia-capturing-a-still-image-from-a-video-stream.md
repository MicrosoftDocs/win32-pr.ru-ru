---
description: 'После начала предварительной версии видеопотока вызовите метод Ивиавидео:: Такепиктуре интерфейса Ивиавидео, чтобы захватить изображение из потокового видео.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Запись изображения с изображением по-прежнему из потока видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be475405f4aa9719514a531a6af0105d7a786f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264535"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a><span data-ttu-id="70d40-103">Запись изображения с изображением по-прежнему из потока видео</span><span class="sxs-lookup"><span data-stu-id="70d40-103">Capturing a Still Image from a Video Stream</span></span>

<span data-ttu-id="70d40-104">После начала предварительной версии видеопотока вызовите метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , чтобы захватить изображение из потокового видео.</span><span class="sxs-lookup"><span data-stu-id="70d40-104">After beginning preview of a video stream, call the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface to capture a still image from the streaming video.</span></span> <span data-ttu-id="70d40-105">Инструкции по получению указателя **ивиавидео** и началу просмотра потокового видео см. в разделе [Предварительный просмотр видео](-wia-previewing-video.md).</span><span class="sxs-lookup"><span data-stu-id="70d40-105">For instructions on how to get an **IWiaVideo** pointer and begin previewing streaming video, see [Previewing Video](-wia-previewing-video.md).</span></span>

<span data-ttu-id="70d40-106">Когда метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) возвращает значение, параметр *пбстрневимажефиленаме* содержит полный путь и имя файла полученного изображения.</span><span class="sxs-lookup"><span data-stu-id="70d40-106">When the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method returns, the *pbstrNewImageFilename* parameter contains the full path and filename of the resulting image file.</span></span> <span data-ttu-id="70d40-107">Файл имеет формат JPEG.</span><span class="sxs-lookup"><span data-stu-id="70d40-107">The file is in JPEG format.</span></span> <span data-ttu-id="70d40-108">Каталог, в котором создается файл, указывается значением свойства [**ивиавидео:: имажесдиректори**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .</span><span class="sxs-lookup"><span data-stu-id="70d40-108">The directory in which the file is created is specified by the value of the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property of the [**IWiaVideo**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) interface.</span></span>

> [!Note]  
> <span data-ttu-id="70d40-109">Получение образа Windows (WIA) не поддерживает видеоустройства в Windows Server 2003, Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="70d40-109">Windows Image Acquisition (WIA) does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="70d40-110">Для этих версий Windows используйте [DirectShow](/previous-versions//ms783323(v=vs.85)) для получения изображений из видео.</span><span class="sxs-lookup"><span data-stu-id="70d40-110">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

 

 
