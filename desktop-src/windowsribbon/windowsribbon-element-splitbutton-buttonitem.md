---
title: Свойство SplitButton. Буттонитем
description: Представляет контейнер для кнопки или выключателя, который предоставляет команду по умолчанию для разворачивающейся кнопки.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- Лента Windows свойства SplitButton. Буттонитем
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bf1e1cb908ce9a86f23f75d17bf2e76797997db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489657"
---
# <a name="splitbuttonbuttonitem-property"></a><span data-ttu-id="6f1dc-104">Свойство SplitButton. Буттонитем</span><span class="sxs-lookup"><span data-stu-id="6f1dc-104">SplitButton.ButtonItem property</span></span>

<span data-ttu-id="6f1dc-105">Представляет контейнер для [кнопки](windowsribbon-controls-button.md) [или выключателя](windowsribbon-controls-togglebutton.md) , который предоставляет команду по умолчанию для [разворачивающейся кнопки](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="6f1dc-105">Represents a container for a [Button](windowsribbon-controls-button.md) or [Toggle Button](windowsribbon-controls-togglebutton.md) that exposes the default Command of a [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="6f1dc-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6f1dc-106">Usage</span></span>

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a><span data-ttu-id="6f1dc-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6f1dc-107">Attributes</span></span>

<span data-ttu-id="6f1dc-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="6f1dc-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6f1dc-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6f1dc-109">Child elements</span></span>



| <span data-ttu-id="6f1dc-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="6f1dc-110">Element</span></span>                                                               | <span data-ttu-id="6f1dc-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6f1dc-111">Description</span></span>                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="6f1dc-112">**Кнопка**</span><span class="sxs-lookup"><span data-stu-id="6f1dc-112">**Button**</span></span>](windowsribbon-element-button.md)<br/>             | <span data-ttu-id="6f1dc-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="6f1dc-113">May occur at most once</span></span><br/> <br/> |
| [<span data-ttu-id="6f1dc-114">**ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="6f1dc-114">**ToggleButton**</span></span>](windowsribbon-element-togglebutton.md)<br/> | <span data-ttu-id="6f1dc-115">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="6f1dc-115">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6f1dc-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6f1dc-116">Parent elements</span></span>



| <span data-ttu-id="6f1dc-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="6f1dc-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="6f1dc-118">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="6f1dc-118">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6f1dc-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6f1dc-119">Remarks</span></span>

<span data-ttu-id="6f1dc-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6f1dc-120">Optional.</span></span>

<span data-ttu-id="6f1dc-121">Может встречаться не более одного раза для каждой [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="6f1dc-121">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

<span data-ttu-id="6f1dc-122">Каждая **SplitButton. буттонитем** может содержать только один дочерний элемент [**Button**](windowsribbon-element-button.md) или [**ToggleButton**](windowsribbon-element-togglebutton.md) .</span><span class="sxs-lookup"><span data-stu-id="6f1dc-122">Each **SplitButton.ButtonItem** can contain only one [**Button**](windowsribbon-element-button.md) or [**ToggleButton**](windowsribbon-element-togglebutton.md) child element.</span></span>

## <a name="examples"></a><span data-ttu-id="6f1dc-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="6f1dc-123">Examples</span></span>

<span data-ttu-id="6f1dc-124">В следующем примере показана базовая разметка для [кнопки Split](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="6f1dc-124">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="6f1dc-125">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. Буттонитем** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="6f1dc-125">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



<span data-ttu-id="6f1dc-126">В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. буттонитем** .</span><span class="sxs-lookup"><span data-stu-id="6f1dc-126">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.ButtonItem** control declarations.</span></span>


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="6f1dc-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6f1dc-127">Requirements</span></span>



| <span data-ttu-id="6f1dc-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6f1dc-128">Requirement</span></span> | <span data-ttu-id="6f1dc-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6f1dc-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6f1dc-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6f1dc-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1dc-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6f1dc-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6f1dc-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6f1dc-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1dc-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6f1dc-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6f1dc-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6f1dc-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1dc-135">Элемент управления "разворачивающаяся кнопка"</span><span class="sxs-lookup"><span data-stu-id="6f1dc-135">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





