---
description: Интерфейс Ивиавидео позволяет приложению просматривать видео и записывать все изображения из него.
ms.assetid: 59eddbdc-4957-44be-a602-0763f3385e89
title: Предварительный просмотр видео (WIA)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 935625c1c16ceea66326963185dd75d96d98ed02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541930"
---
# <a name="previewing-video-wia"></a>Предварительный просмотр видео (WIA)

Интерфейс [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) позволяет приложению просматривать видео и записывать все изображения из него. Чтобы выбрать устройство потоковой передачи и отобразить видеопоток в окне, выполните следующие действия.

-   Вызовите [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения указателя на интерфейс [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) .
-   Используйте метод [**ивиадевмгр:: енумдевицеинфо**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) интерфейса [**ивиадевмгр**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) , чтобы получить указатель на интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . Инструкции по перечислению устройств см. в разделе Перечисление системных устройств.
-   Используйте интерфейс [**иенумвиа \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) для получения указателя на интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для каждого найденного устройства Windows Image (WIA).
-   Используйте интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) для получения свойства DeviceID нужного устройства. Для потокового видеоустройства установлен флаг Стидевицетипестреамингвидео для \_ \_ свойства типа dev-файла WIA \_ .
-   Используйте интерфейс [**ивиапропертистораже**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) , чтобы получить \_ \_ значение свойства каталога WIA ДПВ Images \_ .
-   Вызовите [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения указателя на интерфейс [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) .
-   Задайте для свойства [**ивиавидео:: имажесдиректори**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) интерфейса [**ивиавидео**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) значение, полученное из \_ \_ \_ значения свойства каталога WIA ДПВ Images.
-   Вызовите [**ивиавидео:: креатевидеобивиадевид**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-createvideobywiadevid) в интерфейсе [**ИВИАВИДЕО**](/windows/desktop/api/Wiavideo/nn-wiavideo-iwiavideo) , передав идентификатор устройства потокового изображения и маркер окна, в котором отображается видео.

> [!Note]  
> WIA не поддерживает видео устройства в Windows Server 2003, Windows Vista и более поздних версиях. Для этих версий Windows используйте [DirectShow](/previous-versions//ms783323(v=vs.85)) для получения изображений из видео.

 

 

 
