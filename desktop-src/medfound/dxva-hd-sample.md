---
description: Показывает, как использовать высокое определение (ДКСВА-HD) ускорения видео Microsoft DirectX High Definition.
ms.assetid: dfd5cf5c-7d6e-4894-8d9b-41ef0293b3d3
title: Пример ДКСВА-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ae1945a98bc668aa12cc6cdf8d9e4693cbde27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896570"
---
# <a name="dxva-hd-sample"></a>Пример ДКСВА-HD

Показывает, как использовать высокое определение (ДКСВА-HD) ускорения видео Microsoft DirectX High Definition.

Этот пример по сути является портом [образца DXVA2 \_ видеопрок](dxva2-videoproc-sample.md). Он имеет те же базовые функции, и большинство команд клавиатуры одинаковы.

Пример программно создает видео с первичным потоком и подпотоком. Основной поток отображает SMPTE цветовые полосы. Подпоток смешивается с альфа-смешением в основной поток с помощью ключа яркости. Пользователь может изменить параметры обработки видео, включая плоское значение альфа, прямоугольники источника и назначения, настройки цветов и цветового пространства. На следующем рисунке показано созданное видео.

![снимок экрана с примером дксва-HD](images/dxva-hd-sample.png)

## <a name="apis-demonstrated"></a>Продемонстрированные API

В этом примере демонстрируются следующие интерфейсы ДКСВА-HD:

-   [**\_Устройство идксвахд**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device)
-   [**ИДКСВАХД \_ видеопроцессор**](/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor)

## <a name="requirements"></a>Требования



| Продукт                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Загрузка образца

Этот пример доступен в [репозитории GitHub с классическими примерами Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/DXVA_HD).

## <a name="related-topics"></a>См. также

<dl> <dt>

[ДКСВА-HD](dxva-hd.md)
</dt> <dt>

[Примеры пакетов SDK Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 



