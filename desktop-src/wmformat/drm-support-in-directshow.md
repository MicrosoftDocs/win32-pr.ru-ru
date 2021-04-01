---
title: Поддержка DRM в DirectShow
description: Поддержка DRM в DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media Format SDK, поддержка DRM в DirectShow
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, управление цифровыми правами (DRM)
- Расширенный формат систем (ASF), поддержка DRM в DirectShow
- ASF (расширенный формат систем), поддержка DRM в DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), управление цифровыми правами (DRM)
- ASF (Расширенный системный формат), управление цифровыми правами (DRM)
- DirectShow, поддержка DRM
- Управление цифровыми правами (DRM), DirectShow
- DRM (Управление цифровыми правами), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987183"
---
# <a name="drm-support-in-directshow"></a>Поддержка DRM в DirectShow

Чтение и запись файлов, защищенных с помощью DRM, в DirectShow выполняется по сути так же, как при использовании пакета SDK формата Windows Media. Чтобы начать с, необходима статическая библиотека вмстубдрм, полученная отдельно от корпорации Майкрософт. Кроме того, необходимо реализовать интерфейс **икэйпровидер** , чтобы предоставить приложению доступ к объектам времени выполнения пакета SDK Windows Media Format, когда включена поддержка DRM.

При применении защиты DRM версии 1 используйте интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , который получается, как описано в статье [Чтение ASF-файлов в DirectShow](reading-asf-files-in-directshow.md). При применении защиты DRM версии 7 получите интерфейс [**ивмдрмвритер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) , вызвав **QueryService** в фильтре [модуля записи WM ASF](wm-asf-writer-filter.md) , как показано в фрагменте кода далее в этом разделе.

Все остальные настройки, зависящие от DRM, точно такие же, как описано в разделе [Включение поддержки DRM](enabling-drm-support.md). Используйте **QueryService** для получения интерфейса [**Ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) из фильтра [чтения WM ASF](wm-asf-reader-filter.md) .

DirectX 9,0 содержит образец, Плайвндасф, приложение DirectShow, поддерживающее DRM, которое демонстрирует получение лицензий DRM версии 1 и версии 7. Этот пример также включает реализацию класса **ккэйпровидер** , который поддерживает интерфейс **икэйпровидер** .

 

 




