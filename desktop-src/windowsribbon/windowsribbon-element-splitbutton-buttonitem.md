---
title: Свойство SplitButton. Буттонитем
description: Представляет контейнер для кнопки или выключателя, который предоставляет команду по умолчанию для разворачивающейся кнопки.
ms.assetid: 3d46d606-238d-46d4-b92e-dfd759951770
keywords:
- свойство SplitButton. буттонитем Windows ленты
topic_type:
- apiref
api_name:
- SplitButton.ButtonItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49f316f7c740b434f761bbe4c00906c8f76b5027af9fcc87317af2a51960dab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840694"
---
# <a name="splitbuttonbuttonitem-property"></a>Свойство SplitButton. Буттонитем

Представляет контейнер для [кнопки](windowsribbon-controls-button.md) [или выключателя](windowsribbon-controls-togglebutton.md) , который предоставляет команду по умолчанию для [разворачивающейся кнопки](windowsribbon-controls-splitbutton.md).

## <a name="usage"></a>Использование

``` syntax
<SplitButton.ButtonItem>
  child elements
</SplitButton.ButtonItem>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Описание                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Кнопка**](windowsribbon-element-button.md)<br/>             | Может выполняться не более одного раза<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/> | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                             |
|---------------------------------------------------------------------|
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждой [**SplitButton**](windowsribbon-element-splitbutton.md).

Каждая **SplitButton. буттонитем** может содержать только один дочерний элемент [**Button**](windowsribbon-element-button.md) или [**ToggleButton**](windowsribbon-element-togglebutton.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [кнопки Split](windowsribbon-controls-splitbutton.md).

В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. Буттонитем** со связанной [**группой**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .


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



В этом разделе кода показаны объявления элементов управления [**SplitButton**](windowsribbon-element-splitbutton.md) и **SplitButton. буттонитем** .


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Элемент управления "разворачивающаяся кнопка"](windowsribbon-controls-splitbutton.md)
</dt> </dl>

 

 





