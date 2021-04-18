---
title: Group, элемент
description: Представляет элемент управления "Группа", который выступает в качестве контейнера для группы элементов.
ms.assetid: b0d3fcda-7165-40f4-9e57-c7ab88b31711
keywords:
- Лента для элементов группы
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a42e9efb30397862037426041420d96be8fd387
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413287"
---
# <a name="group-element"></a><span data-ttu-id="fe2d8-104">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="fe2d8-104">Group element</span></span>

<span data-ttu-id="fe2d8-105">Представляет элемент управления " [Группа](windowsribbon-controls-group.md) ", который выступает в качестве контейнера для группы элементов.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="fe2d8-106">Использование</span><span class="sxs-lookup"><span data-stu-id="fe2d8-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="fe2d8-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="fe2d8-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe2d8-108">attribute</span><span class="sxs-lookup"><span data-stu-id="fe2d8-108">Attribute</span></span></th>
<th><span data-ttu-id="fe2d8-109">Тип</span><span class="sxs-lookup"><span data-stu-id="fe2d8-109">Type</span></span></th>
<th><span data-ttu-id="fe2d8-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="fe2d8-110">Required</span></span></th>
<th><span data-ttu-id="fe2d8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="fe2d8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe2d8-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d8-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="fe2d8-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe2d8-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="fe2d8-114">Нет</span><span class="sxs-lookup"><span data-stu-id="fe2d8-114">No</span></span><br/></td>
<td><span data-ttu-id="fe2d8-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fe2d8-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fe2d8-116">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="fe2d8-117">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="fe2d8-118">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe2d8-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d8-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="fe2d8-120">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="fe2d8-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="fe2d8-121">Нет</span><span class="sxs-lookup"><span data-stu-id="fe2d8-121">No</span></span><br/></td>
<td><span data-ttu-id="fe2d8-122">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="fe2d8-123">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="fe2d8-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fe2d8-124">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="fe2d8-125">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="fe2d8-126">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe2d8-127"><strong>сизедефинитион</strong></span><span class="sxs-lookup"><span data-stu-id="fe2d8-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="fe2d8-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="fe2d8-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="fe2d8-129">Нет</span><span class="sxs-lookup"><span data-stu-id="fe2d8-129">No</span></span><br/></td>
<td><span data-ttu-id="fe2d8-130">При указании значения <em>сизедефинитион</em> ограничивается одним из <a href="windowsribbon-templates.md">шаблонов макета</a> , определенных платформой Ribbon.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="fe2d8-131">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="fe2d8-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="fe2d8-132">Любая последовательность из нуля или более символов.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="fe2d8-133">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="fe2d8-134">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="fe2d8-134">Child elements</span></span>



| <span data-ttu-id="fe2d8-135">Элемент</span><span class="sxs-lookup"><span data-stu-id="fe2d8-135">Element</span></span>                                                                             | <span data-ttu-id="fe2d8-136">Описание</span><span class="sxs-lookup"><span data-stu-id="fe2d8-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="fe2d8-137">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="fe2d8-138">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-139">**Установка**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="fe2d8-140">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="fe2d8-142">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-143">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="fe2d8-144">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="fe2d8-146">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-147">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="fe2d8-148">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-149">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="fe2d8-150">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-151">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="fe2d8-152">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="fe2d8-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="fe2d8-153">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="fe2d8-154">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-155">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="fe2d8-156">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="fe2d8-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="fe2d8-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="fe2d8-158">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="fe2d8-160">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-161">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="fe2d8-162">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="fe2d8-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="fe2d8-164">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="fe2d8-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="fe2d8-165">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="fe2d8-165">Parent elements</span></span>



| <span data-ttu-id="fe2d8-166">Элемент</span><span class="sxs-lookup"><span data-stu-id="fe2d8-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="fe2d8-167">**TAB**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="fe2d8-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe2d8-168">Remarks</span></span>

<span data-ttu-id="fe2d8-169">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-169">Optional.</span></span>

<span data-ttu-id="fe2d8-170">Может происходить один или несколько раз для каждого элемента [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="fe2d8-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="fe2d8-171">[**Вкладка**](windowsribbon-element-tab.md) поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="fe2d8-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="fe2d8-172">Разметка Ribbon допустима только в том случае, если дочерние элементы **группы** соответствуют шаблону, указанному для *сизедефинитион*.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="fe2d8-173">Примеры</span><span class="sxs-lookup"><span data-stu-id="fe2d8-173">Examples</span></span>

<span data-ttu-id="fe2d8-174">В следующем примере кода показано использование пользовательского шаблона в **группе**.</span><span class="sxs-lookup"><span data-stu-id="fe2d8-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="fe2d8-175">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="fe2d8-175">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="fe2d8-176">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="fe2d8-176">Minimum supported system</span></span><br/> | <span data-ttu-id="fe2d8-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe2d8-177">Windows 7</span></span> |
| <span data-ttu-id="fe2d8-178">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="fe2d8-178">Can be empty</span></span>                        | <span data-ttu-id="fe2d8-179">Нет</span><span class="sxs-lookup"><span data-stu-id="fe2d8-179">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="fe2d8-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe2d8-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2d8-181">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="fe2d8-181">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="fe2d8-182">Управление группой</span><span class="sxs-lookup"><span data-stu-id="fe2d8-182">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="fe2d8-183">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="fe2d8-183">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

