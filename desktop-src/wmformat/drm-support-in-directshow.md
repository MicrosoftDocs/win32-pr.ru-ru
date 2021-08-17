---
title: Поддержка DRM в DirectShow
description: Поддержка DRM в DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Пакет SDK для формата мультимедиа, поддержка DRM в DirectShow
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Windows Пакет SDK для формата мультимедиа, управление цифровыми правами (DRM)
- Расширенный формат систем (ASF), поддержка DRM в DirectShow
- ASF (расширенный формат систем), поддержка DRM в DirectShow
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), управление цифровыми правами (DRM)
- ASF (Расширенный системный формат), управление цифровыми правами (DRM)
- DirectShow, поддержка DRM
- Управление цифровыми правами (DRM), DirectShow
- DRM (Управление цифровыми правами), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930884"
---
# <a name="drm-support-in-directshow"></a>Поддержка DRM в DirectShow

чтение и запись файлов, защищенных с помощью DRM, в DirectShow выполняется по сути так же, как при использовании пакета SDK для формата мультимедиа Windows напрямую. Чтобы начать с, необходима статическая библиотека вмстубдрм, полученная отдельно от корпорации Майкрософт. кроме того, необходимо реализовать интерфейс **икэйпровидер** , чтобы предоставить приложению доступ к объектам времени выполнения пакета SDK Windows Media Format, когда включена поддержка DRM.

При применении защиты DRM версии 1 используйте интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , который получается, как описано в статье [Чтение ASF-файлов в DirectShow](reading-asf-files-in-directshow.md). При применении защиты DRM версии 7 получите интерфейс [**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) , вызвав **QueryService** в фильтре [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано в фрагменте кода далее в этом разделе.

Все остальные настройки, зависящие от DRM, точно такие же, как описано в разделе [Включение поддержки DRM](enabling-drm-support.md). Используйте **QueryService** для получения интерфейса [**Ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) из фильтра [чтения WM ASF](wm-asf-reader-filter.md) .

DirectX 9,0 содержит пример приложения DirectShow player с поддержкой drm, которое демонстрирует получение лицензий drm версии 1 и версии 7. Этот пример также включает реализацию класса **ккэйпровидер** , который поддерживает интерфейс **икэйпровидер** .

 

 




