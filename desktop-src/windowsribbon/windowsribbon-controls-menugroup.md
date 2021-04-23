---
title: Группа меню
description: Группа меню организует связанные команды и элементы управления в меню или на панели инструментов.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987777"
---
# <a name="menu-group"></a><span data-ttu-id="0c54f-103">Группа меню</span><span class="sxs-lookup"><span data-stu-id="0c54f-103">Menu Group</span></span>

<span data-ttu-id="0c54f-104">Группа меню организует связанные команды и элементы управления в меню или на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0c54f-104">The Menu Group organizes related Commands and controls within a menu or toolbar.</span></span>

-   [<span data-ttu-id="0c54f-105">Введение</span><span class="sxs-lookup"><span data-stu-id="0c54f-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="0c54f-106">Свойства группы меню</span><span class="sxs-lookup"><span data-stu-id="0c54f-106">Menu Group Properties</span></span>](#menu-group-properties)
-   [<span data-ttu-id="0c54f-107">См. также</span><span class="sxs-lookup"><span data-stu-id="0c54f-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="0c54f-108">Введение</span><span class="sxs-lookup"><span data-stu-id="0c54f-108">Introduction</span></span>

<span data-ttu-id="0c54f-109">Элемент управления группы меню, доступный через элемент разметки [**менуграуп**](windowsribbon-element-menugroup.md) , является логическим контейнером для групп элементов или команд в элементах управления на основе меню, включая [контекстное меню](windowsribbon-controls-contextpopup.md) мини-панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0c54f-109">The Menu Group control, exposed through the [**MenuGroup**](windowsribbon-element-menugroup.md) markup element, is a logical container for groups of items or Commands in menu-based controls, including the [Context Popup](windowsribbon-controls-contextpopup.md) Mini-Toolbar.</span></span>

<span data-ttu-id="0c54f-110">Метку можно указать для группы меню с помощью атрибута *лабелтитле* или свойства [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md) связанного объявления команды.</span><span class="sxs-lookup"><span data-stu-id="0c54f-110">A label can be specified for a Menu Group through the *LabelTitle* attribute or [**Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) property of an associated Command declaration.</span></span> <span data-ttu-id="0c54f-111">Значение, присваиваемое *лабелтитле* , подготавливается к просмотру как заголовок категории.</span><span class="sxs-lookup"><span data-stu-id="0c54f-111">The value assigned to *LabelTitle* is rendered as a category header.</span></span>

<span data-ttu-id="0c54f-112">В следующем примере показана разметка команды для элемента управления ["разворачивающаяся кнопка"](windowsribbon-controls-splitbutton.md) , включающая два объявления команды группы меню.</span><span class="sxs-lookup"><span data-stu-id="0c54f-112">The following example demonstrates the Command markup for a [Split Button](windowsribbon-controls-splitbutton.md) control that includes two Menu Group Command declarations.</span></span>


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



<span data-ttu-id="0c54f-113">В следующем примере показана разметка, необходимая для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с тремя объявлениями элементов [**менуграуп**](windowsribbon-element-menugroup.md) , два из которых связаны с командами группы меню из предыдущего примера.</span><span class="sxs-lookup"><span data-stu-id="0c54f-113">The following example demonstrates the markup required for a [**SplitButton**](windowsribbon-element-splitbutton.md) element with three [**MenuGroup**](windowsribbon-element-menugroup.md) element declarations, two of which are associated with the Menu Group Commands from the previous example.</span></span> <span data-ttu-id="0c54f-114">Атрибут *Class* элемента **менуграуп** используется для указания размера пунктов меню.</span><span class="sxs-lookup"><span data-stu-id="0c54f-114">The *Class* attribute of the **MenuGroup** element is used to specify the size of the menu items.</span></span>


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



<span data-ttu-id="0c54f-115">На следующем снимке экрана показано меню (с тремя элементами управления группы меню), созданное на основе разметки в предыдущих примерах.</span><span class="sxs-lookup"><span data-stu-id="0c54f-115">The following screen shot illustrates the menu (with three Menu Group controls) that is generated from the markup in the previous examples.</span></span>

![снимок экрана меню с тремя элементами управления группы меню.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a><span data-ttu-id="0c54f-117">Свойства группы меню</span><span class="sxs-lookup"><span data-stu-id="0c54f-117">Menu Group Properties</span></span>

<span data-ttu-id="0c54f-118">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления группы меню.</span><span class="sxs-lookup"><span data-stu-id="0c54f-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Menu Group control.</span></span>

<span data-ttu-id="0c54f-119">Как правило, свойство группы меню обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="0c54f-119">Typically, a Menu Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="0c54f-120">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="0c54f-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="0c54f-121">Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="0c54f-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="0c54f-122">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="0c54f-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="0c54f-123">В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="0c54f-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="0c54f-124">В следующей таблице перечислены ключи свойств, связанные с элементом управления группы меню.</span><span class="sxs-lookup"><span data-stu-id="0c54f-124">The following table lists the property keys that are associated with the Menu Group control.</span></span>



| <span data-ttu-id="0c54f-125">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="0c54f-125">Property Key</span></span>                                                                                     | <span data-ttu-id="0c54f-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c54f-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c54f-127">Пользовательский интерфейс \_ PKEY \_ включен</span><span class="sxs-lookup"><span data-stu-id="0c54f-127">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                       | <span data-ttu-id="0c54f-128">Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="0c54f-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="0c54f-129">UI \_ PKEY \_ keytip</span><span class="sxs-lookup"><span data-stu-id="0c54f-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="0c54f-130">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0c54f-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0c54f-131">\_Метка PKEY пользовательского интерфейса \_</span><span class="sxs-lookup"><span data-stu-id="0c54f-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="0c54f-132">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0c54f-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0c54f-133">UI \_ PKEY \_ тултипдескриптион</span><span class="sxs-lookup"><span data-stu-id="0c54f-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="0c54f-134">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0c54f-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="0c54f-135">UI \_ PKEY \_ тултиптитле</span><span class="sxs-lookup"><span data-stu-id="0c54f-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="0c54f-136">Может обновляться только через недействительность.</span><span class="sxs-lookup"><span data-stu-id="0c54f-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="0c54f-137">См. также</span><span class="sxs-lookup"><span data-stu-id="0c54f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c54f-138">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="0c54f-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="0c54f-139">**Менуграуп, элемент разметки**</span><span class="sxs-lookup"><span data-stu-id="0c54f-139">**MenuGroup markup element**</span></span>](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 