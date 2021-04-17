---
description: Каждый ДКССАС, соответствующий требованиям, должен определить как минимум один параметр глобального действия с глобальной семантикой.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Глобальный параметр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105710639"
---
# <a name="global-parameter"></a><span data-ttu-id="f648c-103">Глобальный параметр</span><span class="sxs-lookup"><span data-stu-id="f648c-103">Global Parameter</span></span>

<span data-ttu-id="f648c-104">Каждый ДКССАС, соответствующий требованиям, должен определить как минимум один параметр глобального действия с глобальной семантикой.</span><span class="sxs-lookup"><span data-stu-id="f648c-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="f648c-105">Глобальный параметр также может использовать одну или несколько необязательных заметок.</span><span class="sxs-lookup"><span data-stu-id="f648c-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="f648c-106">Синтаксис выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="f648c-107">где:</span><span class="sxs-lookup"><span data-stu-id="f648c-107">where:</span></span>

-   <span data-ttu-id="f648c-108">VariableName — это заданное пользователем имя переменной текстовой строки в формате ASCII.</span><span class="sxs-lookup"><span data-stu-id="f648c-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="f648c-109">Сасглобал — это семантическое ключевое слово, которое определяет этот параметр как глобальный параметр ДКССАС.</span><span class="sxs-lookup"><span data-stu-id="f648c-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="f648c-110">Сасверсион является единственной обязательной заметкой.</span><span class="sxs-lookup"><span data-stu-id="f648c-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="f648c-111">Оптионаланнотатионс может включать следующее:</span><span class="sxs-lookup"><span data-stu-id="f648c-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="f648c-112">сасеффектаусор</span><span class="sxs-lookup"><span data-stu-id="f648c-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="f648c-113">сасеффектаусорингсофтваре</span><span class="sxs-lookup"><span data-stu-id="f648c-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="f648c-114">сасеффекткатегори</span><span class="sxs-lookup"><span data-stu-id="f648c-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="f648c-115">сасеффекткомпани</span><span class="sxs-lookup"><span data-stu-id="f648c-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="f648c-116">сасеффектдескриптион</span><span class="sxs-lookup"><span data-stu-id="f648c-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="f648c-117">сасеффекселп</span><span class="sxs-lookup"><span data-stu-id="f648c-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="f648c-118">сасеффектревисион</span><span class="sxs-lookup"><span data-stu-id="f648c-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="f648c-119">сасверсион</span><span class="sxs-lookup"><span data-stu-id="f648c-119">SasVersion</span></span>

<span data-ttu-id="f648c-120">Единственная обязательная Аннотация — Сасверсион.</span><span class="sxs-lookup"><span data-stu-id="f648c-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="f648c-121">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="f648c-122">где:</span><span class="sxs-lookup"><span data-stu-id="f648c-122">where:</span></span>

-   <span data-ttu-id="f648c-123">Основная указывает на основной выпуск ДКССАС.</span><span class="sxs-lookup"><span data-stu-id="f648c-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="f648c-124">Основные выпуски ДКССАС могут содержать изменения в наборе семантики и заданных заметок.</span><span class="sxs-lookup"><span data-stu-id="f648c-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="f648c-125">Семантика и заметки могут добавляться и удаляться, и в целом обратная совместимость с предыдущими выпусками не гарантируется.</span><span class="sxs-lookup"><span data-stu-id="f648c-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="f648c-126">дополнительный указывает дополнительный выпуск SAS.</span><span class="sxs-lookup"><span data-stu-id="f648c-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="f648c-127">Вспомогательные выпуски ДКССАС могут включать в себя добавление новой семантики или заметок.</span><span class="sxs-lookup"><span data-stu-id="f648c-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="f648c-128">Кроме того, семантика и аннотации могут быть помечены как устаревшие в стандарте ДКССАС.</span><span class="sxs-lookup"><span data-stu-id="f648c-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="f648c-129">Устаревшие семантика и заметки по-прежнему должны поддерживаться ведущими приложениями, но при этом могут выдавать предупреждения диагностики при использовании такой семантики или аннотации.</span><span class="sxs-lookup"><span data-stu-id="f648c-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="f648c-130">Вспомогательные версии обратно совместимы с предыдущими выпусками.</span><span class="sxs-lookup"><span data-stu-id="f648c-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="f648c-131">Редакция указывает редакцию ДКССАС.</span><span class="sxs-lookup"><span data-stu-id="f648c-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="f648c-132">Редакции ДКССАС существуют только как средства для исправления ошибок, удаления неоднозначности и уточнения стандарта.</span><span class="sxs-lookup"><span data-stu-id="f648c-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="f648c-133">Изменения в стандарте обратно совместимы с предыдущими выпусками.</span><span class="sxs-lookup"><span data-stu-id="f648c-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="f648c-134">Текущая версия — 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="f648c-134">The current version is 1.0.0.</span></span> <span data-ttu-id="f648c-135">Для этой заметки значение по умолчанию отсутствует.</span><span class="sxs-lookup"><span data-stu-id="f648c-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="f648c-136">сасеффектаусор</span><span class="sxs-lookup"><span data-stu-id="f648c-136">SasEffectAuthor</span></span>

<span data-ttu-id="f648c-137">Здесь объявляется лицо, создавшее этот результат.</span><span class="sxs-lookup"><span data-stu-id="f648c-137">This declares the person who created the effect.</span></span> <span data-ttu-id="f648c-138">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="f648c-139">где value — это строка, идентифицирующая автора действия.</span><span class="sxs-lookup"><span data-stu-id="f648c-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="f648c-140">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="f648c-141">сасеффектаусорингсофтваре</span><span class="sxs-lookup"><span data-stu-id="f648c-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="f648c-142">Он объявляет программное обеспечение, на котором был создан этот результат.</span><span class="sxs-lookup"><span data-stu-id="f648c-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="f648c-143">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="f648c-144">где value — это строка, идентифицирующая программное обеспечение для создания эффектов.</span><span class="sxs-lookup"><span data-stu-id="f648c-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="f648c-145">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="f648c-146">сасеффекткатегори</span><span class="sxs-lookup"><span data-stu-id="f648c-146">SasEffectCategory</span></span>

<span data-ttu-id="f648c-147">Это объявляет категорию влияния.</span><span class="sxs-lookup"><span data-stu-id="f648c-147">This declares the effect category.</span></span> <span data-ttu-id="f648c-148">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="f648c-149">где value — это строка, идентифицирующая категорию эффектов.</span><span class="sxs-lookup"><span data-stu-id="f648c-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="f648c-150">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-150">The default is an empty string.</span></span> <span data-ttu-id="f648c-151">Категория выражается с помощью значения, похожего на путь, с использованием косой черты в качестве разделителя.</span><span class="sxs-lookup"><span data-stu-id="f648c-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="f648c-152">Эффекты могут принадлежать только одной категории, так как для выражения включения в нескольких путях в одном значении Сасеффекткатегори нет синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="f648c-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="f648c-153">Значение этой заметки не обрабатывается ведущим приложением с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="f648c-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="f648c-154">сасеффекткомпани</span><span class="sxs-lookup"><span data-stu-id="f648c-154">SasEffectCompany</span></span>

<span data-ttu-id="f648c-155">Это объявляет компанию, которая создала этот результат.</span><span class="sxs-lookup"><span data-stu-id="f648c-155">This declares the company that created the effect.</span></span> <span data-ttu-id="f648c-156">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="f648c-157">где value — это строка, идентифицирующая имя компании, которой принадлежит этот результат.</span><span class="sxs-lookup"><span data-stu-id="f648c-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="f648c-158">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="f648c-159">сасеффектдескриптион</span><span class="sxs-lookup"><span data-stu-id="f648c-159">SasEffectDescription</span></span>

<span data-ttu-id="f648c-160">Это описание действия.</span><span class="sxs-lookup"><span data-stu-id="f648c-160">This describes the effect.</span></span> <span data-ttu-id="f648c-161">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="f648c-162">где value — это строка, описывающая результат.</span><span class="sxs-lookup"><span data-stu-id="f648c-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="f648c-163">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="f648c-164">сасеффекселп</span><span class="sxs-lookup"><span data-stu-id="f648c-164">SasEffectHelp</span></span>

<span data-ttu-id="f648c-165">Это строка справки, которая может отображаться для пользователя при запросе справки по связанному с ним результату.</span><span class="sxs-lookup"><span data-stu-id="f648c-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="f648c-166">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="f648c-167">где value — это строка, которая может отображаться, если пользователь запрашивает справку.</span><span class="sxs-lookup"><span data-stu-id="f648c-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="f648c-168">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="f648c-169">сасеффектревисион</span><span class="sxs-lookup"><span data-stu-id="f648c-169">SasEffectRevision</span></span>

<span data-ttu-id="f648c-170">Эта заметка позволяет средствам и пользователям записывать номер редакции связанного файла эффектов.</span><span class="sxs-lookup"><span data-stu-id="f648c-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="f648c-171">Например, пользователи могут вставить соответствующие ключевые слова в значение этой заметки, чтобы вызвать подстановку ключевых слов в своем любимом программном обеспечении управления версиями.</span><span class="sxs-lookup"><span data-stu-id="f648c-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="f648c-172">Он объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="f648c-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="f648c-173">где value — это строка, идентифицирующая редакцию действия.</span><span class="sxs-lookup"><span data-stu-id="f648c-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="f648c-174">Значение по умолчанию - пустая строка.</span><span class="sxs-lookup"><span data-stu-id="f648c-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="f648c-175">Примеры</span><span class="sxs-lookup"><span data-stu-id="f648c-175">Examples</span></span>

<span data-ttu-id="f648c-176">Ниже приведен пример, в котором используется только единственная обязательная Аннотация:</span><span class="sxs-lookup"><span data-stu-id="f648c-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="f648c-177">Ниже приведен пример, в котором используется обязательная Аннотация и несколько необязательных заметок.</span><span class="sxs-lookup"><span data-stu-id="f648c-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="f648c-178">См. также</span><span class="sxs-lookup"><span data-stu-id="f648c-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f648c-179">Справочник по стандарту DirectX для заметок и семантик</span><span class="sxs-lookup"><span data-stu-id="f648c-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



