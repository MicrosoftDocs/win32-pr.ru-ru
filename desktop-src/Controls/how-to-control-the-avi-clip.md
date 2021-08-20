---
title: Управление роликом AVI
description: В этом разделе показано, как использовать макросы управления анимацией для воспроизведения, приостанавливать и закрывать связанный Audio-Video анимированный ролик (AVI).
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fbabd3ea6e0694448e4bd8c01e53161333b2df3904cf1578252bdbe150d3d5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170765"
---
# <a name="how-to-control-the-avi-clip"></a>Управление роликом AVI

В этом разделе показано, как использовать макросы управления анимацией для воспроизведения, приостанавливать и закрывать связанный Audio-Video анимированный ролик (AVI).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Windows Элементы управления](window-controls.md)

### <a name="prerequisites"></a>Необходимые компоненты

-   C/C++
-   Windows Программирование пользовательского интерфейса
-   Файлы AVI

## <a name="instructions"></a>Инструкции


Создайте функцию, которая принимает в качестве параметров маркер для элемента управления анимации и флаг, указывающий действие, выполняемое над связанным роликом AVI.

Функция в следующем примере C++ вызывает один из трех макросов элемента управления анимацией [**( \_ анимация Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**анимация \_ останавливается**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**анимация \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) на основе значения параметра *nвыходные* . Маркер для элемента управления анимации, связанного с роликом AVI, передается через параметр *хвнданим* .


```C++
// DoAnimation - plays, stops, or closes an animation control's 
//               AVI clip, depending on the value of an action flag. 
// hwndAnim    - handle to an animation control. 
// nAction     - flag that determines whether to play, stop, or close 
//               the AVI clip. 

void DoAnimation(HWND hwndAnim, int nAction) 
{ 
    int const PLAYIT = 1, STOPIT = 2, CLOSEIT = 3; 
    switch (nAction) { 
        case PLAYIT: 
         // Play the clip continuously starting with the 
         // first frame. 
            Animate_Play(hwndAnim, 0, -1, -1); 
            break; 

        case STOPIT: 
            Animate_Stop(hwndAnim); 
            break; 

        case CLOSEIT: 
            Animate_Close(hwndAnim); 
            break; 

        default: 
            break; 
    }
    
    return; 
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Об элементах управления анимацией](animation-control-overview.md)
</dt> <dt>

[Справочник по элементу управления анимацией](bumper-animation-animation-control-reference.md)
</dt> <dt>

[Использование элементов управления анимацией](using-animation-control.md)
</dt> <dt>

[Элемент управления анимации](animation-control-reference.md)
</dt> </dl>

 

 




