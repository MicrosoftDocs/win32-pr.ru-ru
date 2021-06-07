---
title: Вертикалменулайаут, элемент
description: Представляет вертикальный макет для элементов в коллекции.
ms.assetid: 4124c639-c078-4eb0-9d36-37d1ffcebac0
keywords:
- Лента Windows для элемента Вертикалменулайаут
topic_type:
- apiref
api_name:
- VerticalMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e6f3e4a691c9691b9bc6c8c6d760bb10635d8d8
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444055"
---
# <a name="verticalmenulayout-element"></a>Вертикалменулайаут, элемент

Представляет вертикальный макет для элементов в коллекции.

## <a name="usage"></a>Использование

``` syntax
<VerticalMenuLayout
  Rows = "xs:integer"
  IsMultipleHighlightingEnabled = "xs:boolean"
  Gripper = "xs:string"/>
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
<td><strong>Полосы захвата</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Маркер изменения размера, присоединенный к раскрывающемся списке коллекции. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Вертикаль<br/> </dt> <dd> По умолчанию. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>исмултиплехигхлигхтинженаблед</strong><br/></td>
<td>xs:boolean<br/></td>
<td>Нет<br/></td>
<td><strong>Windows 8 и более поздние версии</strong><br/> Выделяет все элементы в списке вплоть до, включая, текущий элемент с курсором мыши (а не только элемент onmouseover). Обычно используется для нескольких функций <strong>отмены</strong> и <strong>повтора</strong> .<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> По умолчанию. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Строки</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает число строк элемента, видимых без прокрутки. <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Любое положительное или отрицательное целое число. <br/> Значение по умолчанию равно <strong>-1</strong> , что указывает на отображение максимально возможного количества строк элементов.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                                                                 |
|---------------------------------------------------------------------------------------------------------|
| [**Дропдовнгаллери. Менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md)<br/>       |
| [**Инриббонгаллери. Менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)<br/>       |
| [**Сплитбуттонгаллери. Менулайаут**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> |



## <a name="remarks"></a>Remarks

Обязательный.

Элемент **вертикалменулайаут** или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md) должен выполняться один раз для каждого элемента [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md), [**инриббонгаллери. менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)или [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для элемента **вертикалменулайаут** .

В этом разделе кода показаны объявления элементов управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="element-information"></a>Сведения об элементе


- **Минимальная поддерживаемая система**: Windows 7 
- **Может быть пустым**: Да



 

 





