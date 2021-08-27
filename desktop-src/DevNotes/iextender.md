---
description: Интерфейс Иекстендер предоставляет набор основных свойств, которые добавляются в интерфейс элемента управления. Программисты могут использовать эти свойства, как если бы они были частью элемента управления.
ms.assetid: 901873bd-af6a-415e-865f-21769367c99f
title: Интерфейс Иекстендер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IExtender
- IExtender.Align
- IExtender.get_Align
- IExtender.put_Align
- IExtender.Enabled
- IExtender.get_Enabled
- IExtender.put_Enabled
- IExtender.Height
- IExtender.get_Height
- IExtender.put_Height
- IExtender.Left
- IExtender.get_Left
- IExtender.put_Left
- IExtender.TabStop
- IExtender.get_TabStop
- IExtender.put_TabStop
- IExtender.Top
- IExtender.get_Top
- IExtender.put_Top
- IExtender.Visible
- IExtender.get_Visible
- IExtender.put_Visible
- IExtender.Width
- IExtender.get_Width
- IExtender.put_Width
- IExtender.Name
- IExtender.get_Name
- IExtender.Parent
- IExtender.get_Parent
- IExtender.Hwnd
- IExtender.get_Hwnd
- IExtender.Container
- IExtender.get_Container
api_type:
- COM
api_location:
- Ole2disp.dll
- Oleaut32.dll
ms.openlocfilehash: a341f5d8a0ec554f008232f44156486df83d0fd8
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625119"
---
# <a name="iextender-interface"></a>Интерфейс Иекстендер

Интерфейс **иекстендер** предоставляет набор основных свойств, которые добавляются в интерфейс элемента управления. Программисты могут использовать эти свойства, как если бы они были частью элемента управления.

## <a name="members"></a>Участники

Интерфейс **иекстендер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иекстендер** также имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Интерфейс **иекстендер** содержит следующие методы.



| Метод                         | Описание                                    |
|:-------------------------------|:-----------------------------------------------|
| [**Переместить**](iextender-move.md) | Перемещает Мдиформ, форму или элемент управления.<br/> |



 

### <a name="properties"></a>Свойства

Интерфейс **иекстендер** имеет следующие свойства.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Свойство</th>
<th >Тип доступа</th>
<th >Описание:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td >Выровнять<br/></td>
<td >Чтение/запись<br/></td>
<td >Возвращает или задает значение, определяющее, отображается ли объект в любом месте формы или в верхней, нижней, левой или правой части формы и автоматически изменяется в соответствии с шириной формы.<br/> 
<table>
<thead>
<tr class="header">
<th>Константа</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Вбалигнноне 0</td>
<td>(По умолчанию в форме, отличной от MDI) Нет — размер и расположение можно задать во время разработки или в коде. Параметр игнорируется, если объект находится в форме MDI.</td>
</tr>
<tr class="even">
<td>Вбалигнтоп 1</td>
<td>(По умолчанию в форме MDI) Top — объект находится в верхней части формы, а его ширина равна значению свойства Скалевидс формы.</td>
</tr>
<tr class="odd">
<td>Вбалигнботтом 2</td>
<td>Bottom — объект находится в нижней части формы, а его ширина равна значению свойства Скалевидс в форме.</td>
</tr>
<tr class="even">
<td>Вбалигнлефт 3</td>
<td>Left — объект находится слева от формы, а его ширина равна значению свойства Скалевидс формы.</td>
</tr>
<tr class="odd">
<td>Вбалигнригхт 4</td>
<td>Справа — объект находится справа от формы, а его ширина равна значению свойства Скалевидс в форме.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><p>Контейнер</p></td>
<td ><p>Только для чтения</p></td>
<td ><p>Возвращает контейнер элемента управления в форме.</p></td>
</tr>
<tr class="odd">
<td ><p>Включено</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает значение, определяющее, может ли форма или элемент управления отвечать на создаваемые пользователем события.</p></td>
</tr>
<tr class="even">
<td ><p>Высота:</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает высоту объекта.</p></td>
</tr>
<tr class="odd">
<td ><p>HWND</p></td>
<td ><p>Только для чтения</p></td>
<td ><p>Возвращает маркер для формы или элемента управления.</p></td>
</tr>
<tr class="even">
<td ><p>Левый</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает расстояние между внутренним левым ребром объекта и левым ребром его контейнера.</p></td>
</tr>
<tr class="odd">
<td ><p>Имя</p></td>
<td ><p>Только для чтения</p></td>
<td ><p>Возвращает имя, используемое в коде для задания объекта формы, элемента управления или доступа к данным.</p></td>
</tr>
<tr class="even">
<td ><p>Parent</p></td>
<td ><p>Только для чтения</p></td>
<td ><p>Возвращает форму, объект или коллекцию, содержащую элемент управления или другой объект или коллекцию.</p></td>
</tr>
<tr class="odd">
<td ><p>TabStop</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает значение, указывающее, может ли пользователь использовать клавишу <strong>Tab</strong> для передачи фокуса объекту.</p></td>
</tr>
<tr class="even">
<td ><p>Начало</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает расстояние между внутренним верхним краями объекта и верхней границей его контейнера.</p></td>
</tr>
<tr class="odd">
<td ><p>Видимый</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает значение, указывающее, является ли объект видимым или скрытым.</p></td>
</tr>
<tr class="even">
<td ><p>Ширина</p></td>
<td ><p>Чтение/запись</p></td>
<td ><p>Возвращает или задает ширину объекта.</p></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ole2disp.dll; </dt> <dt>Oleaut32.dll</dt> </dl> |



 

 
