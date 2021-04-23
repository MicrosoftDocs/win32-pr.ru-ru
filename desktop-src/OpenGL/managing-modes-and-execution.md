---
title: Управление режимами и выполнением
description: Управление режимами и выполнением
ms.assetid: 6a1ecc42-194a-4d8f-94f6-fd59696d87cf
keywords:
- OpenGL, режимы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427e04b856c79c9adfdfebf4061f7e96f09db835
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661532"
---
# <a name="managing-modes-and-execution"></a><span data-ttu-id="8cc49-104">Управление режимами и выполнением</span><span class="sxs-lookup"><span data-stu-id="8cc49-104">Managing Modes and Execution</span></span>

<span data-ttu-id="8cc49-105">Воздействие многих функций OpenGL зависит от того, действует ли определенный режим.</span><span class="sxs-lookup"><span data-stu-id="8cc49-105">The effect of many OpenGL functions depends on whether a particular mode is in effect.</span></span> <span data-ttu-id="8cc49-106">Функции [**гленабле**](glenable.md) и [**глдисабле**](gldisable.md) задают такие режимы. [**глисенаблед**](glisenabled.md) определяет, установлен ли определенный режим.</span><span class="sxs-lookup"><span data-stu-id="8cc49-106">The [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) functions set such modes; [**glIsEnabled**](glisenabled.md) determines whether a particular mode is set.</span></span>

<span data-ttu-id="8cc49-107">Вы можете управлять выполнением ранее выданных функций OpenGL с помощью [**глфиниш**](glfinish.md), что приводит к завершению всех таких функций, или [**глфлуш**](glflush.md), что гарантирует, что все такие функции будут выполняться в конечное время.</span><span class="sxs-lookup"><span data-stu-id="8cc49-107">You can control the execution of previously issued OpenGL functions with [**glFinish**](glfinish.md), which forces all such functions to finish, or [**glFlush**](glflush.md), which ensures that all such functions will be completed in a finite time.</span></span>

<span data-ttu-id="8cc49-108">В конкретной реализации OpenGL вы можете управлять определенными режимами работы с указаниями с помощью [**глхинт**](glhint.md).</span><span class="sxs-lookup"><span data-stu-id="8cc49-108">In a particular implementation of OpenGL, you may be able to control certain behaviors with hints by using [**glHint**](glhint.md).</span></span> <span data-ttu-id="8cc49-109">Такое поведение — это качество цвета и интерполяции текстурных координат; точность вычислений тумана; и выборка качества сглаженных точек, линий или многоугольников.</span><span class="sxs-lookup"><span data-stu-id="8cc49-109">Such behaviors are the quality of color and texture coordinate interpolation; the accuracy of fog calculations; and the sampling quality of antialiased points, lines, or polygons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cc49-110">См. также</span><span class="sxs-lookup"><span data-stu-id="8cc49-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cc49-111">Режимы и Справочник по выполнению</span><span class="sxs-lookup"><span data-stu-id="8cc49-111">Modes and Execution Reference</span></span>](modes-and-execution-reference.md)
</dt> </dl>

 

 




