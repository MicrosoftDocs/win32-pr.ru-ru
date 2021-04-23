---
description: Используйте эту аннотацию, чтобы связать параметр Effect с элементом управления пользовательского интерфейса в среде размещения. Это позволит пользователю интерактивно управлять параметром Effect через ведущее приложение.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Заметка пользовательского интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495762"
---
# <a name="ui-annotation"></a><span data-ttu-id="bbe35-104">Заметка пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bbe35-104">UI Annotation</span></span>

<span data-ttu-id="bbe35-105">Используйте эту аннотацию, чтобы связать параметр Effect с элементом управления пользовательского интерфейса в среде размещения.</span><span class="sxs-lookup"><span data-stu-id="bbe35-105">Use this annotation to associate an effect parameter with a UI control in the host environment.</span></span> <span data-ttu-id="bbe35-106">Это позволит пользователю интерактивно управлять параметром Effect через ведущее приложение.</span><span class="sxs-lookup"><span data-stu-id="bbe35-106">This will allow a user to interactively control an effect parameter through the host application.</span></span>

<span data-ttu-id="bbe35-107">ДКССАС определяет набор стандартных элементов управления с точки зрения модели данных и базовое поведение, которое может быть ожидаемым авторами от ведущих приложений.</span><span class="sxs-lookup"><span data-stu-id="bbe35-107">DXSAS defines a set of standard controls in terms of the data model and basic behavior that effect authors can expect from host applications.</span></span> <span data-ttu-id="bbe35-108">Заметка элемента управления используется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-108">The control annotation is used like this:</span></span>


```
string SasUiControl = "ControlType";
```



<span data-ttu-id="bbe35-109">where</span><span class="sxs-lookup"><span data-stu-id="bbe35-109">where</span></span>


```
ControlType
```



<span data-ttu-id="bbe35-110">является одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="bbe35-110">is one of the following:</span></span>



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbe35-111">ControlType</span><span class="sxs-lookup"><span data-stu-id="bbe35-111">ControlType</span></span> | <span data-ttu-id="bbe35-112">Описание</span><span class="sxs-lookup"><span data-stu-id="bbe35-112">Description</span></span>                                                                                                                                                                     | <span data-ttu-id="bbe35-113">Внутренний тип данных</span><span class="sxs-lookup"><span data-stu-id="bbe35-113">Internal Data Type</span></span>                                                                                 | <span data-ttu-id="bbe35-114">Заметки свойств элемента управления</span><span class="sxs-lookup"><span data-stu-id="bbe35-114">Control Property Annotations</span></span>                                                                                 |
| <span data-ttu-id="bbe35-115">Нет</span><span class="sxs-lookup"><span data-stu-id="bbe35-115">None</span></span>        | <span data-ttu-id="bbe35-116">Элемент управления не должен отображаться.</span><span class="sxs-lookup"><span data-stu-id="bbe35-116">No control should be shown.</span></span> <span data-ttu-id="bbe35-117">Обратите внимание, что элемент управления является видимым, если [сасуивисибле](#sasuivisible) имеет значение true, а тип элемента управления имеет любой тип, кроме None.</span><span class="sxs-lookup"><span data-stu-id="bbe35-117">Note that a control is visible if [SasUiVisible](#sasuivisible) is True and the control type is any type other than None.</span></span>                           | <span data-ttu-id="bbe35-118">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bbe35-118">n/a</span></span>                                                                                                | <span data-ttu-id="bbe35-119">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bbe35-119">n/a</span></span>                                                                                                          |
| <span data-ttu-id="bbe35-120">Любой</span><span class="sxs-lookup"><span data-stu-id="bbe35-120">Any</span></span>         | <span data-ttu-id="bbe35-121">Это означает, что Специальный элемент управления не запрашивается.</span><span class="sxs-lookup"><span data-stu-id="bbe35-121">This implies that no special control is requested.</span></span> <span data-ttu-id="bbe35-122">Представленный элемент управления является результатом поведения, определяемого приложением.</span><span class="sxs-lookup"><span data-stu-id="bbe35-122">The control presented is the result of application-defined behavior.</span></span>                                                         | <span data-ttu-id="bbe35-123">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bbe35-123">n/a</span></span>                                                                                                | <span data-ttu-id="bbe35-124">Недоступно</span><span class="sxs-lookup"><span data-stu-id="bbe35-124">n/a</span></span>                                                                                                          |
| <span data-ttu-id="bbe35-125">ColorPicker</span><span class="sxs-lookup"><span data-stu-id="bbe35-125">ColorPicker</span></span> | <span data-ttu-id="bbe35-126">Представляет значение цвета в виде цветовой палитры.</span><span class="sxs-lookup"><span data-stu-id="bbe35-126">Represent a color value as a color swatch.</span></span> <span data-ttu-id="bbe35-127">Значение упаковывается в компоненты XYZ связанного вектора.</span><span class="sxs-lookup"><span data-stu-id="bbe35-127">The value is packed into the XYZ components of the associated vector.</span></span> <span data-ttu-id="bbe35-128">Компонент W связанного вектора всегда имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="bbe35-128">The W component of the associated vector is always set to one.</span></span> | <span data-ttu-id="bbe35-129">float *n* , где *n* — от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="bbe35-129">float *N* where *N* is 1 to 4 inclusive.</span></span>                                                            | [<span data-ttu-id="bbe35-130">сасуиенум</span><span class="sxs-lookup"><span data-stu-id="bbe35-130">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="bbe35-131">Направление</span><span class="sxs-lookup"><span data-stu-id="bbe35-131">Direction</span></span>   | <span data-ttu-id="bbe35-132">Вектор направления.</span><span class="sxs-lookup"><span data-stu-id="bbe35-132">A direction vector.</span></span>                                                                                                                                                             | <span data-ttu-id="bbe35-133">float *n* , где *n* — 2 – 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="bbe35-133">float *N* where *N* is 2 to 4 inclusive.</span></span>                                                            | <span data-ttu-id="bbe35-134">Нет</span><span class="sxs-lookup"><span data-stu-id="bbe35-134">None</span></span>                                                                                                         |
| <span data-ttu-id="bbe35-135">Операция filepicker</span><span class="sxs-lookup"><span data-stu-id="bbe35-135">FilePicker</span></span>  | <span data-ttu-id="bbe35-136">Диалоговое окно, позволяющее пользователю просматривать и выбирать файл.</span><span class="sxs-lookup"><span data-stu-id="bbe35-136">A dialog box that allows the user to browse and select a file.</span></span>                                                                                                                  | <span data-ttu-id="bbe35-137">строка</span><span class="sxs-lookup"><span data-stu-id="bbe35-137">string</span></span>                                                                                             | <span data-ttu-id="bbe35-138">Нет</span><span class="sxs-lookup"><span data-stu-id="bbe35-138">None</span></span>                                                                                                         |
| <span data-ttu-id="bbe35-139">листпиккер</span><span class="sxs-lookup"><span data-stu-id="bbe35-139">ListPicker</span></span>  | <span data-ttu-id="bbe35-140">Список строковых значений, из которых пользователь может выбрать одну запись.</span><span class="sxs-lookup"><span data-stu-id="bbe35-140">A list of string values from which the user can select one entry.</span></span> <span data-ttu-id="bbe35-141">Значения формируются из заметки [сасуиенум](#sasuienum) .</span><span class="sxs-lookup"><span data-stu-id="bbe35-141">The values are generated from the [SasUiEnum](#sasuienum) annotation.</span></span>                                         | <span data-ttu-id="bbe35-142">Массив строк вместе с целочисленным значением, содержащим индекс выбранного строкового значения.</span><span class="sxs-lookup"><span data-stu-id="bbe35-142">An array of strings along with an integer value containing the index of the selected string value.</span></span> | [<span data-ttu-id="bbe35-143">сасуиенум</span><span class="sxs-lookup"><span data-stu-id="bbe35-143">SasUiEnum</span></span>](#sasuienum)                                                                                      |
| <span data-ttu-id="bbe35-144">Числовой</span><span class="sxs-lookup"><span data-stu-id="bbe35-144">Numeric</span></span>     | <span data-ttu-id="bbe35-145">Набор числовых элементов управления вводом (например, текстовых полей).</span><span class="sxs-lookup"><span data-stu-id="bbe35-145">A set of numerical input controls (such as text boxes).</span></span>                                                                                                                         | <span data-ttu-id="bbe35-146">float *m* x *N* , где *m* и *n* — от 1 до 4 включительно.</span><span class="sxs-lookup"><span data-stu-id="bbe35-146">float *M* x *N* where *M* and *N* are 1 to 4 inclusive.</span></span>                                               | <span data-ttu-id="bbe35-147">[Сасуимин](#sasuimin), [сасуимакс](#sasuimax), [сасуистриде](#sasuistride)</span><span class="sxs-lookup"><span data-stu-id="bbe35-147">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)</span></span>                                    |
| <span data-ttu-id="bbe35-148">Ползунок</span><span class="sxs-lookup"><span data-stu-id="bbe35-148">Slider</span></span>      | <span data-ttu-id="bbe35-149">Набор ползунков.</span><span class="sxs-lookup"><span data-stu-id="bbe35-149">A set of sliders.</span></span>                                                                                                                                                               | <span data-ttu-id="bbe35-150">float *m* x *N* , где *m* и *n* — от 1 до 4 включительно</span><span class="sxs-lookup"><span data-stu-id="bbe35-150">float *M* x *N* where *M* and *N* are 1 to 4 inclusive</span></span>                                                | <span data-ttu-id="bbe35-151">[Сасуимин](#sasuimin), [сасуимакс](#sasuimax), [сасуистепс](#sasuisteps), [сасуистепсповер](#sasuistepspower)</span><span class="sxs-lookup"><span data-stu-id="bbe35-151">[SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower)</span></span> |
| <span data-ttu-id="bbe35-152">Строка</span><span class="sxs-lookup"><span data-stu-id="bbe35-152">String</span></span>      | <span data-ttu-id="bbe35-153">Текстовое поле для редактирования содержимого строки.</span><span class="sxs-lookup"><span data-stu-id="bbe35-153">An text box for editing string content.</span></span>                                                                                                                                         | <span data-ttu-id="bbe35-154">строка</span><span class="sxs-lookup"><span data-stu-id="bbe35-154">string</span></span>                                                                                             | <span data-ttu-id="bbe35-155">Нет</span><span class="sxs-lookup"><span data-stu-id="bbe35-155">None</span></span>                                                                                                         |



 

<span data-ttu-id="bbe35-156">Если внутренний тип данных не идентичен типу связанного параметра, то при передаче данных из параметра ведущего приложения в параметр Effect происходит приведение.</span><span class="sxs-lookup"><span data-stu-id="bbe35-156">If the internal data type is not identical to the associated parameter's type, casting will occur when data is transferred from the host application parameter to the effect parameter.</span></span>

<span data-ttu-id="bbe35-157">Значение по умолчанию — строка None.</span><span class="sxs-lookup"><span data-stu-id="bbe35-157">The default is the string "None".</span></span>

## <a name="ui-common-properties"></a><span data-ttu-id="bbe35-158">Общие свойства пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="bbe35-158">UI Common Properties</span></span>

### <a name="sasuidescription"></a><span data-ttu-id="bbe35-159">сасуидескриптион</span><span class="sxs-lookup"><span data-stu-id="bbe35-159">SasUiDescription</span></span>

<span data-ttu-id="bbe35-160">Используйте эту заметку, чтобы указать строку для описания инструмента.</span><span class="sxs-lookup"><span data-stu-id="bbe35-160">Use this annotation to specify a string to describe a tool.</span></span> <span data-ttu-id="bbe35-161">Это можно использовать для элементов пользовательского интерфейса, таких как всплывающие подсказки.</span><span class="sxs-lookup"><span data-stu-id="bbe35-161">This could be used for UI elements such as tool tips.</span></span>


```
string SasUiDescription = "descriptive string";
```



<span data-ttu-id="bbe35-162">Например:</span><span class="sxs-lookup"><span data-stu-id="bbe35-162">For instance:</span></span>


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



<span data-ttu-id="bbe35-163">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bbe35-163">The default is an empty string.</span></span>

### <a name="sasuilabel"></a><span data-ttu-id="bbe35-164">сасуилабел</span><span class="sxs-lookup"><span data-stu-id="bbe35-164">SasUiLabel</span></span>

<span data-ttu-id="bbe35-165">Используйте эту заметку, чтобы указать строку для обозначения любого элемента управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bbe35-165">Use this annotation to specify a string to label any UI control.</span></span>


```
string SasUiLabel = "some label;
```



<span data-ttu-id="bbe35-166">Пример:</span><span class="sxs-lookup"><span data-stu-id="bbe35-166">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



<span data-ttu-id="bbe35-167">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bbe35-167">The default is an empty string.</span></span>

### <a name="sasuivisible"></a><span data-ttu-id="bbe35-168">сасуивисибле</span><span class="sxs-lookup"><span data-stu-id="bbe35-168">SasUiVisible</span></span>

<span data-ttu-id="bbe35-169">Используйте эту заметку, чтобы указать, следует ли отображать связанный параметр для пользователя.</span><span class="sxs-lookup"><span data-stu-id="bbe35-169">Use this annotation to specify whether the associated parameter should be displayed to the user.</span></span>


```
bool SasUiVisible = false;
```



<span data-ttu-id="bbe35-170">Если задано значение true, ведущее приложение должно отображать элемент управления пользовательского интерфейса для изменения параметра эффектов с заметками.</span><span class="sxs-lookup"><span data-stu-id="bbe35-170">If set to True, the host application should display a UI control for editing the annotated effect parameter.</span></span> <span data-ttu-id="bbe35-171">Если задано значение false, то пользовательский интерфейс не отображается в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="bbe35-171">If false, no UI is displayed in the host application.</span></span>

<span data-ttu-id="bbe35-172">Пример:</span><span class="sxs-lookup"><span data-stu-id="bbe35-172">Here is an example:</span></span>


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



<span data-ttu-id="bbe35-173">Значение по умолчанию равно True.</span><span class="sxs-lookup"><span data-stu-id="bbe35-173">The default is True.</span></span>

## <a name="ui-control-properties"></a><span data-ttu-id="bbe35-174">Свойства элемента управления ИП</span><span class="sxs-lookup"><span data-stu-id="bbe35-174">UI Control Properties</span></span>

<span data-ttu-id="bbe35-175">Заметки свойств элемента управления — это дополнительные модификаторы, которые помогают определить, как работает конкретный элемент управления.</span><span class="sxs-lookup"><span data-stu-id="bbe35-175">Control property annotations are additional modifiers that help determine how a particular control operates.</span></span>

### <a name="sasuienum"></a><span data-ttu-id="bbe35-176">сасуиенум</span><span class="sxs-lookup"><span data-stu-id="bbe35-176">SasUiEnum</span></span>

<span data-ttu-id="bbe35-177">Эта заметка позволяет ограничить диапазон значений для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="bbe35-177">This annotation allows you to restrict the range of values for a control.</span></span> <span data-ttu-id="bbe35-178">Заметка содержит строку значений, разделенных запятыми.</span><span class="sxs-lookup"><span data-stu-id="bbe35-178">The annotation contains a string of values delimited by commas.</span></span>

<span data-ttu-id="bbe35-179">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="bbe35-179">The default is an empty string.</span></span>

### <a name="sasuimax"></a><span data-ttu-id="bbe35-180">сасуимакс</span><span class="sxs-lookup"><span data-stu-id="bbe35-180">SasUiMax</span></span>

<span data-ttu-id="bbe35-181">Эта заметка указывает максимальное значение связанного параметра.</span><span class="sxs-lookup"><span data-stu-id="bbe35-181">This annotation specifies the maximum value of the associated parameter.</span></span> <span data-ttu-id="bbe35-182">Он может быть связан только с числовым типом параметра.</span><span class="sxs-lookup"><span data-stu-id="bbe35-182">It can only be associated with a numerically-typed parameter.</span></span> <span data-ttu-id="bbe35-183">Максимальное значение параметра будет фактически вычислено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-183">The maximum value of the parameter will actually be calculated as:</span></span>


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



<span data-ttu-id="bbe35-184">\_Тип параметра \_ Max — это максимальное значение для типа, используемого связанным параметром.</span><span class="sxs-lookup"><span data-stu-id="bbe35-184">PARAMETER\_TYPE\_MAX is the maximum value for the type used by the associated parameter.</span></span> <span data-ttu-id="bbe35-185">Это означает, что значение параметра, принимая во внимание [сасуимакс](#sasuimax) аннотацию, вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-185">This means that the value of the parameter, taking into account the [SasUiMax](#sasuimax) annotation is calculated as:</span></span>


```
ParameterValue = min(NewParameterValue, MaxValue);
```



<span data-ttu-id="bbe35-186">Значение по умолчанию — ФЛТ \_ Max, как определено в Math. h.</span><span class="sxs-lookup"><span data-stu-id="bbe35-186">The default value is FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuimin"></a><span data-ttu-id="bbe35-187">сасуимин</span><span class="sxs-lookup"><span data-stu-id="bbe35-187">SasUiMin</span></span>

<span data-ttu-id="bbe35-188">В этой заметке указывается минимальное значение связанного параметра.</span><span class="sxs-lookup"><span data-stu-id="bbe35-188">This annotation specifies the minimum value of the associated parameter.</span></span> <span data-ttu-id="bbe35-189">Он может быть связан только с любым числовым типом параметра.</span><span class="sxs-lookup"><span data-stu-id="bbe35-189">It can only be associated with any numerically-typed parameter.</span></span> <span data-ttu-id="bbe35-190">Минимальное значение параметра будет фактически вычислено следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-190">The minimum value of the parameter will actually be calculated as:</span></span>


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



<span data-ttu-id="bbe35-191">\_Тип параметра \_ min является минимальным значением для типа, используемого связанным параметром.</span><span class="sxs-lookup"><span data-stu-id="bbe35-191">PARAMETER\_TYPE\_MIN is the minimum value for the type used by the associated parameter.</span></span> <span data-ttu-id="bbe35-192">Это означает, что значение параметра, принимая во внимание [сасуимин](#sasuimin) аннотацию, вычисляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-192">This means that the value of the parameter, taking into account the [SasUiMin](#sasuimin) annotation is calculated as:</span></span>


```
ParameterValue = max(NewParameterValue, MinValue);
```



<span data-ttu-id="bbe35-193">Значение по умолчанию —-ФЛТ \_ Max, как определено в Math. h.</span><span class="sxs-lookup"><span data-stu-id="bbe35-193">The default value is -FLT\_MAX as defined in Math.h.</span></span>

### <a name="sasuisteps"></a><span data-ttu-id="bbe35-194">сасуистепс</span><span class="sxs-lookup"><span data-stu-id="bbe35-194">SasUiSteps</span></span>

<span data-ttu-id="bbe35-195">Эта заметка указывает количество шагов, которые могут быть использованы при увеличении или уменьшении значения связанного параметра.</span><span class="sxs-lookup"><span data-stu-id="bbe35-195">This annotation specifies the number of steps that can be used when incrementing or decrementing the associated parameter value.</span></span> <span data-ttu-id="bbe35-196">Аннотация имеет смысл только для параметра с числовым типом.</span><span class="sxs-lookup"><span data-stu-id="bbe35-196">The annotation is only meaningful on a numerically-typed parameter.</span></span> <span data-ttu-id="bbe35-197">Ноль указывает, что ведущее приложение будет выбирать разумное количество шагов.</span><span class="sxs-lookup"><span data-stu-id="bbe35-197">Zero specifies that the host application will choose a reasonable number of steps.</span></span>

<span data-ttu-id="bbe35-198">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="bbe35-198">The default value is 0.</span></span>

### <a name="sasuistepspower"></a><span data-ttu-id="bbe35-199">сасуистепсповер</span><span class="sxs-lookup"><span data-stu-id="bbe35-199">SasUiStepsPower</span></span>

<span data-ttu-id="bbe35-200">Эта заметка указывает экспоненту в функции Power, которая имеет диапазон \[ 0,0 f, 1,0 f \] .</span><span class="sxs-lookup"><span data-stu-id="bbe35-200">This annotation specifies the exponent in the power function, which has the range \[0.0f, 1.0f\].</span></span> <span data-ttu-id="bbe35-201">Ведущие приложения должны реализовать следующий метод при вычислении значений параметров:</span><span class="sxs-lookup"><span data-stu-id="bbe35-201">Host applications must implement the following method when calculating parameter values:</span></span>


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



<span data-ttu-id="bbe35-202">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="bbe35-202">The default value is 1.0f.</span></span>

### <a name="sasuistride"></a><span data-ttu-id="bbe35-203">сасуистриде</span><span class="sxs-lookup"><span data-stu-id="bbe35-203">SasUiStride</span></span>

<span data-ttu-id="bbe35-204">В этой заметке указывается шаг приращения, который должен использоваться при увеличении или уменьшении этого значения.</span><span class="sxs-lookup"><span data-stu-id="bbe35-204">This annotation specifies the increment that should be used when incrementing or decrementing this value.</span></span> <span data-ttu-id="bbe35-205">В отличие от [сасуистепс](#sasuisteps), [сасуистриде](#sasuistride) полезен для элемента управления "Счетчик", например, когда данные не привязаны, а пользователь должен увеличивать значение параметра по шагам, а не по заранее определенному количеству шагов.</span><span class="sxs-lookup"><span data-stu-id="bbe35-205">Unlike [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) is useful with a spinner control, for instance, where the data is unbounded and the user would rather increment the parameter value by stride rather than by a pre-defined number of steps.</span></span> <span data-ttu-id="bbe35-206">Ведущие приложения должны увеличиваться (или уменьшаться в зависимости от поведения элемента управления) на значение Сасуистриде следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbe35-206">Host applications should increment (or decrement depending on the control behavior) by the value of SasUiStride as follows:</span></span>


```
ParameterValue = ParameterValue +/- SasUiStride
```



<span data-ttu-id="bbe35-207">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="bbe35-207">The default value is 1.0f.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbe35-208">См. также</span><span class="sxs-lookup"><span data-stu-id="bbe35-208">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe35-209">Справочник по стандарту DirectX для заметок и семантик</span><span class="sxs-lookup"><span data-stu-id="bbe35-209">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



