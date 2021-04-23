---
title: ToggleButton, элемент
description: Представляет элемент управления "выключатель".
ms.assetid: f26a90e6-9e9a-4fde-8753-50b8b1d09f80
keywords:
- Лента Windows для элемента ToggleButton
topic_type:
- apiref
api_name:
- ToggleButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 652ea7b535f41cc3dbb40f25bbe49ab4fe52f5ff
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104336143"
---
# <a name="togglebutton-element"></a><span data-ttu-id="141fe-104">ToggleButton, элемент</span><span class="sxs-lookup"><span data-stu-id="141fe-104">ToggleButton element</span></span>

<span data-ttu-id="141fe-105">Представляет элемент управления ["выключатель"](windowsribbon-controls-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="141fe-105">Represents a [Toggle Button](windowsribbon-controls-togglebutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="141fe-106">Использование</span><span class="sxs-lookup"><span data-stu-id="141fe-106">Usage</span></span>

``` syntax
<ToggleButton
  CommandName = "xs:positiveInteger or xs:string"
  ApplicationDefaults.IsChecked = "Boolean"/>
```

## <a name="attributes"></a><span data-ttu-id="141fe-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="141fe-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="141fe-108">attribute</span><span class="sxs-lookup"><span data-stu-id="141fe-108">Attribute</span></span></th>
<th><span data-ttu-id="141fe-109">Тип</span><span class="sxs-lookup"><span data-stu-id="141fe-109">Type</span></span></th>
<th><span data-ttu-id="141fe-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="141fe-110">Required</span></span></th>
<th><span data-ttu-id="141fe-111">Описание</span><span class="sxs-lookup"><span data-stu-id="141fe-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="141fe-112"><strong>Аппликатиондефаултс. Check</strong></span><span class="sxs-lookup"><span data-stu-id="141fe-112"><strong>ApplicationDefaults.IsChecked</strong></span></span><br/></td>
<td><span data-ttu-id="141fe-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="141fe-113">Boolean</span></span><br/></td>
<td><span data-ttu-id="141fe-114">Нет</span><span class="sxs-lookup"><span data-stu-id="141fe-114">No</span></span><br/></td>
<td><span data-ttu-id="141fe-115">Этот атрибут допустим, только если элемент <strong>ToggleButton</strong> является дочерним для <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>куиккакцесстулбар. аппликатиондефаултс</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="141fe-115">This attribute is valid only when the <strong>ToggleButton</strong> element is a child of <a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a>.</span></span> <br/> <span data-ttu-id="141fe-116">Ограничено одним из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="141fe-116">Restricted to one of the following values:</span></span><br/> <br/><span data-ttu-id="141fe-117">
<dt><span></span><span></span><strong></strong> условия</span><span class="sxs-lookup"><span data-stu-id="141fe-117">
<dt><span></span><span></span><strong></strong> (true)</span></span><br/> </dt> <dd> <span data-ttu-id="141fe-118">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="141fe-118">Default.</span></span> <br/> </dd> <span data-ttu-id="141fe-119"><dt><span></span><span></span><strong></strong> IsFalse</span><span class="sxs-lookup"><span data-stu-id="141fe-119"><dt><span></span><span></span><strong></strong> (false)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="141fe-120"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="141fe-120"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="141fe-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="141fe-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="141fe-122">Нет</span><span class="sxs-lookup"><span data-stu-id="141fe-122">No</span></span><br/></td>
<td><span data-ttu-id="141fe-123">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="141fe-123">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="141fe-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="141fe-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="141fe-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="141fe-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="141fe-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="141fe-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="141fe-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="141fe-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="141fe-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="141fe-128">Child elements</span></span>

<span data-ttu-id="141fe-129">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="141fe-129">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="141fe-130">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="141fe-130">Parent elements</span></span>



| <span data-ttu-id="141fe-131">Элемент</span><span class="sxs-lookup"><span data-stu-id="141fe-131">Element</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="141fe-132">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="141fe-132">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>                                                     |
| [<span data-ttu-id="141fe-133">**DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="141fe-133">**DropDownButton**</span></span>](windowsribbon-element-dropdownbutton.md)<br/>                                                 |
| [<span data-ttu-id="141fe-134">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="141fe-134">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>                                               |
| [<span data-ttu-id="141fe-135">**Группа**</span><span class="sxs-lookup"><span data-stu-id="141fe-135">**Group**</span></span>](windowsribbon-element-group.md)<br/>                                                                   |
| [<span data-ttu-id="141fe-136">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="141fe-136">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                                                           |
| [<span data-ttu-id="141fe-137">**Куиккакцесстулбар. Аппликатиондефаултс**</span><span class="sxs-lookup"><span data-stu-id="141fe-137">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> |
| [<span data-ttu-id="141fe-138">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="141fe-138">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/>                                                       |
| [<span data-ttu-id="141fe-139">**SplitButton. Буттонитем**</span><span class="sxs-lookup"><span data-stu-id="141fe-139">**SplitButton.ButtonItem**</span></span>](windowsribbon-element-splitbutton-buttonitem.md)<br/>                                 |
| [<span data-ttu-id="141fe-140">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="141fe-140">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/>                                         |



## <a name="remarks"></a><span data-ttu-id="141fe-141">Комментарии</span><span class="sxs-lookup"><span data-stu-id="141fe-141">Remarks</span></span>

<span data-ttu-id="141fe-142">Необязательный или обязательный в зависимости от родительского элемента.</span><span class="sxs-lookup"><span data-stu-id="141fe-142">Optional or required, depending on the parent element.</span></span>

<span data-ttu-id="141fe-143">Может встречаться не более одного раза для каждого элемента [**SplitButton. буттонитем**](windowsribbon-element-splitbutton-buttonitem.md) .</span><span class="sxs-lookup"><span data-stu-id="141fe-143">May occur at most once for each [**SplitButton.ButtonItem**](windowsribbon-element-splitbutton-buttonitem.md) element.</span></span>

<span data-ttu-id="141fe-144">Может возникнуть один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**менуграуп**](windowsribbon-element-menugroup.md), [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md)или [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="141fe-144">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**DropDownGallery**](windowsribbon-element-dropdowngallery.md), [**MenuGroup**](windowsribbon-element-menugroup.md), [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md), [**SplitButton**](windowsribbon-element-splitbutton.md), or [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="141fe-145">Примеры</span><span class="sxs-lookup"><span data-stu-id="141fe-145">Examples</span></span>

<span data-ttu-id="141fe-146">В следующем примере показана базовая разметка для элемента **ToggleButton** .</span><span class="sxs-lookup"><span data-stu-id="141fe-146">The following example demonstrates the basic markup for the **ToggleButton** element.</span></span>

<span data-ttu-id="141fe-147">В этом разделе кода показано объявление элемента **ToggleButton** в элементе [**куиккакцесстулбар. аппликатиондефаултс**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) .</span><span class="sxs-lookup"><span data-stu-id="141fe-147">This section of code shows a **ToggleButton** element declaration within the [**QuickAccessToolbar.ApplicationDefaults**](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="element-information"></a><span data-ttu-id="141fe-148">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="141fe-148">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="141fe-149">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="141fe-149">Minimum supported system</span></span><br/> | <span data-ttu-id="141fe-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="141fe-150">Windows 7</span></span> |
| <span data-ttu-id="141fe-151">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="141fe-151">Can be empty</span></span>                        | <span data-ttu-id="141fe-152">Да</span><span class="sxs-lookup"><span data-stu-id="141fe-152">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="141fe-153">См. также</span><span class="sxs-lookup"><span data-stu-id="141fe-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="141fe-154">Элемент управления "выключатель"</span><span class="sxs-lookup"><span data-stu-id="141fe-154">Toggle Button control</span></span>](windowsribbon-controls-togglebutton.md)
</dt> </dl>

 

 





