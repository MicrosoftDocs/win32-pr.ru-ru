---
description: Записать DV в файл
ms.assetid: f7a8bcbb-a744-43c4-a226-354ae2d94df8
title: Записать DV в файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 713e49eba3016b353362c541ba31ffd6a1ae5de7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341915"
---
# <a name="capture-dv-to-file"></a>Записать DV в файл

В этом разделе описывается запись цифрового видео (DV) с цифровой камеры или с ленты Втр.

1.  Создайте экземпляр фильтра [драйвера мсдв](msdv-driver.md) . Дополнительные сведения см. [в разделе Выбор устройства записи](selecting-a-capture-device.md).
2.  Инициализируйте построитель диаграмм записи, как описано в разделе [о построителе диаграмм записи](about-the-capture-graph-builder.md).
3.  Создайте граф записи в зависимости от типа целевого файла:
    -   [Запись файла DV типа 1](capture-a-type-1-dv-file.md)
    -   [Запись файла DV типа 2](capture-a-type-2-dv-file.md)
    -   [Записать DV в Распакованный RGB](capture-dv-to-uncompressed-rgb.md)
4.  Запустите граф.

Захват с ленты Втр работает так же, как запись живого видео с камеры, за исключением того, что необходимо воспроизвести ленту, как описано в разделе [Управление](controlling-a-dv-camcorder.md)видеокамерой. Чтобы избежать потери кадров, сначала запустите граф, а затем воспроизводите ленту. Когда передача завершится, сначала завершите ленту, а затем закройте граф.

> [!Note]  
> Видеокамера должна быть в режиме Втр. См. раздел [режим устройства](device-mode.md).

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровое видео в DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Файлы видео AVI типа-1 и Type-2](type-1-vs--type-2-dv-avi-files.md)
</dt> <dt>

[Видеозапись](video-capture.md)
</dt> </dl>

 

 



