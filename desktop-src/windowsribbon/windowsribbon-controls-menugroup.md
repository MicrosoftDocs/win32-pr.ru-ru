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
# <a name="menu-group"></a>Группа меню

Группа меню организует связанные команды и элементы управления в меню или на панели инструментов.

-   [Введение](#introduction)
-   [Свойства группы меню](#menu-group-properties)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Элемент управления группы меню, доступный через элемент разметки [**менуграуп**](windowsribbon-element-menugroup.md) , является логическим контейнером для групп элементов или команд в элементах управления на основе меню, включая [контекстное меню](windowsribbon-controls-contextpopup.md) мини-панели инструментов.

Метку можно указать для группы меню с помощью атрибута *лабелтитле* или свойства [**Command. Лабелтитле**](windowsribbon-element-command-labeltitle.md) связанного объявления команды. Значение, присваиваемое *лабелтитле* , подготавливается к просмотру как заголовок категории.

В следующем примере показана разметка команды для элемента управления ["разворачивающаяся кнопка"](windowsribbon-controls-splitbutton.md) , включающая два объявления команды группы меню.


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



В следующем примере показана разметка, необходимая для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с тремя объявлениями элементов [**менуграуп**](windowsribbon-element-menugroup.md) , два из которых связаны с командами группы меню из предыдущего примера. Атрибут *Class* элемента **менуграуп** используется для указания размера пунктов меню.


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



На следующем снимке экрана показано меню (с тремя элементами управления группы меню), созданное на основе разметки в предыдущих примерах.

![снимок экрана меню с тремя элементами управления группы меню.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Свойства группы меню

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления группы меню.

Как правило, свойство группы меню обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления группы меню.



| Ключ свойства                                                                                     | Примечания                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Пользовательский интерфейс \_ PKEY \_ включен](windowsribbon-reference-properties-uipkey-enabled.md)                       | Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [UI \_ PKEY \_ keytip](windowsribbon-reference-properties-uipkey-keytip.md)                         | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [\_Метка PKEY пользовательского интерфейса \_](windowsribbon-reference-properties-uipkey-label.md)                           | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ тултипдескриптион](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Может обновляться только через недействительность.                                                                                                                                                                                     |
| [UI \_ PKEY \_ тултиптитле](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Может обновляться только через недействительность.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Менуграуп, элемент разметки**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 