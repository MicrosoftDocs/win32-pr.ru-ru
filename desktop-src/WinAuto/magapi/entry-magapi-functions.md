---
title: Функции (API для увеличения)
description: В этом разделе содержатся справочные сведения о функциях API лупы.
ms.assetid: 82b7d82b-b8cd-4f80-ad30-f7db20c57742
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 33418b0d74ec55b7e67cdf5a6130cbd867186dac
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105721073"
---
# <a name="magnification-api-functions"></a>Функции API Лупы

В этом разделе содержатся справочные сведения о функциях API лупы.

## <a name="in-this-section"></a>В этом разделе

| Раздел | Описание |
|:---|:---|
| [**магжетколореффект**](/windows/win32/api/Magnification/nf-magnification-maggetcoloreffect)<br/> | Возвращает матрицу преобразования цвета для элемента управления "Экранная лупа".<br/> |
| [**магжетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreencoloreffect)<br/>  |  Извлекает матрицу преобразования цвета, связанную с полноэкранной экранной лупой.<br/> |
| [**магжетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-maggetfullscreentransform)<br/>  | Получает параметры увеличения для экранной лупы в полноэкранном режиме.<br/>  |
| [***Магжетимажескалингкаллбакк** _](/windows/win32/api/Magnification/nf-magnification-maggetimagescalingcallback)<br/>  | _ * Не рекомендуется в Windows 7 и более поздних версиях * *<br/>Извлекает зарегистрированную функцию обратного вызова, которая реализует пользовательское преобразование для масштабирования изображения. <br/> |
| [**магжетинпуттрансформ**](/windows/win32/api/Magnification/nf-magnification-maggetinputtransform)<br/>  | Извлекает текущее преобразование ввода для пера и сенсорного ввода, представленное в виде исходного прямоугольника и прямоугольника назначения.<br/>  |
| [**магжетвиндовфилтерлист**](/windows/win32/api/Magnification/nf-magnification-maggetwindowfilterlist)<br/>  | Извлекает список окон, которые были увеличены или исключены из увеличения.<br/>  |
| [**магжетвиндовсаурце**](/windows/win32/api/Magnification/nf-magnification-maggetwindowsource)<br/>  | Возвращает прямоугольник области, которая будет увеличена.<br/>  |
| [**магжетвиндовтрансформ**](/windows/win32/api/Magnification/nf-magnification-maggetwindowtransform)<br/>  | Извлекает матрицу преобразования, связанную с элементом управления "Экранная лупа". <br/>  |
| [***Магимажескалингкаллбакк** _](/windows/win32/api/Magnification/nc-magnification-magimagescalingcallback)<br/>  | _ * Не рекомендуется в Windows 7 и более поздних версиях * *<br/>Прототип функции обратного вызова, который реализует пользовательское преобразование для масштабирования изображения.<br/>  |
| [**магинитиализе**](/windows/win32/api/Magnification/nf-magnification-maginitialize)<br/>  | Создает и инициализирует объекты времени выполнения экранной лупы. <br/>  |
| [**магсетколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetcoloreffect)<br/>  | >задает матрицу преобразования цвета для элемента управления "Экранная лупа".<br/>  |
| [**магсетфуллскринколореффект**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreencoloreffect)<br/>  | Изменяет матрицу преобразования цветов, связанную с полноэкранной экранной лупой.<br/>  |
| [**магсетфуллскринтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetfullscreentransform)<br/>  | Изменяет параметры увеличения для полноэкранной экранной лупы.<br/>  |
| [***Магсетимажескалингкаллбакк** _](/windows/win32/api/Magnification/nf-magnification-magsetimagescalingcallback)<br/>  | _ * Не рекомендуется в Windows 7 и более поздних версиях * *<br/>Задает функцию обратного вызова для фильтрации и масштабирования внешних изображений.<br/>  |
| [**магсетинпуттрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetinputtransform)<br/>  | Задает текущее активное преобразование ввода для пера и сенсорного ввода, представленное в виде исходного прямоугольника и прямоугольника назначения.<br/>  |
| [**магсетвиндовфилтерлист**](/windows/win32/api/Magnification/nf-magnification-magsetwindowfilterlist)<br/>  | Задает список окон, которые будут увеличены, или список окон, которые будут исключены из увеличения.<br/>  |
| [**магсетвиндовсаурце**](/windows/win32/api/Magnification/nf-magnification-magsetwindowsource)<br/>  | Задает исходный прямоугольник для окна лупы.<br/>  |
| [**магсетвиндовтрансформ**](/windows/win32/api/Magnification/nf-magnification-magsetwindowtransform)<br/>  | Задает матрицу преобразования для элемента управления "Экранная лупа". <br/>  |
| [**магшовсистемкурсор**](/windows/win32/api/Magnification/nf-magnification-magshowsystemcursor)<br/>  | Показывает или скрывает системный курсор.<br/>  |
| [**магунинитиализе**](/windows/win32/api/Magnification/nf-magnification-maguninitialize)<br/>  | Уничтожает объекты времени выполнения экранной лупы.<br/>  |

## <a name="related-topics"></a>Связанные темы

[Reference](entry-magapi-ref.md)
