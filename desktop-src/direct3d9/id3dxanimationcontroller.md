---
description: Этот интерфейс используется для управления возможностями анимации, подключения наборов анимации к анимированным кадрам преобразования.
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: Интерфейс ID3DXAnimationController (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703866"
---
# <a name="id3dxanimationcontroller-interface"></a>Интерфейс ID3DXAnimationController

Этот интерфейс используется для управления возможностями анимации, подключения наборов анимации к анимированным кадрам преобразования. Интерфейс содержит методы для смешивания нескольких анимаций и изменения параметров смешения с течением времени для обеспечения плавного перехода и других эффектов.

## <a name="members"></a>Элементы

Интерфейс **ID3DXAnimationController** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationController** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXAnimationController** содержит следующие методы.



| Метод                                                                                   | Описание                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | Выполняет анимацию сетки и перемещает глобальное время анимации на заданный объем.<br/>                                                              |
| [**клонеаниматионконтроллер**](id3dxanimationcontroller--cloneanimationcontroller.md)   | Выполняет клонирование или копирование контроллера анимации.<br/>                                                                                                  |
| [**Animation**](id3dxanimationcontroller--getanimationset.md)                     | Возвращает набор анимации.<br/>                                                                                                                       |
| [**жетаниматионсетбинаме**](id3dxanimationcontroller--getanimationsetbyname.md)         | Возвращает набор анимации по его имени.<br/>                                                                                                       |
| [**жеткуррентприоритибленд**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | Возвращает маркер события для события приоритета Blend, выполняющегося в данный момент.<br/>                                                                 |
| [**жеткурренттраккевент**](id3dxanimationcontroller--getcurrenttrackevent.md)           | Возвращает обработчик событий для события, которое в данный момент выполняется в указанной дорожке анимации.<br/>                                                     |
| [**жетевентдеск**](id3dxanimationcontroller--geteventdesc.md)                           | Возвращает описание указанного события анимации.<br/>                                                                                           |
| [**жетмакснуманиматионаутпутс**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | Получение максимального количества выходных данных анимации, которые может поддерживать контроллер анимации.<br/>                                                            |
| [**жетмакснуманиматионсетс**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | Возвращает максимальное число наборов анимации, которое может поддерживать контроллер анимации.<br/>                                                              |
| [**жетмакснумевентс**](id3dxanimationcontroller--getmaxnumevents.md)                     | Возвращает максимальное число событий, которое может поддерживать контроллер анимации.<br/>                                                                      |
| [**жетмакснумтраккс**](id3dxanimationcontroller--getmaxnumtracks.md)                     | Возвращает максимальное число дорожек в контроллере анимации.<br/>                                                                               |
| [**жетнуманиматионсетс**](id3dxanimationcontroller--getnumanimationsets.md)             | Возвращает число наборов анимации, зарегистрированных в данный момент в контроллере анимации.<br/>                                                       |
| [**жетприоритибленд**](id3dxanimationcontroller--getpriorityblend.md)                   | Получает текущий приоритет смешения цветов, используемый контроллером анимации.<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | Возвращает глобальное время анимации.<br/>                                                                                                              |
| [**жеттракканиматионсет**](id3dxanimationcontroller--gettrackanimationset.md)           | Возвращает набор анимации для данной записи.<br/>                                                                                                  |
| [**жеттраккдеск**](id3dxanimationcontroller--gettrackdesc.md)                           | Возвращает описание записи.<br/>                                                                                                                  |
| [**жетупкомингприоритибленд**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | Возвращает обработчик события для следующего приоритетного события Blend, которое было запланировано после указанного события.<br/>                                         |
| [**жетупкомингтраккевент**](id3dxanimationcontroller--getupcomingtrackevent.md)         | Возвращает обработчик события для следующего события, запланированного на выполнение после указанного события в дорожке анимации.<br/>                                  |
| [**кэйприоритибленд**](id3dxanimationcontroller--keypriorityblend.md)                   | Задает смешение ключей событий для указанной записи анимации.<br/>                                                                                  |
| [**кэйтраккенабле**](id3dxanimationcontroller--keytrackenable.md)                       | Задает ключ события, который включает или отключает запись анимации.<br/>                                                                               |
| [**кэйтраккпоситион**](id3dxanimationcontroller--keytrackposition.md)                   | Задает ключ события, который изменяет местное время анимации.<br/>                                                                         |
| [**кэйтраккспид**](id3dxanimationcontroller--keytrackspeed.md)                         | Задает ключ события, который изменяет частоту воспроизведения анимированной записи.<br/>                                                                       |
| [**кэйтракквеигхт**](id3dxanimationcontroller--keytrackweight.md)                       | Задает ключ события, который изменяет вес анимированной анимации. Вес используется как множитель при объединении нескольких дорожек.<br/> |
| [**регистераниматионаутпут**](id3dxanimationcontroller--registeranimationoutput.md)     | Добавляет выходные данные анимации в контроллер анимации и регистрирует указатели для преобразований масштабирования, вращения и преобразования (SRT).<br/>          |
| [**регистераниматионсет**](id3dxanimationcontroller--registeranimationset.md)           | Добавляет набор эффектов анимации к контроллеру анимации.<br/>                                                                                           |
| [**ресеттиме**](id3dxanimationcontroller--resettime.md)                                 | Сбрасывает глобальное время анимации в ноль. Все события, ожидающие обработки, сохраняют свои исходные расписания, но в новом периоде времени.<br/>                 |
| [**сетприоритибленд**](id3dxanimationcontroller--setpriorityblend.md)                   | Задает весовой коэффициент смешения, используемый контроллером анимации.<br/>                                                                          |
| [**сеттракканиматионсет**](id3dxanimationcontroller--settrackanimationset.md)           | Применяет набор анимации к указанной дорожке.<br/>                                                                                            |
| [**сеттраккдеск**](id3dxanimationcontroller--settrackdesc.md)                           | Задает описание записи.<br/>                                                                                                                  |
| [**сеттраккенабле**](id3dxanimationcontroller--settrackenable.md)                       | Включает или отключает запись в контроллере анимации.<br/>                                                                                     |
| [**сеттраккпоситион**](id3dxanimationcontroller--settrackposition.md)                   | Задает для трассировки указанное время локальной анимации.<br/>                                                                                        |
| [**сеттраккприорити**](id3dxanimationcontroller--settrackpriority.md)                   | Задает приоритет смешивания для указанного направления анимации.<br/>                                                                         |
| [**сеттраккспид**](id3dxanimationcontroller--settrackspeed.md)                         | Задает скорость записи. Скорость записи аналогична множителю, который используется для ускорения или снижения скорости воспроизведения.<br/>            |
| [**сеттракквеигхт**](id3dxanimationcontroller--settrackweight.md)                       | Задает вес записи. Вес используется для определения способа смешения нескольких дорожек.<br/>                                                |
| [**ункэйаллприоритиблендс**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | Удаляет все события с запланированным приоритетом перехода с контроллера анимации.<br/>                                                                   |
| [**ункэйаллтраккевентс**](id3dxanimationcontroller--unkeyalltrackevents.md)             | Удаляет все события из указанной записи анимации.<br/>                                                                                         |
| [**ункэйевент**](id3dxanimationcontroller--unkeyevent.md)                               | Удаляет указанное событие из записи анимации, предотвращая выполнение события.<br/>                                                    |
| [**унрегистераниматионсет**](id3dxanimationcontroller--unregisteranimationset.md)       | Удаляет набор эффектов анимации из контроллера анимации.<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | Проверяет, является ли указанный обработчик событий допустимым, а событие анимации еще не завершено.<br/>                                              |



 

## <a name="remarks"></a>Комментарии

Создание объекта контроллера анимации с помощью [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md).

Тип LPD3DXANIMATIONCONTROLLER определяется как указатель на интерфейс **ID3DXAnimationController** .


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



Тип D3DXEVENTHANDLE определяется как обработчик событий для событий контроллера анимации.


```
typedef DWORD D3DXEVENTHANDLE;
```



Тип LPD3DXEVENTHANDLE определяется как указатель на обработчик событий для событий контроллера анимации.


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
