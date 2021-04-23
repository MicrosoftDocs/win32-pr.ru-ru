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
ms.openlocfilehash: 5be084ff6fc92d4eac4bbaffb3c507142f91eba8
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/11/2020
ms.locfileid: "105691428"
---
# <a name="helpbutton-element"></a><span data-ttu-id="2c9f6-104">Хелпбуттон, элемент</span><span class="sxs-lookup"><span data-stu-id="2c9f6-104">HelpButton element</span></span>

<span data-ttu-id="2c9f6-105">Представляет элемент управления [кнопки справки](windowsribbon-controls-helpbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="2c9f6-105">Represents the [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="2c9f6-106">Использование</span><span class="sxs-lookup"><span data-stu-id="2c9f6-106">Usage</span></span>

``` syntax
<HelpButton
  CommandName = "xs:positiveInteger or xs:string"/>
```

## <a name="attributes"></a><span data-ttu-id="2c9f6-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2c9f6-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c9f6-108">attribute</span><span class="sxs-lookup"><span data-stu-id="2c9f6-108">Attribute</span></span></th>
<th><span data-ttu-id="2c9f6-109">Тип</span><span class="sxs-lookup"><span data-stu-id="2c9f6-109">Type</span></span></th>
<th><span data-ttu-id="2c9f6-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="2c9f6-110">Required</span></span></th>
<th><span data-ttu-id="2c9f6-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2c9f6-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c9f6-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="2c9f6-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="2c9f6-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="2c9f6-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="2c9f6-114">Нет</span><span class="sxs-lookup"><span data-stu-id="2c9f6-114">No</span></span><br/></td>
<td><span data-ttu-id="2c9f6-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="2c9f6-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="2c9f6-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="2c9f6-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="2c9f6-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="2c9f6-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="2c9f6-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2c9f6-120">Child elements</span></span>

<span data-ttu-id="2c9f6-121">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-121">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="2c9f6-122">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2c9f6-122">Parent elements</span></span>



| <span data-ttu-id="2c9f6-123">Элемент</span><span class="sxs-lookup"><span data-stu-id="2c9f6-123">Element</span></span>                                                                         |
|---------------------------------------------------------------------------------|
| [<span data-ttu-id="2c9f6-124">**Лента. Хелпбуттон**</span><span class="sxs-lookup"><span data-stu-id="2c9f6-124">**Ribbon.HelpButton**</span></span>](windowsribbon-element-ribbon-helpbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2c9f6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c9f6-125">Remarks</span></span>

<span data-ttu-id="2c9f6-126">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-126">Optional.</span></span>

<span data-ttu-id="2c9f6-127">Может встречаться не более одного раза для каждой [**ленты. хелпбуттон**](windowsribbon-element-ribbon-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="2c9f6-127">May occur at most once for each [**Ribbon.HelpButton**](windowsribbon-element-ribbon-helpbutton.md).</span></span>

<span data-ttu-id="2c9f6-128">Открывает диалоговое окно Справка по приложению при щелчке.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-128">Launches an application help dialog box when clicked.</span></span>

## <a name="examples"></a><span data-ttu-id="2c9f6-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="2c9f6-129">Examples</span></span>

<span data-ttu-id="2c9f6-130">В следующем примере показана базовая разметка, необходимая для реализации элемента управления [кнопки справки](windowsribbon-controls-helpbutton.md) на ленте.</span><span class="sxs-lookup"><span data-stu-id="2c9f6-130">The following example demonstrates the basic markup that is required to implement a Ribbon [Help Button](windowsribbon-controls-helpbutton.md) control.</span></span>

<span data-ttu-id="2c9f6-131">В этом разделе кода показано объявление команды **хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="2c9f6-131">This section of code shows the **HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="2c9f6-132">В этом разделе кода показано объявление элемента управления **хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="2c9f6-132">This section of code shows the **HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="element-information"></a><span data-ttu-id="2c9f6-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2c9f6-133">Element information</span></span>



|                                     |           |
|-------------------------------------|-----------|
| <span data-ttu-id="2c9f6-134">Минимальная поддерживаемая система</span><span class="sxs-lookup"><span data-stu-id="2c9f6-134">Minimum supported system</span></span><br/> | <span data-ttu-id="2c9f6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c9f6-135">Windows 7</span></span> |
| <span data-ttu-id="2c9f6-136">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="2c9f6-136">Can be empty</span></span>                        | <span data-ttu-id="2c9f6-137">Да</span><span class="sxs-lookup"><span data-stu-id="2c9f6-137">Yes</span></span>       |



## <a name="see-also"></a><span data-ttu-id="2c9f6-138">См. также</span><span class="sxs-lookup"><span data-stu-id="2c9f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c9f6-139">Элемент управления кнопки "Справка"</span><span class="sxs-lookup"><span data-stu-id="2c9f6-139">Help Button control</span></span>](windowsribbon-controls-helpbutton.md)
</dt> </dl>

 

 





