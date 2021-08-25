---
title: ГЛКС и ВГЛ/Windows
description: некоторые функции вгл и функции Windows являются более или менее аналогом функций окна глкс X. в следующем списке показаны функции глкс и соответствующие им функции вгл/Windows, если они доступны.
ms.assetid: 428c0fdc-a541-4720-908f-99f0539d9f4b
keywords:
- OpenGL на Windows, функции глкс
- Функции ГЛКС OpenGL
- Функции ВГЛ по сравнению с функциями ГЛКС
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24b88caeed9aea7bae8e38f73818ac180aad9117806508f40550b02eb8a4e76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035391"
---
# <a name="glx-and-wglwindows"></a>ГЛКС и ВГЛ/Windows

некоторые функции вгл и функции Windows являются более или менее аналогом функций окна глкс X. в следующем списке показаны функции глкс и соответствующие им функции вгл/Windows, если они доступны.



| Функции ГЛКС             | функции вгл и Windows                                                                                                                                       |
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

 

 