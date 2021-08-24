---
description: Фильтр модуля подготовки MIDI отрисовывает данные MIDI из фильтра средства синтаксического анализа MIDI.
ms.assetid: 2675a21d-41d0-4095-96c4-f12f52c00d5a
title: фильтр модуля подготовки MIDI (Windows. devices. midi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MIDI
api_type:
- HeaderDef
api_location:
- windows.devices.midi.h
ms.openlocfilehash: 3727fb322e03338723eb3c9da1ac86d4e6a7145424cb04b0c050b67f83aa141a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791454"
---
# <a name="midi-renderer-filter"></a>Фильтр модуля подготовки MIDI

Фильтр модуля подготовки MIDI отрисовывает данные MIDI из фильтра [средства синтаксического анализа MIDI](midi-parser-filter.md) .



| Метка | Значение |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра                        | [**Иамклоккславе**](/windows/desktop/api/Strmif/nn-strmif-iamclockslave), [**иамдиректсаунд**](/previous-versions/windows/desktop/api/Amaudio/nn-amaudio-iamdirectsound), [**иамресаурцеконтрол**](/windows/desktop/api/Strmif/nn-strmif-iamresourcecontrol), [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**ибасикаудио**](/windows/desktop/api/Control/nn-control-ibasicaudio), [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) |
| Типы носителей входных закрепления                    | MEDIATYPE \_ MIDI, медиасубтипе \_ null                                                                                                                                                                                                                                                                                                                                                  |
| Интерфейсы входных закрепления                     | [**Имеминпутпин**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**Ипин**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**икуалитиконтрол**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                                                                                                                                                                                               |
| Типы носителей для выходного ПИН-кода                   | Неприменимо                                                                                                                                                                                                                                                                                                                                                                       |
| Интерфейсы выходного ПИН-кода                    | Неприменимо                                                                                                                                                                                                                                                                                                                                                                       |
| Фильтровать CLSID                             | \_АВИМИДИРЕНДЕР CLSID                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID страницы свойств                      | Нет страницы свойств                                                                                                                                                                                                                                                                                                                                                                     |
| Исполняемый объект                               | quartz.dll                                                                                                                                                                                                                                                                                                                                                                           |
| [Заслуживают](merit.md)                       | неуспешный \_ приоритет                                                                                                                                                                                                                                                                                                                                                                     |
| [Категория фильтра](filter-categories.md) | \_МИДИРЕНДЕРЕРКАТЕГОРИ CLSID                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Remarks

GUID для типа формата имеет **значение NULL**, но блок форматирования содержит следующую структуру:


```C++
typedef struct _MIDIFORMAT {
    DWORD       dwDivision;
    DWORD       dwReserved[7];
} MIDIFORMAT, FAR * LPMIDIFORMAT;
```



Элемент **двдивисион** указывает деление времени файла. Деление времени указывается в заголовке любого стандартного файла MIDI (SMF) в `MThd` блоке. Модуль подготовки MIDI задает это свойство в потоке данных MIDI, вызывая функцию **мидистреампроперти** .

Примеры из фильтра средства синтаксического анализа MIDI содержат одну секунду данных MIDI. Модуль подготовки MIDI использует функцию **мидистреамаут** для отображения данных MIDI. Каждый пример представляет собой точку синхронизации: начало буфера содержит все команды, необходимые для задания правильного состояния визуализации буфера.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Windows. devices. midi. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[DirectShow Фильтрующ](directshow-filters.md)
</dt> </dl>

 

 




