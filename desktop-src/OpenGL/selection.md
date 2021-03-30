---
title: Выбор
description: Выбор возвращает текущее содержимое стека имен, которое представляет собой массив имен с целочисленными значениями.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- режим выбора OpenGL
- попадания по выделению OpenGL
- записи попаданий OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330672"
---
# <a name="selection"></a><span data-ttu-id="317d8-106">Выбор</span><span class="sxs-lookup"><span data-stu-id="317d8-106">Selection</span></span>

<span data-ttu-id="317d8-107">Выбор возвращает текущее содержимое стека имен, которое представляет собой массив имен с целочисленными значениями.</span><span class="sxs-lookup"><span data-stu-id="317d8-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="317d8-108">Вы назначаете имена и строите стек имен в коде моделирования, который указывает геометрию объектов, которые необходимо нарисовать.</span><span class="sxs-lookup"><span data-stu-id="317d8-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="317d8-109">Затем в режиме выбора каждый раз, когда примитив пересекает громкость обрезки, происходит выделение.</span><span class="sxs-lookup"><span data-stu-id="317d8-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="317d8-110">Запись попадания, которая записывается в массив выбора, предоставленный с помощью [**глселектбуффер**](glselectbuffer.md), содержит сведения о содержимом стека имен во время попадания.</span><span class="sxs-lookup"><span data-stu-id="317d8-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="317d8-111">Вызовите [**глселектбуффер**](glselectbuffer.md) , прежде чем переводить OpenGL в режим выбора с помощью [**глрендермоде**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="317d8-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="317d8-112">Все содержимое стека имен не гарантируется, пока вы не вызовите **глрендермоде** , чтобы извлечь из режима выбора OpenGL.</span><span class="sxs-lookup"><span data-stu-id="317d8-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="317d8-113">Управлять стеком имен с помощью [**глинитнамес**](glinitnames.md), [**гллоаднаме**](glloadname.md), [**глпушнаме**](glpushname.md)и [**глпопнаме**](glpopname.md).</span><span class="sxs-lookup"><span data-stu-id="317d8-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="317d8-114">Для выбора можно также использовать [**глупиккматрикс**](glupickmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="317d8-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




