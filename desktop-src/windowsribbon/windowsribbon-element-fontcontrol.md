---
title: Фонтконтрол, элемент
description: Представляет элемент управления "Шрифт", который является специализированным контейнером для отдельных элементов управления, предназначенных для обработки шрифтов.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Лента Windows для элемента Фонтконтрол
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443405"
---
# <a name="fontcontrol-element"></a>Фонтконтрол, элемент

Представляет [элемент управления "шрифт](windowsribbon-controls-fontcontrol.md)", который является специализированным контейнером для отдельных элементов управления, предназначенных для обработки шрифтов.

## <a name="usage"></a>Использование

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
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
<td><strong>CommandName</strong><br/></td>
<td>xs: Поситивеинтежер или xs: String<br/></td>
<td>Нет<br/></td>
<td>Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)<br/> </dt> <dd> Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно. <br/> Значение должно быть уникальным в XML-документе ленты. <br/> Максимальная длина: 100 символов. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>фонттипе</strong><br/></td>
<td>xs:string<br/></td>
<td>Нет<br/></td>
<td>Ограничено одним из следующих значений: <br/> <br/>
<dt><span></span><span></span><strong></strong> (Фонтонли)<br/> </dt> <dd> По умолчанию. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Установка атрибута <em>фонттипе</em> для <code>FontOnly</code> включения следующих функций:<br/>
<ul>
<li>Поле со списком <strong>семейства шрифтов</strong> .</li>
<li>Поле со списком " <strong>Размер шрифта</strong> ".</li>
<li><p>Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</p>
<blockquote>
[!Note]<br />
Выключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию, но могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Фонтвисколор)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Установка атрибута <em>фонттипе</em> для <code>FontWithColor</code> включения следующих функций:<br/>
<ul>
<li>Поле со списком <strong>семейства шрифтов</strong> .</li>
<li>Поле со списком " <strong>Размер шрифта</strong> ".</li>
<li><strong>Увеличение</strong> и уменьшение <strong>размера шрифта шрифта и кнопок</strong> увеличения и уменьшения.</li>
<li><p>Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</p>
<blockquote>
[!Note]<br />
Выключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию, но могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Палитра цветов <strong>текста</strong> .</li>
<li><p>Палитра цветов <strong>выделения текста</strong> .</p>
<blockquote>
[!Note]<br />
Этот элемент управления скрыт по умолчанию, но его можно отобразить, задав для атрибута <em>ишигхлигхтбуттонвисибле</em> значение <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (Ричфонт)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Установка атрибута <em>фонттипе</em> для <code>RichFont</code> включения следующих функций:<br/>
<ul>
<li>Поле со списком <strong>семейства шрифтов</strong> .</li>
<li>Поле со списком " <strong>Размер шрифта</strong> ".</li>
<li><strong>Увеличение</strong> и уменьшение <strong>размера шрифта шрифта и кнопок</strong> увеличения и уменьшения.</li>
<li><p>Переключатели <strong>полужирный</strong>, <strong>курсив</strong>, <strong>Подчеркнутый</strong>и <strong>Зачеркнутый</strong> .</p>
<blockquote>
[!Note]<br />
Переключатели <strong>зачеркивания</strong> и <strong>подчеркивания</strong> отображаются по умолчанию и не могут быть скрыты путем установки атрибутов <em>исстрикесраугхбуттонвисибле</em> и <em>исундерлинебуттонвисибле</em> в значение <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Палитра цветов <strong>текста</strong> .</li>
<li><p>Палитра цветов <strong>выделения текста</strong> .</p>
<blockquote>
[!Note]<br />
Этот элемент управления отображается по умолчанию и не может быть скрыт путем присвоения атрибуту <em>ишигхлигхтбуттонвисибле</em> значения <code>false</code> .
</blockquote>
<p><br/></p></li>
<li>Выключатели <strong>подстрочных</strong> и <strong>верхних индексов</strong> .</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>исгровшринкбуттонграупвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td><strong>Windows 8 и более поздние версии</strong><br/> Ограничено одним из следующих значений: <br/>
<blockquote>
[!Note]<br />
Кнопки увеличения и сжатия никогда не отображаются в <a href="windowsribbon-element-minitoolbar.md"><strong>минитулбар</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию, если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> По умолчанию, если значение <em>фонттипе</em> равно <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ишигхлигхтбуттонвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы): <br/>
<blockquote>
[!Note]<br />
Выделение цветом доступно только из <strong>фонтконтрол</strong> , если значение атрибута <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию, если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .<br/> Действует, только если значение <em>фонттипе</em> равно <code>FontWithColor</code> или <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> По умолчанию, если значение <em>фонттипе</em> равно <code>FontOnly</code> .<br/> Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>исстрикесраугхбуттонвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы): <br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>исундерлинебуттонвисибле</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы): <br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> Действует, только если значение <em>фонттипе</em> равно <code>FontOnly</code> или <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>максимумфонтсизе</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Максимальный отображаемый размер точки.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Целочисленное значение в диапазоне от 1 до 9999 включительно.<br/> Значение по умолчанию — <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>минимумфонтсизе</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Нет<br/></td>
<td>Минимальный размер точки для вывода.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер)<br/> </dt> <dd> Целочисленное значение в диапазоне от 1 до 9999 включительно.<br/> Значение по умолчанию — <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>шовтруетипеонли</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> Отображаются только шрифты TrueType и OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> По умолчанию. Для типа отображаемых шрифтов ограничение не размещается.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>шоввертикалфонтс</strong><br/></td>
<td>Логическое<br/></td>
<td>Нет<br/></td>
<td>Ограничение на одно из следующих значений (0 и 1 недопустимы):<br/>
<blockquote>
[!Note]<br />
Вертикальным шрифтам предшествует символ @ в списке <strong>семейств шрифтов</strong> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> условия<br/> </dt> <dd> По умолчанию. Отображает вертикальные шрифты, которые <strong>отображаются на панели</strong> управления " <strong>шрифты</strong> ". <br/> </dd> <dt><span></span><span></span><strong></strong> IsFalse<br/> </dt> <dd> Позволяет приложению, не поддерживающему вертикальный текст, скрывать любые вертикальные шрифты, которые отображаются <strong>на панели</strong> управления <strong>шрифтами</strong> .<br/>
<blockquote>
[!Note]<br />
В Windows Vista панель управления « <strong>шрифты</strong> » не предлагает функции <strong>отображения</strong> или <strong>скрытия</strong> . В этом случае атрибут <em>шоввертикалфонтс</em> должен иметь значение <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Дочерние элементы

Нет дочерних элементов.

## <a name="parent-elements"></a>Родительские элементы



| Элемент                                                               |
|-----------------------------------------------------------------------|
| [**контролграуп**](windowsribbon-element-controlgroup.md)<br/> |
| [**Группа**](windowsribbon-element-group.md)<br/>               |
| [**менуграуп**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Remarks

Необязательный элемент.

Может встречаться не более одного раза для каждого элемента [**контролграуп**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md)или [**менуграуп**](windowsribbon-element-menugroup.md) .

Все атрибуты команды **фонтконтрол** , объявленные в разметке, такие как [**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) или [**Command. тултиптитле**](windowsribbon-element-command-tooltiptitle.md), переопределяются атрибутами отдельных элементов управления, составляющих **фонтконтрол**.

Любая попытка выбрать цветовую палитру из палитры [элементов управления шрифта](windowsribbon-controls-fontcontrol.md) может привести к нарушению прав доступа, если с элементом управления не связан ни один обработчик команд.

## <a name="examples"></a>Примеры

В следующем примере показана базовая разметка для трех типов [элементов управления шрифта](windowsribbon-controls-fontcontrol.md).

В этом разделе кода показаны объявления команд **фонтконтрол** , каждая из которых содержит объявление контейнера [**группы**](windowsribbon-element-group.md) .


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



В этом разделе кода показаны объявления элементов управления **фонтконтрол** , где каждая **фонтконтрол** и [**Группа**](windowsribbon-element-group.md) объявляются на одной вкладке.


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>Сведения об элементе

* **Минимальная поддерживаемая система**: Windows 7
* **Может быть пустым**: Да



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элемент управления "Шрифт"](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Пример Фонтконтрол](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





