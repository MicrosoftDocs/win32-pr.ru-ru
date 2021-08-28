---
description: Контакты порта видео в записи файлов
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Контакты порта видео в записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049384"
---
# <a name="video-port-pins-in-file-capture"></a>Контакты порта видео в записи файлов

Если устройство записи имеет порт видео, то ПИН-код видеопорта должен быть подключен к модулю обработки видео, даже если требуется только запись в файл.

если вы вызываете [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) со значением **\_ \_ запись категории пин-кода** , а устройство имеет пин-код видеопорта, Graph построитель записи автоматически подключает пин-код видеопорта к [наложение Mixer](overlay-mixer-filter.md) фильтр и подключает Mixer наложения к модулю визуализации видео. построитель Graph захвата скрывает окно видео, вызывая [**ивидеовиндов::p ut \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) со значением **оафалсе**. если позже приложение вызывает **RenderStream** с **\_ \_ предварительной версией категории пин-кода**, для отображения видеоокна в построителе Graph построитель вызовов **поместит функцию \_ автоотображения** со значением **оатруе**.

после вызова **RenderStream** с **\_ \_ захватом категории пин-кода** можно проверить, добавлен ли модуль подготовки видео, выполнив запрос фильтра Graph Manager для интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Запись видео в файл](capturing-video-to-a-file.md)
</dt> </dl>

 

 



