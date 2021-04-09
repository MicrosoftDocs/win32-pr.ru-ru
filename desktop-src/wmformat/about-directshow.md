---
title: О программе DirectShow (пакет SDK для формата Windows Media 11)
description: О DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104071005"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>О программе DirectShow (пакет SDK для формата Windows Media 11)

DirectShow — Это высокоуровневая, Модульная и расширяемая архитектура потоковой передачи данных для платформы Windows. Он предоставляет базовые программные компоненты и API-интерфейсы для широкого спектра цифровых аудио-и видеоприложений на рынке. DirectShow доступна в составе пакета средств разработки программного обеспечения Microsoft DirectX. Дополнительные сведения о DirectShow см. в разделе пакет SDK для платформы Microsoft.

В DirectShow все компоненты потоковой передачи данных называются *фильтрами*. Фильтр может представлять устройство, программный кодировщик или декодер, модуль подготовки звука или видео или любую возможность обработки звуковых видео. Чтобы позволить приложениям на основе DirectShow читать и записывать содержимое формата Windows Media, включая содержимое, защищенное цифровыми Rights Management (DRM), корпорация Майкрософт предоставляет два фильтра, которые инкапсулируют части пакета SDK Windows Media Format. Это [средство чтения WM ASF](wm-asf-reader-filter.md) и [модуль записи WM ASF](wm-asf-writer-filter.md). Эти фильтры и интерфейсы, которые они предоставляют, вместе называются компонентами КАСФ после библиотеки DLL, в которой они упакованы. (Q означает Quartz, то есть раннее кодовое имя для DirectShow.)

> [!Note]  
> Использование кодеков Windows Media Audio и Video 9 с помощью компонентов DirectShow КАСФ требует наличия Microsoft Windows Millennium Edition или более поздней версии или DirectX 8,0 или более поздней версии.

 

На следующей схеме показан граф фильтра DirectShow для воспроизведения видеофайлов Windows Media.

![Граф воспроизведения видео Windows Media](images/wmv-wmasfreader.png)

[Модуль чтения WM ASF](wm-asf-reader-filter.md) — это компонент касф, декодеры — это компоненты пакета SDK для Windows Media Format, размещенные в фильтре оболочки DMO (компонент касф), а модули подготовки отчетов — компоненты DirectShow.

 

 




