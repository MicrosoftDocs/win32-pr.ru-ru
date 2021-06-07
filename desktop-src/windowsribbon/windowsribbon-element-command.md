---
title: Command, элемент
description: Представляет определение команды.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Лента Windows для командных элементов
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e1df5b62c7b2d7c55345ba8d6da366d04697054
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443485"
---
# <a name="command-element"></a><span data-ttu-id="12570-104">Command, элемент</span><span class="sxs-lookup"><span data-stu-id="12570-104">Command element</span></span>

<span data-ttu-id="12570-105">Представляет определение команды.</span><span class="sxs-lookup"><span data-stu-id="12570-105">Represents a Command definition.</span></span>

## <a name="usage"></a><span data-ttu-id="12570-106">Использование</span><span class="sxs-lookup"><span data-stu-id="12570-106">Usage</span></span>

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
```

## <a name="attributes"></a><span data-ttu-id="12570-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12570-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="12570-108">attribute</span><span class="sxs-lookup"><span data-stu-id="12570-108">Attribute</span></span></th>
<th><span data-ttu-id="12570-109">Тип</span><span class="sxs-lookup"><span data-stu-id="12570-109">Type</span></span></th>
<th><span data-ttu-id="12570-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="12570-110">Required</span></span></th>
<th><span data-ttu-id="12570-111">Описание</span><span class="sxs-lookup"><span data-stu-id="12570-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="12570-112"><strong>Комментарий</strong></span><span class="sxs-lookup"><span data-stu-id="12570-112"><strong>Comment</strong></span></span><br/></td>
<td><span data-ttu-id="12570-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-114">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-114">No</span></span><br/></td>
<td><span data-ttu-id="12570-115">Используется для добавления аннотации в элемент Command.</span><span class="sxs-lookup"><span data-stu-id="12570-115">Used to annotate the command element.</span></span><br/> <br/><span data-ttu-id="12570-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-117">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="12570-117">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> <span data-ttu-id="12570-118">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="12570-118">Maximum length: 250 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12570-119"><strong>Id</strong></span><span class="sxs-lookup"><span data-stu-id="12570-119"><strong>Id</strong></span></span><br/></td>
<td><span data-ttu-id="12570-120">xs: Поситивеинтежер Union xs: String</span><span class="sxs-lookup"><span data-stu-id="12570-120">xs:positiveInteger union xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-121">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-121">No</span></span><br/></td>
<td><span data-ttu-id="12570-122">Уникальный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="12570-122">The unique resource ID.</span></span> <br/> <br/><span data-ttu-id="12570-123">
<dt><span></span><span></span><strong></strong> (Объединение xs: Поситивеинтежер и xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-123">
<dt><span></span><span></span><strong></strong> (The union of xs:positiveInteger and xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-124">Целочисленное значение в диапазоне от 2 до 59999, включительно или 0x2 и 0xea5f в шестнадцатеричном, включающем.</span><span class="sxs-lookup"><span data-stu-id="12570-124">An integer value between 2 and 59999, inclusive, or 0x2 and 0xea5f in hexadecimal, inclusive.</span></span> <br/> <span data-ttu-id="12570-125">Максимальная длина — 10 символов, включая необязательные нули в начале.</span><span class="sxs-lookup"><span data-stu-id="12570-125">Maximum length is 10 characters, including optional leading zeros.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12570-126"><strong>Keytip</strong></span><span class="sxs-lookup"><span data-stu-id="12570-126"><strong>Keytip</strong></span></span><br/></td>
<td><span data-ttu-id="12570-127">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-127">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-128">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-128">No</span></span><br/></td>
<td><span data-ttu-id="12570-129">Строка, представляющая сочетание клавиш для элемента Command.</span><span class="sxs-lookup"><span data-stu-id="12570-129">A string that represents the keyboard shortcut of a command element.</span></span><br/> <br/><span data-ttu-id="12570-130">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-130">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-131">Строка, состоящая из любой последовательности символов, включая пробелы.</span><span class="sxs-lookup"><span data-stu-id="12570-131">A string composed of any sequence of characters, including white space.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12570-132"><strong>лабелдескриптион</strong></span><span class="sxs-lookup"><span data-stu-id="12570-132"><strong>LabelDescription</strong></span></span><br/></td>
<td><span data-ttu-id="12570-133">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-133">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-134">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-134">No</span></span><br/></td>
<td><span data-ttu-id="12570-135">Строка, представляющая текст, отображаемый в элементе Command.</span><span class="sxs-lookup"><span data-stu-id="12570-135">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="12570-136">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-136">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-137">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="12570-137">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12570-138"><strong>лабелтитле</strong></span><span class="sxs-lookup"><span data-stu-id="12570-138"><strong>LabelTitle</strong></span></span><br/></td>
<td><span data-ttu-id="12570-139">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-139">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-140">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-140">No</span></span><br/></td>
<td><span data-ttu-id="12570-141">Строка, представляющая текст, отображаемый в элементе Command.</span><span class="sxs-lookup"><span data-stu-id="12570-141">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="12570-142">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-142">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-143">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="12570-143">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12570-144"><strong>Имя</strong></span><span class="sxs-lookup"><span data-stu-id="12570-144"><strong>Name</strong></span></span><br/></td>
<td><span data-ttu-id="12570-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-145">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-146">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-146">No</span></span><br/></td>
<td><span data-ttu-id="12570-147"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-147"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-148">Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность цифр, букв или знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="12570-148">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="12570-149">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="12570-149">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12570-150"><strong>Символ</strong></span><span class="sxs-lookup"><span data-stu-id="12570-150"><strong>Symbol</strong></span></span><br/></td>
<td><span data-ttu-id="12570-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-151">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-152">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-152">No</span></span><br/></td>
<td><span data-ttu-id="12570-153"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-153"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-154">Строка, состоящая из буквы или символа подчеркивания, за которой следует любая последовательность цифр, букв или знаков подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="12570-154">A string that consists of a letter or underscore followed by any sequence of digits, letters, or underscores.</span></span><br/> <span data-ttu-id="12570-155">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="12570-155">Maximum length: 100 characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="12570-156"><strong>тултипдескриптион</strong></span><span class="sxs-lookup"><span data-stu-id="12570-156"><strong>TooltipDescription</strong></span></span><br/></td>
<td><span data-ttu-id="12570-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-157">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-158">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-158">No</span></span><br/></td>
<td><span data-ttu-id="12570-159">Строка, представляющая текст, отображаемый в элементе Command.</span><span class="sxs-lookup"><span data-stu-id="12570-159">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="12570-160">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-160">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-161">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="12570-161">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="12570-162"><strong>тултиптитле</strong></span><span class="sxs-lookup"><span data-stu-id="12570-162"><strong>TooltipTitle</strong></span></span><br/></td>
<td><span data-ttu-id="12570-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="12570-163">xs:string</span></span><br/></td>
<td><span data-ttu-id="12570-164">Нет</span><span class="sxs-lookup"><span data-stu-id="12570-164">No</span></span><br/></td>
<td><span data-ttu-id="12570-165">Строка, представляющая текст, отображаемый в элементе Command.</span><span class="sxs-lookup"><span data-stu-id="12570-165">A string that represents the text displayed on a command element.</span></span><br/> <br/><span data-ttu-id="12570-166">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="12570-166">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="12570-167">Строка, состоящая из любой последовательности символов, включая пробелы и символы разрыва строки.</span><span class="sxs-lookup"><span data-stu-id="12570-167">A string composed of any sequence of characters, including white space and line-break characters.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="12570-168">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="12570-168">Child elements</span></span>



| <span data-ttu-id="12570-169">Элемент</span><span class="sxs-lookup"><span data-stu-id="12570-169">Element</span></span>                                                                                                     | <span data-ttu-id="12570-170">Описание</span><span class="sxs-lookup"><span data-stu-id="12570-170">Description</span></span>                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="12570-171">**Command. комментарий**</span><span class="sxs-lookup"><span data-stu-id="12570-171">**Command.Comment**</span></span>](windowsribbon-element-command-comment.md)<br/>                                 | <span data-ttu-id="12570-172">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-172">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-173">**Command.Id**</span><span class="sxs-lookup"><span data-stu-id="12570-173">**Command.Id**</span></span>](windowsribbon-element-command-id.md)<br/>                                           | <span data-ttu-id="12570-174">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-174">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-175">**Command. keytip**</span><span class="sxs-lookup"><span data-stu-id="12570-175">**Command.Keytip**</span></span>](windowsribbon-element-command-keytip.md)<br/>                                   | <span data-ttu-id="12570-176">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-176">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-177">**Command. Лабелдескриптион**</span><span class="sxs-lookup"><span data-stu-id="12570-177">**Command.LabelDescription**</span></span>](windowsribbon-element-command-labeldescription.md)<br/>               | <span data-ttu-id="12570-178">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-178">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-179">**Command. Лабелтитле**</span><span class="sxs-lookup"><span data-stu-id="12570-179">**Command.LabelTitle**</span></span>](windowsribbon-element-command-labeltitle.md)<br/>                           | <span data-ttu-id="12570-180">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-180">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-181">**Command. Ларжехигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="12570-181">**Command.LargeHighContrastImages**</span></span>](windowsribbon-element-command-largehighcontrastimages.md)<br/> | <span data-ttu-id="12570-182">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-182">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-183">**Command. Ларжеимажес**</span><span class="sxs-lookup"><span data-stu-id="12570-183">**Command.LargeImages**</span></span>](windowsribbon-element-command-largeimages.md)<br/>                         | <span data-ttu-id="12570-184">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-184">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-185">**Command.Name**</span><span class="sxs-lookup"><span data-stu-id="12570-185">**Command.Name**</span></span>](windowsribbon-element-command-name.md)<br/>                                       | <span data-ttu-id="12570-186">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-186">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-187">**Command. Смаллхигхконтрастимажес**</span><span class="sxs-lookup"><span data-stu-id="12570-187">**Command.SmallHighContrastImages**</span></span>](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | <span data-ttu-id="12570-188">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-188">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-189">**Command. Смаллимажес**</span><span class="sxs-lookup"><span data-stu-id="12570-189">**Command.SmallImages**</span></span>](windowsribbon-element-command-smallimages.md)<br/>                         | <span data-ttu-id="12570-190">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-190">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-191">**Command. Symbol**</span><span class="sxs-lookup"><span data-stu-id="12570-191">**Command.Symbol**</span></span>](windowsribbon-element-command-symbol.md)<br/>                                   | <span data-ttu-id="12570-192">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-192">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-193">**Command. Тултипдескриптион**</span><span class="sxs-lookup"><span data-stu-id="12570-193">**Command.TooltipDescription**</span></span>](windowsribbon-element-command-tooltipdescription.md)<br/>           | <span data-ttu-id="12570-194">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-194">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="12570-195">**Command. Тултиптитле**</span><span class="sxs-lookup"><span data-stu-id="12570-195">**Command.TooltipTitle**</span></span>](windowsribbon-element-command-tooltiptitle.md)<br/>                       | <span data-ttu-id="12570-196">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="12570-196">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="12570-197">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="12570-197">Parent elements</span></span>



| <span data-ttu-id="12570-198">Элемент</span><span class="sxs-lookup"><span data-stu-id="12570-198">Element</span></span>                                                                               |
|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="12570-199">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="12570-199">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="12570-200">Remarks</span><span class="sxs-lookup"><span data-stu-id="12570-200">Remarks</span></span>

<span data-ttu-id="12570-201">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="12570-201">Required.</span></span>

<span data-ttu-id="12570-202">Может происходить один или несколько раз для каждого элемента [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="12570-202">May occur one or more times for each [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>

<span data-ttu-id="12570-203">Дочерние элементы элемента **Command** могут происходить в любом порядке.</span><span class="sxs-lookup"><span data-stu-id="12570-203">The child elements of the **Command** element may occur in any order.</span></span>

<span data-ttu-id="12570-204">Как правило, ресурсы команды объявляются в разметке ленты, но их также можно задать во время выполнения с помощью вызова [**сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="12570-204">Typically, Command resources are declared in Ribbon markup, but they can also be set at run time with a call to [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> <span data-ttu-id="12570-205">Например, можно задать свойство [UI \_ PKEY \_ KeyTip](windowsribbon-reference-properties-uipkey-keytip.md) для команды вместо объявления значения в разметке с помощью элемента [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .</span><span class="sxs-lookup"><span data-stu-id="12570-205">For example, it is possible to set the [UI\_PKEY\_Keytip](windowsribbon-reference-properties-uipkey-keytip.md) property for a Command instead of declaring a value in markup with the [**Command.Keytip**](windowsribbon-element-command-keytip.md) element.</span></span>

<span data-ttu-id="12570-206">В случаях, когда свойства команды, такие как метки и изображения, не могут быть заданы с помощью [**сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , их можно сделать недействительными при вызове [**инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span><span class="sxs-lookup"><span data-stu-id="12570-206">In cases where Command properties, such as labels and images, cannot be set with [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) they can be invalidated with a call to [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).</span></span> <span data-ttu-id="12570-207">После недействительности платформа запрашивает в ведущем приложении сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="12570-207">After invalidation, the framework queries the host application for the resource details.</span></span>

> [!Note]  
> <span data-ttu-id="12570-208">Невозможно восстановить ресурс из таблицы ресурсов разметки после того, как она стала недействительной.</span><span class="sxs-lookup"><span data-stu-id="12570-208">A resource cannot be reinstated from the markup resource table after it has been invalidated.</span></span>

 

<span data-ttu-id="12570-209">В файл заголовка разметки ленты добавляется определение команды для каждой **команды** , объявленной в разметке.</span><span class="sxs-lookup"><span data-stu-id="12570-209">A Command definition is added to the Ribbon markup header file for each **Command** declared in markup.</span></span>

<span data-ttu-id="12570-210">Значение *KeyTip* выступает в качестве сочетания клавиш для команды, если эта команда не предоставлена через пункт меню.</span><span class="sxs-lookup"><span data-stu-id="12570-210">The value of *Keytip* acts as the keyboard accelerator for a Command unless that Command is exposed through a menu item.</span></span> <span data-ttu-id="12570-211">В этом случае платформа игнорирует значение *KeyTip* и вместо этого использует символ, предшествующий амперсанду, как указано в *лабелтитле* или [ \_ \_ метке PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md).</span><span class="sxs-lookup"><span data-stu-id="12570-211">In this case, the framework ignores the *Keytip* value and instead uses a character preceded by an ampersand as specified by *LabelTitle* or [UI\_PKEY\_Label](windowsribbon-reference-properties-uipkey-label.md).</span></span> <span data-ttu-id="12570-212">Если амперсанд не указан с помощью *лабелтитле* или \_ метки PKEY пользовательского интерфейса \_ , keytip или сочетание клавиш не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="12570-212">If no ampersand is specified by *LabelTitle* or UI\_PKEY\_Label, no keytip or keyboard accelerator is exposed.</span></span>

## <a name="examples"></a><span data-ttu-id="12570-213">Примеры</span><span class="sxs-lookup"><span data-stu-id="12570-213">Examples</span></span>

<span data-ttu-id="12570-214">В следующем примере показан манифест элементов **команды** для вкладки " **Главная** ".</span><span class="sxs-lookup"><span data-stu-id="12570-214">The following example shows a manifest of **Command** elements for a **Home** tab.</span></span>


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a><span data-ttu-id="12570-215">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="12570-215">Element information</span></span>

* <span data-ttu-id="12570-216">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="12570-216">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="12570-217">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="12570-217">**Can be empty**: No</span></span>



 

