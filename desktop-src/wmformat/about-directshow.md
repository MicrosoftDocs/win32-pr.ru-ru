---
title: узнайте о DirectShow в пакете SDK для Windows Media Format 11 — высокоуровневой, модульной, расширяемой и потоковой передачи данных для Windowsной платформы.
description: О DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840418"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>сведения о DirectShow (пакет SDK для Windows Media Format 11)

DirectShow — это высокоуровневая, модульная, расширяемая архитектура потоковой передачи данных для Windowsной платформы. Он предоставляет базовые программные компоненты и API-интерфейсы для широкого спектра цифровых аудио-и видеоприложений на рынке. DirectShow доступен в составе пакета средств разработки программного обеспечения Microsoft DirectX. дополнительные сведения о DirectShow см. в разделе пакет SDK для платформы Microsoft.

в DirectShow все компоненты потоковой передачи данных называются *фильтрами*. Фильтр может представлять устройство, программный кодировщик или декодер, модуль подготовки звука или видео или любую возможность обработки звуковых видео. чтобы разрешить приложениям на основе DirectShow чтение и запись содержимого Windowsного формата мультимедиа, включая содержимое, защищенное цифровыми Rights Management (DRM), корпорация майкрософт предоставляет два фильтра, которые инкапсулируют части пакета SDK Windowsного формата мультимедиа. Это [средство чтения WM ASF](wm-asf-reader-filter.md) и [модуль записи WM ASF](wm-asf-writer-filter.md). Эти фильтры и интерфейсы, которые они предоставляют, вместе называются компонентами КАСФ после библиотеки DLL, в которой они упакованы. (Q означает Quartz, раннее кодовое имя для DirectShow.)

> [!Note]  
> для использования кодеков Windows Media Audio и Video 9 с помощью компонентов DirectShow касф требуется Microsoft Windows Millennium Edition или более поздней версии или DirectX 8,0 или более поздней версии.

 

на следующей диаграмме показана DirectShow диаграмма фильтра для воспроизведения видеофайлов Windows мультимедиа.

![Граф воспроизведения видео Windows Media](images/wmv-wmasfreader.png)

[модуль чтения WM ASF](wm-asf-reader-filter.md) — это компонент касф, декодеры Windows компоненты пакета SDK для формата носителя, размещенные в DMOном фильтре (компоненте касф), а модули подготовки отчетов — DirectShow компоненты.

 

 




