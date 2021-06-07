---
title: Фловменулайаут, элемент
description: Представляет горизонтальный макет с разрывами строк для элементов в коллекции.
ms.assetid: 40c3a2e1-e58a-4d34-a237-b1bea116c82e
keywords:
- Лента Windows для элемента Фловменулайаут
topic_type:
- apiref
api_name:
- FlowMenuLayout
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31a040fb51ad46feb30147fea97c19210cc16094
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111442885"
---
# <a name="flowmenulayout-element"></a>Фловменулайаут, элемент

Представляет горизонтальный макет с разрывами строк для элементов в коллекции.

## <a name="usage"></a>Использование

``` syntax
<FlowMenuLayout
  Rows = "xs:integer"
  Columns = "xs:integer"
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
<td><strong>Столбцы</strong><br/></td>
<td>xs:integer<br/></td>
<td>Нет<br/></td>
<td>Указывает количество элементов, отображаемых в одной строке.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: integer)<br/> </dt> <dd> Любое положительное или отрицательное целое число. <br/> Значение по умолчанию — <strong>2</strong>. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Полосы захвата</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Маркер изменения размера, присоединенный к раскрывающемся списке коллекции. <br/> <img src="images/controls/gripper.png" alt="Screen shot of a vertical gripper." /><br/> Ограничено одним из следующих значений:<br/> <br/>
<dt><span></span><span></span><strong></strong> None<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Вертикаль<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Нижне<br/> </dt> <dd> По умолчанию. <br/> </dd> </dl></td>
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

Элемент [**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или **фловменулайаут** должен выполняться один раз для каждого элемента [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md), [**инриббонгаллери. менулайаут**](windowsribbon-element-inribbongallery-menulayout.md)или [**SplitButtonGallery. MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md) .

Элементы упорядочиваются в соответствии со свойствами разрыва строки, присущими атрибутам *Row* и *Column* . Если содержимое превышает длину одной строки, меню разбивает строки, заключает строки и соответствующим образом выровнять содержимое.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md).

В этом разделе кода показано объявление элемента управления [**дропдовнгаллери. менулайаут**](windowsribbon-element-dropdowngallery-menulayout.md) со спецификацией **фловменулайаут** .


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="element-information"></a>Сведения об элементе

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да


 

 





