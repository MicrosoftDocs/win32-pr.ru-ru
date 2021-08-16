---
description: Интерфейсы аудиозаписи и подготовки к просмотру
ms.assetid: 79b42ffd-703a-4a7c-bb2d-5cfc2fbeb16c
title: Интерфейсы аудиозаписи и подготовки к просмотру
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ffdf586ec8566abddadcb0b7109680664963a63071472a3ac7aa895981e643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824254"
---
# <a name="audio-capture-and-rendering-interfaces"></a>Интерфейсы аудиозаписи и подготовки к просмотру

Эти интерфейсы поддерживают запись звука и отрисовку в DirectShow



| Интерфейс                                              | Описание                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иамаудиоинпутмиксер**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer)       | Получите доступ к аналоговым входным данным на звуковой плате системы и настройте такие характеристики, как моно или стерео, уровень Mix, уровень панорамы, громкость, частота высоких частот и низкие значения. |
| [**иамаудиорендерерстатс**](/windows/desktop/api/Strmif/nn-strmif-iamaudiorendererstats) | Получение статистических сведений о производительности аудио рендереринг.                                                                                          |
| [**иамбуффернеготиатион**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)   | Управление тем, как фильтр записи звука выделяет буферы.                                                                                                   |
| [**иамклоккславе**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave)                 | Контролируйте допуск модуля подготовки звука, если он соответствует тарифам с другими часами.                                                                      |
| [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound)               | Позволяет приложению указать, какое окно имеет фокус для управления воспроизведением звука DirectSound.                                                      |
| [**иамресаурцеконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol)       | Держите ресурс звукового устройства, прежде чем он понадобится.                                                                                                        |
| [**иамстреамконфиг**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)             | Запросите и задайте формат вывода фильтра записи.                                                                                                         |
| [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio)                     | Задайте громкость звукового выхода и баланс.                                                                                                                      |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Интерфейсы](interfaces.md)
</dt> </dl>

 

 



