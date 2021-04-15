---
title: Управление роликом AVI
description: В этом разделе показано, как использовать макросы управления анимацией для воспроизведения, приостанавливать и закрывать связанный Audio-Video анимированный ролик (AVI).
ms.assetid: 4B19F929-B306-4EBF-B82F-6539FAA42BA6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c11f7d8f519f98f3293d5be29fac0e0a40dd704
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488595"
---
# <a name="how-to-control-the-avi-clip"></a><span data-ttu-id="5a8c7-103">Управление роликом AVI</span><span class="sxs-lookup"><span data-stu-id="5a8c7-103">How to Control the AVI Clip</span></span>

<span data-ttu-id="5a8c7-104">В этом разделе показано, как использовать макросы управления анимацией для воспроизведения, приостанавливать и закрывать связанный Audio-Video анимированный ролик (AVI).</span><span class="sxs-lookup"><span data-stu-id="5a8c7-104">This topic demonstrates how to use the animation control macros to play, stop, and close an associated Audio-Video Interleaved (AVI) clip.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5a8c7-105">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="5a8c7-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5a8c7-106">Технологии</span><span class="sxs-lookup"><span data-stu-id="5a8c7-106">Technologies</span></span>

-   [<span data-ttu-id="5a8c7-107">Элементы управления Windows</span><span class="sxs-lookup"><span data-stu-id="5a8c7-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="5a8c7-108">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5a8c7-108">Prerequisites</span></span>

-   <span data-ttu-id="5a8c7-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="5a8c7-109">C/C++</span></span>
-   <span data-ttu-id="5a8c7-110">Программирование пользовательского интерфейса Windows</span><span class="sxs-lookup"><span data-stu-id="5a8c7-110">Windows User Interface Programming</span></span>
-   <span data-ttu-id="5a8c7-111">Файлы AVI</span><span class="sxs-lookup"><span data-stu-id="5a8c7-111">AVI files</span></span>

## <a name="instructions"></a><span data-ttu-id="5a8c7-112">Инструкции</span><span class="sxs-lookup"><span data-stu-id="5a8c7-112">Instructions</span></span>


<span data-ttu-id="5a8c7-113">Создайте функцию, которая принимает в качестве параметров маркер для элемента управления анимации и флаг, указывающий действие, выполняемое над связанным роликом AVI.</span><span class="sxs-lookup"><span data-stu-id="5a8c7-113">Create a function that takes as parameters a handle to the animation control and a flag that indicates the action to be performed on the associated AVI clip.</span></span>

<span data-ttu-id="5a8c7-114">Функция в следующем примере C++ вызывает один из трех макросов элемента управления анимацией [**( \_ анимация Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**анимация \_ останавливается**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**анимация \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) на основе значения параметра *nвыходные* .</span><span class="sxs-lookup"><span data-stu-id="5a8c7-114">The function in the following C++ example calls one of three animation control macros ([**Animate\_Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play), [**Animate\_Stop**](/windows/desktop/api/Commctrl/nf-commctrl-animate_stop), [**Animate\_Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close)) based on the value of the *nAction* parameter.</span></span> <span data-ttu-id="5a8c7-115">Маркер для элемента управления анимации, связанного с роликом AVI, передается через параметр *хвнданим* .</span><span class="sxs-lookup"><span data-stu-id="5a8c7-115">The handle to the animation control that is associated with the AVI clip is passed via the *hwndAnim* parameter.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5a8c7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5a8c7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8c7-117">Об элементах управления анимацией</span><span class="sxs-lookup"><span data-stu-id="5a8c7-117">About Animation Controls</span></span>](animation-control-overview.md)
</dt> <dt>

[<span data-ttu-id="5a8c7-118">Справочник по элементу управления анимацией</span><span class="sxs-lookup"><span data-stu-id="5a8c7-118">Animation Control Reference</span></span>](bumper-animation-animation-control-reference.md)
</dt> <dt>

[<span data-ttu-id="5a8c7-119">Использование элементов управления анимацией</span><span class="sxs-lookup"><span data-stu-id="5a8c7-119">Using Animation Controls</span></span>](using-animation-control.md)
</dt> <dt>

[<span data-ttu-id="5a8c7-120">Элемент управления анимации</span><span class="sxs-lookup"><span data-stu-id="5a8c7-120">Animation Control</span></span>](animation-control-reference.md)
</dt> </dl>

 

 




