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
# <a name="capturing-a-still-image-from-a-video-stream"></a>Запись изображения с изображением по-прежнему из потока видео

После начала предварительной версии видеопотока вызовите метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , чтобы захватить изображение из потокового видео. Инструкции по получению указателя **ивиавидео** и началу просмотра потокового видео см. в разделе [Предварительный просмотр видео](-wia-previewing-video.md).

Когда метод [**ивиавидео:: такепиктуре**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) возвращает значение, параметр *пбстрневимажефиленаме* содержит полный путь и имя файла полученного изображения. Файл имеет формат JPEG. Каталог, в котором создается файл, указывается значением свойства [**ивиавидео:: имажесдиректори**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .

> [!Note]  
> Получение образа Windows (WIA) не поддерживает видеоустройства в Windows Server 2003, Windows Vista и более поздних версиях. Для этих версий Windows используйте [DirectShow](/previous-versions//ms783323(v=vs.85)) для получения изображений из видео.

 

 

 
