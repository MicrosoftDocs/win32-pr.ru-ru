---
title: Элемент Ribbon
description: Представляет элемент управления ленты в представлении ленты.
ms.assetid: 51083180-4e86-4c90-9fd1-a58c12bcc756
keywords:
- элемент ленты Windows лента
topic_type:
- apiref
api_name:
- Ribbon
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5dd422013bdaf81d5d6aac6d0a34f4c9479af26cd79f64b854299caa3cac3f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118202205"
---
# <a name="ribbon-element"></a>Элемент Ribbon

Представляет элемент управления ленты в представлении ленты.

## <a name="usage"></a>Использование

``` syntax
<Ribbon
  Name = "xs:string"
  GroupSpacing = "xs:string">
  child elements
</Ribbon>
```

## <a name="attributes"></a>Атрибуты



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>Тип</th>
<th>Обязательно</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>граупспаЦинг</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td><dt><span></span><span></span><strong></strong> Значительные<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> Высокое<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Достаточ<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Имя</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Используется для добавления аннотации в элемент Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Любая последовательность из нуля или более символов.<br/> Максимальная длина не ограничена.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы



| Элемент                                                                                         | Описание                                   |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Лента. Аппликатионмену**](windowsribbon-element-ribbon-applicationmenu.md)<br/>       | Может выполняться не более одного раза<br/> <br/> |
| [**Лента. Контекстуалтабс**](windowsribbon-element-ribbon-contextualtabs.md)<br/>         | Может выполняться не более одного раза<br/> <br/> |
| [**Лента. Хелпбуттон**](windowsribbon-element-ribbon-helpbutton.md)<br/>                 | Может выполняться не более одного раза<br/> <br/> |
| [**Лента. Куиккакцесстулбар**](windowsribbon-element-ribbon-quickaccesstoolbar.md)<br/> | Может выполняться не более одного раза<br/> <br/> |
| [**Лента. Сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md)<br/>       | Может выполняться не более одного раза<br/> <br/> |
| [**Лента. вкладки**](windowsribbon-element-ribbon-tabs.md)<br/>                             | Может выполняться не более одного раза<br/> <br/> |



## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                         |
|---------------------------------------------------------------------------------|
| [**Application. views**](windowsribbon-element-application-views.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Должен выполняться только один раз для каждого элемента [**Application. views**](windowsribbon-element-application-views.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для представления **ленты** .


```XML
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
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="element-information"></a>Сведения об элементе




* **минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: нет



 

 





