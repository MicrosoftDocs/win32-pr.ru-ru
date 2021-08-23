---
description: При рисовании и рисовании используются следующие функции.
ms.assetid: ec18323e-c13b-4328-83bf-9e4ed4a712b8
title: Функции рисования и рисования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a51b8acb0ea187c17d220d80f105ad6ae49371688d4eb8671c2a8eb5949b6e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666624"
---
# <a name="painting-and-drawing-functions"></a>Функции рисования и рисования

При рисовании и рисовании используются следующие функции.



| Функция                                       | Описание                                                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**бегинпаинт**](/windows/desktop/api/Winuser/nf-winuser-beginpaint)               | Подготавливает окно для рисования.                                                                             |
| [**драваниматедректс**](/windows/desktop/api/Winuser/nf-winuser-drawanimatedrects) | Рисует прямоугольник и анимирует его для обозначения активности значка или окна.                                      |
| [**дравкаптион**](/windows/desktop/api/Winuser/nf-winuser-drawcaption)             | Рисует заголовок окна.                                                                                     |
| [**драведже**](/windows/desktop/api/Winuser/nf-winuser-drawedge)                   | Рисует один или несколько краев прямоугольника.                                                                       |
| [**дравфокусрект**](/windows/desktop/api/Winuser/nf-winuser-drawfocusrect)         | Рисует прямоугольник в стиле, который указывает, что прямоугольник имеет фокус.                                  |
| [**дравфрамеконтрол**](/windows/desktop/api/Winuser/nf-winuser-drawframecontrol)   | Рисует элемент управления Frame.                                                                                      |
| [**дравстате**](/windows/desktop/api/Winuser/nf-winuser-drawstatea)                 | Отображает изображение и применяет визуальный эффекты для обозначения состояния.                                          |
| [**дравстатепрок**](/windows/desktop/api/Winuser/nc-winuser-drawstateproc)         | Функция обратного вызова, которая визуализирует сложное изображение для [**дравстате**](/windows/desktop/api/Winuser/nf-winuser-drawstatea).                        |
| [**ендпаинт**](/windows/desktop/api/Winuser/nf-winuser-endpaint)                   | Помечает конец рисования в окне.                                                                      |
| [**ексклудеупдатергн**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn)   | Предотвращает рисование в недопустимых областях окна.                                                          |
| [**гдифлуш**](/windows/desktop/api/Wingdi/nf-wingdi-gdiflush)                   | Очищает текущий пакет вызывающего потока.                                                                 |
| [**гдижетбатчлимит**](/windows/desktop/api/Wingdi/nf-wingdi-gdigetbatchlimit)   | Возвращает максимальное число вызовов функций, которые могут накапливаться в текущем пакете вызывающего потока. |
| [**гдисетбатчлимит**](/windows/desktop/api/Wingdi/nf-wingdi-gdisetbatchlimit)   | Задает максимальное число вызовов функций, которые могут накапливаться в текущем пакете вызывающего потока.    |
| [**жетбкколор**](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor)               | Возвращает цвет фона для контекста устройства.                                                          |
| [**жетбкмоде**](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)                 | Возвращает режим фонового набора для контекста устройства.                                                       |
| [**жетбаундсрект**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect)         | Возвращает накопленный ограничивающий прямоугольник для контекста устройства.                                               |
| [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2)                     | Возвращает режим фонового набора для контекста устройства.                                                           |
| [**жетупдатерект**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect)         | Возвращает координаты наименьшего прямоугольника, охватывающего область обновления окна.                 |
| [**жетупдатергн**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn)           | Возвращает область обновления окна.                                                                         |
| [**жетвиндовдк**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc)             | Возвращает контекст устройства для окна, включая строку заголовка, меню и полосы прокрутки.                          |
| [**жетвиндовргн**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgn)           | Возвращает копию области окна окна.                                                               |
| [**жетвиндовргнбокс**](/windows/desktop/api/Winuser/nf-winuser-getwindowrgnbox)     | Возвращает размеры ограниченного ограничивающего прямоугольника для области окна.                   |
| [**грайстринг**](/windows/desktop/api/Winuser/nf-winuser-graystringa)               | Рисует серый текст в месте расположения.                                                                              |
| [**инвалидатерект**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect)       | Добавляет прямоугольник в область обновления окна.                                                               |
| [**инвалидатергн**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn)         | Делает недействительным клиентскую область в пределах региона.                                                                |
| [**локквиндовупдате**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate)   | Отключает или включает рисование в окне.                                                                    |
| [**аутпутпрок**](/windows/desktop/api/Winuser/nc-winuser-graystringproc)               | Функция обратного вызова, используемая с функцией [**грайстринг**](/windows/desktop/api/Winuser/nf-winuser-graystringa) . Он используется для рисования строки.   |
| [**паинтдесктоп**](/windows/desktop/api/Winuser/nf-winuser-paintdesktop)           | Заполняет область обрезки в контексте устройства шаблоном.                                               |
| [**редраввиндов**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow)           | Обновляет регион в клиентской области окна.                                                                 |
| [**сетбкколор**](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor)               | Задает значение цвета для фона.                                                                       |
| [**сетбкмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode)                 | Задает режим фонового набора для контекста устройства.                                                           |
| [**сетбаундсрект**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect)         | Управляет накоплением сведений об ограничивающем прямоугольнике для контекста устройства.                           |
| [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2)                     | Задает режим фонового набора.                                                                               |
| [**сетвиндовргн**](/windows/desktop/api/Winuser/nf-winuser-setwindowrgn)           | Задает область окна для окна.                                                                         |
| [**упдатевиндов**](/windows/desktop/api/Winuser/nf-winuser-updatewindow)           | Обновляет клиентскую область окна.                                                                        |
| [**валидатерект**](/windows/desktop/api/Winuser/nf-winuser-validaterect)           | Проверяет клиентскую область внутри прямоугольника.                                                               |
| [**валидатергн**](/windows/desktop/api/Winuser/nf-winuser-validatergn)             | Проверяет клиентскую область в пределах региона.                                                                  |
| [**виндовфромдк**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)           | Возвращает маркер окна, связанного с контекстом устройства.                                            |



 

 

 



