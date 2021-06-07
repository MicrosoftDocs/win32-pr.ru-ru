---
title: Хелпбуттон, элемент
description: Представляет элемент управления кнопки справки.
ms.assetid: 24c709da-539e-4ea0-bd3e-d3fbd72dfb97
keywords:
- Лента Windows для элемента Хелпбуттон
topic_type:
- apiref
api_name:
- HelpButton
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f34f04133b7628cce01ac0ce2808923b4f6bbdb
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442845"
---
# <a name="helpbutton-element"></a><span data-ttu-id="c5e6c-104">Хелпбуттон, элемент</span><span class="sxs-lookup"><span data-stu-id="c5e6c-104">HelpButton element</span></span>

<span data-ttu-id="c5e6c-105">Представляет элемент управления [кнопки справки](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="c5e6c-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="c5e6c-106">Использование</span><span class="sxs-lookup"><span data-stu-id="c5e6c-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="c5e6c-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c5e6c-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5e6c-108">attribute</span><span class="sxs-lookup"><span data-stu-id="c5e6c-108">Attribute</span></span></th>
<th><span data-ttu-id="c5e6c-109">Тип</span><span class="sxs-lookup"><span data-stu-id="c5e6c-109">Type</span></span></th>
<th><span data-ttu-id="c5e6c-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c5e6c-110">Required</span></span></th>
<th><span data-ttu-id="c5e6c-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c5e6c-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5e6c-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="c5e6c-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="c5e6c-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="c5e6c-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="c5e6c-114">Нет</span><span class="sxs-lookup"><span data-stu-id="c5e6c-114">No</span></span><br/></td>
<td><span data-ttu-id="c5e6c-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="c5e6c-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="c5e6c-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="c5e6c-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="c5e6c-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="c5e6c-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="c5e6c-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c5e6c-120">Child elements</span></span>

<span data-ttu-id="c5e6c-121">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="c5e6c-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c5e6c-122">Parent elements</span></span>



| <span data-ttu-id="c5e6c-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="c5e6c-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="c5e6c-124">**Лента. Хелпбуттон**</span><span class="sxs-lookup"><span data-stu-id="c5e6c-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="c5e6c-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="c5e6c-125">Remarks</span></span>

<span data-ttu-id="c5e6c-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-126">Optional.</span></span>

<span data-ttu-id="c5e6c-127">Может встречаться не более одного раза для каждой [**ленты. хелпбуттон**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="c5e6c-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="c5e6c-128">Открывает диалоговое окно Справка по приложению при щелчке.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="c5e6c-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="c5e6c-129">Examples</span></span>

<span data-ttu-id="c5e6c-130">В следующем примере показана базовая разметка, необходимая для реализации элемента управления [кнопки справки](windowsribbon-controls-helpbutton.md) на ленте.</span><span class="sxs-lookup"><span data-stu-id="c5e6c-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="c5e6c-131">В этом разделе кода показано объявление команды **хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="c5e6c-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="c5e6c-132">В этом разделе кода показано объявление элемента управления **хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="c5e6c-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="c5e6c-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="c5e6c-133">Element information</span></span>

* <span data-ttu-id="c5e6c-134">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="c5e6c-134">**Minimum supported system**: Windows 7</span></span>
* <span data-ttu-id="c5e6c-135">**Может быть пустым**: Да</span><span class="sxs-lookup"><span data-stu-id="c5e6c-135">**Can be empty**: Yes</span></span>



## <a name="see-also"></a><span data-ttu-id="c5e6c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c5e6c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5e6c-137">Элемент управления кнопки "Справка"</span><span class="sxs-lookup"><span data-stu-id="c5e6c-137">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





