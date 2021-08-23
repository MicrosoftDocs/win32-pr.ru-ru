---
title: DirectShow и Windows носитель
description: DirectShow и Windows носитель
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- DirectShow, о программе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027912"
---
# <a name="directshow-and-windows-media"></a>DirectShow и Windows носитель

в качестве альтернативы использованию пакета SDK для Windowsного формата мультимедиа приложения также могут считывать и записывать Windows содержимое на основе мультимедиа с помощью архитектуры Microsoft® DirectShow® потоковой передачи, как описано в следующих разделах.



| Section                                                                                   | Описание                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [О DirectShow](about-directshow.md)                                                  | описывает DirectShow в общих условиях и указывает, где можно получить дополнительные сведения о ней.                                                     |
| [Зачем использовать DirectShow?](why-use-directshow.md)                                             | описывает, как DirectShow упрощает выполнение определенных задач при создании и воспроизведении Windows содержимого на основе мультимедиа.                              |
| [Чтение файлов ASF в DirectShow](reading-asf-files-in-directshow.md)                    | Описание воспроизведения файлов ASF с помощью DirectShow.                                                                                           |
| [Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md)                  | Описание создания файлов ASF с помощью DirectShow.                                                                                         |
| [\_Уведомление о событии состояния ВМТ в DirectShow](wmt-status-notification-in-directshow.md) | Описывает, какие события **\_ состояния ВМТ** обрабатываются фильтрами модуля чтения ASF и модулем записи ASF, и как приложения могут получить эти события. |
| [Поддержка DRM в DirectShow](drm-support-in-directshow.md)                                | Описание процесса чтения и записи файлов с защитой DRM с помощью DirectShow.                                                                     |
| [DirectShow Справочник по КАСФ](directshow-qasf-reference.md)                                | содержит справочную документацию по компонентам DirectShow, поддерживающим Windows мультимедиа.                                              |



 

три примера приложений в пакете SDK иллюстрируют использование DirectShow: дскопи, дсплай и дссикфм. Дополнительные сведения см. в разделе [примеры приложений](sample-applications.md).

> [!Note]  
> для приложений, использующих компоненты касф, включенные в этот пакет sdk, необходимо установить среду выполнения SDK Microsoft DirectX® 8,1 или более поздней версии на Windows® 2000, Windows 98 и Windows 95 systems. в частности, эта среда выполнения необходима для фильтра оболочки DMO, в котором размещаются кодеки Windows Media в графе фильтра DirectShow.

 

 

 




