---
title: DirectShow и Windows Media
description: DirectShow и Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779751"
---
# <a name="directshow-and-windows-media"></a>DirectShow и Windows Media

В качестве альтернативы эксклюзивному использованию пакета SDK формата Windows Media приложения могут также считывать и записывать содержимое Windows Media, используя архитектуру Microsoft® DirectShow® потоковой передачи, как описано в следующих разделах.



| Section                                                                                   | Описание                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [О DirectShow](about-directshow.md)                                                  | Описание DirectShow в общих чертах и сведения о месте получения дополнительных сведений о ней.                                                     |
| [Зачем использовать DirectShow?](why-use-directshow.md)                                             | Описывает, как DirectShow упрощает определенные задачи при создании и воспроизведении содержимого на основе Windows Media.                              |
| [Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)                    | Описывает, как воспроизводить файлы ASF с помощью DirectShow.                                                                                           |
| [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)                  | Описывает создание файлов ASF с помощью DirectShow.                                                                                         |
| [\_Уведомление о событии состояния ВМТ в DirectShow](wmt-status-notification-in-directshow.md) | Описывает, какие события **\_ состояния ВМТ** обрабатываются фильтрами модуля чтения ASF и модулем записи ASF, и как приложения могут получить эти события. |
| [Поддержка DRM в DirectShow](drm-support-in-directshow.md)                                | Описывает чтение и запись защищенных DRM файлов с помощью DirectShow.                                                                     |
| [Справочник по КАСФ DirectShow](directshow-qasf-reference.md)                                | Содержит справочную документацию по компонентам DirectShow, поддерживающим Windows Media.                                              |



 

Три примера приложений в пакете SDK иллюстрируют использование DirectShow: Дскопи, Дсплай и Дссикфм. Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).

> [!Note]  
> Для приложений, использующих компоненты КАСФ, включенные в этот пакет SDK, необходимо установить Microsoft DirectX® 8,1 или более поздней версии пакета SDK для Windows® 2000, Windows 98 и Windows 95 Systems. В частности, эта среда выполнения необходима для фильтра оболочки DMO, который размещает кодеки Windows Media в графе фильтра DirectShow.

 

 

 




