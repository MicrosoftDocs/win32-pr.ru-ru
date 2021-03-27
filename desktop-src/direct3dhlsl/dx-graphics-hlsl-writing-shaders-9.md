---
title: Создание шейдеров HLSL в Direct3D 9
description: Создание шейдеров HLSL в Direct3D 9
ms.assetid: 7db6b264-c96c-4298-9b8a-d0c488390e4e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 504a1d9ff5a2aa2b37227f0016cdc97d28d967fe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070392"
---
# <a name="writing-hlsl-shaders-in-direct3d-9"></a><span data-ttu-id="5a0a2-103">Создание шейдеров HLSL в Direct3D 9</span><span class="sxs-lookup"><span data-stu-id="5a0a2-103">Writing HLSL Shaders in Direct3D 9</span></span>

-   [<span data-ttu-id="5a0a2-104">Основные сведения о шейдере вершин</span><span class="sxs-lookup"><span data-stu-id="5a0a2-104">Vertex-Shader Basics</span></span>](#vertex-shader-basics)
-   [<span data-ttu-id="5a0a2-105">Основы построителя текстуры</span><span class="sxs-lookup"><span data-stu-id="5a0a2-105">Pixel-Shader Basics</span></span>](#pixel-shader-basics)
    -   [<span data-ttu-id="5a0a2-106">Стадия текстуры и состояния образца</span><span class="sxs-lookup"><span data-stu-id="5a0a2-106">Texture Stage and Sampler States</span></span>](#texture-stage-and-sampler-states)
    -   [<span data-ttu-id="5a0a2-107">Входные шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="5a0a2-107">Pixel Shader Inputs</span></span>](#pixel-shader-inputs)
    -   [<span data-ttu-id="5a0a2-108">Выходные данные шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="5a0a2-108">Pixel Shader Outputs</span></span>](#pixel-shader-outputs)
-   [<span data-ttu-id="5a0a2-109">Входные и переменные шейдеров</span><span class="sxs-lookup"><span data-stu-id="5a0a2-109">Shader Inputs and Shader Variables</span></span>](#shader-inputs-and-shader-variables)
    -   [<span data-ttu-id="5a0a2-110">Объявление переменных шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-110">Declaring Shader Variables</span></span>](#declaring-shader-variables)
    -   [<span data-ttu-id="5a0a2-111">Входные данные универсального шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-111">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
    -   [<span data-ttu-id="5a0a2-112">Различные входные и семантические значения шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-112">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
    -   [<span data-ttu-id="5a0a2-113">Пробы и объекты текстуры</span><span class="sxs-lookup"><span data-stu-id="5a0a2-113">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)
-   [<span data-ttu-id="5a0a2-114">Написание функций</span><span class="sxs-lookup"><span data-stu-id="5a0a2-114">Writing Functions</span></span>](#writing-functions)
-   [<span data-ttu-id="5a0a2-115">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="5a0a2-115">Flow Control</span></span>](#flow-control)
-   [<span data-ttu-id="5a0a2-116">См. также</span><span class="sxs-lookup"><span data-stu-id="5a0a2-116">Related topics</span></span>](#related-topics)

## <a name="vertex-shader-basics"></a><span data-ttu-id="5a0a2-117">Основы Vertex-Shader</span><span class="sxs-lookup"><span data-stu-id="5a0a2-117">Vertex-Shader Basics</span></span>

<span data-ttu-id="5a0a2-118">При выполнении операции программируемый шейдер вершин заменяет обработку вершин, выполняемую конвейером Microsoft Direct3D Graphics.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-118">When in operation, a programmable vertex shader replaces the vertex processing done by the Microsoft Direct3D graphics pipeline.</span></span> <span data-ttu-id="5a0a2-119">При использовании шейдера вершин сведения о состоянии, касающиеся операций преобразования и освещения, игнорируются с помощью фиксированного конвейера функций.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-119">While using a vertex shader, state information regarding transformation and lighting operations is ignored by the fixed function pipeline.</span></span> <span data-ttu-id="5a0a2-120">Если шейдер вершин отключен и возвращается фиксированная обработка функций, применяются все текущие параметры состояния.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-120">When the vertex shader is disabled and fixed function processing is returned, all current state settings apply.</span></span>

<span data-ttu-id="5a0a2-121">Тесселяция примитивов высокого порядка следует выполнять перед выполнением шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-121">Tessellation of high-order primitives should be done before the vertex shader executes.</span></span> <span data-ttu-id="5a0a2-122">Реализации, которые выполняют тесселяцию поверхности после обработки шейдера, должны сделать это таким образом, что не очевидно для приложения и кода шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-122">Implementations that perform surface tessellation after the shader processing must do so in a way that is not apparent to the application and shader code.</span></span>

<span data-ttu-id="5a0a2-123">Как минимум Вершинный шейдер должен выводить расположение вершины в однородном пространстве для обрезки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-123">As a minimum, a vertex shader must output vertex position in homogeneous clip space.</span></span> <span data-ttu-id="5a0a2-124">При необходимости шейдер вершин может выводить координаты текстуры, цвет вершины, освещение вершин, факторы тумана и т. д.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-124">Optionally, the vertex shader can output texture coordinates, vertex color, vertex lighting, fog factors, and so on.</span></span>

## <a name="pixel-shader-basics"></a><span data-ttu-id="5a0a2-125">Основы Pixel-Shader</span><span class="sxs-lookup"><span data-stu-id="5a0a2-125">Pixel-Shader Basics</span></span>

<span data-ttu-id="5a0a2-126">Обработка пикселей выполняется построителейми текстур пикселей на отдельных пикселях.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-126">Pixel processing is performed by pixel shaders on individual pixels.</span></span> <span data-ttu-id="5a0a2-127">Шейдеры пикселей работают совместно с шейдерами вершин; выходные данные шейдера вершин предоставляют входные данные для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-127">Pixel shaders work in concert with vertex shaders; the output of a vertex shader provides the inputs for a pixel shader.</span></span> <span data-ttu-id="5a0a2-128">Другие операции с пикселями (смешение тумана, операции с трафаретами и наложение целевого объекта визуализации) происходят после выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-128">Other pixel operations (fog blending, stencil operations, and render-target blending) occur after execution of the shader.</span></span>

### <a name="texture-stage-and-sampler-states"></a><span data-ttu-id="5a0a2-129">Стадия текстуры и состояния образца</span><span class="sxs-lookup"><span data-stu-id="5a0a2-129">Texture Stage and Sampler States</span></span>

<span data-ttu-id="5a0a2-130">Шейдер пикселей полностью заменяет функциональные возможности смешения пикселей, заданные многотекстурным смешением, включая операции, ранее определенные состояниями стадии текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-130">A pixel shader completely replaces the pixel-blending functionality specified by the multi-texture blender including operations previously defined by the texture stage states.</span></span> <span data-ttu-id="5a0a2-131">Операции выборки текстур и фильтрации, которые управляются состояниями стандартного этапа текстуры для минификации, увеличения, MIP и режима адресации, можно инициализировать в шейдерах.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-131">Texture sampling and filtering operations which were controlled by the standard texture stage states for minification, magnification, mip filtering, and the wrap addressing modes, can be initialized in shaders.</span></span> <span data-ttu-id="5a0a2-132">Приложение может изменить эти состояния, не требуя повторного формирования шейдера, привязанного к текущему объекту.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-132">The application is free to change these states without requiring the regeneration of the currently bound shader.</span></span> <span data-ttu-id="5a0a2-133">Задание состояния можно сделать еще проще, если шейдеры спроектированы в пределах влияния.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-133">Setting state can be made even easier if your shaders are designed within an effect.</span></span>

### <a name="pixel-shader-inputs"></a><span data-ttu-id="5a0a2-134">Входные шейдеры пикселей</span><span class="sxs-lookup"><span data-stu-id="5a0a2-134">Pixel Shader Inputs</span></span>

<span data-ttu-id="5a0a2-135">Для версий построителя текстуры PS \_ 1 \_ 1 — PS \_ 2 \_ 0 рассеянные и бликовые цвета загружаются в диапазоне от 0 до 1 перед использованием шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-135">For pixel shader versions ps\_1\_1 - ps\_2\_0, diffuse and specular colors are saturated (clamped) in the range 0 to 1 before use by the shader.</span></span>

<span data-ttu-id="5a0a2-136">Предполагается, что входные значения цветов для шейдера пикселей верны, но это не гарантируется (для всех аппаратных средств).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-136">Color values input to the pixel shader are assumed to be perspective correct, but this is not guaranteed (for all hardware).</span></span> <span data-ttu-id="5a0a2-137">Цвета, выбираемые из координат текстуры, обрабатываются с точки зрения правильности и записываются в 0 – 1 диапазон во время итерации.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-137">Colors sampled from texture coordinates are iterated in a perspective correct manner, and are clamped to the 0 to 1 range during iteration.</span></span>

### <a name="pixel-shader-outputs"></a><span data-ttu-id="5a0a2-138">Выходные данные шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="5a0a2-138">Pixel Shader Outputs</span></span>

<span data-ttu-id="5a0a2-139">Для версий построителя текстуры PS \_ 1 \_ 1 — PS \_ 1 \_ 4 результат, выдаваемый шейдером пикселей, — это содержимое Register R0.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-139">For pixel shader versions ps\_1\_1 - ps\_1\_4, the result emitted by the pixel shader is the contents of register r0.</span></span> <span data-ttu-id="5a0a2-140">Любое содержимое, которое он содержит после завершения обработки шейдера, отправляется на этап тумана и нацеливание на целевой объект.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-140">Whatever it contains when the shader completes processing is sent to the fog stage and render-target blender.</span></span>

<span data-ttu-id="5a0a2-141">Для версий построителя текстуры PS \_ 2 \_ 0 и выше выходной цвет создается из OC0-oC4.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-141">For pixel shader versions ps\_2\_0 and above, output color is emitted from oC0 - oC4.</span></span>

## <a name="shader-inputs-and-shader-variables"></a><span data-ttu-id="5a0a2-142">Входные и переменные шейдеров</span><span class="sxs-lookup"><span data-stu-id="5a0a2-142">Shader Inputs and Shader Variables</span></span>

-   [<span data-ttu-id="5a0a2-143">Объявление переменных шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-143">Declaring Shader Variables</span></span>](#declaring-shader-variables)
-   [<span data-ttu-id="5a0a2-144">Входные данные универсального шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-144">Uniform Shader Inputs</span></span>](#uniform-shader-inputs)
-   [<span data-ttu-id="5a0a2-145">Различные входные и семантические значения шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-145">Varying Shader Inputs and Semantics</span></span>](#varying-shader-inputs-and-semantics)
-   [<span data-ttu-id="5a0a2-146">Пробы и объекты текстуры</span><span class="sxs-lookup"><span data-stu-id="5a0a2-146">Samplers and Texture Objects</span></span>](#samplers-and-texture-objects)

### <a name="declaring-shader-variables"></a><span data-ttu-id="5a0a2-147">Объявление переменных шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-147">Declaring Shader Variables</span></span>

<span data-ttu-id="5a0a2-148">Простейшее объявление переменной включает тип и имя переменной, например следующее объявление с плавающей запятой:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-148">The simplest variable declaration includes a type and a variable name, such as this floating-point declaration:</span></span>


```
float fVar;
```



<span data-ttu-id="5a0a2-149">Вы можете инициализировать переменную в той же инструкции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-149">You can initialize a variable in the same statement.</span></span>


```
float fVar = 3.1f;
```



<span data-ttu-id="5a0a2-150">Массив переменных можно объявить,</span><span class="sxs-lookup"><span data-stu-id="5a0a2-150">An array of variables can be declared,</span></span>


```
int iVar[3];
```



<span data-ttu-id="5a0a2-151">или объявлен и инициализирован в одной инструкции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-151">or declared and initialized in the same statement.</span></span>


```
int iVar[3] = {1,2,3};
```



<span data-ttu-id="5a0a2-152">Ниже приведено несколько объявлений, демонстрирующих многие характеристики переменных языка шейдера высокого уровня (HLSL):</span><span class="sxs-lookup"><span data-stu-id="5a0a2-152">Here are a few declarations that demonstrate many of the characteristics of high-level shader language (HLSL) variables:</span></span>


```
float4 color;
uniform float4 position : POSITION; 
const float4 lightDirection = {0,0,1};
```



<span data-ttu-id="5a0a2-153">В объявлениях данных может использоваться любой допустимый тип, включая:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-153">Data declarations can use any valid type including:</span></span>

-   [<span data-ttu-id="5a0a2-154">Типы данных (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-154">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
-   [<span data-ttu-id="5a0a2-155">Тип вектора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-155">Vector Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-vector.md)
-   [<span data-ttu-id="5a0a2-156">Тип матрицы (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-156">Matrix Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-matrix.md)
-   [<span data-ttu-id="5a0a2-157">Тип шейдера (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-157">Shader Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-shader.md)
-   [<span data-ttu-id="5a0a2-158">Тип образца (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-158">Sampler Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-sampler.md)
-   [<span data-ttu-id="5a0a2-159">Определяемый пользователем тип (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-159">User-Defined Type (DirectX HLSL)</span></span>](dx-graphics-hlsl-user-defined.md)

<span data-ttu-id="5a0a2-160">Шейдер может иметь переменные верхнего уровня, аргументы и функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-160">A shader can have top-level variables, arguments, and functions.</span></span>


```
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```



<span data-ttu-id="5a0a2-161">Переменные верхнего уровня объявляются за пределами всех функций.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-161">Top-level variables are declared outside of all functions.</span></span> <span data-ttu-id="5a0a2-162">Аргументы верхнего уровня — это параметры функции верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-162">Top-level arguments are parameters to a top-level function.</span></span> <span data-ttu-id="5a0a2-163">Функция верхнего уровня — это любая функция, вызываемая приложением (в отличие от функции, которая вызывается другой функцией).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-163">A top-level function is any function called by the application (as opposed to a function that is called by another function).</span></span>

### <a name="uniform-shader-inputs"></a><span data-ttu-id="5a0a2-164">Входные данные универсального шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-164">Uniform Shader Inputs</span></span>

<span data-ttu-id="5a0a2-165">Шейдеры вершин и пикселей принимают два вида входных данных: разные и однородные.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-165">Vertex and pixel shaders accept two kinds of input data: varying and uniform.</span></span> <span data-ttu-id="5a0a2-166">Различные входные данные являются уникальными для каждого выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-166">The varying input is the data that is unique to each execution of the shader.</span></span> <span data-ttu-id="5a0a2-167">Для шейдера вершин различные данные (например, "расположение", "нормальный" и т. д.) поступают из потоков вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-167">For a vertex shader, the varying data (for example: position, normal, etc.) comes from the vertex streams.</span></span> <span data-ttu-id="5a0a2-168">Однородные данные (например, "цвет материала", "универсальное преобразование" и т. д.) являются постоянными для нескольких выполнений шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-168">The uniform data (for example: material color, world transform, etc.) is constant for multiple executions of a shader.</span></span> <span data-ttu-id="5a0a2-169">Для тех, кто знаком с моделями шейдера сборки, универсальные данные задаются постоянными регистрами и различными данными по регистрам v и t.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-169">For those familiar with the assembly shader models, uniform data is specified by constant registers and varying data by the v and t registers.</span></span>

<span data-ttu-id="5a0a2-170">Однородные данные могут быть заданы двумя методами.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-170">Uniform data can be specified by two methods.</span></span> <span data-ttu-id="5a0a2-171">Наиболее распространенным методом является объявление глобальных переменных и их использование в шейдере.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-171">The most common method is to declare global variables and use them within a shader.</span></span> <span data-ttu-id="5a0a2-172">Любое использование глобальных переменных в шейдере приведет к добавлению этой переменной в список универсальных переменных, необходимых для этого шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-172">Any use of global variables within a shader will result in adding that variable to the list of uniform variables required by that shader.</span></span> <span data-ttu-id="5a0a2-173">Второй метод заключается в пометке входного параметра функции шейдера верхнего уровня как универсального.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-173">The second method is to mark an input parameter of the top-level shader function as uniform.</span></span> <span data-ttu-id="5a0a2-174">Эта маркировка указывает, что заданная переменная должна быть добавлена в список универсальных переменных.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-174">This marking specifies that the given variable should be added to the list of uniform variables.</span></span>

<span data-ttu-id="5a0a2-175">Универсальные переменные, используемые шейдером, передаются обратно в приложение через таблицу констант.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-175">Uniform variables used by a shader are communicated back to the application via the constant table.</span></span> <span data-ttu-id="5a0a2-176">Таблица констант — это имя таблицы символов, которое определяет, как универсальные переменные, используемые шейдером, помещаются в постоянные регистры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-176">The constant table is the name for the symbol table that defines how the uniform variables used by a shader fit into the constant registers.</span></span> <span data-ttu-id="5a0a2-177">Параметры универсальной функции отображаются в таблице констант в начале символа доллара ($), в отличие от глобальных переменных.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-177">The uniform function parameters appear in the constant table prepended with a dollar sign ($), unlike the global variables.</span></span> <span data-ttu-id="5a0a2-178">Знак доллара необходим, чтобы избежать конфликтов имен между локальными универсальными входными данными и глобальными переменными с одним и тем же именем.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-178">The dollar sign is required to avoid name collisions between local uniform inputs and global variables of the same name.</span></span>

<span data-ttu-id="5a0a2-179">Таблица констант содержит расположения регистров констант всех универсальных переменных, используемых шейдером.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-179">The constant table contains the constant register locations of all uniform variables used by the shader.</span></span> <span data-ttu-id="5a0a2-180">Таблица также содержит сведения о типе и значение по умолчанию, если оно указано.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-180">The table also includes the type information and the default value, if specified.</span></span>

### <a name="varying-shader-inputs-and-semantics"></a><span data-ttu-id="5a0a2-181">Различные входные и семантические значения шейдера</span><span class="sxs-lookup"><span data-stu-id="5a0a2-181">Varying Shader Inputs and Semantics</span></span>

<span data-ttu-id="5a0a2-182">Различные входные параметры (функции шейдера верхнего уровня) должны быть помечены как семантическое или универсальное ключевое слово, указывающее, что значение является константой для выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-182">Varying input parameters (of a top-level shader function) must be marked either with a semantic or uniform keyword indicating the value is constant for the execution of the shader.</span></span> <span data-ttu-id="5a0a2-183">Если входные шейдеры верхнего уровня не помечены семантическим или равномерным ключевым словом, то шейдер не будет компилироваться.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-183">If a top-level shader input is not marked with a semantic or uniform keyword, then the shader will fail to compile.</span></span>

<span data-ttu-id="5a0a2-184">Семантика ввода — это имя, используемое для связывания заданного ввода с выходными данными предыдущей части графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-184">The input semantic is a name used to link the given input to an output of the previous part of the graphics pipeline.</span></span> <span data-ttu-id="5a0a2-185">Например, в шейдере вершин используется входная семантическая POSITION0 для указания места, где должны быть связаны данные о положении из буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-185">For example, the input semantic POSITION0 is used by the vertex shaders to specify where the position data from the vertex buffer should be linked.</span></span>

<span data-ttu-id="5a0a2-186">Шейдеры пикселей и вершин имеют разные наборы входных данных в соответствии с различными частями графического конвейера, которые передаются в каждый блок шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-186">Pixel and vertex shaders have different sets of input semantics due to the different parts of the graphics pipeline that feed into each shader unit.</span></span> <span data-ttu-id="5a0a2-187">Семантика ввода шейдера вершин описывает сведения о каждой вершине (например: расположение, нормаль, координаты текстуры, цвет, тангенс, бинормал и т. д.), загружаемые из буфера вершин в форму, которая может использоваться шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-187">Vertex shader input semantics describe the per-vertex information (for example: position, normal, texture coordinates, color, tangent, binormal, etc.) to be loaded from a vertex buffer into a form that can be consumed by the vertex shader.</span></span> <span data-ttu-id="5a0a2-188">Семантика ввода непосредственно сопоставляется с использованием объявления вершин и индекса использования.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-188">The input semantics directly map to the vertex declaration usage and the usage index.</span></span>

<span data-ttu-id="5a0a2-189">Семантика ввода шейдера пикселей описывает сведения, предоставляемые на пиксель блоком растрирования.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-189">Pixel shader input semantics describe the information that is provided per pixel by the rasterization unit.</span></span> <span data-ttu-id="5a0a2-190">Данные создаются путем интерполяции между выходными данными шейдера вершин для каждой вершины текущего примитива.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-190">The data is generated by interpolating between outputs of the vertex shader for each vertex of the current primitive.</span></span> <span data-ttu-id="5a0a2-191">Семантическая семантика ввода шейдера пикселей связывает цвет вывода и сведения о координатах текстуры с входными параметрами.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-191">The basic pixel shader input semantics link the output color and texture coordinate information to input parameters.</span></span>

<span data-ttu-id="5a0a2-192">Семантика ввода может быть назначена входным шейдером двумя методами:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-192">Input semantics can be assigned to shader input by two methods:</span></span>

-   <span data-ttu-id="5a0a2-193">Добавление двоеточия и семантического имени в объявление параметра.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-193">Appending a colon and the semantic name to the parameter declaration.</span></span>
-   <span data-ttu-id="5a0a2-194">Определение входной структуры с семантикой ввода, назначенной каждому члену структуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-194">Defining an input structure with input semantics assigned to each structure member.</span></span>

<span data-ttu-id="5a0a2-195">Шейдер вершин и пиксель предоставляют выходные данные на последующий этап графического конвейера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-195">Vertex and pixel shaders provide output data to the subsequent graphics pipeline stage.</span></span> <span data-ttu-id="5a0a2-196">Семантика вывода используется для указания того, как данные, формируемые шейдером, должны быть связаны с входами следующего этапа.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-196">Output semantics are used to specify how data generated by the shader should be linked to the inputs of the next stage.</span></span> <span data-ttu-id="5a0a2-197">Например, семантика вывода для шейдера вершин используется для связывания выходных данных интерполяции в средствах программ-прорисовки, чтобы создать входные данные для шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-197">For example, the output semantics for a vertex shader are used to link the outputs of the interpolators in the rasterizer to generate the input data for the pixel shader.</span></span> <span data-ttu-id="5a0a2-198">Выходные данные шейдера пикселей являются значениями, переданными в альфа-смешение для каждого целевого объекта прорисовки, или значение глубины, записанное в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-198">The pixel shader outputs are the values provided to the alpha blending unit for each of the render targets or the depth value written to the depth buffer.</span></span>

<span data-ttu-id="5a0a2-199">Семантика вывода шейдера вершин используется для связи шейдера с шейдером пикселей и с стадией средства развертки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-199">Vertex shader output semantics are used to link the shader both to the pixel shader and to the rasterizer stage.</span></span> <span data-ttu-id="5a0a2-200">Шейдер вершин, используемый средством программной прорисовки и недоступный для шейдера пикселей, должен создавать данные о положении как минимум.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-200">A vertex shader that is consumed by the rasterizer and not exposed to the pixel shader must generate position data as a minimum.</span></span> <span data-ttu-id="5a0a2-201">Шейдеры вершин, создающие координаты текстуры и данные цвета, предоставляют эти данные в шейдер пикселей после выполнения интерполяции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-201">Vertex shaders that generate texture coordinate and color data provide that data to a pixel shader after interpolation is done.</span></span>

<span data-ttu-id="5a0a2-202">Семантика вывода шейдера пикселей привязывает выходные цвета шейдера пикселей к правильному целевому объекту рендеринга.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-202">Pixel shader output semantics bind the output colors of a pixel shader with the correct render target.</span></span> <span data-ttu-id="5a0a2-203">Выходной цвет шейдера пикселей связан с стадией альфа-смешения, который определяет, как изменяются целевые объекты отрисовки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-203">The pixel shader output color is linked to the alpha blend stage, which determines how the destination render targets are modified.</span></span> <span data-ttu-id="5a0a2-204">Выходные данные глубины шейдера пикселей можно использовать для изменения значений глубины назначения в текущем растровом расположении.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-204">The pixel shader depth output can be used to change the destination depth values at the current raster location.</span></span> <span data-ttu-id="5a0a2-205">Выходные данные глубины и несколько целевых объектов рендеринга поддерживаются только в некоторых моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-205">The depth output and multiple render targets are only supported with some shader models.</span></span>

<span data-ttu-id="5a0a2-206">Синтаксис для семантики вывода идентичен синтаксису для указания семантики ввода.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-206">The syntax for output semantics is identical to the syntax for specifying input semantics.</span></span> <span data-ttu-id="5a0a2-207">Семантика может быть указана непосредственно в параметрах, объявленных как "out", или назначена во время определения структуры, возвращаемой как параметр "out", либо возвращаемое значение функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-207">The semantics can be either specified directly on parameters declared as "out" parameters or assigned during the definition of a structure that either returned as an "out" parameter or the return value of a function.</span></span>

<span data-ttu-id="5a0a2-208">Семантика определяет, откуда поступают данные.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-208">Semantics identify where data comes from.</span></span> <span data-ttu-id="5a0a2-209">Семантика — это необязательные идентификаторы, которые определяют входные и выходные данные шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-209">Semantics are optional identifiers that identify shader inputs and outputs.</span></span> <span data-ttu-id="5a0a2-210">Семантика отображается в одном из трех мест:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-210">Semantics appear in one of three places:</span></span>

-   <span data-ttu-id="5a0a2-211">После элемента структуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-211">After a structure member.</span></span>
-   <span data-ttu-id="5a0a2-212">После аргумента в списке входных аргументов функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-212">After an argument in a function's input argument list.</span></span>
-   <span data-ttu-id="5a0a2-213">После списка входных аргументов функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-213">After the function's input argument list.</span></span>

<span data-ttu-id="5a0a2-214">В этом примере используется структура для предоставления одного или нескольких входных шейдеров вершин и еще одна структура для предоставления одного или нескольких выходных данных шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-214">This example uses a structure to provide one or more vertex shader inputs, and another structure to provide one or more vertex shader outputs.</span></span> <span data-ttu-id="5a0a2-215">Каждый из членов структуры использует семантику.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-215">Each of the structure members uses a semantic.</span></span>


```
vector vClr;

struct VS_INPUT
{
    float4 vPosition : POSITION;
    float3 vNormal : NORMAL;
    float4 vBlendWeights : BLENDWEIGHT;
};

struct VS_OUTPUT
{
    float4  vPosition : POSITION;
    float4  vDiffuse : COLOR;

};

float4x4 mWld1;
float4x4 mWld2;
float4x4 mWld3;
float4x4 mWld4;

float Len;
float4 vLight;

float4x4 mTot;

VS_OUTPUT VS_Skinning_Example(const VS_INPUT v, uniform float len=100)
{
    VS_OUTPUT out;

    // Skin position (to world space)
    float3 vPosition = 
        mul(v.vPosition, (float4x3) mWld1) * v.vBlendWeights.x +
        mul(v.vPosition, (float4x3) mWld2) * v.vBlendWeights.y +
        mul(v.vPosition, (float4x3) mWld3) * v.vBlendWeights.z +
        mul(v.vPosition, (float4x3) mWld4) * v.vBlendWeights.w;
    // Skin normal (to world space)
    float3 vNormal =
        mul(v.vNormal, (float3x3) mWld1) * v.vBlendWeights.x + 
        mul(v.vNormal, (float3x3) mWld2) * v.vBlendWeights.y + 
        mul(v.vNormal, (float3x3) mWld3) * v.vBlendWeights.z + 
        mul(v.vNormal, (float3x3) mWld4) * v.vBlendWeights.w;
    
    // Output stuff
    out.vPosition    = mul(float4(vPosition + vNormal * Len, 1), mTot);
    out.vDiffuse  = dot(vLight,vNormal);

    return out;
}
```



<span data-ttu-id="5a0a2-216">Входная структура определяет данные из буфера вершин, которые будут предоставлять входные шейдеры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-216">The input structure identifies the data from the vertex buffer that will provide the shader inputs.</span></span> <span data-ttu-id="5a0a2-217">Этот шейдер сопоставляет данные из элементов "расположение", "нормальный" и "блендвеигхт" в буфере вершин с регистрами шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-217">This shader maps the data from the position, normal, and blendweight elements of the vertex buffer into vertex shader registers.</span></span> <span data-ttu-id="5a0a2-218">Тип входных данных не должен точно совпадать с типом данных объявления вершины.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-218">The input data type does not have to exactly match the vertex declaration data type.</span></span> <span data-ttu-id="5a0a2-219">Если он не полностью соответствует, данные вершин будут автоматически преобразованы в тип данных HLSL при его написании в регистрах шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-219">If it doesn't exactly match, the vertex data will automatically be converted into the HLSL's data type when it is written into the shader registers.</span></span> <span data-ttu-id="5a0a2-220">Например, если обычные данные были определены в приложении как тип UINT, они будут преобразованы в float3 при чтении шейдером.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-220">For instance, if the normal data were defined to be of type UINT by the application, it would be converted into a float3 when read by the shader.</span></span>

<span data-ttu-id="5a0a2-221">Если данные в потоке вершин содержат меньше компонентов, чем соответствующий тип данных шейдера, отсутствующие компоненты будут инициализированы значением 0 (за исключением w, который инициализируется значением 1).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-221">If the data in the vertex stream contains fewer components than the corresponding shader data type, the missing components will be initialized to 0 (except for w, which is initialized to 1).</span></span>

<span data-ttu-id="5a0a2-222">Семантика ввода аналогична значениям в [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-222">Input semantics are similar to the values in the [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span>

<span data-ttu-id="5a0a2-223">Выходная структура определяет выходные параметры шейдера вершин в параметрах "расположение" и "цвет".</span><span class="sxs-lookup"><span data-stu-id="5a0a2-223">The output structure identifies the vertex shader output parameters of position and color.</span></span> <span data-ttu-id="5a0a2-224">Эти выходные данные будут использоваться конвейером для растрирования треугольника (при простой обработке).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-224">These outputs will be used by the pipeline for triangle rasterization (in primitive processing).</span></span> <span data-ttu-id="5a0a2-225">Вывод, помеченный как данные о положении, определяет расположение вершины в однородном пространстве.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-225">The output marked as position data denotes the position of a vertex in homogeneous space.</span></span> <span data-ttu-id="5a0a2-226">Как минимум Вершинный шейдер должен формировать данные о положении.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-226">As a minimum, a vertex shader must generate position data.</span></span> <span data-ttu-id="5a0a2-227">Положение пространства на экране вычислено после завершения шейдера вершин путем деления координат (x, y, z) на w.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-227">The screen space position is computed after the vertex shader completes by dividing the (x, y, z) coordinate by w.</span></span> <span data-ttu-id="5a0a2-228">В пространстве экрана-1 и 1 — минимальное и максимальное значения x и y границ окна просмотра, а z — для тестирования z-буфера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-228">In screen space, -1 and 1 are the minimum and maximum x and y values of the boundaries of the viewport, while z is used for z-buffer testing.</span></span>

<span data-ttu-id="5a0a2-229">Семантика вывода также аналогична значениям в [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-229">Output semantics are also similar to the values in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage).</span></span> <span data-ttu-id="5a0a2-230">В общем случае выходная структура для шейдера вершин также может использоваться в качестве входной структуры для шейдера пикселей, если построитель текстуры не считывает данные из любой переменной, помеченной как расположение, размер точки или семантика тумана.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-230">In general, an output structure for a vertex shader can also be used as the input structure for a pixel shader, provided the pixel shader does not read from any variable marked with the position, point size, or fog semantics.</span></span> <span data-ttu-id="5a0a2-231">Эти семантики связаны с скалярными значениями для каждой вершины, которые не используются в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-231">These semantics are associated with per-vertex scalar values that are not used by a pixel shader.</span></span> <span data-ttu-id="5a0a2-232">Если эти значения необходимы для шейдера пикселей, их можно скопировать в другую выходную переменную, использующую семантику шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-232">If these values are needed for the pixel shader, they can be copied into another output variable that uses a pixel shader semantic.</span></span>

<span data-ttu-id="5a0a2-233">Глобальные переменные назначаются для регистрации автоматически компилятором.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-233">Global variables are assigned to registers automatically by the compiler.</span></span> <span data-ttu-id="5a0a2-234">Глобальные переменные также называются единообразными, поскольку содержимое переменной одинаково для всех пикселей, обрабатываемых при каждом вызове шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-234">Global variables are also called uniform parameters because the contents of the variable is the same for all pixels processed each time the shader is called.</span></span> <span data-ttu-id="5a0a2-235">Регистры содержатся в таблице констант, которую можно считать с помощью интерфейса [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) .</span><span class="sxs-lookup"><span data-stu-id="5a0a2-235">The registers are contained in the constant table, which can be read using the [**ID3DXConstantTable**](/windows/desktop/direct3d9/id3dxconstanttable) interface.</span></span>

<span data-ttu-id="5a0a2-236">Семантика ввода для шейдеров пикселей сопоставляет значения с конкретными аппаратными регистрами для транспортировки между шейдерами вершин и шейдерами пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-236">Input semantics for pixel shaders map values into specific hardware registers for transport between vertex shaders and pixel shaders.</span></span> <span data-ttu-id="5a0a2-237">Каждый тип регистра имеет определенные свойства.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-237">Each register type has specific properties.</span></span> <span data-ttu-id="5a0a2-238">Поскольку в настоящее время существует только две семантики для цветов и координат текстуры, большинство данных обычно помечаются как координаты текстуры, даже если это не так.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-238">Because there are currently only two semantics for color and texture coordinates, it is common for most data to be marked as a texture coordinate even when it is not.</span></span>

<span data-ttu-id="5a0a2-239">Обратите внимание, что выходная структура шейдера вершин использует входные данные с данными о положении, которые не используются шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-239">Notice that the vertex shader output structure used an input with position data, which is not used by the pixel shader.</span></span> <span data-ttu-id="5a0a2-240">HLSL позволяет использовать допустимые выходные данные шейдера вершин, которые не являются допустимыми входными данными для шейдера пикселей при условии, что на него нет ссылок в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-240">HLSL allows valid output data of a vertex shader that is not valid input data for a pixel shader, provided that it is not referenced in the pixel shader.</span></span>

<span data-ttu-id="5a0a2-241">Входные аргументы также могут быть массивами.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-241">Input arguments can also be arrays.</span></span> <span data-ttu-id="5a0a2-242">Семантика автоматически увеличивается компилятором для каждого элемента массива.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-242">Semantics are automatically incremented by the compiler for each element of the array.</span></span> <span data-ttu-id="5a0a2-243">Например, рассмотрим следующее явное объявление:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-243">For instance, consider the following explicit declaration:</span></span>


```
struct VS_OUTPUT
{
    float4 Position   : POSITION;
    float3 Diffuse    : COLOR0;
    float3 Specular   : COLOR1;               
    float3 HalfVector : TEXCOORD3;
    float3 Fresnel    : TEXCOORD2;               
    float3 Reflection : TEXCOORD0;               
    float3 NoiseCoord : TEXCOORD1;               
};

float4 Sparkle(VS_OUTPUT In) : COLOR
```



<span data-ttu-id="5a0a2-244">Явное объявление, приведенное выше, эквивалентно следующему объявлению, в котором семантика будет автоматически увеличиваться компилятором:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-244">The explicit declaration given above is equivalent to the following declaration that will have semantics automatically incremented by the compiler:</span></span>


```
float4 Sparkle(float4 Position : POSITION,
                 float3 Col[2] : COLOR0,
                 float3 Tex[4] : TEXCOORD0) : COLOR0
{
   // shader statements
   ...
```



<span data-ttu-id="5a0a2-245">Точно так же, как и семантика ввода, семантика вывода определяет использование данных для выходных данных построителя текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-245">Just like input semantics, output semantics identify data usage for pixel shader output data.</span></span> <span data-ttu-id="5a0a2-246">Многие шейдеры пикселей записывают только один выходной цвет.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-246">Many pixel shaders write to only one output color.</span></span> <span data-ttu-id="5a0a2-247">Шейдеры пикселей также могут записывать значение глубины в один или несколько целевых объектов отрисовки одновременно (до четырех).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-247">Pixel shaders can also write out a depth value into one or more multiple render targets at the same time (up to four).</span></span> <span data-ttu-id="5a0a2-248">Как и шейдеры вершин, шейдеры пикселей используют структуру для возвращения более чем одного результата.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-248">Like vertex shaders, pixel shaders use a structure to return more than one output.</span></span> <span data-ttu-id="5a0a2-249">Этот шейдер записывает 0 в компоненты цвета, а также в компонент глубины.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-249">This shader writes 0 to the color components, as well as to the depth component.</span></span>


```
struct PS_OUTPUT
{
    float4 Color[4] : COLOR0;
    float  Depth  : DEPTH;
};

PS_OUTPUT main(void)
{
    PS_OUTPUT out;

   // Shader statements
   ...

  // Write up to four pixel shader output colors
  out.Color[0] =  ...
  out.Color[1] =  ...
  out.Color[2] =  ...
  out.Color[3] =  ...

  // Write pixel depth 
  out.Depth =  ...

    return out;
}
```



<span data-ttu-id="5a0a2-250">Выходные цвета шейдера пикселей должны иметь тип float4.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-250">Pixel shader output colors must be of type float4.</span></span> <span data-ttu-id="5a0a2-251">При записи нескольких цветов все выходные цвета должны использоваться последовательно.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-251">When writing multiple colors, all output colors must be used contiguously.</span></span> <span data-ttu-id="5a0a2-252">Иными словами, [COLOR1](dx-graphics-hlsl-semantics.md) не может быть выходным, если [COLOR0](dx-graphics-hlsl-semantics.md) уже не записан.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-252">In other words, [COLOR1](dx-graphics-hlsl-semantics.md) cannot be an output unless [COLOR0](dx-graphics-hlsl-semantics.md) has already been written.</span></span> <span data-ttu-id="5a0a2-253">Выходные данные глубины шейдера пикселей должны иметь тип float1.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-253">Pixel shader depth output must be of type float1.</span></span>

### <a name="samplers-and-texture-objects"></a><span data-ttu-id="5a0a2-254">Пробы и объекты текстуры</span><span class="sxs-lookup"><span data-stu-id="5a0a2-254">Samplers and Texture Objects</span></span>

<span data-ttu-id="5a0a2-255">Образец содержит состояние образца.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-255">A sampler contains sampler state.</span></span> <span data-ttu-id="5a0a2-256">Состояние образца определяет текстуру для выборки и управляет фильтрацией, выполненной во время выборки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-256">Sampler state specifies the texture to be sampled, and controls the filtering that is done during sampling.</span></span> <span data-ttu-id="5a0a2-257">Для выборки текстуры необходимы три вещи.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-257">Three things are required to sample a texture:</span></span>

-   <span data-ttu-id="5a0a2-258">Текстура</span><span class="sxs-lookup"><span data-stu-id="5a0a2-258">A texture</span></span>
-   <span data-ttu-id="5a0a2-259">Образец (с состоянием образца)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-259">A sampler (with sampler state)</span></span>
-   <span data-ttu-id="5a0a2-260">Инструкция выборки</span><span class="sxs-lookup"><span data-stu-id="5a0a2-260">A sampling instruction</span></span>

<span data-ttu-id="5a0a2-261">Пробы можно инициализировать с помощью текстур и состояния образца, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-261">Samplers can be initialized with textures and sampler state as shown here:</span></span>


```
sampler s = sampler_state 
{ 
  texture = NULL; 
  mipfilter = LINEAR; 
};
```



<span data-ttu-id="5a0a2-262">Ниже приведен пример кода для выборки двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-262">Here's an example of the code to sample a 2D texture:</span></span>


```
texture tex0;
sampler2D s_2D;

float2 sample_2D(float2 tex : TEXCOORD0) : COLOR
{
  return tex2D(s_2D, tex);
}
```



<span data-ttu-id="5a0a2-263">Текстура объявляется с помощью переменной текстуры tex0.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-263">The texture is declared with a texture variable tex0.</span></span>

<span data-ttu-id="5a0a2-264">В этом примере объявляется переменная образца с именем s \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-264">In this example, a sampler variable named s\_2D is declared.</span></span> <span data-ttu-id="5a0a2-265">Образец содержит состояние образца внутри фигурных скобок.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-265">The sampler contains the sampler state inside of curly braces.</span></span> <span data-ttu-id="5a0a2-266">Это включает в себя текстуру, которая будет выдавать выборку и, при необходимости, состояние фильтра (т. е. режимы переноса, режимы фильтрации и т. д.).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-266">This includes the texture that will be sampled and, optionally, the filter state (that is, wrap modes, filter modes, etc.).</span></span> <span data-ttu-id="5a0a2-267">Если состояние выборки опущено, то применяется состояние образца по умолчанию, определяющее линейную фильтрацию и режим переноса для координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-267">If the sampler state is omitted, a default sampler state is applied specifying linear filtering and a wrap mode for the texture coordinates.</span></span> <span data-ttu-id="5a0a2-268">Функция выборки принимает координату текстуры с плавающей точкой с двумя компонентами и возвращает цвет из двух компонентов.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-268">The sampler function takes a two-component floating-point texture coordinate, and returns a two-component color.</span></span> <span data-ttu-id="5a0a2-269">Он представлен типом возвращаемого значения float2 и представляет данные в красном и зеленом компонентах.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-269">This is represented with the float2 return type and represents data in the red and green components.</span></span>

<span data-ttu-id="5a0a2-270">Определены четыре типа выборки (см. [Ключевые слова](dx-graphics-hlsl-appendix.md)), а поиск текстур выполняется встроенными функциями: [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**текскубе (s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-270">Four types of samplers are defined (see [Keywords](dx-graphics-hlsl-appendix.md)) and texture lookups are performed by the intrinsic functions: [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md), [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md), [**tex3D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex3d.md), [**texCUBE(s, t) (DirectX HLSL)**](dx-graphics-hlsl-texcube.md).</span></span> <span data-ttu-id="5a0a2-271">Ниже приведен пример трехмерной выборки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-271">Here is an example of 3D sampling:</span></span>


```
texture tex0;
sampler3D s_3D;

float3 sample_3D(float3 tex : TEXCOORD0) : COLOR
{
  return tex3D(s_3D, tex);
}
```



<span data-ttu-id="5a0a2-272">В этом объявлении образца используется состояние образца по умолчанию для параметров фильтра и режима адреса.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-272">This sampler declaration uses default sampler state for the filter settings and address mode.</span></span>

<span data-ttu-id="5a0a2-273">Ниже приведен пример соответствующей выборки Куба.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-273">Here is the corresponding cube sampling example:</span></span>


```
texture tex0;
samplerCUBE s_CUBE;

float3 sample_CUBE(float3 tex : TEXCOORD0) : COLOR
{
  return texCUBE(s_CUBE, tex);
}
```



<span data-ttu-id="5a0a2-274">И, наконец, ниже приведен пример одномерной выборки:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-274">And finally, here is the 1D sampling example:</span></span>


```
texture tex0;
sampler1D s_1D;

float sample_1D(float tex : TEXCOORD0) : COLOR
{
  return tex1D(s_1D, tex);
}
```



<span data-ttu-id="5a0a2-275">Так как среда выполнения не поддерживает одномерное текстуры, компилятор будет использовать двухмерную текстуру с набором знаний, что координата y не имеет значения.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-275">Because the runtime does not support 1D textures, the compiler will use a 2D texture with the knowledge that the y-coordinate is unimportant.</span></span> <span data-ttu-id="5a0a2-276">Поскольку [**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) реализован в виде 2D-поиска текстур, компилятор может эффективно выбирать компонент y.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-276">Since [**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) is implemented as a 2D texture lookup, the compiler is free to choose the y-component in an efficient manner.</span></span> <span data-ttu-id="5a0a2-277">В некоторых редких случаях компилятор не может выбрать эффективный компонент y, в этом случае будет выдаваться предупреждение.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-277">In some rare scenarios, the compiler cannot choose an efficient y-component, in which case it will issue a warning.</span></span>


```
texture tex0;
sampler s_1D_float;

float4 main(float texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float, texCoords);
}
```



<span data-ttu-id="5a0a2-278">Этот пример неэффективен, так как компилятор должен переместить входную координату в другой регистр (поскольку Уточняющий запрос одномерного типа реализуется как 2D-Поиск, а координата текстуры объявлена как float1).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-278">This particular example is inefficient because the compiler must move the input coordinate into another register (because a 1D lookup is implemented as a 2D lookup and the texture coordinate is declared as a float1).</span></span> <span data-ttu-id="5a0a2-279">Если код перезаписывается с использованием входных данных float2 вместо float1, компилятор может использовать входную координату текстуры, так как известно, что y инициализировано как-то.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-279">If the code is rewritten using a float2 input instead of a float1, the compiler can use the input texture coordinate because it knows that y is initialized to something.</span></span>


```
texture tex0;
sampler s_1D_float2;

float4 main(float2 texCoords : TEXCOORD) : COLOR
{
    return tex1D(s_1D_float2, texCoords);
}
```



<span data-ttu-id="5a0a2-280">Все поиски текстур можно добавить с помощью "смещения" или "proj" (то есть [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**ТЕКСКУБЕПРОЖ (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-280">All texture lookups can be appended with "bias" or "proj" (that is, [**tex2Dbias (DirectX HLSL)**](dx-graphics-hlsl-tex2dbias.md), [**texCUBEproj (DirectX HLSL)**](dx-graphics-hlsl-texcubeproj.md)).</span></span> <span data-ttu-id="5a0a2-281">При использовании суффикса "proj" Координата текстуры делится на компонент w-Component.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-281">With the "proj" suffix, the texture coordinate is divided by the w-component.</span></span> <span data-ttu-id="5a0a2-282">При «смещении» уровень MIP смещается на w-Component.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-282">With "bias," the mip level is shifted by the w-component.</span></span> <span data-ttu-id="5a0a2-283">Таким же, все поиски текстур с суффиксом всегда принимают float4 входные данные.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-283">Thus, all texture lookups with a suffix always take a float4 input.</span></span> <span data-ttu-id="5a0a2-284">[**tex1D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) и [**tex2D (s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) игнорируют компоненты из и z соответственно.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-284">[**tex1D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex1d.md) and [**tex2D(s, t) (DirectX HLSL)**](dx-graphics-hlsl-tex2d.md) ignore the yz- and z-components respectively.</span></span>

<span data-ttu-id="5a0a2-285">В массиве также можно использовать пробы, хотя в настоящее время нет серверной части, поддерживающей динамический доступ к массиву образцов.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-285">Samplers may also be used in array, although no back end currently supports dynamic array access of samplers.</span></span> <span data-ttu-id="5a0a2-286">Таким образом, следующий код является допустимым, так как он может быть разрешен во время компиляции:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-286">Therefore, the following is valid because it can be resolved at compile time:</span></span>


```
tex2D(s[0],tex)
```



<span data-ttu-id="5a0a2-287">Однако этот пример является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-287">However, this example is not valid.</span></span>


```
tex2D(s[a],tex)
```



<span data-ttu-id="5a0a2-288">Динамический доступ к пробам в основном полезен для написания программ с помощью литеральных циклов.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-288">Dynamic access of samplers is primarily useful for writing programs with literal loops.</span></span> <span data-ttu-id="5a0a2-289">Следующий код иллюстрирует доступ к массиву образцов:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-289">The following code illustrates sampler array accessing:</span></span>


```
sampler sm[4];

float4 main(float4 tex[4] : TEXCOORD) : COLOR
{
    float4 retColor = 1;

    for(int i = 0; i < 4;i++)
    {
        retColor *= tex2D(sm[i],tex[i]);
    }

    return retColor;
}
```



> [!Note]
>
> <span data-ttu-id="5a0a2-290">Использование среды выполнения отладки Microsoft Direct3D может помочь в перехвате несоответствий между числом компонентов в текстуре и образцом.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-290">Using the Microsoft Direct3D debug runtime can help you catch mismatches between the number of components in a texture and a sampler.</span></span>

 

## <a name="writing-functions"></a><span data-ttu-id="5a0a2-291">Написание функций</span><span class="sxs-lookup"><span data-stu-id="5a0a2-291">Writing Functions</span></span>

<span data-ttu-id="5a0a2-292">Функции разбивают большие задачи на меньшие.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-292">Functions break large tasks into smaller ones.</span></span> <span data-ttu-id="5a0a2-293">Небольшие задачи проще в отладке и могут использоваться повторно, если они проверены.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-293">Small tasks are easier to debug and can be reused, once proven.</span></span> <span data-ttu-id="5a0a2-294">Функции можно использовать для скрытия сведений о других функциях, что упрощает отслеживание программы, состоящей из функций.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-294">Functions can be used to hide details of other functions, which makes a program composed of functions easier to follow.</span></span>

<span data-ttu-id="5a0a2-295">Функции HLSL похожи на функции C несколькими способами: они содержат определение и тело функции, а также объявляют типы возвращаемых значения и списки аргументов.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-295">HLSL functions are similar to C functions in several ways: They both contain a definition and a function body and they both declare return types and argument lists.</span></span> <span data-ttu-id="5a0a2-296">Как и функции C, проверка HLSL выполняет проверку типов аргументов, типов аргументов и возвращаемого значения во время компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-296">Like C functions, HLSL validation does type checking on the arguments, argument types, and the return value during shader compilation.</span></span>

<span data-ttu-id="5a0a2-297">В отличие от функций C, функции точки входа HLSL используют семантику для привязки аргументов функции к входным и выходным данным шейдера (функции HLSL, которые называются внутренними семантиками).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-297">Unlike C functions, HLSL entry point functions use semantics to bind function arguments to shader inputs and outputs (HLSL functions called internally ignore semantics).</span></span> <span data-ttu-id="5a0a2-298">Это упрощает привязку данных буфера к шейдеру и привязывает выходные данные шейдера к входным данным шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-298">This makes it easier to bind buffer data to a shader, and bind shader outputs to shader inputs.</span></span>

<span data-ttu-id="5a0a2-299">Функция содержит объявление и тело, а объявление должно предшествовать телу.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-299">A function contains a declaration and a body, and the declaration must precede the body.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="5a0a2-300">Объявление функции включает все перед фигурными скобками:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-300">The function declaration includes everything in front of the curly braces:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="5a0a2-301">Объявление функции содержит:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-301">A function declaration contains:</span></span>

-   <span data-ttu-id="5a0a2-302">Тип возвращаемого значения</span><span class="sxs-lookup"><span data-stu-id="5a0a2-302">A return type</span></span>
-   <span data-ttu-id="5a0a2-303">Имя функции</span><span class="sxs-lookup"><span data-stu-id="5a0a2-303">A function name</span></span>
-   <span data-ttu-id="5a0a2-304">Список аргументов (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-304">An argument list (optional)</span></span>
-   <span data-ttu-id="5a0a2-305">Семантика вывода (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-305">An output semantic (optional)</span></span>
-   <span data-ttu-id="5a0a2-306">Аннотация (необязательно)</span><span class="sxs-lookup"><span data-stu-id="5a0a2-306">An annotation (optional)</span></span>

<span data-ttu-id="5a0a2-307">Тип возвращаемого значения может быть любым из базовых типов данных HLSL, таких как float4:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-307">The return type can be any of the HLSL basic data types such as a float4:</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
   ...
}
```



<span data-ttu-id="5a0a2-308">Возвращаемым типом может быть структура, которая уже определена:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-308">The return type can be a structure that has already been defined:</span></span>


```
struct VS_OUTPUT
{
    float4  vPosition        : POSITION;
    float4  vDiffuse         : COLOR;
}; 

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="5a0a2-309">Если функция не возвращает значение, в качестве возвращаемого типа можно использовать void.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-309">If the function does not return a value, void can be used as the return type.</span></span>


```
void VertexShader_Tutorial_1(float4 inPos : POSITION )
{
   ...
}
```



<span data-ttu-id="5a0a2-310">Тип возвращаемого значения всегда отображается первым в объявлении функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-310">The return type always appears first in a function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
```



<span data-ttu-id="5a0a2-311">Список аргументов объявляет входные аргументы функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-311">An argument list declares the input arguments to a function.</span></span> <span data-ttu-id="5a0a2-312">Он также может объявлять значения, которые будут возвращены.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-312">It may also declare values that will be returned.</span></span> <span data-ttu-id="5a0a2-313">Некоторые аргументы являются входными и выходными аргументами.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-313">Some arguments are both input and output arguments.</span></span> <span data-ttu-id="5a0a2-314">Ниже приведен пример шейдера, который принимает четыре входных аргумента.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-314">Here is an example of a shader that takes four input arguments.</span></span>


```
float4 Light(float3 LightDir : TEXCOORD1, 
             uniform float4 LightColor,  
             float2 texcrd : TEXCOORD0, 
             uniform sampler samp) : COLOR 
{
    float3 Normal = tex2D(samp,texcrd);

    return dot((Normal*2 - 1), LightDir)*LightColor;
}
```



<span data-ttu-id="5a0a2-315">Эта функция возвращает окончательный цвет, который является смешением образца текстуры и светлого цвета.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-315">This function returns a final color, that is a blend of a texture sample and the light color.</span></span> <span data-ttu-id="5a0a2-316">Функция принимает четыре входных значения.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-316">The function takes four inputs.</span></span> <span data-ttu-id="5a0a2-317">У двух входов есть семантика: Лигхтдир имеет семантику [TEXCOORD1](dx-graphics-hlsl-semantics.md) , а текскрд имеет семантику [TEXCOORD0](dx-graphics-hlsl-semantics.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0a2-317">Two inputs have semantics: LightDir has the [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, and texcrd has the [TEXCOORD0](dx-graphics-hlsl-semantics.md) semantic.</span></span> <span data-ttu-id="5a0a2-318">Семантика означает, что данные для этих переменных будут поступать из буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-318">The semantics mean that the data for these variables will come from the vertex buffer.</span></span> <span data-ttu-id="5a0a2-319">Несмотря на то, что переменная Лигхтдир имеет семантику [TEXCOORD1](dx-graphics-hlsl-semantics.md) , параметр, вероятно, не является координатой текстуры.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-319">Even though the LightDir variable has a [TEXCOORD1](dx-graphics-hlsl-semantics.md) semantic, the parameter is probably not a texture coordinate.</span></span> <span data-ttu-id="5a0a2-320">Семантический тип Текскурдн часто используется для предоставления семантики для типа, который не является стандартным (отсутствует семантика ввода шейдера вершин для самого светлого направления).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-320">The TEXCOORDn semantic type is often used to supply a semantic for a type that is not predefined (there is no vertex shader input semantic for a light direction).</span></span>

<span data-ttu-id="5a0a2-321">Два других входа Лигхтколор и SAMP помечаются ключевым словом [Uniform](dx-graphics-hlsl-appendix.md) .</span><span class="sxs-lookup"><span data-stu-id="5a0a2-321">The other two inputs LightColor and samp are labeled with the [uniform](dx-graphics-hlsl-appendix.md) keyword.</span></span> <span data-ttu-id="5a0a2-322">Это универсальные константы, которые не меняются между вызовами Draw.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-322">These are uniform constants that will not change between draw calls.</span></span> <span data-ttu-id="5a0a2-323">Значения этих параметров берутся из глобальных переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-323">The values for these parameters come from shader global variables.</span></span>

<span data-ttu-id="5a0a2-324">Аргументы могут быть помечены как входные данные с ключевым словом in, а выходные аргументы — ключевым словом out.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-324">Arguments can be labeled as inputs with the in keyword, and output arguments with the out keyword.</span></span> <span data-ttu-id="5a0a2-325">Аргументы не могут передаваться по ссылке; Однако аргумент может быть как входным, так и выходным, если он объявлен с ключевым словом InOut.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-325">Arguments cannot be passed by reference; however, an argument can be both an input and an output if it is declared with the inout keyword.</span></span> <span data-ttu-id="5a0a2-326">Аргументы, передаваемые в функцию, помеченную ключевым словом InOut, считаются копиями исходного объекта до тех пор, пока функция не вернется и они будут скопированы обратно.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-326">Arguments passed to a function that are marked with the inout keyword are considered copies of the original until the function returns, and they are copied back.</span></span> <span data-ttu-id="5a0a2-327">Ниже приведен пример с использованием INOUT:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-327">Here's an example using inout:</span></span>


```
void Increment_ByVal(inout float A, inout float B) 
{ 
    A++; B++;
}
```



<span data-ttu-id="5a0a2-328">Эта функция увеличивает значения в A и B и возвращает их.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-328">This function increments the values in A and B and returns them.</span></span>

<span data-ttu-id="5a0a2-329">Тело функции — это весь код после объявления функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-329">The function body is all of the code after the function declaration.</span></span>


```
float4 VertexShader_Tutorial_1(float4 inPos : POSITION ) : POSITION
{
    return mul(inPos, WorldViewProj );
};
```



<span data-ttu-id="5a0a2-330">Текст состоит из операторов, заключенных в фигурные скобки.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-330">The body consists of statements which are surrounded by curly braces.</span></span> <span data-ttu-id="5a0a2-331">Тело функции реализует все функциональные возможности с помощью переменных, литералов, выражений и инструкций.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-331">The function body implements all of the functionality using variables, literals, expressions, and statements.</span></span>

<span data-ttu-id="5a0a2-332">Текст шейдера выполняет две вещи: он вычисляет матрицу и возвращает результат float4.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-332">The shader body does two things: it performs a matrix multiply and returns a float4 result.</span></span> <span data-ttu-id="5a0a2-333">Умножение матрицы осуществляется с помощью функции [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) , которая выполняет умножение матрицы 4x4.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-333">The matrix multiply is accomplished with the [**mul (DirectX HLSL)**](dx-graphics-hlsl-mul.md) function, which performs a 4x4 matrix multiply.</span></span> <span data-ttu-id="5a0a2-334">**mul (DirectX HLSL)** называется встроенной функцией, так как она уже встроена в библиотеку HLSL функций.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-334">**mul (DirectX HLSL)** is called an intrinsic function because it is already built into the HLSL library of functions.</span></span> <span data-ttu-id="5a0a2-335">Встроенные функции будут подробно рассмотрены в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-335">Intrinsic functions will be covered in more detail in the next section.</span></span>

<span data-ttu-id="5a0a2-336">Матрица умножает сочетание входного вектора POS и составной матрицы Ворлдвиевпрож.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-336">The matrix multiply combines an input vector Pos and a composite matrix WorldViewProj.</span></span> <span data-ttu-id="5a0a2-337">Результат — данные о положении, преобразованные в пространство экрана.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-337">The result is position data transformed into screen space.</span></span> <span data-ttu-id="5a0a2-338">Это минимальный способ обработки шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-338">This is the minimum vertex shader processing we can do.</span></span> <span data-ttu-id="5a0a2-339">Если вместо шейдера вершин использовался конвейер фиксированной функции, то данные вершин могут быть выведены после выполнения этого преобразования.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-339">If we were using the fixed function pipeline instead of a vertex shader, the vertex data could be drawn after doing this transform.</span></span>

<span data-ttu-id="5a0a2-340">Последняя инструкция в теле функции является оператором Return.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-340">The last statement in a function body is a return statement.</span></span> <span data-ttu-id="5a0a2-341">Как и в C, эта инструкция возвращает управление из функции в инструкцию, которая вызвала функцию.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-341">Just like C, this statement returns control from the function to the statement that called the function.</span></span>

<span data-ttu-id="5a0a2-342">Возвращаемые функцией типы могут быть любыми простыми типами данных, определенными в HLSL, включая bool, int половины, float и Double.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-342">Function return types can be any of the simple data types defined in HLSL, including bool, int half, float, and double.</span></span> <span data-ttu-id="5a0a2-343">Возвращаемыми типами могут быть один из сложных типов данных, таких как векторы и матрицы.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-343">Return types can be one of the complex data types such as vectors and matrices.</span></span> <span data-ttu-id="5a0a2-344">Типы HLSL, которые ссылаются на объекты, не могут использоваться в качестве возвращаемых типов.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-344">HLSL types that refer to objects cannot be used as return types.</span></span> <span data-ttu-id="5a0a2-345">Сюда входят PixelShader, вертексшадер, текстура и образцы.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-345">This includes pixelshader, vertexshader, texture, and sampler.</span></span>

<span data-ttu-id="5a0a2-346">Ниже приведен пример функции, которая использует структуру для возвращаемого типа.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-346">Here is an example of a function that uses a structure for a return type.</span></span>


```
float4x4 WorldViewProj : WORLDVIEWPROJ;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VS_HLL_Example(float4 inPos : POSITION )
{
    VS_OUTPUT Out;

    Out.Pos = mul(inPos,  WorldViewProj );

    return Out;
};
```



<span data-ttu-id="5a0a2-347">Тип возвращаемого значения float4 был заменен структурой VS \_ Output, которая теперь содержит один элемент float4.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-347">The float4 return type has been replaced with the structure VS\_OUTPUT, which now contains a single float4 member.</span></span>

<span data-ttu-id="5a0a2-348">Оператор Return сообщает об окончании функции.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-348">A return statement signals the end of a function.</span></span> <span data-ttu-id="5a0a2-349">Это простейший оператор return.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-349">This is the simplest return statement.</span></span> <span data-ttu-id="5a0a2-350">Он возвращает управление из функции в вызывающую программу.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-350">It returns control from the function to the calling program.</span></span> <span data-ttu-id="5a0a2-351">Он не возвращает значения.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-351">It returns no value.</span></span>


```
void main()
{
    return ;
}
```



<span data-ttu-id="5a0a2-352">Оператор return может возвращать одно или несколько значений.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-352">A return statement can return one or more values.</span></span> <span data-ttu-id="5a0a2-353">В этом примере возвращается литеральное значение:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-353">This example returns a literal value:</span></span>


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



<span data-ttu-id="5a0a2-354">Этот пример возвращает скалярный результат выражения:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-354">This example returns the scalar result of an expression:</span></span>


```
return  light.enabled = true ;
```



<span data-ttu-id="5a0a2-355">Этот пример возвращает float4, созданный из локальной переменной и литерала:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-355">This example returns a float4 constructed from a local variable and a literal:</span></span>


```
return  float4(color.rgb, 1) ;
```



<span data-ttu-id="5a0a2-356">Этот пример возвращает float4, созданный на основе результата, возвращенного из подставляемой функции, и несколько литеральных значений:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-356">This example returns a float4 that is constructed from the result returned from an intrinsic function, and a few literal values:</span></span>


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



<span data-ttu-id="5a0a2-357">В этом примере возвращается структура, содержащая один или несколько элементов:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-357">This example returns a structure that contains one or more members:</span></span>


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="flow-control"></a><span data-ttu-id="5a0a2-358">Управление потоком</span><span class="sxs-lookup"><span data-stu-id="5a0a2-358">Flow Control</span></span>

<span data-ttu-id="5a0a2-359">Большинство текущих устройств шейдера вершин и построителя текстуры разработано для выполнения построчного шейдера с выполнением каждой инструкции один раз.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-359">Most current vertex and pixel shader hardware is designed to run a shader line by line, executing each instruction once.</span></span> <span data-ttu-id="5a0a2-360">HLSL поддерживает управление потоком, которое включает в себя статическое ветвление, предикатные инструкции, статические циклы, Динамическое ветвление и динамическое зацикливание.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-360">HLSL supports flow control, which includes static branching, predicated instructions, static looping, dynamic branching, and dynamic looping.</span></span>

<span data-ttu-id="5a0a2-361">Ранее использование оператора if привело к появлению кода шейдера на языке ассемблера, который реализует как сторона If, так и else в потоке кода.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-361">Previously, using an if statement resulted in assembly-language shader code that implements both the if side and the else side of the code flow.</span></span> <span data-ttu-id="5a0a2-362">Ниже приведен пример кода HLSL, который был скомпилирован для VS \_ 1 \_ 1:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-362">Here is an example of the in HLSL code that was compiled for vs\_1\_1:</span></span>


```
if (Value > 0)
    oPos = Value1; 
else
    oPos = Value2; 
```



<span data-ttu-id="5a0a2-363">Вот итоговый код сборки:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-363">And here is the resulting assembly code:</span></span>


```
// Calculate linear interpolation value in r0.w
mov r1.w, c2.x               
slt r0.w, c3.x, r1.w         
// Linear interpolation between value1 and value2
mov r7, -c1                      
add r2, r7, c0                   
mad oPos, r0.w, r2, c1  
```



<span data-ttu-id="5a0a2-364">Некоторые аппаратные средства поддерживают либо статический, либо динамический цикл, но для большинства требуется линейное выполнение.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-364">Some hardware allows for either static or dynamic looping, but most require linear execution.</span></span> <span data-ttu-id="5a0a2-365">В моделях, которые не поддерживают циклы, все циклы должны быть отменены.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-365">On the models that do not support looping, all loops must be unrolled.</span></span> <span data-ttu-id="5a0a2-366">Примером является пример примера [депсоффиелд](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) , использующий невыполненные циклы, даже \_ для \_ шейдеров PS 1 1.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-366">An example is the [DepthOfField Sample](https://msdn.microsoft.com/library/Ee416592(v=VS.85).aspx) sample that uses unrolled loops even for ps\_1\_1 shaders.</span></span>

<span data-ttu-id="5a0a2-367">HLSL теперь включает поддержку каждого из этих типов управления потоком:</span><span class="sxs-lookup"><span data-stu-id="5a0a2-367">HLSL now includes support for each of these types of flow control:</span></span>

-   <span data-ttu-id="5a0a2-368">Статическая ветвь</span><span class="sxs-lookup"><span data-stu-id="5a0a2-368">static branching</span></span>
-   <span data-ttu-id="5a0a2-369">инструкции с предикатами</span><span class="sxs-lookup"><span data-stu-id="5a0a2-369">predicated instructions</span></span>
-   <span data-ttu-id="5a0a2-370">статические циклы</span><span class="sxs-lookup"><span data-stu-id="5a0a2-370">static looping</span></span>
-   <span data-ttu-id="5a0a2-371">Динамическое ветвление</span><span class="sxs-lookup"><span data-stu-id="5a0a2-371">dynamic branching</span></span>
-   <span data-ttu-id="5a0a2-372">динамическое зацикливание</span><span class="sxs-lookup"><span data-stu-id="5a0a2-372">dynamic looping</span></span>

<span data-ttu-id="5a0a2-373">Статическое ветвление позволяет переключать или отключать блоки кода шейдера на основе константы шейдера Boolean.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-373">Static branching allows blocks of shader code to be switched on or off based on a Boolean shader constant.</span></span> <span data-ttu-id="5a0a2-374">Это удобный способ включения или отключения путей кода в зависимости от типа объекта, для которого выполняется визуализация.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-374">This is a convenient method for enabling or disabling code paths based on the type of object currently being rendered.</span></span> <span data-ttu-id="5a0a2-375">Между вызовами Draw можно выбрать, какие функции должны поддерживаться с помощью текущего шейдера, а затем установить логические флаги, необходимые для получения такого поведения.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-375">Between draw calls, you can decide which features you want to support with the current shader and then set the Boolean flags required to get that behavior.</span></span> <span data-ttu-id="5a0a2-376">Все инструкции, отключенные логической константой, пропускаются во время выполнения шейдера.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-376">Any statements that are disabled by a Boolean constant are skipped during shader execution.</span></span>

<span data-ttu-id="5a0a2-377">Наиболее знакомая поддержка ветвления — Динамическое ветвление.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-377">The most familiar branching support is dynamic branching.</span></span> <span data-ttu-id="5a0a2-378">При динамической ветвлении условие сравнения находится в переменной, что означает, что сравнение выполняется для каждой вершины или каждого пикселя во время выполнения (в отличие от сравнения, происходящих во время компиляции, или между двумя вызовами Draw).</span><span class="sxs-lookup"><span data-stu-id="5a0a2-378">With dynamic branching, the comparison condition resides in a variable, which means that the comparison is done for each vertex or each pixel at run time (as opposed to the comparison occurring at compile time, or between two draw calls).</span></span> <span data-ttu-id="5a0a2-379">Снижение производительности — это стоимость ветви, а также стоимость инструкций, выполняемых на стороне филиала.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-379">The performance hit is the cost of the branch plus the cost of the instructions on the side of the branch taken.</span></span> <span data-ttu-id="5a0a2-380">Динамическое ветвление реализуется в модели шейдеров 3 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-380">Dynamic branching is implemented in shader model 3 or higher.</span></span> <span data-ttu-id="5a0a2-381">Оптимизация шейдеров, работающих с этими моделями, аналогична оптимизации кода, выполняемого на ЦП.</span><span class="sxs-lookup"><span data-stu-id="5a0a2-381">Optimizing shaders that work with these models is similar to optimizing code that runs on a CPU.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5a0a2-382">См. также</span><span class="sxs-lookup"><span data-stu-id="5a0a2-382">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a0a2-383">Руководство по программированию для HLSL</span><span class="sxs-lookup"><span data-stu-id="5a0a2-383">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 