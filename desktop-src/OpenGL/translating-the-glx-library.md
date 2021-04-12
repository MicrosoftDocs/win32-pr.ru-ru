---
title: Преобразование библиотеки ГЛКС
description: Преобразование библиотеки ГЛКС
ms.assetid: 040fe6f1-f6ba-4dfa-b294-447efd686361
keywords:
- OpenGL в Windows, Библиотека ГЛКС
- перенос в OpenGL, Библиотека ГЛКС
- Перенос с OpenGL, Библиотека ГЛКС
- ГЛКС библиотека OpenGL
- Функции кслиб OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e4cede2b74dc2881f867370744ee14c00cceba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413482"
---
# <a name="translating-the-glx-library"></a>Преобразование библиотеки ГЛКС

Системные программы OpenGL X используют расширение OpenGL с библиотекой X Window System (ГЛКС). Библиотека представляет собой набор функций и подпрограмм, которые инициализируют формат пикселей, отрисовку элементов управления и выполнение других задач, специфичных для OpenGL. Он подключает библиотеку OpenGL к системе Window X, управляя дескрипторами окон и контекстами отрисовки. Эти функции необходимо преобразовать в эквивалентные функции Windows. В следующей таблице перечислены функции X Window System ГЛКС и их эквивалентные функции Windows.



| Функция ГЛКС/Кслиб         | Функция Windows                                                                                                                                       |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **глксчусевисуал**       | [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                         |
| **глкскопиконтекст**        | Не применяется                                                                                                                                        |
| **глкскреатеконтекст**      | [**вглкреатеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                           |
| **глкскреатеглкспиксмап**    | [**Креатедибитмап**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)[**креатедибсектион**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                   |
| **глксдестройконтекст**     | [**вглделетеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                           |
| **глксдестройглкспиксмап**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                   |
| **глксжетконфиг**          | [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                     |
| **глксжеткуррентконтекст**  | [**вглжеткуррентконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                   |
| **глксжеткуррентдравабле** | [**вглжеткуррентдк**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                             |
| **глксисдирект**           | Не применяется                                                                                                                                        |
| **глксмакекуррент**        | [**вглмакекуррент**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                               |
| **глкскуерекстенсион**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **глкскуериверсион**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                      |
| **глкссвапбуфферс**        | [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                     |
| **глксусексфонт**           | [**вглусефонтбитмапс**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)                                                                                                         |
| **ксжетвисуалинфо**        | [**жетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                               |
| **кскреатевиндов**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa), [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa), [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc), [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **кссинк**                 | [**гдифлуш**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                           |
| Не применяется           | [**сетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                               |



 

Некоторые функции ГЛКС не имеют эквивалентной функции Windows. Чтобы перенести эти функции в Windows, перепишите код, чтобы получить те же функциональные возможности. Например, **глксваитгл** не имеет эквивалентной функции Windows, но можно добиться того же результата, выполнив все ожидающие команды OpenGL, вызвав [**глфиниш**](glfinish.md).

В следующих разделах описано, как переносить функции ГЛКС, которые задают формат пикселей, и управлять контекстами отрисовки, пиксмапс и точечными рисунками.

 

 