---
title: Элемент счетчика
description: Представляет элемент управления "Счетчик".
ms.assetid: 6a174ec9-0fde-4171-a363-0e330ac31a8b
keywords:
- Лента Windows для элемента счетчика
topic_type:
- apiref
api_name:
- Spinner
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1ec2e074271e125199ddfd4ff8fac7b2af80c33
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444815"
---
# <a name="spinner-element"></a><span data-ttu-id="ecac7-104">Элемент счетчика</span><span class="sxs-lookup"><span data-stu-id="ecac7-104">Spinner element</span></span>

<span data-ttu-id="ecac7-105">Представляет элемент управления " [Счетчик](windowsribbon-controls-spinner.md) ".</span><span class="sxs-lookup"><span data-stu-id="ecac7-105">Represents a [Spinner](windowsribbon-controls-spinner.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="ecac7-106">Использование</span><span class="sxs-lookup"><span data-stu-id="ecac7-106">Usage</span></span>

``` syntax
<Spinner
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="ecac7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ecac7-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ecac7-108">attribute</span><span class="sxs-lookup"><span data-stu-id="ecac7-108">Attribute</span></span></th>
<th><span data-ttu-id="ecac7-109">Тип</span><span class="sxs-lookup"><span data-stu-id="ecac7-109">Type</span></span></th>
<th><span data-ttu-id="ecac7-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ecac7-110">Required</span></span></th>
<th><span data-ttu-id="ecac7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ecac7-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ecac7-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="ecac7-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="ecac7-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="ecac7-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="ecac7-114">Нет</span><span class="sxs-lookup"><span data-stu-id="ecac7-114">No</span></span><br/></td>
<td><span data-ttu-id="ecac7-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ecac7-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="ecac7-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="ecac7-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="ecac7-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="ecac7-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="ecac7-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="ecac7-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="ecac7-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="ecac7-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="ecac7-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ecac7-120">Child elements</span></span>

<span data-ttu-id="ecac7-121">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="ecac7-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ecac7-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ecac7-122">Parent elements</span></span>



| <span data-ttu-id="ecac7-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="ecac7-123">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ecac7-124">**контролграуп**</span><span class="sxs-lookup"><span data-stu-id="ecac7-124">**ControlGroup**</span></span>](windowsribbon-element-controlgroup.md)<br/>             |
| [<span data-ttu-id="ecac7-125">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="ecac7-125">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/>       |
| [<span data-ttu-id="ecac7-126">**Группа**</span><span class="sxs-lookup"><span data-stu-id="ecac7-126">**Group**</span></span>](windowsribbon-element-group.md)<br/>                           |
| [<span data-ttu-id="ecac7-127">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="ecac7-127">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/>                   |
| [<span data-ttu-id="ecac7-128">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="ecac7-128">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ecac7-129">Remarks</span><span class="sxs-lookup"><span data-stu-id="ecac7-129">Remarks</span></span>

<span data-ttu-id="ecac7-130">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ecac7-130">Optional.</span></span>

<span data-ttu-id="ecac7-131">Может происходить один или несколько раз для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md) или [**Group**](windowsribbon-element-group.md) .</span><span class="sxs-lookup"><span data-stu-id="ecac7-131">May occur one or more times for each [**ControlGroup**](windowsribbon-element-controlgroup.md) or [**Group**](windowsribbon-element-group.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="ecac7-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="ecac7-132">Examples</span></span>

<span data-ttu-id="ecac7-133">В следующем примере показана базовая разметка для [счетчика](windowsribbon-controls-spinner.md).</span><span class="sxs-lookup"><span data-stu-id="ecac7-133">The following example demonstrates the basic markup for the [Spinner](windowsribbon-controls-spinner.md).</span></span>

<span data-ttu-id="ecac7-134">В этом разделе кода показаны объявления команд **счетчика** с элементом [**группы**](windowsribbon-element-group.md) , который выступает в качестве родительского контейнера для элемента **счетчика** .</span><span class="sxs-lookup"><span data-stu-id="ecac7-134">This section of code shows the **Spinner** Command declarations, with a [**Group**](windowsribbon-element-group.md) element that functions as the parent container for the **Spinner** element.</span></span>


```XML
<Command Name="GroupSpinner1" Symbol="IDR_CMD_GROUPSPINNER1" Id="30010">
  <Command.LabelTitle>
    <String Id="210">Resize</String>
  </Command.LabelTitle>
</Command>
<Command Name="Spinner_Size" Symbol="IDR_CMD_SPINNER_RESIZE" Id="30015">
  <Command.LabelTitle>
    <String Id="215">Resize by:</String>
  </Command.LabelTitle>
</Command>
```



<span data-ttu-id="ecac7-135">В этом разделе кода показаны объявления элемента управления " **Счетчик** ".</span><span class="sxs-lookup"><span data-stu-id="ecac7-135">This section of code shows the **Spinner** control declarations.</span></span>


```XML
<Group CommandName="GroupSpinner1">
  <Spinner CommandName="Spinner_Size" />
</Group>
```



## <a name="element-information"></a><span data-ttu-id="ecac7-136">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ecac7-136">Element information</span></span>

- <span data-ttu-id="ecac7-137">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="ecac7-137">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="ecac7-138">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="ecac7-138">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="ecac7-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecac7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecac7-140">Элемент управления "Счетчик"</span><span class="sxs-lookup"><span data-stu-id="ecac7-140">Spinner control</span></span>](windowsribbon-controls-spinner.md)
</dt> </dl>

 

 





