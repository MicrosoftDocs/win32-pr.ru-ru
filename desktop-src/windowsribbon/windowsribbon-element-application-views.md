---
title: Свойство Application. views
description: Представляет контейнер для каждого представления платформы ленты, в частности Ribbon и Контекстпопуп.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- свойство Application. views Windows лента
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe063397698a74da0421cf0c9c3b2ef46861f1477e0f4ac99fe5d6e6063c7251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964313"
---
# <a name="applicationviews-property"></a>Свойство Application. views

Представляет контейнер для каждого представления платформы ленты, в частности [**Ribbon**](windowsribbon-element-ribbon.md) и [**контекстпопуп**](windowsribbon-element-contextpopup.md).

## <a name="usage"></a>Использование

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a>Атрибуты

Атрибуты отсутствуют.

## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                               | Описание                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [**контекстпопуп**](windowsribbon-element-contextpopup.md)<br/> | Может происходить один или несколько раз<br/> <br/> |
| [**Лента**](windowsribbon-element-ribbon.md)<br/>             | Должно выполняться только один раз<br/> <br/>     |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                             |
|---------------------------------------------------------------------|
| [**Развертывание**](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен выполняться ровно один раз для каждого элемента [**приложения**](windowsribbon-element-application.md) .

## <a name="examples"></a>Примеры

В следующем примере показан элемент **Application. views** , содержащий манифест элементов управления ленты, каждый со ссылкой на команду, объявленную в элементе [**Application. Commands**](windowsribbon-element-application-commands.md) .


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>              |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Application. Commands**](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





