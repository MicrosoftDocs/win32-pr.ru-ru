---
title: Свойство SplitButton. Менуграупс
description: Представляет контейнер для набора пунктов раскрывающегося меню в стандартном элементе управления "разворачивающаяся кнопка".
ms.assetid: 6328ad49-037b-4cd5-90f6-b91646e260ee
keywords:
- Лента Windows свойства SplitButton. Менуграупс
topic_type:
- apiref
api_name:
- SplitButton.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b8af4639040d6b6302b4d2b5761d750074389a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802248"
---
# <a name="splitbuttonmenugroups-property"></a><span data-ttu-id="66f9b-104">Свойство SplitButton. Менуграупс</span><span class="sxs-lookup"><span data-stu-id="66f9b-104">SplitButton.MenuGroups property</span></span>

<span data-ttu-id="66f9b-105">Представляет контейнер для набора пунктов раскрывающегося меню в стандартном элементе управления ["разворачивающаяся кнопка"](windowsribbon-controls-splitbutton.md) .</span><span class="sxs-lookup"><span data-stu-id="66f9b-105">Represents a container for a set of drop-down menu items in a standard [Split Button](windowsribbon-controls-splitbutton.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="66f9b-106">Использование</span><span class="sxs-lookup"><span data-stu-id="66f9b-106">Usage</span></span>

``` syntax
<SplitButton.MenuGroups>
  child elements
</SplitButton.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="66f9b-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="66f9b-107">Attributes</span></span>

<span data-ttu-id="66f9b-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="66f9b-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="66f9b-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="66f9b-109">Child elements</span></span>



| <span data-ttu-id="66f9b-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="66f9b-110">Element</span></span>                                                         | <span data-ttu-id="66f9b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="66f9b-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="66f9b-112">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="66f9b-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="66f9b-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="66f9b-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="66f9b-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="66f9b-114">Parent elements</span></span>



| <span data-ttu-id="66f9b-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="66f9b-115">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="66f9b-116">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="66f9b-116">**SplitButton**</span></span>](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="66f9b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66f9b-117">Remarks</span></span>

<span data-ttu-id="66f9b-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="66f9b-118">Optional.</span></span>

<span data-ttu-id="66f9b-119">Может встречаться не более одного раза для каждой [**SplitButton**](windowsribbon-element-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="66f9b-119">May occur at most once for each [**SplitButton**](windowsribbon-element-splitbutton.md).</span></span>

## <a name="examples"></a><span data-ttu-id="66f9b-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="66f9b-120">Examples</span></span>

<span data-ttu-id="66f9b-121">В следующем примере показана базовая разметка для [кнопки Split](windowsribbon-controls-splitbutton.md).</span><span class="sxs-lookup"><span data-stu-id="66f9b-121">The following example demonstrates the basic markup for the [Split Button](windowsribbon-controls-splitbutton.md).</span></span>

<span data-ttu-id="66f9b-122">В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. Менуграупс** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="66f9b-122">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** Command declarations, with an associated [**Group**](windowsribbon-element-group.md) that functions as the parent container for the **SplitButton** element.</span></span>


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



<span data-ttu-id="66f9b-123">В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. менуграупс** .</span><span class="sxs-lookup"><span data-stu-id="66f9b-123">This section of code shows the [**SplitButton**](windowsribbon-element-splitbutton.md) and **SplitButton.MenuGroups** control declarations.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="66f9b-124">Требования</span><span class="sxs-lookup"><span data-stu-id="66f9b-124">Requirements</span></span>



| <span data-ttu-id="66f9b-125">Требование</span><span class="sxs-lookup"><span data-stu-id="66f9b-125">Requirement</span></span> | <span data-ttu-id="66f9b-126">Значение</span><span class="sxs-lookup"><span data-stu-id="66f9b-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="66f9b-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66f9b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="66f9b-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66f9b-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="66f9b-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66f9b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="66f9b-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66f9b-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="66f9b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66f9b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f9b-132">Элемент управления "разворачивающаяся кнопка"</span><span class="sxs-lookup"><span data-stu-id="66f9b-132">Split Button control</span></span>](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





