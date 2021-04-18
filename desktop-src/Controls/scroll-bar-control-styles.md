---
title: Стили элемента управления "полоса прокрутки" (Winuser. h)
description: Чтобы создать элемент управления "полоса прокрутки" с помощью функции CreateWindow или CreateWindowEx, укажите класс SCROLLBAR, соответствующие константы стиля окна и сочетание следующих стилей элемента управления "полоса прокрутки".
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657275"
---
# <a name="scroll-bar-control-styles"></a>Стили элемента управления "полоса прокрутки"

Чтобы создать элемент управления "полоса прокрутки" с помощью функции [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) или [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , укажите класс ScrollBar, соответствующие константы стиля окна и сочетание следующих стилей элемента управления "полоса прокрутки". Некоторые стили создают элемент управления "полоса прокрутки", который использует ширину или высоту по умолчанию. Однако при вызове **CreateWindow** или **CreateWindowEx** необходимо всегда указывать координаты x и y и другие измерения полосы прокрутки.



| Константа                                                                                                                                                                                                | Описание                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**SBS \_ боттомалигн**</dt> </dl>                                     | Выровняйте нижнюю границу полосы прокрутки по нижнему краю прямоугольника, определенного параметрами *x*, *y*, *нвидс* и *нхеигхт* функции [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . Высота полосы прокрутки по умолчанию для полос прокрутки системы. Используйте этот стиль в стиле SBS \_ горизонтали.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**SBS \_ горизонтали**</dt> </dl>                                                          | Обозначает горизонтальную полосу прокрутки. Если не указан ни один из \_ стилей SBS боттомалигн и SBS \_ топалигн, то у полосы прокрутки есть высота, ширина и расположение, заданные параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**SBS \_ лефталигн**</dt> </dl>                                           | Выровняйте левый конец полосы прокрутки по левому краю прямоугольника, определенного параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Ширина полосы прокрутки по умолчанию используется для полос прокрутки системы. Используйте этот стиль в стиле по \_ вертикали на SBS.<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**SBS \_ RIGHTALIGN**</dt> </dl>                                        | Выдает правому краю полосы прокрутки по правому краю прямоугольника, определяемого параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Ширина полосы прокрутки по умолчанию используется для полос прокрутки системы. Используйте этот стиль в стиле по \_ вертикали на SBS.<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**SBS \_ сизебокс**</dt> </dl>                                                 | Задает поле размера. Если не указать ни сизебоксботтомригхталигн SBS, \_ ни \_ стиль сизебокстоплефталигн SBS, поле размер будет иметь высоту, ширину и расположение, заданные параметрами *x*, *y*, *нвидс* и *нхеигхт* [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**SBS \_ сизебоксботтомригхталигн**</dt> </dl> | Выровняйте нижний правый угол поля размера с нижним правым углом прямоугольника, заданного параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Поле Размер имеет размер по умолчанию для полей системный размер. Используйте этот стиль в \_ стилях SBS сизебокс или SBS \_ сизегрип.<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**SBS \_ сизебокстоплефталигн**</dt> </dl>             | Выровняйте верхний левый угол поля размера с верхним левым углом прямоугольника, заданного параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Поле Размер имеет размер по умолчанию для полей системный размер. Используйте этот стиль в \_ стилях SBS сизебокс или SBS \_ сизегрип.<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**SBS \_ сизегрип**</dt> </dl>                                              | То же, что и SBS \_ сизебокс, но с порожденным ребром. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**SBS \_ топалигн**</dt> </dl>                                              | Выровняйте верхний край полосы прокрутки по верхнему краю прямоугольника, определенного параметрами *x*, *y*, *нвидс* и *нхеигхт* объекта [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). Высота полосы прокрутки по умолчанию для полос прокрутки системы. Используйте этот стиль в стиле SBS \_ горизонтали.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**SBS по \_ вертикали**</dt> </dl>                                                          | Обозначает вертикальную полосу прокрутки. Если не указать ни RIGHTALIGN SBS \_ , ни \_ стиль лефталигн SBS, полоса прокрутки будет иметь высоту, ширину и расположение, заданные параметрами *x*, *y*, *нвидс* и *нхеигхт* [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                     |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

