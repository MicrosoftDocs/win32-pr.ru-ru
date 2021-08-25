---
description: 'После начала предварительной версии видеопотока вызовите метод Ивиавидео:: Такепиктуре интерфейса Ивиавидео, чтобы захватить изображение из потокового видео.'
ms.assetid: 2b8c465b-0dbf-4741-a701-200862cc3de3
title: Запись изображения с изображением по-прежнему из потока видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af98dc313ddde7f2da160515ab53d31357a6d9cc96e1737ed01767b40fb0e7c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814284"
---
# <a name="capturing-a-still-image-from-a-video-stream"></a>Запись изображения с изображением по-прежнему из потока видео

После начала предварительной версии видеопотока вызовите метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , чтобы захватить изображение из потокового видео. Инструкции по получению указателя **ивиавидео** и началу просмотра потокового видео см. в разделе [Предварительный просмотр видео](-wia-previewing-video.md).

Когда метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) возвращает значение, параметр *пбстрневимажефиленаме* содержит полный путь и имя файла полученного изображения. Файл имеет формат JPEG. Каталог, в котором создается файл, указывается значением свойства [**ивиавидео:: имажесдиректори**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> Windows получение изображений (WIA) не поддерживает видео-устройства в Windows Server 2003, Windows Vista или более поздней версии. для этих версий Windows используйте [DirectShow](/previous-versions//ms783323(v=vs.85)) для получения изображений из видео.

 

 

 
