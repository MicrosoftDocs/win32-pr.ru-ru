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
ms.openlocfilehash: 1162055491f61ae6feffa385bbc5015e4f1b66f0
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442875"
---
# <a name="group-element"></a><span data-ttu-id="0f6ab-104">Group, элемент</span><span class="sxs-lookup"><span data-stu-id="0f6ab-104">Group element</span></span>

<span data-ttu-id="0f6ab-105">Представляет элемент управления " [Группа](windowsribbon-controls-group.md) ", который выступает в качестве контейнера для группы элементов.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-105">Represents a [Group](windowsribbon-controls-group.md) control that functions as a container for a group of elements.</span></span>

## <a name="usage"></a><span data-ttu-id="0f6ab-106">Использование</span><span class="sxs-lookup"><span data-stu-id="0f6ab-106">Usage</span></span>

``` syntax
<Group
  SizeDefinition = "xs:string"
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</Group>
```

## <a name="attributes"></a><span data-ttu-id="0f6ab-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0f6ab-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0f6ab-108">attribute</span><span class="sxs-lookup"><span data-stu-id="0f6ab-108">Attribute</span></span></th>
<th><span data-ttu-id="0f6ab-109">Тип</span><span class="sxs-lookup"><span data-stu-id="0f6ab-109">Type</span></span></th>
<th><span data-ttu-id="0f6ab-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="0f6ab-110">Required</span></span></th>
<th><span data-ttu-id="0f6ab-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0f6ab-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0f6ab-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="0f6ab-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="0f6ab-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f6ab-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="0f6ab-114">Нет</span><span class="sxs-lookup"><span data-stu-id="0f6ab-114">No</span></span><br/></td>
<td><span data-ttu-id="0f6ab-115"><dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="0f6ab-115"><dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0f6ab-116">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-116">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="0f6ab-117">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-117">White space is valid and ignored.</span></span><br/> <span data-ttu-id="0f6ab-118">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-118">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0f6ab-119"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="0f6ab-119"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="0f6ab-120">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="0f6ab-120">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="0f6ab-121">Нет</span><span class="sxs-lookup"><span data-stu-id="0f6ab-121">No</span></span><br/></td>
<td><span data-ttu-id="0f6ab-122">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-122">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="0f6ab-123">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="0f6ab-123">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0f6ab-124">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-124">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="0f6ab-125">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-125">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="0f6ab-126">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-126">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0f6ab-127"><strong>сизедефинитион</strong></span><span class="sxs-lookup"><span data-stu-id="0f6ab-127"><strong>SizeDefinition</strong></span></span><br/></td>
<td><span data-ttu-id="0f6ab-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="0f6ab-128">xs:string</span></span><br/></td>
<td><span data-ttu-id="0f6ab-129">Нет</span><span class="sxs-lookup"><span data-stu-id="0f6ab-129">No</span></span><br/></td>
<td><span data-ttu-id="0f6ab-130">При указании значения <em>сизедефинитион</em> ограничивается одним из <a href="windowsribbon-templates.md">шаблонов макета</a> , определенных платформой Ribbon.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-130">When specified, the value of <em>SizeDefinition</em> is constrained to one of the <a href="windowsribbon-templates.md">layout templates</a> defined by the Ribbon framework.</span></span> <br/> <br/><span data-ttu-id="0f6ab-131">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="0f6ab-131">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="0f6ab-132">Любая последовательность из нуля или более символов.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-132">Any sequence of zero or more characters.</span></span><br/> <span data-ttu-id="0f6ab-133">Максимальная длина не ограничена.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-133">The maximum length is unbounded.</span></span><br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="0f6ab-134">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0f6ab-134">Child elements</span></span>



| <span data-ttu-id="0f6ab-135">Элемент</span><span class="sxs-lookup"><span data-stu-id="0f6ab-135">Element</span></span>                                                                             | <span data-ttu-id="0f6ab-136">Описание</span><span class="sxs-lookup"><span data-stu-id="0f6ab-136">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0f6ab-137">**Button**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-137">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="0f6ab-138">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-139">**Установка**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-139">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="0f6ab-140">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-141">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-141">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="0f6ab-142">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-143">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-143">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>               | <span data-ttu-id="0f6ab-144">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-144">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-145">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-145">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>           | <span data-ttu-id="0f6ab-146">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-147">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-147">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="0f6ab-148">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-149">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-149">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="0f6ab-150">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-150">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-151">**фонтконтрол**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-151">**FontControl**</span></span>](windowsribbon-element-fontcontrol.md)<br/>                 | <span data-ttu-id="0f6ab-152">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="0f6ab-152">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="0f6ab-153">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-153">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/>         | <span data-ttu-id="0f6ab-154">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-154">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-155">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-155">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/>           | <span data-ttu-id="0f6ab-156">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="0f6ab-156">May occur at most once</span></span><br/> <br/>      |
| [<span data-ttu-id="0f6ab-157">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-157">**Spinner**</span></span>](windowsribbon-element-spinner.md)<br/>                         | <span data-ttu-id="0f6ab-158">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-158">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-159">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-159">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="0f6ab-160">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-160">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-161">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-161">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="0f6ab-162">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-162">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="0f6ab-163">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-163">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="0f6ab-164">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0f6ab-164">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0f6ab-165">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0f6ab-165">Parent elements</span></span>



| <span data-ttu-id="0f6ab-166">Элемент</span><span class="sxs-lookup"><span data-stu-id="0f6ab-166">Element</span></span>                                             |
|-----------------------------------------------------|
| [<span data-ttu-id="0f6ab-167">**Вкладка**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-167">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0f6ab-168">Remarks</span><span class="sxs-lookup"><span data-stu-id="0f6ab-168">Remarks</span></span>

<span data-ttu-id="0f6ab-169">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-169">Optional.</span></span>

<span data-ttu-id="0f6ab-170">Может происходить один или несколько раз для каждого элемента [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6ab-170">May occur one or more times for each [**Tab**](windowsribbon-element-tab.md) element.</span></span>

<span data-ttu-id="0f6ab-171">[**Вкладка**](windowsribbon-element-tab.md) поддерживает [режимы приложений](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="0f6ab-171">[**Tab**](windowsribbon-element-tab.md) supports [application modes](ribbon-applicationmodes.md).</span></span>

<span data-ttu-id="0f6ab-172">Разметка Ribbon допустима только в том случае, если дочерние элементы **группы** соответствуют шаблону, указанному для *сизедефинитион*.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-172">The Ribbon markup is valid only when the child elements of **Group** correspond to the template specified for *SizeDefinition*.</span></span>

## <a name="examples"></a><span data-ttu-id="0f6ab-173">Примеры</span><span class="sxs-lookup"><span data-stu-id="0f6ab-173">Examples</span></span>

<span data-ttu-id="0f6ab-174">В следующем примере кода показано использование пользовательского шаблона в **группе**.</span><span class="sxs-lookup"><span data-stu-id="0f6ab-174">The following code example illustrates the use of a custom template in a **Group**.</span></span>


```
<Group CommandName="cmdCustomGroup1" SizeDefinition="CustomTemplate">
  <Button CommandName="cmdCommand1" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="0f6ab-175">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0f6ab-175">Element information</span></span>

* <span data-ttu-id="0f6ab-176">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="0f6ab-176">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="0f6ab-177">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="0f6ab-177">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="0f6ab-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f6ab-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6ab-179">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="0f6ab-179">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> <dt>

[<span data-ttu-id="0f6ab-180">Управление группой</span><span class="sxs-lookup"><span data-stu-id="0f6ab-180">Group control</span></span>](windowsribbon-controls-group.md)
</dt> <dt>

[<span data-ttu-id="0f6ab-181">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="0f6ab-181">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

