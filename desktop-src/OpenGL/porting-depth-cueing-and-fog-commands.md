---
title: Перенос команд cueing и туман глубины
description: Перенос команд cueing и туман глубины
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Перенос GL по IRI, глубина cueing
- Перенос из IRI GL, Depth cueing
- перенос в OpenGL из IRI GL, Depth cueing
- Перенос по стандарту OpenGL из IRI GL, Depth cueing
- Перенос GL в ГК, туман
- Перенос из IRI GL, туман
- Перенос на OpenGL из IRI GL, туман
- Перенос по стандарту OpenGL из IRI GL, тумана
- cueing глубины
- туман
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258809"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="91425-113">Перенос команд cueing и туман глубины</span><span class="sxs-lookup"><span data-stu-id="91425-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="91425-114">При переносе команд Depth-cueing и тумана учитывайте следующие моменты:</span><span class="sxs-lookup"><span data-stu-id="91425-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="91425-115">Вызов IRI GL, **фогвертекс**, задает режим и параметры, влияющие на этот режим.</span><span class="sxs-lookup"><span data-stu-id="91425-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="91425-116">В OpenGL вы вызываете [**глфог**](glfog.md) один раз, чтобы установить режим, а затем снова дважды или больше, чтобы задать различные параметры.</span><span class="sxs-lookup"><span data-stu-id="91425-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="91425-117">В OpenGL глубина cueing не является отдельной функцией.</span><span class="sxs-lookup"><span data-stu-id="91425-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="91425-118">Используйте линейную туман, а не глубину cueing.</span><span class="sxs-lookup"><span data-stu-id="91425-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="91425-119">(В этом разделе приводится пример того, как это сделать.) В следующих функциях IRI GL нет прямого эквивалента OpenGL:</span><span class="sxs-lookup"><span data-stu-id="91425-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="91425-120">**депскуе**</span><span class="sxs-lookup"><span data-stu-id="91425-120">**depthcue**</span></span>

    <span data-ttu-id="91425-121">**лргбранже**</span><span class="sxs-lookup"><span data-stu-id="91425-121">**lRGBrange**</span></span>

    <span data-ttu-id="91425-122">**лшадеранже**</span><span class="sxs-lookup"><span data-stu-id="91425-122">**lshaderange**</span></span>

    <span data-ttu-id="91425-123">**жетдкм**</span><span class="sxs-lookup"><span data-stu-id="91425-123">**getdcm**</span></span>

-   <span data-ttu-id="91425-124">Чтобы настроить качество тумана, используйте [**глхинт**](glhint.md)( \_ Указание тумана GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="91425-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="91425-125">В следующей таблице перечислены функции IRI GL по управлению туманом и их эквивалентные функции OpenGL.</span><span class="sxs-lookup"><span data-stu-id="91425-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="91425-126">Функция IRI GL</span><span class="sxs-lookup"><span data-stu-id="91425-126">IRIS GL function</span></span>         | <span data-ttu-id="91425-127">Функция OpenGL</span><span class="sxs-lookup"><span data-stu-id="91425-127">OpenGL function</span></span>                                     | <span data-ttu-id="91425-128">Значение</span><span class="sxs-lookup"><span data-stu-id="91425-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="91425-129">**фогвертекс**</span><span class="sxs-lookup"><span data-stu-id="91425-129">**fogvertex**</span></span>            | [<span data-ttu-id="91425-130">**глфог**</span><span class="sxs-lookup"><span data-stu-id="91425-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="91425-131">Задает различные параметры тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="91425-132">**фогвертекс**(FG \_ On)</span><span class="sxs-lookup"><span data-stu-id="91425-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="91425-133">[**гленабле**](glenable.md) ( \_ туман GL)</span><span class="sxs-lookup"><span data-stu-id="91425-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="91425-134">Включает туман.</span><span class="sxs-lookup"><span data-stu-id="91425-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="91425-135">**фогвертекс**(FG \_ Off)</span><span class="sxs-lookup"><span data-stu-id="91425-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="91425-136">[**глдисабле**](gldisable.md) ( \_ туман GL)</span><span class="sxs-lookup"><span data-stu-id="91425-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="91425-137">Отключает туман.</span><span class="sxs-lookup"><span data-stu-id="91425-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="91425-138">**депскуе**</span><span class="sxs-lookup"><span data-stu-id="91425-138">**depthcue**</span></span>             | <span data-ttu-id="91425-139">[**глфог**](glfog.md) (GL- \_ туман \_ Mod, \_ линейная, GL)</span><span class="sxs-lookup"><span data-stu-id="91425-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="91425-140">Использует линейный туман для глубины cueing.</span><span class="sxs-lookup"><span data-stu-id="91425-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="91425-141">В следующей таблице перечислены параметры, которые можно передать в **глфог**.</span><span class="sxs-lookup"><span data-stu-id="91425-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="91425-142">Параметр тумана</span><span class="sxs-lookup"><span data-stu-id="91425-142">Fog parameter</span></span>    | <span data-ttu-id="91425-143">Значение</span><span class="sxs-lookup"><span data-stu-id="91425-143">Meaning</span></span>                       | <span data-ttu-id="91425-144">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="91425-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="91425-145">\_плотность тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="91425-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="91425-146">Плотность тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-146">Fog density.</span></span>                  | <span data-ttu-id="91425-147">1.0</span><span class="sxs-lookup"><span data-stu-id="91425-147">1.0</span></span>                      |
| <span data-ttu-id="91425-148">Начало работы с \_ туманом GL \_</span><span class="sxs-lookup"><span data-stu-id="91425-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="91425-149">Близкое расстояние для линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-149">Near distance for linear fog.</span></span> | <span data-ttu-id="91425-150">0,0</span><span class="sxs-lookup"><span data-stu-id="91425-150">0.0</span></span>                      |
| <span data-ttu-id="91425-151">Окончание GL в главной \_ \_ части</span><span class="sxs-lookup"><span data-stu-id="91425-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="91425-152">Дальнее расстояние линейного тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="91425-153">1.0</span><span class="sxs-lookup"><span data-stu-id="91425-153">1.0</span></span>                      |
| <span data-ttu-id="91425-154">\_индекс тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="91425-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="91425-155">Цветовой индекс тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-155">Fog color index.</span></span>              | <span data-ttu-id="91425-156">0,0</span><span class="sxs-lookup"><span data-stu-id="91425-156">0.0</span></span>                      |
| <span data-ttu-id="91425-157">\_Цвет тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="91425-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="91425-158">Цвет RGBA тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-158">Fog RGBA color.</span></span>               | <span data-ttu-id="91425-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="91425-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="91425-160">\_режим тумана GL \_</span><span class="sxs-lookup"><span data-stu-id="91425-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="91425-161">Режим тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-161">Fog mode.</span></span>                     | <span data-ttu-id="91425-162">См. следующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="91425-162">See the following table.</span></span> |



 

<span data-ttu-id="91425-163">Параметр плотности тумана OpenGL отличается от стандарта в IRI GL.</span><span class="sxs-lookup"><span data-stu-id="91425-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="91425-164">Они связаны следующим образом:</span><span class="sxs-lookup"><span data-stu-id="91425-164">They are related as follows:</span></span>

-   <span data-ttu-id="91425-165">Если *фогмоде* = EXP2</span><span class="sxs-lookup"><span data-stu-id="91425-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="91425-166">*опенглфогденсити* = (*ирисглфогденсити* ) ( **sqrt** ( **Журнал** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="91425-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="91425-167">Если *фогмоде* = exp</span><span class="sxs-lookup"><span data-stu-id="91425-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="91425-168">*опенглфогденсити* = (*ирисглфогденсити* ) ( **Журнал** (1/255))</span><span class="sxs-lookup"><span data-stu-id="91425-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="91425-169">где **sqrt** — это квадратный корень, **log** — это натуральный логарифм, *ирисглфогденсити* — плотность тумана в форме IRI, а *опенглфогденсити* — плотность тумана OpenGL.</span><span class="sxs-lookup"><span data-stu-id="91425-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="91425-170">Для переключения между вычислением тумана в режиме "на пиксель" и режимом вершины используйте [**глхинт**](glhint.md)( \_ Указание тумана в ГК \_ , *хинтмоде*).</span><span class="sxs-lookup"><span data-stu-id="91425-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="91425-171">Доступны два режима подсказок:</span><span class="sxs-lookup"><span data-stu-id="91425-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="91425-172">\_Вычисление тумана НИЦЕСТ GL на пиксельном уровне</span><span class="sxs-lookup"><span data-stu-id="91425-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="91425-173">\_Самый быстрый расчет тумана на вершину в ГК</span><span class="sxs-lookup"><span data-stu-id="91425-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="91425-174">В следующей таблице перечислены режимы и эквиваленты типов тумана IRI GL.</span><span class="sxs-lookup"><span data-stu-id="91425-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="91425-175">Режим тумана IRI GL</span><span class="sxs-lookup"><span data-stu-id="91425-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="91425-176">Режим тумана OpenGL</span><span class="sxs-lookup"><span data-stu-id="91425-176">OpenGL fog mode</span></span> | <span data-ttu-id="91425-177">Режим подсказки</span><span class="sxs-lookup"><span data-stu-id="91425-177">Hint mode</span></span>                         | <span data-ttu-id="91425-178">Значение</span><span class="sxs-lookup"><span data-stu-id="91425-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="91425-179">FG \_ вткс \_ exp, FG \_ PIX \_ exp</span><span class="sxs-lookup"><span data-stu-id="91425-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="91425-180">\_exp ГК</span><span class="sxs-lookup"><span data-stu-id="91425-180">GL\_EXP</span></span>         | <span data-ttu-id="91425-181">\_самая быстрая, GL, \_ ницест</span><span class="sxs-lookup"><span data-stu-id="91425-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="91425-182">Интенсивный режим тумана (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="91425-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="91425-183">FG \_ вткс \_ EXP2, FG \_ PIX \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="91425-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="91425-184">\_EXP2 GL</span><span class="sxs-lookup"><span data-stu-id="91425-184">GL\_EXP2</span></span>        | <span data-ttu-id="91425-185">\_самая быстрая, GL, \_ ницест</span><span class="sxs-lookup"><span data-stu-id="91425-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="91425-186">Режим ХАЗе.</span><span class="sxs-lookup"><span data-stu-id="91425-186">Haze mode.</span></span>                               |
| <span data-ttu-id="91425-187">FG \_ вткс \_ ссыл, FG \_ PIX \_</span><span class="sxs-lookup"><span data-stu-id="91425-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="91425-188">Линейная (GL) \_</span><span class="sxs-lookup"><span data-stu-id="91425-188">GL\_LINEAR</span></span>      | <span data-ttu-id="91425-189">\_самая быстрая, GL, \_ ницест</span><span class="sxs-lookup"><span data-stu-id="91425-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="91425-190">Линейный режим тумана.</span><span class="sxs-lookup"><span data-stu-id="91425-190">Linear fog mode.</span></span> <span data-ttu-id="91425-191">(Используйте для глубины cueing.)</span><span class="sxs-lookup"><span data-stu-id="91425-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="91425-192">В следующем примере кода показано cueing глубины в OpenGL:</span><span class="sxs-lookup"><span data-stu-id="91425-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





