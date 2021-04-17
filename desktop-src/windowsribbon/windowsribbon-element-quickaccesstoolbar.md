---
title: Куиккакцесстулбар, элемент
description: Представляет панель быстрого доступа (QAT), маленькую панель инструментов, которая отображает ярлыки для команд ленты.
ms.assetid: 59aa35c3-a844-46b3-b066-c9a321fb0891
keywords:
- Лента Windows для элемента Куиккакцесстулбар
topic_type:
- apiref
api_name:
- QuickAccessToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0076890a8d9858d4bf410ecfdd866bf4f48fdbb6
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "104412445"
---
# <a name="quickaccesstoolbar-element"></a><span data-ttu-id="90236-104">Куиккакцесстулбар, элемент</span><span class="sxs-lookup"><span data-stu-id="90236-104">QuickAccessToolbar element</span></span>

<span data-ttu-id="90236-105">Представляет [панель быстрого доступа (QAT)](windowsribbon-controls-quickaccesstoolbar.md), маленькую панель инструментов, которая отображает ярлыки для команд ленты.</span><span class="sxs-lookup"><span data-stu-id="90236-105">Represents the [Quick Access Toolbar (QAT)](windowsribbon-controls-quickaccesstoolbar.md), a small toolbar that displays shortcuts to Ribbon Commands.</span></span>

## <a name="usage"></a><span data-ttu-id="90236-106">Использование</span><span class="sxs-lookup"><span data-stu-id="90236-106">Usage</span></span>

``` syntax
<QuickAccessToolbar
  CommandName = "xs:positiveInteger or xs:string"
  CustomizeCommandName = "xs:positiveInteger or xs:string">
  child elements
</QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="90236-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="90236-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90236-108">attribute</span><span class="sxs-lookup"><span data-stu-id="90236-108">Attribute</span></span></th>
<th><span data-ttu-id="90236-109">Тип</span><span class="sxs-lookup"><span data-stu-id="90236-109">Type</span></span></th>
<th><span data-ttu-id="90236-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="90236-110">Required</span></span></th>
<th><span data-ttu-id="90236-111">Описание</span><span class="sxs-lookup"><span data-stu-id="90236-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90236-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="90236-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="90236-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="90236-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="90236-114">Нет</span><span class="sxs-lookup"><span data-stu-id="90236-114">No</span></span><br/></td>
<td><span data-ttu-id="90236-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="90236-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="90236-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="90236-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="90236-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="90236-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="90236-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="90236-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="90236-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="90236-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90236-120"><strong>кустомизекомманднаме</strong></span><span class="sxs-lookup"><span data-stu-id="90236-120"><strong>CustomizeCommandName</strong></span></span><br/></td>
<td><span data-ttu-id="90236-121">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="90236-121">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="90236-122">Нет</span><span class="sxs-lookup"><span data-stu-id="90236-122">No</span></span><br/></td>
<td><span data-ttu-id="90236-123">Вставляет дополнительный элемент команды в меню QAT.</span><span class="sxs-lookup"><span data-stu-id="90236-123">Inserts an additional Command item in the QAT menu.</span></span><br/> <br/><span data-ttu-id="90236-124">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="90236-124">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <img src="images/markup/qat-customizecommandname.png" alt="Screen shot of a QAT menu with the More commands... Command item." /><br/> <span data-ttu-id="90236-125">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="90236-125">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="90236-126">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="90236-126">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="90236-127">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="90236-127">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="90236-128">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="90236-128">Child elements</span></span>



| <span data-ttu-id="90236-129">Элемент</span><span class="sxs-lookup"><span data-stu-id="90236-129">Element</span></span>                                                                                                                   | <span data-ttu-id="90236-130">Описание</span><span class="sxs-lookup"><span data-stu-id="90236-130">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="90236-131">**Куиккакцесстулбар. Аппликатиондефаултс**</span><span class="sxs-lookup"><span data-stu-id="90236-131">**QuickAccessToolbar.ApplicationDefaults**</span></span>](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md)<br/> | <span data-ttu-id="90236-132">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="90236-132">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="90236-133">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="90236-133">Parent elements</span></span>



| <span data-ttu-id="90236-134">Элемент</span><span class="sxs-lookup"><span data-stu-id="90236-134">Element</span></span>                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90236-135">**Лента. Куиккакцесстулбар**</span><span class="sxs-lookup"><span data-stu-id="90236-135">**Ribbon.QuickAccessToolbar**</span></span>](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="90236-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90236-136">Remarks</span></span>

<span data-ttu-id="90236-137">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="90236-137">Required.</span></span>

<span data-ttu-id="90236-138">Должен выполняться ровно один раз для каждой [**ленты. куиккакцесстулбар**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span><span class="sxs-lookup"><span data-stu-id="90236-138">Must occur exactly once for each [**Ribbon.QuickAccessToolbar**](windowsribbon-element-ribbon-quickaccesstoolbar.md).</span></span>

<span data-ttu-id="90236-139">Элементы в QAT могут быть добавлены или удалены во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="90236-139">Items in the QAT can be added or removed at run time.</span></span>

<span data-ttu-id="90236-140">Для обеспечения согласованности между приложениями ленты рекомендуется запустить диалоговое окно настройки QAT с помощью обработчика команд *кустомизекомманднаме* .</span><span class="sxs-lookup"><span data-stu-id="90236-140">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a QAT customization dialog.</span></span>

## <a name="examples"></a><span data-ttu-id="90236-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="90236-141">Examples</span></span>

<span data-ttu-id="90236-142">В следующем примере показана базовая разметка для **куиккакцесстулбар**.</span><span class="sxs-lookup"><span data-stu-id="90236-142">The following example demonstrates the basic markup for the **QuickAccessToolbar**.</span></span>

<span data-ttu-id="90236-143">В этом разделе кода показано объявление команды **куиккакцесстулбар** .</span><span class="sxs-lookup"><span data-stu-id="90236-143">This section of code shows the **QuickAccessToolbar** Command declaration.</span></span>


```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```



<span data-ttu-id="90236-144">В этом разделе кода показано объявление элемента управления **куиккакцесстулбар** .</span><span class="sxs-lookup"><span data-stu-id="90236-144">This section of code shows the **QuickAccessToolbar** control declaration.</span></span>


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



## <a name="element-information"></a><span data-ttu-id="90236-145">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="90236-145">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="90236-146">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="90236-146">Minimum supported system</span></span><br/> | <span data-ttu-id="90236-147">Windows 7</span><span class="sxs-lookup"><span data-stu-id="90236-147">Windows 7</span></span> |
| <span data-ttu-id="90236-148">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="90236-148">Can be empty</span></span>                        | <span data-ttu-id="90236-149">Нет</span><span class="sxs-lookup"><span data-stu-id="90236-149">No</span></span>        |



## <a name="see-also"></a><span data-ttu-id="90236-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="90236-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90236-151">Элемент управления панели быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="90236-151">Quick Access Toolbar control</span></span>](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





