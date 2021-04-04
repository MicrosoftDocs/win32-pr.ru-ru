---
title: ГЛКС и ВГЛ/Windows
description: Некоторые функции ВГЛ и функции Windows являются более или менее аналогом функций окон ГЛКС X. В следующем списке показаны функции ГЛКС и соответствующие им функции ВГЛ/Windows, если они доступны.
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- OpenGL в Windows, функции ГЛКС
- Функции ГЛКС OpenGL
- Функции ВГЛ по сравнению с функциями ГЛКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaa2c0ce28bd22e8b6efee4edc395223be2bf11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792811"
---
# <a name="glx-and-wglwindows"></a>ГЛКС и ВГЛ/Windows

Некоторые функции ВГЛ и функции Windows являются более или менее аналогом функций окон ГЛКС X. В следующем списке показаны функции ГЛКС и соответствующие им функции ВГЛ/Windows, если они доступны.



| Функции ГЛКС             | Функции ВГЛ и Windows                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **глксчусевисуал**       | [**чусепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                                                                                                              |
| **глкскопиконтекст**        |                                                                                                                                                             |
| **глкскреатеконтекст**      | [**вглкреатеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglcreatecontext)                                                                                                                |
| **глкскреатеглкспиксмап**    | [**Креатедибитмап**](/windows/desktop/api/wingdi/nf-wingdi-createdibitmap)  /  [ **Креатедибсектион**](/windows/desktop/api/wingdi/nf-wingdi-createdibsection)                                                                     |
| **глксдестройконтекст**     | [**вглделетеконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wgldeletecontext)                                                                                                                |
| **глксдестройглкспиксмап**   | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                                                                        |
| **глксжетконфиг**          | [**дескрибепикселформат**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)                                                                                                          |
| **глксжеткуррентконтекст**  | [**вглжеткуррентконтекст**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentcontext)                                                                                                        |
| **глксжеткуррентдравабле** | [**вглжеткуррентдк**](/windows/desktop/api/wingdi/nf-wingdi-wglgetcurrentdc)                                                                                                                  |
| **глксисдирект**           |                                                                                                                                                             |
| **глксмакекуррент**        | [**вглмакекуррент**](/windows/desktop/api/wingdi/nf-wingdi-wglmakecurrent)                                                                                                                    |
| **глкскуерекстенсион**     | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **глкскуериверсион**       | [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion)                                                                                                                           |
| **глкссвапбуфферс**        | [**свапбуфферс**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)                                                                                                                          |
| **глксусексфонт**           | [**вглусефонтбитмапс**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontbitmapsa)  /  [ **вглусефонтаутлинес**](/windows/desktop/api/wingdi/nf-wingdi-wglusefontoutlinesa)                                                           |
| **глксваитгл**             |                                                                                                                                                             |
| **глксваиткс**              |                                                                                                                                                             |
| **ксжетвисуалинфо**        | [**жетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                                                                                                                    |
| **кскреатевиндов**         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)  /  [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) и [**GetDC**](/windows/desktop/api/winuser/nf-winuser-getdc)  /  [**бегинпаинт**](/windows/desktop/api/winuser/nf-winuser-beginpaint) |
| **кссинк**                 | [**гдифлуш**](/windows/desktop/api/wingdi/nf-wingdi-gdiflush)                                                                                                                                |
|                           | [**сетпикселформат**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                                                                                                                    |
|                           | [**вглжетпрокаддресс**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)                                                                                                              |
|                           | [**вглшарелистс**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists)                                                                                                                      |



 

Дополнительные сведения см. в руководстве по *переносу*.

 

 