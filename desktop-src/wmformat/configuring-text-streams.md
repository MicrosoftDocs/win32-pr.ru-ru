---
title: Настройка текстовых потоков
description: Настройка текстовых потоков
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- потоки, Настройка текстовых потоков
- кодеки, Настройка текстовых потоков
- текстовые потоки, Настройка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486813"
---
# <a name="configuring-text-streams"></a>Настройка текстовых потоков

Текстовые потоки в основном совпадают с пользовательскими произвольными потоками. Нет сведений о конфигурации, связанных с текстовым потоком для определения типа кодировки текста, поэтому объект модуля записи не может проверить образцы.

Чтобы настроить текстовый поток, необходимо убедиться, что структура [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) содержит основной тип носителя вммедиатипе \_ текста. Кроме того, необходимо задать скорость потока и окно буфера для него.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Вычисление скорости потока и значений окна буфера для произвольных потоков**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Общая конфигурация для всех потоков**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Настройка произвольных типов потоков**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Текстовые потоки**](text-streams.md)
</dt> </dl>

 

 




