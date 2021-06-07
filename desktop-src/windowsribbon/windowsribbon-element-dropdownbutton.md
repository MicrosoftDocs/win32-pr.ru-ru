---
title: DropDownButton, элемент
description: Представляет стандартный элемент управления "кнопка Drop-Down".
ms.assetid: 41031be2-43bc-4f75-b37a-1dcecc1635e1
keywords:
- Лента Windows для элемента DropDownButton
topic_type:
- apiref
api_name:
- DropDownButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a42b8ffb6d39c1da8993972c0b25995f778bdaca
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442965"
---
# <a name="dropdownbutton-element"></a><span data-ttu-id="372a6-104">DropDownButton, элемент</span><span class="sxs-lookup"><span data-stu-id="372a6-104">DropDownButton element</span></span>

<span data-ttu-id="372a6-105">Представляет стандартный элемент управления "раскрывающийся [список"](windowsribbon-controls-dropdownbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="372a6-105">Represents a standard [Drop-Down Button](windowsribbon-controls-dropdownbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="372a6-106">Использование</span><span class="sxs-lookup"><span data-stu-id="372a6-106">Usage</span></span>

``` syntax
<DropDownButton
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</DropDownButton>
```

## <a name="attributes"></a><span data-ttu-id="372a6-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="372a6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="372a6-108">attribute</span><span class="sxs-lookup"><span data-stu-id="372a6-108">Attribute</span></span></th>
<th><span data-ttu-id="372a6-109">Тип</span><span class="sxs-lookup"><span data-stu-id="372a6-109">Type</span></span></th>
<th><span data-ttu-id="372a6-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="372a6-110">Required</span></span></th>
<th><span data-ttu-id="372a6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="372a6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="372a6-112"><strong>аппликатионмодес</strong></span><span class="sxs-lookup"><span data-stu-id="372a6-112"><strong>ApplicationModes</strong></span></span><br/></td>
<td><span data-ttu-id="372a6-113">xs:string</span><span class="sxs-lookup"><span data-stu-id="372a6-113">xs:string</span></span><br/></td>
<td><span data-ttu-id="372a6-114">Нет</span><span class="sxs-lookup"><span data-stu-id="372a6-114">No</span></span><br/></td>
<td><span data-ttu-id="372a6-115">Допустимо, только если <a href="windowsribbon-element-menugroup.md"><strong>менуграуп</strong></a> является родительским элементом.</span><span class="sxs-lookup"><span data-stu-id="372a6-115">Valid only if <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> is the parent element.</span></span><br/> <br/><span data-ttu-id="372a6-116">
<dt><span></span><span></span><strong></strong> (xs: String)</span><span class="sxs-lookup"><span data-stu-id="372a6-116">
<dt><span></span><span></span><strong></strong> (xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="372a6-117">Строка, содержащая разделенный запятыми список целых чисел от 0 до 31.</span><span class="sxs-lookup"><span data-stu-id="372a6-117">A string that contains a comma-separated list of integers between 0 and 31.</span></span><br/> <span data-ttu-id="372a6-118">Пробелы допустимы и пропускаются.</span><span class="sxs-lookup"><span data-stu-id="372a6-118">White space is valid and ignored.</span></span><br/> <span data-ttu-id="372a6-119">Максимальная длина: 250 символов.</span><span class="sxs-lookup"><span data-stu-id="372a6-119">Maximum length: 250 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="372a6-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="372a6-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="372a6-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="372a6-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="372a6-122">Нет</span><span class="sxs-lookup"><span data-stu-id="372a6-122">No</span></span><br/></td>
<td><span data-ttu-id="372a6-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="372a6-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="372a6-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="372a6-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="372a6-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="372a6-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="372a6-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="372a6-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="372a6-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="372a6-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="372a6-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="372a6-128">Child elements</span></span>



| <span data-ttu-id="372a6-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="372a6-129">Element</span></span>                                                                             | <span data-ttu-id="372a6-130">Описание</span><span class="sxs-lookup"><span data-stu-id="372a6-130">Description</span></span>                                        |
|-------------------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="372a6-131">**Button**</span><span class="sxs-lookup"><span data-stu-id="372a6-131">**Button**</span></span>](windowsribbon-element-button.md)<br/>                           | <span data-ttu-id="372a6-132">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-132">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-133">**Установка**</span><span class="sxs-lookup"><span data-stu-id="372a6-133">**CheckBox**</span></span>](windowsribbon-element-checkbox.md)<br/>                       | <span data-ttu-id="372a6-134">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-134">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-135">**ComboBox**</span><span class="sxs-lookup"><span data-stu-id="372a6-135">**ComboBox**</span></span>](windowsribbon-element-combobox.md)<br/>                       | <span data-ttu-id="372a6-136">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-136">May occur one or more times</span></span><br/> <br/> |
| <span data-ttu-id="372a6-137">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="372a6-137">**DropDownButton**</span></span><br/>                                                       | <span data-ttu-id="372a6-138">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-138">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-139">**дропдовнколорпиккер**</span><span class="sxs-lookup"><span data-stu-id="372a6-139">**DropDownColorPicker**</span></span>](windowsribbon-element-dropdowncolorpicker.md)<br/> | <span data-ttu-id="372a6-140">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-140">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-141">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="372a6-141">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>         | <span data-ttu-id="372a6-142">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-142">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-143">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="372a6-143">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                     | <span data-ttu-id="372a6-144">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="372a6-144">Must occur at least once</span></span><br/> <br/>    |
| [<span data-ttu-id="372a6-145">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="372a6-145">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                 | <span data-ttu-id="372a6-146">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-146">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-147">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="372a6-147">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>   | <span data-ttu-id="372a6-148">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-148">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="372a6-149">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="372a6-149">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/>               | <span data-ttu-id="372a6-150">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="372a6-150">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="372a6-151">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="372a6-151">Parent elements</span></span>



| <span data-ttu-id="372a6-152">Элемент</span><span class="sxs-lookup"><span data-stu-id="372a6-152">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="372a6-153">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="372a6-153">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| <span data-ttu-id="372a6-154">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="372a6-154">**DropDownButton**</span></span><br/>                                                     |
| [<span data-ttu-id="372a6-155">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="372a6-155">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="372a6-156">**Группа**</span><span class="sxs-lookup"><span data-stu-id="372a6-156">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="372a6-157">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="372a6-157">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="372a6-158">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="372a6-158">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>               |
| [<span data-ttu-id="372a6-159">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="372a6-159">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="372a6-160">Remarks</span><span class="sxs-lookup"><span data-stu-id="372a6-160">Remarks</span></span>

<span data-ttu-id="372a6-161">Необязательный или обязательный в зависимости от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="372a6-161">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="372a6-162">Может возникать один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="372a6-162">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), **DropDownButton**, [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

<span data-ttu-id="372a6-163">**DropDownButton** поддерживает [режимы приложений](ribbon-applicationmodes.md) , если они размещены в левом столбце меню приложения.</span><span class="sxs-lookup"><span data-stu-id="372a6-163">**DropDownButton** supports [application modes](ribbon-applicationmodes.md) when it is hosted in the left column of the Application Menu.</span></span>

<span data-ttu-id="372a6-164">[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) и [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) не являются допустимыми дочерними элементами **DropDownButton** , если **DropDownButton** является потомком [**аппликатионмену**](windowsribbon-element-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="372a6-164">[**DropDownGallery**](windowsribbon-element-dropdowngallery.md) and [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) are not valid child elements of **DropDownButton** when **DropDownButton** is a descendant of [**ApplicationMenu**](windowsribbon-element-applicationmenu.md).</span></span>

## <a name="examples"></a><span data-ttu-id="372a6-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="372a6-165">Examples</span></span>

<span data-ttu-id="372a6-166">В следующем примере показана базовая разметка для **DropDownButton**.</span><span class="sxs-lookup"><span data-stu-id="372a6-166">The following example demonstrates the basic markup for the **DropDownButton**.</span></span>

<span data-ttu-id="372a6-167">В этом разделе кода показаны объявления команд **DropDownButton** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="372a6-167">This section of code shows the **DropDownButton** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **DropDownButton** element.</span></span>


```XML
<!-- DropDownButton -->
<Command Name="cmdDropDownButtonGroup"
         Symbol="cmdDropDownButtonGroup"
         Comment="DropDownButton Group"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDropDownButton"
         Symbol="cmdDropDownButton"
         Comment="DropDownButton"
         LabelTitle="DropDownButton"/>
<Command Name="cmdDDBButton1"
         Symbol="cmdDDBButton1"
         Comment="DDBButton1"
         LabelTitle="DDB Button"/>
<Command Name="cmdDDBColorPicker"
         Symbol="cmdDDBColorPicker"
         Comment="DDBColorPicker"
         LabelTitle="DDB ColorPicker"/>
```



<span data-ttu-id="372a6-168">В этом разделе кода показаны объявления элементов управления **DropDownButton** .</span><span class="sxs-lookup"><span data-stu-id="372a6-168">This section of code shows the **DropDownButton** control declarations.</span></span>


```XML
<Group CommandName="cmdDropDownButtonGroup">
  <DropDownButton CommandName="cmdDropDownButton">
    <MenuGroup>
      <Button CommandName="cmdDDBButton1"/>
      <DropDownColorPicker CommandName="cmdDDBColorPicker"/>
    </MenuGroup>
  </DropDownButton>
</Group>
```



## <a name="element-information"></a><span data-ttu-id="372a6-169">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="372a6-169">Element information</span></span>

* <span data-ttu-id="372a6-170">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="372a6-170">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="372a6-171">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="372a6-171">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="372a6-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="372a6-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372a6-173">Элемент управления "Кнопка раскрывающегося списка"</span><span class="sxs-lookup"><span data-stu-id="372a6-173">Drop-Down Button control</span></span>](windowsribbon-controls-dropdownbutton.md)
</dt> <dt>

[<span data-ttu-id="372a6-174">**сетмодес**</span><span class="sxs-lookup"><span data-stu-id="372a6-174">**SetModes**</span></span>](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> </dl>

 

