---
title: Свойство Command. Смаллхигхконтрастимажес
description: Представляет контейнер изображений; в данном случае это небольшие изображения для использования с параметрами системы с высокой контрастностью.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- свойство Command. смаллхигхконтрастимажес, Windows лента
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ddee0ccadc966b89d381e02cca5ac1ae336c98671c82a3e4f39f8ebdd6cbeb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329294"
---
# <a name="commandsmallhighcontrastimages-property"></a>Свойство Command. Смаллхигхконтрастимажес

Представляет контейнер изображений; в данном случае это небольшие изображения для использования с параметрами системы с высокой контрастностью.

## <a name="usage"></a>Использование

``` syntax
<Command.SmallHighContrastImages>
  child elements
</Command.SmallHighContrastImages>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                 | Описание                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Изображение**](windowsribbon-element-image.md)<br/> | Может происходить один или несколько раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                     |
|-------------------------------------------------------------|
| [**Команда**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Для каждой [**команды**](windowsribbon-element-command.md)может выполняться не более одного раза.

Ресурсы изображений должны соответствовать стандартному графическому формату точечного рисунка (BMP), используемому в Windows.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента [**SplitButton**](windowsribbon-element-splitbutton.md) с элементом [**менуграуп**](windowsribbon-element-menugroup.md) .

В этом разделе кода показаны объявления команд [**SplitButton**](windowsribbon-element-splitbutton.md) и [**менуграуп**](windowsribbon-element-menugroup.md) с большими и малыми изображениями с высокой контрастностью. Также объявлена связанная [**Группа**](windowsribbon-element-group.md) , которая выступает в качестве родительского контейнера для элемента **SplitButton** .


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Указание ресурсов изображения ленты](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ смаллхигхконтрастимаже](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





