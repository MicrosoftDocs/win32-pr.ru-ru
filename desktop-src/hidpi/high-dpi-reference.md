---
title: Ссылка High DPI
description: Ссылка High DPI
ms.assetid: 07A2D45E-721C-4DA8-82A5-38B2FB94BC6D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9c6a9302541683dbf97c06194285f9e8cfcf3c0
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118419"
---
# <a name="high-dpi-reference"></a>Ссылка High DPI

## <a name="functions"></a>Функции



| Раздел                                                                                         |Описание                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аджуствиндовректексфордпи**](/windows/desktop/api/Winuser/nf-winuser-adjustwindowrectexfordpi)                             | Вариант [аджуствиндовректекс](/windows/desktop/api/winuser/nf-winuser-adjustwindowrectex) , возвращающий значения, масштабируемые до определенного dpi.       |
| [**аредпиаваренессконтекстсекуал**](/windows/desktop/api/Winuser/nf-winuser-aredpiawarenesscontextsequal)                     | Определяет, эквивалентны ли два значения [**\_ \_ контекста, осведомленности о dpi**](dpi-awareness-context.md) .                                                            |
| [**енабленонклиентдпискалинг**](/windows/desktop/api/Winuser/nf-winuser-enablenonclientdpiscaling)                           | Включает автоматическое масштабирование неклиентской области указанного окна верхнего уровня.                                                                               |
| [**жетаваренессфромдпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-getawarenessfromdpiawarenesscontext)       | Возвращает значение [**определения \_ количества точек на дюйм**](/windows/desktop/api/windef/ne-windef-dpi_awareness) из [**\_ \_ контекста, осведомленного о dpi**](dpi-awareness-context.md)                                       |
| [**жетдпиформонитор**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)                                             | Запрашивает сведения о DPI, связанные с монитором.                                                                                                            |
| [**жетдпифорсистем**](/windows/desktop/api/Winuser/nf-winuser-getdpiforsystem)                                               | Возвращает значение DPI системы.                                                                                                                                           |
| [**жетдпифорвиндов**](/windows/desktop/api/Winuser/nf-winuser-getdpiforwindow)                                               | Возвращает текущее значение DPI для указанного окна.                                                                                                                 |
| [**жетпроцессдпиаваренесс**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)                                 | Возвращает режим виртуализации с разрешением указанного процесса.                                                                                                   |
| [**жетсистемметриксфордпи**](/windows/desktop/api/Winuser/nf-winuser-getsystemmetricsfordpi)                                 | Вариант [жетсистемметрикс](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) , возвращающий значения, масштабируемые до определенного dpi.         |
| [**жетсреаддпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-getthreaddpiawarenesscontext)                     | Возвращает контекст осведомленности об активных точках на дюйм для текущего потока.                                                                                                |
| [**жетвиндовдпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-getwindowdpiawarenesscontext)                     | Возвращает контекст осведомленности о DPI для окна.                                                                                                                 |
| [**исвалиддпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-isvaliddpiawarenesscontext)                         | Определяет, является [**ли \_ \_ контекст, осведомленный о dpi**](dpi-awareness-context.md) , допустимым и поддерживаемым текущей системой.                                            |
| [**логикалтофисикалпоинтфорпермонитордпи**](/windows/desktop/api/winuser/nf-winuser-logicaltophysicalpointforpermonitordpi) | Преобразует точку в окне из логических координат в физические координаты, независимо от осведомленности о DPI вызывающего объекта.                                   |
| [**фисикалтологикалпоинтфорпермонитордпи**](/windows/desktop/api/winuser/nf-winuser-physicaltologicalpointforpermonitordpi) | Преобразует точку в окне из физических координат в логические, независимо от осведомленности о DPI вызывающего объекта.                                   |
| [**сетпроцессдпиаваренесс**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)                                 | Задает режим виртуализации DPI для текущего процесса.                                                                                                         |
| [**сетсреаддпиаваренессконтекст**](/windows/desktop/api/Winuser/nf-winuser-setthreaddpiawarenesscontext)                     | Изменяет контекст осведомленности об активных точках на дюйм для текущего потока.                                                                                                  |
| [**системпараметерсинфофордпи**](/windows/desktop/api/Winuser/nf-winuser-systemparametersinfofordpi)                         | Вариант [системпараметерсинфо](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) , возвращающий значения, масштабируемые до определенного dpi.     |
| [**сетпроцессдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiawarenesscontext)                   | Задает контекст осведомленности относительно DPI для текущего процесса.                                                                                                           |
| [**сетдиалогдпичанжебехавиор**](/windows/desktop/api/winuser/nf-winuser-setdialogdpichangebehavior)                         | Переопределяет поведение по умолчанию для масштабирования DPI для каждого монитора.                                                                                               |
| [**жетдиалогдпичанжебехавиор**](/windows/desktop/api/winuser/nf-winuser-getdialogdpichangebehavior)                         | Извлекает режим масштабирования DPI для каждого монитора в диалоговом окне.                                                                                                       |
| [**сетдиалогконтролдпичанжебехавиор**](/windows/desktop/api/winuser/nf-winuser-setdialogcontroldpichangebehavior)                     | Переопределяет поведение масштабирования по умолчанию для каждого монитора для дочернего окна в диалоговом окне.                                                                             |
| [**жетдиалогконтролдпичанжебехавиор**](/windows/desktop/api/winuser/nf-winuser-getdialogcontroldpichangebehavior)                     | Возвращает все переопределения режима масштабирования DPI для каждого монитора, переопределяющие дочернее окно в диалоговом окне.                                                                           |
| [**опенсемедатафордпи**](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedatafordpi)                                       | Вариант [опенсемедата](/windows/desktop/api/uxtheme/nf-uxtheme-openthemedata) , открывающий дескрипторы тем, которые связаны с конкретным dpi. |
| [**жетсистемдпифорпроцесс**](/windows/desktop/api/winuser/nf-winuser-getsystemdpiforprocess)                                 | Возвращает значение DPI системы, связанное с данным процессом.                                                                                                         |
| [**жетдпифромдпиаваренессконтекст**](/windows/desktop/api/winuser/nf-winuser-getdpifromdpiawarenesscontext)                   | Извлекает значение DPI из заданного маркера [ \_ \_ контекста](dpi-awareness-context.md) для определения dpi.                                                                       |
| [**сетсреаддпихостингбехавиор**](/windows/desktop/api/winuser/nf-winuser-setthreaddpihostingbehavior)                       | Переопределяет поведение размещения текущего потока по умолчанию.                                                                                                 |
| [**жетсреаддпихостингбехавиор**](/windows/desktop/api/winuser/nf-winuser-getthreaddpihostingbehavior)                       | Возвращает поведение размещения текущего потока по DPI.                                                                                                         |
| [**жетвиндовдпихостингбехавиор**](/windows/desktop/api/winuser/nf-winuser-getwindowdpihostingbehavior)                       | Возвращает поведение при размещении DPI для указанного окна.                                                                                                       |



 

## <a name="types"></a>Типы



| Раздел                                                                           |Описание                                                                                        |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_Поддержка dpi**](/windows/desktop/api/windef/ne-windef-dpi_awareness)                                    | Представляет режимы виртуализации координат DPI.                                        |
| [**\_контекст осведомленности о dpi \_**](dpi-awareness-context.md)                   | Маркер, представляющий режим виртуализации DPI и связанные поведения.           |
| [**\_поведение при \_ \_ изменении dpi элемента управления диалогового окна \_**](/windows/desktop/api/winuser/ne-winuser-dialog_control_dpi_change_behaviors) | Описание поведения масштабирования DPI для каждого монитора переопределения для дочерних окон в диалоговых окнах. |
| [**\_поведение при \_ изменении \_ dpi в диалоговом окне**](/windows/desktop/api/winuser/ne-winuser-dialog_dpi_change_behaviors)      | Описывает поведение масштабирования DPI для каждого монитора переопределение для диалоговых окон.                      |
| [**\_тип dpi \_ монитора**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-monitor_dpi_type)                 | Представляет тип DPI, связанный с монитором.                                  |
| [**\_поддержка обработки dpi \_**](/windows/desktop/api/ShellScalingApi/ne-shellscalingapi-process_dpi_awareness)                   | Представляет режим виртуализации координат DPI для процесса.                        |
| [**\_поведение при размещении dpi \_**](/windows/win32/api/windef/ne-windef-dpi_hosting_behavior)                    | Представляет поведение при размещении DPI для окна.                                      |



 

## <a name="messages"></a>Сообщения



| Раздел                                                                   | Описание                                                                                                                                        |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DPICHANGED**](wm-dpichanged.md)                            | Уведомляет окно верхнего уровня о том, что его значение DPI изменилось.                                                                                   |
| [**WM \_ DPICHANGED \_ бефорепарент**](wm-dpichanged-beforeparent.md) | Уведомляет дочернее окно о том, что значение DPI, связанное с содержащим его окном, изменилось. Доставляется до уведомления родительского окна. |
| [**WM \_ DPICHANGED \_ афтерпарент**](wm-dpichanged-afterparent.md)   | Уведомляет дочернее окно о том, что значение DPI, связанное с содержащим его окном, изменилось. Доставляется после уведомления родительского окна.  |
| [**WM \_ жетдпискаледсизе**](wm-getdpiscaledsize.md)                | Позволяет окнам верхнего уровня изменять *нелинейный* размер в ответ на изменения dpi.                                                           |



 

 

 
