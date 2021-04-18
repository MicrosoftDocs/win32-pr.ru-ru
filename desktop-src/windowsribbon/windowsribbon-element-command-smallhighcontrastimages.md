---
title: Свойство Command. Смаллхигхконтрастимажес
description: Представляет контейнер изображений; в данном случае это небольшие изображения для использования с параметрами системы с высокой контрастностью.
ms.assetid: d1c441eb-885a-4dc1-b98d-5a36cab2f837
keywords:
- Лента Windows для свойства Command. Смаллхигхконтрастимажес
topic_type:
- apiref
api_name:
- Command.SmallHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56291ad4e56e5f941fe4cb2790ac6afab27ad67b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672809"
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
| [**Get-Help**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Комментарии

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



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Указание ресурсов изображения ленты](windowsribbon-imageformats.md)
</dt> <dt>

[UI \_ PKEY \_ смаллхигхконтрастимаже](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md)
</dt> </dl>

 

 





