---
description: Контакты порта видео в записи файлов
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Контакты порта видео в записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673447"
---
# <a name="video-port-pins-in-file-capture"></a>Контакты порта видео в записи файлов

Если устройство записи имеет порт видео, то ПИН-код видеопорта должен быть подключен к модулю обработки видео, даже если требуется только запись в файл.

Если вы вызываете [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) со значением **\_ \_ запись категории ПИН-кода** , а устройство имеет ПИН-код видеопорта, то построитель диаграмм автоматически подключает ПИН-код видеопорта к фильтру [микшера наложения](overlay-mixer-filter.md) и подключает микшер наложения к модулю визуализации видео. Построитель графа записи скрывает окно видео, вызывая [**ивидеовиндов::p UT \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) со значением **оафалсе**. Если позже приложение вызывает **RenderStream** с **\_ \_ предварительной версией категории ПИН-кода**, построитель диаграмм выполнит вызов **поместит \_ Автоотображение** со значением **оатруе**, чтобы отобразить окно видео.

После вызова **RenderStream** с **\_ \_ захватом категории ПИН-кода** можно проверить, добавлен ли модуль подготовки видео, выполнив запрос к диспетчеру графа фильтра для интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



