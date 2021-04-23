---
title: Синтаксис переменных
description: Используйте следующие синтаксические правила для объявления переменных HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, переменный синтаксис (DirectX HLSL)
- "\"интерполяция\", синтаксис переменных (DirectX HLSL)"
- Shared, синтаксис переменных (DirectX HLSL)
- граупшаред, синтаксис переменных (DirectX HLSL)
- статический синтаксис переменных (DirectX HLSL)
- унифицированный синтаксис переменных (DirectX HLSL)
- volatile, переменный синтаксис (DirectX HLSL)
- точный синтаксис переменных (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6e63bafa62a9857af678e0848c81237dcd0d585
ms.sourcegitcommit: 4e0bde7dfa48a0b60bca4a5230eb2b05be3778d3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2020
ms.locfileid: "104997190"
---
# <a name="variable-syntax"></a><span data-ttu-id="0bc97-111">Синтаксис переменных</span><span class="sxs-lookup"><span data-stu-id="0bc97-111">Variable Syntax</span></span>

<span data-ttu-id="0bc97-112">Используйте следующие синтаксические правила для объявления переменных HLSL.</span><span class="sxs-lookup"><span data-stu-id="0bc97-112">Use the following syntax rules to declare HLSL variables.</span></span>



|                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc97-113">\[*Хранилище \_ Тип класса* \] \[ *\_ Модификатор* \] *имя типа* \[ *индекс* \] \[ *: семантика* \] \[ *: паккоффсет* \] \[ *: Register* \] ;    \[  \] Заметки \[ *= Начальный \_ Значение*                    \]</span><span class="sxs-lookup"><span data-stu-id="0bc97-113">\[*Storage\_Class*\] \[*Type\_Modifier*\] *Type Name*\[*Index*\]     \[*: Semantic*\]     \[*: Packoffset*\]     \[*: Register*\];    \[*Annotations*\]     \[*= Initial\_Value*\]</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="0bc97-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bc97-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc97-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*\_Класс хранения*</span><span class="sxs-lookup"><span data-stu-id="0bc97-115"><span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Storage\_Class*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc97-116">Необязательные модификаторы класса хранения, которые предоставляют указаниям компилятора сведения об области действия переменной и времени существования; Модификаторы можно указывать в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="0bc97-116">Optional storage-class modifiers that give the compiler hints about variable scope and lifetime; the modifiers can be specified in any order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0bc97-117">Значение</span><span class="sxs-lookup"><span data-stu-id="0bc97-117">Value</span></span></th>
<th><span data-ttu-id="0bc97-118">Описание</span><span class="sxs-lookup"><span data-stu-id="0bc97-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0bc97-119"><strong>extern</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-119"><strong>extern</strong></span></span></td>
<td><span data-ttu-id="0bc97-120">Пометьте глобальную переменную как внешний входное значение для шейдера; Это обозначение по умолчанию для всех глобальных переменных.</span><span class="sxs-lookup"><span data-stu-id="0bc97-120">Mark a global variable as an external input to the shader; this is the default marking for all global variables.</span></span> <span data-ttu-id="0bc97-121">Не может использоваться вместе со <strong>статическим</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bc97-121">Cannot be combined with <strong>static</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bc97-122"><strong>Интерполяция</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-122"><strong>nointerpolation</strong></span></span></td>
<td><span data-ttu-id="0bc97-123">Не выдавайте интерполяцию выходов шейдера вершин перед передачей их в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="0bc97-123">Do not interpolate the outputs of a vertex shader before passing them to a pixel shader.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bc97-124"><strong>точен</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-124"><strong>precise</strong></span></span></td>
<td><span data-ttu-id="0bc97-125">Ключевое слово <strong>точной</strong> при применении к переменной ограничит любые вычисления, используемые для получения значения, присвоенного этой переменной, следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0bc97-125">The <strong>precise</strong> keyword when applied to a variable will restrict any calculations used to produce the value assigned to that variable in the following ways:</span></span>

*   <span data-ttu-id="0bc97-126">Отдельные операции хранятся отдельно.</span><span class="sxs-lookup"><span data-stu-id="0bc97-126">Separate operations are kept separate.</span></span> <span data-ttu-id="0bc97-127">Например, когда операция Mul и Add может быть назначена с помощью команды Mad, <strong>Точная</strong> заставляет операции оставаться отдельными.</span><span class="sxs-lookup"><span data-stu-id="0bc97-127">For example, where a mul and add operation might have been fused into a mad operation, <strong>precise</strong> forces the operations to remain separate.</span></span> <span data-ttu-id="0bc97-128">Вместо этого необходимо явно использовать встроенную функцию Mad.</span><span class="sxs-lookup"><span data-stu-id="0bc97-128">Instead, you must explicitly use the mad intrinsic function.</span></span>
*   <span data-ttu-id="0bc97-129">Поддерживается порядок операций.</span><span class="sxs-lookup"><span data-stu-id="0bc97-129">Order of operations are maintained.</span></span> <span data-ttu-id="0bc97-130">Если порядок инструкций может быть изменен в случайном порядке для повышения производительности, <strong>Точная</strong> проверка того, что компилятор сохраняет порядок как записанный.</span><span class="sxs-lookup"><span data-stu-id="0bc97-130">Where the order of instructions might have been shuffled to improve performance, <strong>precise</strong> ensures that the compiler preserves the order as written.</span></span>
*   <span data-ttu-id="0bc97-131">Ненадежные операции IEEE ограничены.</span><span class="sxs-lookup"><span data-stu-id="0bc97-131">IEEE unsafe operations are restricted.</span></span> <span data-ttu-id="0bc97-132">Если компилятор может использовать быстрые математические операции, которые не задают значения NaN (не число) и INF (бесконечное значение), <strong>точнее</strong> принуждает требования IEEE к значениям NaN и INF.</span><span class="sxs-lookup"><span data-stu-id="0bc97-132">Where the compiler might have used fast math operations that don't account for NaN (not a number) and INF (infinite) values, <strong>precise</strong> forces IEEE requirements concerning NaN and INF values to be respected.</span></span> <span data-ttu-id="0bc97-133">Без <strong>точной</strong>оптимизации и математические операции не являются стандартом IEEE.</span><span class="sxs-lookup"><span data-stu-id="0bc97-133">Without <strong>precise</strong>, these optimizations and mathematical operations are not IEEE safe.</span></span>
*   <span data-ttu-id="0bc97-134">Уточнение переменной <strong>точности</strong> не делает операций, использующих переменную <strong>точности</strong>.</span><span class="sxs-lookup"><span data-stu-id="0bc97-134">Qualifying a variable <strong>precise</strong> doesn't make operations that use the variable <strong>precise</strong>.</span></span> <span data-ttu-id="0bc97-135">Так как <strong>точное</strong> распространение выполняется только для операций, которые вносят вклад в значения, присвоенные <strong>точной</strong>переменной, правильная <strong>точность</strong> вычислений может быть непростой, поэтому мы рекомендуем пометить <strong>выходные данные</strong> шейдера непосредственно там, где они объявляются, будь то на поле структуры или в выходном параметре, или на тип возвращаемого значения функции записи.</span><span class="sxs-lookup"><span data-stu-id="0bc97-135">Since <strong>precise</strong> propagates only to operations that contribute to the values that are assigned to the <strong>precise</strong>-qualified variable, correctly making desired calculations <strong>precise</strong> can be tricky, so we recommended that you mark the shader outputs <strong>precise</strong> directly where you declare them, whether that's on a structure field, or on an output parameter, or the return type of the entry function.</span></span>

<span data-ttu-id="0bc97-136">Возможность управления оптимизацией таким образом поддерживает недисперсию результата для измененной выходной переменной путем отключения оптимизаций, которые могут повлиять на окончательный результат из-за различий в накопленной точности.</span><span class="sxs-lookup"><span data-stu-id="0bc97-136">The ability to control optimizations in this way maintains result invariance for the modified output variable by disabling optimizations that might affect final results due to differences in accumulated precision differences.</span></span> <span data-ttu-id="0bc97-137">Это полезно, если требуется, чтобы шейдеры для тесселяции поддерживали стыки исправлений с ограниченными водами или совпасть со значениями глубины за несколько проходов.</span><span class="sxs-lookup"><span data-stu-id="0bc97-137">It is useful when you want shaders for tessellation to maintain water-tight patch seams or match depth values over multiple passes.</span></span>

<span data-ttu-id="0bc97-138">[Пример кода](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span><span class="sxs-lookup"><span data-stu-id="0bc97-138">[Sample code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl):</span></span> 
```HLSL
matrix g_mWorldViewProjection;
void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position)
{
  // operation is precise because it contributes to the precise parameter OutPos
  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );
}
```
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bc97-139"><strong>используемый</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-139"><strong>shared</strong></span></span></td>
<td><span data-ttu-id="0bc97-140">Пометьте переменную для совместного использования эффектов; Это подсказка для компилятора.</span><span class="sxs-lookup"><span data-stu-id="0bc97-140">Mark a variable for sharing between effects; this is a hint to the compiler.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bc97-141"><strong>граупшаред</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-141"><strong>groupshared</strong></span></span></td>
<td><span data-ttu-id="0bc97-142">Пометьте переменную для общей памяти группы потоков для шейдеров вычислений.</span><span class="sxs-lookup"><span data-stu-id="0bc97-142">Mark a variable for thread-group-shared memory for compute shaders.</span></span> <span data-ttu-id="0bc97-143">В D3D10 максимальный общий размер всех переменных с классом хранения граупшаред — 16 КБ, в D3D11 максимальный размер — 32 КБ.</span><span class="sxs-lookup"><span data-stu-id="0bc97-143">In D3D10 the maximum total size of all variables with the groupshared storage class is 16kb, in D3D11 the maximum size is 32kb.</span></span> <span data-ttu-id="0bc97-144">См. примеры.</span><span class="sxs-lookup"><span data-stu-id="0bc97-144">See examples.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bc97-145"><strong>static</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-145"><strong>static</strong></span></span></td>
<td><span data-ttu-id="0bc97-146">Пометьте локальную переменную, чтобы она была инициализирована один раз и сохранялась между вызовами функций.</span><span class="sxs-lookup"><span data-stu-id="0bc97-146">Mark a local variable so that it is initialized one time and persists between function calls.</span></span> <span data-ttu-id="0bc97-147">Если объявление не содержит инициализатор, значение устанавливается равным нулю.</span><span class="sxs-lookup"><span data-stu-id="0bc97-147">If the declaration does not include an initializer, the value is set to zero.</span></span> <span data-ttu-id="0bc97-148">Глобальная переменная, помеченная как <strong>static</strong> , невидима для приложения.</span><span class="sxs-lookup"><span data-stu-id="0bc97-148">A global variable marked <strong>static</strong> is not visible to an application.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0bc97-149"><strong>счет</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-149"><strong>uniform</strong></span></span></td>
<td><span data-ttu-id="0bc97-150">Пометьте переменную, данные которой являются постоянными в ходе выполнения шейдера (например, цвет материала в шейдере вершин); глобальные переменные считаются <strong>универсальными</strong> по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0bc97-150">Mark a variable whose data is constant throughout the execution of a shader (such as a material color in a vertex shader); global variables are considered <strong>uniform</strong> by default.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0bc97-151"><strong>volatile</strong></span><span class="sxs-lookup"><span data-stu-id="0bc97-151"><strong>volatile</strong></span></span></td>
<td><span data-ttu-id="0bc97-152">Пометьте переменную, которая часто изменяется; Это подсказка для компилятора.</span><span class="sxs-lookup"><span data-stu-id="0bc97-152">Mark a variable that changes frequently; this is a hint to the compiler.</span></span> <span data-ttu-id="0bc97-153">Этот модификатор класса хранения применяется только к локальной переменной.</span><span class="sxs-lookup"><span data-stu-id="0bc97-153">This storage class modifier only applies to a local variable.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="0bc97-154">Компилятор HLSL в настоящее время игнорирует этот модификатор класса хранения.</span><span class="sxs-lookup"><span data-stu-id="0bc97-154">The HLSL compiler currently ignores this storage class modifier.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="0bc97-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Модификатор типа*</span><span class="sxs-lookup"><span data-stu-id="0bc97-155"><span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*Type\_Modifier*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-156">Необязательный модификатор типа переменной.</span><span class="sxs-lookup"><span data-stu-id="0bc97-156">Optional variable-type modifier.</span></span>



| <span data-ttu-id="0bc97-157">Значение</span><span class="sxs-lookup"><span data-stu-id="0bc97-157">Value</span></span>             | <span data-ttu-id="0bc97-158">Описание</span><span class="sxs-lookup"><span data-stu-id="0bc97-158">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc97-159">**const**</span><span class="sxs-lookup"><span data-stu-id="0bc97-159">**const**</span></span>         | <span data-ttu-id="0bc97-160">Пометьте переменную, которая не может быть изменена шейдером, поэтому она должна быть инициализирована в объявлении переменной.</span><span class="sxs-lookup"><span data-stu-id="0bc97-160">Mark a variable that cannot be changed by a shader, therefore, it must be initialized in the variable declaration.</span></span> <span data-ttu-id="0bc97-161">Глобальные переменные считаются **константами** по умолчанию (это поведение подавляется путем указания компилятору флага/ЖЕК).</span><span class="sxs-lookup"><span data-stu-id="0bc97-161">Global variables are considered **const** by default (suppress this behavior by supplying the /Gec flag to the compiler).</span></span> |
| <span data-ttu-id="0bc97-162">**\_Основная строка**</span><span class="sxs-lookup"><span data-stu-id="0bc97-162">**row\_major**</span></span>    | <span data-ttu-id="0bc97-163">Пометьте переменную, в которой хранятся четыре компонента, в одну строку, чтобы их можно было хранить в одном регистре констант.</span><span class="sxs-lookup"><span data-stu-id="0bc97-163">Mark a variable that stores four components in a single row so they can be stored in a single constant register.</span></span>                                                                                                                             |
| <span data-ttu-id="0bc97-164">**\_основной столбец**</span><span class="sxs-lookup"><span data-stu-id="0bc97-164">**column\_major**</span></span> | <span data-ttu-id="0bc97-165">Пометьте переменную, в которой хранится 4 компонента, в один столбец, чтобы оптимизировать матричную формулу.</span><span class="sxs-lookup"><span data-stu-id="0bc97-165">Mark a variable that stores 4 components in a single column to optimize matrix math.</span></span>                                                                                                                                                         |



 

> [!Note]  
> <span data-ttu-id="0bc97-166">Если не указать значение модификатора типа, компилятор использует **столбец \_ Major** в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0bc97-166">If you do not specify a type-modifier value, the compiler uses **column\_major** as the default value.</span></span>

 

</dd> <dt>

<span data-ttu-id="0bc97-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Тип*</span><span class="sxs-lookup"><span data-stu-id="0bc97-167"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Type*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-168">Любой тип HLSL, указанный в [типах данных (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="0bc97-168">Any HLSL type listed in [Data Types (DirectX HLSL)](dx-graphics-hlsl-data-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Имя* \[ *Индекс*\]</span><span class="sxs-lookup"><span data-stu-id="0bc97-169"><span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Name*\[*Index*\]</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-170">Строка ASCII, однозначно определяющая переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="0bc97-170">ASCII string that uniquely identifies a shader variable.</span></span> <span data-ttu-id="0bc97-171">Чтобы определить необязательный массив, используйте **индекс** для размера массива, который является положительным целым числом = 1.</span><span class="sxs-lookup"><span data-stu-id="0bc97-171">To define an optional array, use **index** for the array size, which is a positive integer = 1.</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Семантическ*</span><span class="sxs-lookup"><span data-stu-id="0bc97-172"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-173">Необязательные параметры — сведения об использовании, используемые компилятором для связывания входных и выходных данных шейдера.</span><span class="sxs-lookup"><span data-stu-id="0bc97-173">Optional parameter-usage information, used by the compiler to link shader inputs and outputs.</span></span> <span data-ttu-id="0bc97-174">Существует несколько предопределенных [семантик](dx-graphics-hlsl-semantics.md) для шейдеров вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="0bc97-174">There are several predefined [semantics](dx-graphics-hlsl-semantics.md) for vertex and pixel shaders.</span></span> <span data-ttu-id="0bc97-175">Компилятор игнорирует семантику, если только они не объявлены в глобальной переменной или параметр, переданный в шейдер.</span><span class="sxs-lookup"><span data-stu-id="0bc97-175">The compiler ignores semantics unless they are declared on a global variable, or a parameter passed into a shader.</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*паккоффсет*</span><span class="sxs-lookup"><span data-stu-id="0bc97-176"><span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-177">Необязательное ключевое слово для констант упаковки шейдера вручную.</span><span class="sxs-lookup"><span data-stu-id="0bc97-177">Optional keyword for manually packing shader constants.</span></span> <span data-ttu-id="0bc97-178">См. [паккоффсет (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span><span class="sxs-lookup"><span data-stu-id="0bc97-178">See [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Зарегистрировать*</span><span class="sxs-lookup"><span data-stu-id="0bc97-179"><span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Register*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-180">Необязательное ключевое слово для присваивания переменной шейдера конкретному регистру вручную.</span><span class="sxs-lookup"><span data-stu-id="0bc97-180">Optional keyword for manually assigning a shader variable to a particular register.</span></span> <span data-ttu-id="0bc97-181">См. раздел [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span><span class="sxs-lookup"><span data-stu-id="0bc97-181">See [register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Заметки*</span><span class="sxs-lookup"><span data-stu-id="0bc97-182"><span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation(s)*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-183">Необязательные метаданные в виде строки, присоединенной к глобальной переменной.</span><span class="sxs-lookup"><span data-stu-id="0bc97-183">Optional metadata, in the form of a string, attached to a global variable.</span></span> <span data-ttu-id="0bc97-184">Заметка используется платформой эффектов и игнорируется HLSL; более подробный синтаксис см. в разделе [синтаксис аннотации](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span><span class="sxs-lookup"><span data-stu-id="0bc97-184">An annotation is used by the effect framework and ignored by HLSL; to see more detailed syntax, see [annotation syntax](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).</span></span>

</dd> <dt>

<span data-ttu-id="0bc97-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Начальное \_ значение*</span><span class="sxs-lookup"><span data-stu-id="0bc97-185"><span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*Initial\_Value*</span></span>
</dt> <dd>

<span data-ttu-id="0bc97-186">Необязательные начальные значения; число значений должно соответствовать числу компонентов в *типе*.</span><span class="sxs-lookup"><span data-stu-id="0bc97-186">Optional initial value(s); the number of values should match the number of components in *Type*.</span></span> <span data-ttu-id="0bc97-187">Каждая глобальная переменная, помеченная как **extern** , должна быть инициализирована литеральным значением. Каждая переменная, помеченная как **static** , должна быть инициализирована с помощью константы.</span><span class="sxs-lookup"><span data-stu-id="0bc97-187">Each global variable marked **extern** must be initialized with a literal value; each variable marked **static** must be initialized with a constant.</span></span>

<span data-ttu-id="0bc97-188">Глобальные переменные, не помеченные как **static** или **extern** , не компилируются в шейдер.</span><span class="sxs-lookup"><span data-stu-id="0bc97-188">Global variables that are not marked **static** or **extern** are not compiled into the shader.</span></span> <span data-ttu-id="0bc97-189">Компилятор не задает автоматически значения по умолчанию для глобальных переменных и не может использовать их при оптимизации.</span><span class="sxs-lookup"><span data-stu-id="0bc97-189">The compiler does not automatically set default values for global variables and cannot use them in optimizations.</span></span> <span data-ttu-id="0bc97-190">Чтобы инициализировать этот тип глобальной переменной, используйте отражение, чтобы получить его значение, а затем скопируйте значение в буфер констант.</span><span class="sxs-lookup"><span data-stu-id="0bc97-190">To initialize this type of global variable, use reflection to get its value and then copy the value to a constant buffer.</span></span> <span data-ttu-id="0bc97-191">Например, можно использовать метод [**ID3D11ShaderReflection:: жетвариаблебинаме**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) для получения переменной, использовать метод [**ID3D11ShaderReflectionVariable:: DESC**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) , чтобы получить описание переменной шейдера, и получить начальное значение из элемента **DefaultValue** в переменной пошагового [**\_ шейдера \_ \_ D3D11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) .</span><span class="sxs-lookup"><span data-stu-id="0bc97-191">For example, you can use the [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) method to get the variable, use the [**ID3D11ShaderReflectionVariable::GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) method to get the shader-variable description, and get the initial value from the **DefaultValue** member of the [**D3D11\_SHADER\_VARIABLE\_DESC**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) structure.</span></span> <span data-ttu-id="0bc97-192">Чтобы скопировать значение в буфер констант, необходимо убедиться, что буфер был создан с доступом на запись ЦП ([**D3D11 доступ на \_ \_ \_ запись ЦП**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span><span class="sxs-lookup"><span data-stu-id="0bc97-192">To copy the value to the constant buffer, you must ensure that the buffer was created with CPU write access ([**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)).</span></span> <span data-ttu-id="0bc97-193">Дополнительные сведения о создании буфера констант см. [в разделе инструкции. Создание буфера констант](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span><span class="sxs-lookup"><span data-stu-id="0bc97-193">For more information about how to create a constant buffer, see [How to: Create a Constant Buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).</span></span>

<span data-ttu-id="0bc97-194">Кроме того, можно использовать [платформу Effects](../direct3d11/d3d11-graphics-programming-guide-effects.md) для автоматической обработки отражения и установки начального значения.</span><span class="sxs-lookup"><span data-stu-id="0bc97-194">You can also use the [effects framework](../direct3d11/d3d11-graphics-programming-guide-effects.md) to automatically process the reflecting and setting the initial value.</span></span> <span data-ttu-id="0bc97-195">Например, можно использовать метод [**ID3DX11EffectPass:: Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .</span><span class="sxs-lookup"><span data-stu-id="0bc97-195">For example, you can use the [**ID3DX11EffectPass::Apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) method.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="0bc97-196">Примеры</span><span class="sxs-lookup"><span data-stu-id="0bc97-196">Examples</span></span>

<span data-ttu-id="0bc97-197">Ниже приведено несколько примеров объявления переменных шейдера.</span><span class="sxs-lookup"><span data-stu-id="0bc97-197">Here are several examples of shader-variable declarations.</span></span>


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a><span data-ttu-id="0bc97-198">Общая группа</span><span class="sxs-lookup"><span data-stu-id="0bc97-198">Group Shared</span></span>

<span data-ttu-id="0bc97-199">HLSL позволяет потокам шейдера вычислений обмениваться значениями через общую память.</span><span class="sxs-lookup"><span data-stu-id="0bc97-199">HLSL enables threads of a compute shader to exchange values via shared memory.</span></span> <span data-ttu-id="0bc97-200">HLSL предоставляет примитивы барьера, такие как [**граупмеморибарриервисграупсинк**](groupmemorybarrierwithgroupsync.md), и т. д., чтобы обеспечить правильный порядок операций чтения и записи в общую память в шейдере и избежать состязаний с данными.</span><span class="sxs-lookup"><span data-stu-id="0bc97-200">HLSL provides barrier primitives such as [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), and so on to ensure the correct ordering of reads and writes to shared memory in the shader and to avoid data races.</span></span>

> [!Note]  
> <span data-ttu-id="0bc97-201">Оборудование выполняет потоки в группах (деформация или волна-переднюю часть), а синхронизация барьера иногда может быть опущена, чтобы повысить производительность, если только синхронизация потоков, принадлежащих одной группе, верна.</span><span class="sxs-lookup"><span data-stu-id="0bc97-201">Hardware executes threads in groups (warps or wave-fronts), and barrier synchronization can sometimes be omitted to increase performance when only synchronizing threads that belong to the same group is correct.</span></span> <span data-ttu-id="0bc97-202">Но мы настоятельно не рекомендуем это проявления по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="0bc97-202">But we highly discourage this omission for these reasons:</span></span>
>
> -   <span data-ttu-id="0bc97-203">Это подавление приводит к непереносимому коду, который может не работать на определенном оборудовании и не работает на программных средствах прорисовки, которые обычно выполняют потоки в небольших группах.</span><span class="sxs-lookup"><span data-stu-id="0bc97-203">This omission results in non-portable code, which might not work on some hardware and doesn't work on software rasterizers that typically execute threads in smaller groups.</span></span>
> -   <span data-ttu-id="0bc97-204">Улучшения производительности, которые могут быть достигнуты в этом пропуске, будут незначительными по сравнению с использованием барьера всего потока.</span><span class="sxs-lookup"><span data-stu-id="0bc97-204">The performance improvements that you might achieve with this omission will be minor compared to using all-thread barrier.</span></span>

 

<span data-ttu-id="0bc97-205">В Direct3D 10 отсутствует синхронизация потоков при записи в **граупшаред**, поэтому каждый поток ограничен одним местом в массиве для записи.</span><span class="sxs-lookup"><span data-stu-id="0bc97-205">In Direct3D 10 there is no synchronization of threads when writing to **groupshared**, so this means that each thread is limited to a single location in an array for writing.</span></span> <span data-ttu-id="0bc97-206">Используйте системное значение [SV \_ граупиндекс](dx-graphics-hlsl-semantics.md) для индексирования этого массива при записи, чтобы избежать конфликта между двумя потоками.</span><span class="sxs-lookup"><span data-stu-id="0bc97-206">Use the [SV\_GroupIndex](dx-graphics-hlsl-semantics.md) system value to index into this array when writing to ensure that no two threads can collide.</span></span> <span data-ttu-id="0bc97-207">С точки зрения чтения все потоки имеют доступ ко всему массиву для чтения.</span><span class="sxs-lookup"><span data-stu-id="0bc97-207">In terms of reading, all threads have access to the entire array for reading.</span></span>


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a><span data-ttu-id="0bc97-208">Упаковоч</span><span class="sxs-lookup"><span data-stu-id="0bc97-208">Packing</span></span>

<span data-ttu-id="0bc97-209">Упаковка подкомпонентов векторов и скаляров, размер которых достаточно велик для предотвращения пересечения границ регистров.</span><span class="sxs-lookup"><span data-stu-id="0bc97-209">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundarys.</span></span> <span data-ttu-id="0bc97-210">Например, все они допустимы:</span><span class="sxs-lookup"><span data-stu-id="0bc97-210">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



<span data-ttu-id="0bc97-211">Невозможно смешивать типы упаковки.</span><span class="sxs-lookup"><span data-stu-id="0bc97-211">Cannot mix packing types.</span></span>

<span data-ttu-id="0bc97-212">Как и ключевое слово Register, паккоффсет может быть конкретным целевым.</span><span class="sxs-lookup"><span data-stu-id="0bc97-212">Like the register keyword, a packoffset can be target specific.</span></span> <span data-ttu-id="0bc97-213">Упаковка вспомогательных компонентов доступна только с ключевым словом паккоффсет, а не с ключевым словом Register.</span><span class="sxs-lookup"><span data-stu-id="0bc97-213">Subcomponent packing is only available with the packoffset keyword, not the register keyword.</span></span> <span data-ttu-id="0bc97-214">В объявлении кбуффер ключевое слово Register не учитывается для целевых объектов Direct3D 10, так как предполагается совместимость с различными платформами.</span><span class="sxs-lookup"><span data-stu-id="0bc97-214">Inside a cbuffer declaration, the register keyword is ignored for Direct3D 10 targets as it is assumed to be for cross-platform compatibility.</span></span>

<span data-ttu-id="0bc97-215">Упакованные элементы могут перекрываться, и компилятор не выдает ошибок или предупреждений.</span><span class="sxs-lookup"><span data-stu-id="0bc97-215">Packed elements may overlap and the compiler will give no error or warning.</span></span> <span data-ttu-id="0bc97-216">В этом примере Element2 и Element3 будут перекрываться с помощью Element1. x и Element1. y.</span><span class="sxs-lookup"><span data-stu-id="0bc97-216">In this example, Element2 and Element3 will overlap with Element1.x and Element1.y.</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



<span data-ttu-id="0bc97-217">Пример, в котором используется паккоффсет: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0bc97-217">A sample that uses packoffset is: [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0bc97-218">См. также</span><span class="sxs-lookup"><span data-stu-id="0bc97-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bc97-219">Переменные (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0bc97-219">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

