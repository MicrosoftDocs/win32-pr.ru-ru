---
title: Свойство Ribbon. табуляции
description: Представляет контейнер для всех основных вкладок на ленте.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Лента окна свойств ленты. табуляции
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489309"
---
# <a name="ribbontabs-property"></a>Свойство Ribbon. табуляции

Представляет контейнер для всех основных вкладок на ленте.

## <a name="usage"></a>Использование

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                             | Описание                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [**TAB**](windowsribbon-element-tab.md)<br/> | Должен быть хотя бы один раз<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                   |
|-----------------------------------------------------------|
| [**Лента**](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a>Комментарии

Обязательный.

Может происходить один или несколько раз для каждой [**ленты**](windowsribbon-element-ribbon.md).

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **Ribbon. Табуляторы** с объявлением **домашней** [**вкладки**](windowsribbon-element-tab.md) .


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>              |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Лента. Контекстуалтабс**](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





