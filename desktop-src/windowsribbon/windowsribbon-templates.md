---
title: Настройка ленты с помощью определений размеров и политик масштабирования
description: элементы управления, размещенные на панели команд ленты, подчиняются правилам макета, которые применяются Windowsной платформой ribbon и основаны на сочетаниях поведения по умолчанию и шаблонов макета (определяемых платформой и настраиваемых), как объявлено в разметке ленты. Эти правила определяют поведение адаптивного макета для платформы Ribbon, влияющее на то, как элементы управления на панели команд адаптируются к различным размерам ленты во время выполнения.
ms.assetid: b5869394-3fa9-4817-add9-54487434fc4f
keywords:
- Windows Лента, Настройка
- Лента, Настройка
- Windows Лента, шаблоны Сизедефинитион
- Лента, шаблоны Сизедефинитион
- Windows Лента, пользовательские шаблоны
- Лента, пользовательские шаблоны
- настройка ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eff1a9d1b2582d5386ce6ea0e02e20cfb5a806e1aaa4a98529474a756b5a8a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933799"
---
# <a name="customizing-a-ribbon-through-size-definitions-and-scaling-policies"></a>Настройка ленты с помощью определений размеров и политик масштабирования

элементы управления, размещенные на панели команд ленты, подчиняются правилам макета, которые применяются Windowsной платформой ribbon и основаны на сочетаниях поведения по умолчанию и шаблонов макета (определяемых платформой и настраиваемых), как объявлено в разметке ленты. Эти правила определяют поведение адаптивного макета для платформы Ribbon, влияющее на то, как элементы управления на панели команд адаптируются к различным размерам ленты во время выполнения.

-   [Введение](#introduction)
    -   [Шаблоны Сизедефинитион ленты](#customizing-a-ribbon-through-size-definitions-and-scaling-policies)
    -   [Пользовательские шаблоны](#custom-templates)
-   [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

Адаптивный макет, как определено платформой Ribbon, — это способность всех элементов управления в пользовательском интерфейсе ленты динамически настраивать организацию, размер, формат и относительный масштаб на основе изменений размера ленты во время выполнения.

Платформа предоставляет функции адаптивного макета через набор элементов разметки, предназначенных для указания и настройки различных поведений макета. Коллекция шаблонов, именуемая [**сизедефинитионс**](windowsribbon-element-sizedefinition.md), определяется платформой, каждая из которых поддерживает различные сценарии управления и макета. Однако платформа также поддерживает пользовательские шаблоны, если предопределенные шаблоны не предоставляют интерфейс пользователя или макеты, необходимые для приложения.

Чтобы элементы управления отображались в предпочтительном макете на определенном уровне ленты, стандартные шаблоны и пользовательские шаблоны работают совместно с элементом [**скалингполици**](windowsribbon-element-scalingpolicy.md) . Этот элемент содержит манифест настроек размера, которые платформа использует в качестве инструкции при отрисовке ленты.

> [!Note]  
> Платформа Ribbon обеспечивает поведение макета по умолчанию на основе набора встроенных эвристических методов для Организации и представления элементов управления во время выполнения без необходимости использования предопределенных шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) . Однако эта возможность предназначена только для создания прототипов.

 

### <a name="ribbon-sizedefinition-templates"></a>Шаблоны Сизедефинитион ленты

Платформа Ribbon предоставляет исчерпывающий набор шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) , которые определяют поведение размера и макета для [группы](windowsribbon-controls-group.md) элементов управления ленты. Эти шаблоны охватывают наиболее распространенные сценарии организации элементов управления в приложении на ленте.

Чтобы обеспечить единообразное взаимодействие с пользователем в приложениях ленты, каждый шаблон [**сизедефинитион**](windowsribbon-element-sizedefinition.md) накладывает ограничения на элементы управления или семейство элементов управления, которые он поддерживает.

Например, семейство элементов управления Button содержит:

-   [Кнопка](windowsribbon-controls-button.md)
-   [Выключатель](windowsribbon-controls-togglebutton.md)
-   [Кнопка раскрывающегося списка](windowsribbon-controls-dropdownbutton.md)
-   [Разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md)
-   [Раскрывающийся список](windowsribbon-controls-dropdowngallery.md)
-   [Коллекция разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)
-   [Выбор цвета для раскрывающегося списка](windowsribbon-controls-dropdowncolorpicker.md)

Хотя входное семейство элементов управления включает:

-   [Поле со списком](windowsribbon-controls-combobox.md)
-   [Spinner](windowsribbon-controls-spinner.md)

[Флажок](windowsribbon-controls-checkbox.md) и [коллекция в ленте](windowsribbon-controls-inribbongallery.md) не принадлежат семейству кнопок или семейству входных данных. Эти два элемента управления можно использовать только в том случае, если явно указано в шаблоне [**сизедефинитион**](windowsribbon-element-sizedefinition.md) .

Ниже приведен список шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) с описанием макета и элементов управления, которые допускаются каждым шаблоном.

> [!IMPORTANT]
> Если элементы управления, объявленные в разметке, не соответствуют типу, упорядочению и количеству, определенным в связанном шаблоне, то [Ошибка проверки](windowsribbon-compilationerrors.md) заносится в журнал [компилятором разметки](windowsribbon-intentcl.md) , а компиляция завершается.

 



онебуттон

Одна кнопка — Управление семейством.<br/> Поддерживается только большой размер группы.<br/>

![Рисунок шаблона онебуттон сизедефинитион.](images/overviews/sizedefinition-onebutton.png)

твобуттонс

Две кнопки — элементы управления семейства.<br/> Поддерживаются только размеры больших и средних групп.<br/>

![Рисунок шаблона твобуттонс Large сизедефинитион.](images/overviews/sizedefinition-twobuttons-large.png)

![Рисунок шаблона твобуттонс Medium сизедефинитион.](images/overviews/sizedefinition-twobuttons-medium.png)

срибуттонс

Три кнопки — элементы управления семейства.<br/> Поддерживаются только размеры больших и средних групп.<br/>

![Рисунок шаблона срибуттонс Large сизедефинитион.](images/overviews/sizedefinition-threebuttons-large.png)

![Рисунок шаблона срибуттонс Medium сизедефинитион.](images/overviews/sizedefinition-threebuttons-medium.png)

ThreeButtons-OneBigAndTwoSmall

Три кнопки — элементы управления семейства.<br/> Первая кнопка представлена на самом деле во всех трех размерах.<br/>

![Рисунок шаблона срибуттонс-онебигандтвосмалл Large сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-large.png)

![Рисунок шаблона срибуттонс-онебигандтвосмалл Medium сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-medium.png)

![Рисунок шаблона срибуттонс-онебигандтвосмалл Small сизедефинитион.](images/overviews/sizedefinition-threebuttons-onebigandtwosmall-small.png)

срибуттонсандонечеккбокс

Три кнопки — элементы управления семейством, сопровождаемые одним элементом управления CheckBox.<br/> Поддерживаются только размеры больших и средних групп.<br/>

![Рисунок шаблона срибуттонсандонечеккбокс Large сизедефинитион.](images/overviews/sizedefinition-threebuttonsandonecheckbox-large.png)

![Рисунок шаблона срибуттонсандонечеккбокс Medium сизедефинитион.](images/overviews/sizedefinition-threebuttonsandonecheckbox-medium.png)

фаурбуттонс

Четыре кнопки — элементы управления семейства.<br/>

![Рисунок шаблона фаурбуттонс Large сизедефинитион.](images/overviews/sizedefinition-fourbuttons-large.png)

![Рисунок шаблона фаурбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fourbuttons-medium.png)

![Рисунок шаблона фаурбуттонс Small сизедефинитион.](images/overviews/sizedefinition-fourbuttons-small.png)

фивебуттонс

Пять элементов управления "Кнопка".<br/>

![Рисунок шаблона фивебуттонс Large сизедефинитион.](images/overviews/sizedefinition-fivebuttons-large.png)

![Рисунок шаблона фивебуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fivebuttons-medium.png)

![Рисунок шаблона фивебуттонс Small сизедефинитион.](images/overviews/sizedefinition-fivebuttons-small.png)

фивеорсиксбуттонс

Пять элементов управления "Кнопка" и необязательная кнопка "шестая".<br/>

![Рисунок шаблона фивеорсиксбуттонс Large сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-large.png)

![Рисунок шаблона фивеорсиксбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-medium.png)

![Рисунок шаблона фивеорсиксбуттонс Small сизедефинитион.](images/overviews/sizedefinition-fiveorsixbuttons-small.png)

сиксбуттонс

Шесть элементов управления "Кнопка".<br/>

![Рисунок шаблона сиксбуттонс Large сизедефинитион.](images/overviews/sizedefinition-sixbuttons-large.png)

![Рисунок шаблона сиксбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-sixbuttons-medium.png)

![Рисунок шаблона сиксбуттонс Small сизедефинитион.](images/overviews/sizedefinition-sixbuttons-small.png)

SixButtons-TwoColumns

Шесть кнопок — элементы управления семейства (альтернативная презентация).<br/>

![Рисунок шаблона сиксбуттонс-твоколумнс Large сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-large.png)

![шаблон сиксбуттонс-твоколумнс Medium сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-medium.png)

![Рисунок шаблона сиксбуттонс-твоколумнс Small сизедефинитион.](images/overviews/sizedefinition-sixbuttons-twocolumns-small.png)

севенбуттонс

Семь элементов управления "Кнопка" — "семейство".<br/>

![Рисунок шаблона севенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-sevenbuttons-large.png)

![Рисунок шаблона севенбуттонс медиумсизедефинитион.](images/overviews/sizedefinition-sevenbuttons-medium.png)

![Рисунок шаблона севенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-sevenbuttons-small.png)

еигхтбуттонс

Восемь элементов управления "Кнопка".<br/>

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Large сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-large.png)

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Medium сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-medium.png)

![Рисунок шаблона еигхтбуттонс-ластсрисмалл Small сизедефинитион.](images/overviews/sizedefinition-eightbuttons-lastthreesmall-small.png)

EightButtons-LastThreeSmall

Восемь кнопок — элементы управления семейства (альтернативная презентация).<br/>

> [!Note]  
> Все элементы управления, объявленные с помощью этого шаблона, должны содержаться в двух элементах [**контролграуп**](windowsribbon-element-controlgroup.md) : один для первых пяти элементов и один для последних трех элементов.

<br/> В следующем примере показана разметка, необходимая для этого шаблона.<br/>

```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="EightButtons-LastThreeSmall">
  <ControlGroup>
    <Button CommandName="cmdSDButton1" />
    <Button CommandName="cmdSDButton2" />
    <Button CommandName="cmdSDButton3" />
    <Button CommandName="cmdSDButton4" />
    <Button CommandName="cmdSDButton5" />
  </ControlGroup>
  <ControlGroup>
    <Button CommandName="cmdSDButton6" />
    <Button CommandName="cmdSDButton7" />
    <Button CommandName="cmdSDButton8" />
  </ControlGroup>
</Group>
```



![Рисунок шаблона еигхтбуттонс Large сизедефинитион.](images/overviews/sizedefinition-eightbuttons-large.png)

![Рисунок шаблона еигхтбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-eightbuttons-medium.png)

![Рисунок шаблона еигхтбуттонс Small сизедефинитион.](images/overviews/sizedefinition-eightbuttons-small.png)

нинебуттонс

Девять элементов управления "Кнопка".

![Рисунок шаблона нинебуттонс Large сизедефинитион.](images/overviews/sizedefinition-ninebuttons-large.png)

![Рисунок шаблона нинебуттонс Medium сизедефинитион.](images/overviews/sizedefinition-ninebuttons-medium.png)

![Рисунок шаблона нинебуттонс Small сизедефинитион.](images/overviews/sizedefinition-ninebuttons-small.png)

тенбуттонс

Десять элементов управления для семейства кнопок.

![Рисунок шаблона тенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-tenbuttons-large.png)

![Рисунок шаблона тенбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-tenbuttons-medium.png)

![Рисунок шаблона тенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-tenbuttons-small.png)

елевенбуттонс

Одиннадцать кнопок — элементы управления семейства.

![Рисунок шаблона елевенбуттонс Large сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-large.png)

![Рисунок шаблона елевенбуттонс Medium сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-medium.png)

![Рисунок шаблона елевенбуттонс Small сизедефинитион.](images/overviews/sizedefinition-elevenbuttons-small.png)

онефонтконтрол

Один [**фонтконтрол**](windowsribbon-element-fontcontrol.md).

Поддерживаются только размеры больших и средних групп.

> [!IMPORTANT]
> Включение [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в определение пользовательского шаблона не поддерживается платформой.

 

![Рисунок шаблона онефонтконтрол Large сизедефинитион.](images/overviews/sizedefinition-onefontcontrol-large.png)

![Рисунок шаблона онефонтконтрол Medium сизедефинитион.](images/overviews/sizedefinition-onefontcontrol-medium.png)

онеинриббонгаллери

Один элемент управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .

Поддерживаются только крупные и небольшие размеры групп.

![Рисунок шаблона онеинриббонгаллери Large сизедефинитион.](images/overviews/sizedefinition-oneinribbongallery-large.png)

![Рисунок шаблона онеинриббонгаллери Small сизедефинитион.](images/overviews/sizedefinition-oneinribbongallery-small.png)

инриббонгаллеряндбигбуттон

Один элемент управления [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) и элемент управления семейства Button.

Поддерживаются только крупные и небольшие размеры групп.

![Рисунок шаблона инриббонгаллеряндбигбуттон Large сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbigbutton-large.png)

![Рисунок шаблона инриббонгаллеряндбигбуттон Small сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbigbutton-small.png)

InRibbonGalleryAndButtons-GalleryScalesFirst

Один элемент управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) и два или три элемента управления семейства кнопок.

Коллекция сворачивается в всплывающее представление в средних и мелких группах.

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Large сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-large.png)

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Medium сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-medium.png)

![Рисунок шаблона инриббонгаллеряндбуттонс-галлерискалесфирст Small сизедефинитион.](images/overviews/sizedefinition-inribbongalleryandbuttons-galleryscalesfirst-small.png)

буттонграупс

Комплексное размещение элементов управления "Кнопка" 32 (большинство из них необязательны).

> [!Note]  
> Помимо необязательной полной кнопки крупного шаблона Буттонграупс, все элементы управления, объявленные с помощью этого шаблона, должны содержаться в элементах [**контролграуп**](windowsribbon-element-controlgroup.md) .

 

В следующем примере показана разметка, необходимая для вывода всех элементов управления 32 (обязательных и необязательных) с помощью этого шаблона.


```
<Group CommandName="cmdSizeDefinitionsGroup"
       SizeDefinition="ButtonGroups">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton16" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton30" />
      <Button CommandName="cmdSDButton31" />
    </ControlGroup>
  </ControlGroup>
  <Button CommandName="cmdSDButton32" />            
</Group>
```



![Рисунок шаблона буттонграупс Large сизедефинитион.](images/overviews/sizedefinition-buttongroups-large.png)

![Рисунок шаблона буттонграупс Medium сизедефинитион.](images/overviews/sizedefinition-buttongroups-medium.png)

![Рисунок шаблона буттонграупс Small сизедефинитион.](images/overviews/sizedefinition-buttongroups-small.png)

буттонграупсандинпутс

Два элемента управления для семейства входных данных (второй — необязательный), за которыми следует комплексное упорядочение 29 элементов управления "Кнопка" (большинство из которых являются необязательными).

Поддерживаются только размеры больших и средних групп.

> [!Note]  
> Все элементы управления, объявленные с помощью этого шаблона, должны содержаться в элементах [**контролграуп**](windowsribbon-element-controlgroup.md) .

 

В следующем примере показана разметка, необходимая для вывода всех элементов управления (обязательных и необязательных) с помощью этого шаблона.


```
<Group CommandName="cmdSizeDefinitionsGroup" 
       SizeDefinition="ButtonGroupsAndInputs">
  <!-- Row 1 -->
  <ControlGroup>
    <ControlGroup>
      <ComboBox CommandName="cmdSDComboBox" />
      <Spinner CommandName="cmdSDSpinner" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton1" />
      <Button CommandName="cmdSDButton2" />
      <Button CommandName="cmdSDButton3" />
      <Button CommandName="cmdSDButton4" />
      <Button CommandName="cmdSDButton5" />
      <Button CommandName="cmdSDButton6" />
      <Button CommandName="cmdSDButton7" />
      <Button CommandName="cmdSDButton8" />
      <Button CommandName="cmdSDButton9" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton10" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton11" />
      <Button CommandName="cmdSDButton12" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton13" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton14" />
    </ControlGroup>
  </ControlGroup>
  <!-- Row 2 -->  
  <ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton15" />
      <Button CommandName="cmdSDButton16" />
      <Button CommandName="cmdSDButton17" />
      <Button CommandName="cmdSDButton18" />
      <Button CommandName="cmdSDButton19" />
      <Button CommandName="cmdSDButton20" />
      <Button CommandName="cmdSDButton21" />
      <Button CommandName="cmdSDButton22" />
      <Button CommandName="cmdSDButton23" />
      <Button CommandName="cmdSDButton24" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton25" />
      <Button CommandName="cmdSDButton26" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton27" />
      <Button CommandName="cmdSDButton28" />
    </ControlGroup>
    <ControlGroup>
      <Button CommandName="cmdSDButton29" />
    </ControlGroup>
  </ControlGroup>
</Group>
```



![Рисунок шаблона буттонграупсандинпутс Large сизедефинитион.](images/overviews/sizedefinition-buttongroupsandinputs-large.png)

![Рисунок шаблона буттонграупсандинпутс Medium сизедефинитион.](images/overviews/sizedefinition-buttongroupsandinputs-medium.png)

бигбуттонсандсмаллбуттонсоринпутс

Две кнопки — элементы управления семействами (необязательные), за которыми следует две или три кнопки или элементы управления для семейства входных данных.

Поддерживаются только размеры больших и средних групп.

![Рисунок шаблона бигбуттонсандсмаллбуттонсоринпутс Large сизедефинитион.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-large.png)

![Рисунок шаблона бигбуттонсандсмаллбуттонсоринпутс Medium сизедефинитион.](images/overviews/sizedefinition-bigbuttonsandsmallbuttonsorinputs-medium.png)



 

### <a name="basic-sizedefinition-example"></a>Пример Basic Сизедефинитион

В следующем примере кода показана базовая Демонстрация объявления шаблона [**сизедефинитион**](windowsribbon-element-sizedefinition.md) в разметке ленты.

*Онеинриббонгаллери* [**сизедефинитион**](windowsribbon-element-sizedefinition.md) используется в этом конкретном примере, но все шаблоны инфраструктуры указаны аналогичным образом.


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



### <a name="complex-sizedefinition-example-with-scaling-policies"></a>Сложный пример Сизедефинитион с политиками масштабирования

Поведением сворачивания шаблонов [**сизедефинитион**](windowsribbon-element-sizedefinition.md) можно управлять с помощью политик масштабирования в разметке ленты.

Элемент [**скалингполици**](windowsribbon-element-scalingpolicy.md) содержит манифест для объявлений [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) и [**Scale**](windowsribbon-element-scale.md) , задающих параметры адаптивного макета для одного или нескольких элементов [**группы**](windowsribbon-element-group.md) при изменении размера ленты.

> [!Note]  
> Настоятельно рекомендуется указывать соответствующие сведения о политике масштабирования таким образом, чтобы большинство, если не все, элементы [**группы**](windowsribbon-element-group.md) были связаны с элементом [**Scale**](windowsribbon-element-scale.md) , где атрибут *size* равен `Popup` . Это позволяет платформе визуализировать ленту с минимально возможным размером и поддерживать самые разнообразные устройства отображения, прежде чем автоматически представить механизм прокрутки.

 

В следующем примере кода показан манифест [**скалингполици**](windowsribbon-element-scalingpolicy.md) , указывающий предпочтение [**скалингполици. идеалсизес**](windowsribbon-element-scalingpolicy-idealsizes.md) [**сизедефинитион**](windowsribbon-element-sizedefinition.md) для каждой из четырех групп элементов управления на вкладке " **Главная** ". Кроме того, элементы [**масштаба**](windowsribbon-element-scale.md) задаются для влияния на режим свертывания в порядке убывания размера каждой группы.


```C++
<Tab CommandName="Home">
  <Tab.ScalingPolicy>
    <ScalingPolicy>
      <ScalingPolicy.IdealSizes>
        <Scale Group="GroupClipboard" Size="Medium"/>
        <Scale Group="GroupView" Size="Large"/>
        <Scale Group="GroupFont" Size="Large"/>
        <Scale Group="GroupParagraph" Size="Large"/>
      </ScalingPolicy.IdealSizes>
      <Scale Group="GroupClipboard" Size="Small"/>
      <Scale Group="GroupClipboard" Size="Popup"/>
      <Scale Group="GroupFont" Size="Medium"/>
      <Scale Group="GroupFont" Size="Popup"/>
      <Scale Group="GroupParagraph" Size="Medium"/>
      <Scale Group="GroupParagraph" Size="Popup"/>
      <!-- 
        GroupView group is associated with the OneButton SizeDefinition.
        Since this template is constrained to one size (Large) there
        is no need to declare further scaling preferences.
      -->
    </ScalingPolicy>
  </Tab.ScalingPolicy>

  <Group CommandName="GroupClipboard" SizeDefinition="FourButtons">
    <Button CommandName="Paste"/>
    <Button CommandName="Cut"/>
    <Button CommandName="Copy"/>
    <Button CommandName="SelectAll"/>
  </Group>

  <Group CommandName="GroupFont"  ApplicationModes="1">
    <FontControl CommandName="Font" FontType="FontWithColor" />
  </Group>

  <Group CommandName="GroupParagraph"  ApplicationModes="1" SizeDefinition="ButtonGroups">
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="Numbered" />
        <ToggleButton CommandName="Bulleted" />
      </ControlGroup>
    </ControlGroup>
    <ControlGroup>
      <ControlGroup>
        <ToggleButton CommandName="LeftJustify" />
        <ToggleButton CommandName="CenterJustify" />
        <ToggleButton CommandName="RightJustify" />
      </ControlGroup>
      <ControlGroup/>
      <ControlGroup>
        <Button CommandName="Outdent" />
        <Button CommandName="Indent" />
      </ControlGroup>
    </ControlGroup>
  </Group>

  <Group CommandName="GroupView" SizeDefinition="OneButton" >
    <ToggleButton CommandName="ViewSource"/>
  </Group>

</Tab>
```



### <a name="custom-templates"></a>Пользовательские шаблоны

Если поведение макета по умолчанию и стандартные шаблоны [**сизедефинитион**](windowsribbon-element-sizedefinition.md) не предлагают гибкости или поддержки для конкретного сценария макета, платформа Ribbon поддерживает пользовательские шаблоны с помощью элемента [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) .

Пользовательские шаблоны можно объявить двумя способами: автономный метод, использующий элемент [**Ribbon. сизедефинитионс**](windowsribbon-element-ribbon-sizedefinitions.md) для объявления многократно используемых именованных шаблонов или встроенный метод, зависящий от [**группы**](windowsribbon-element-group.md).

### <a name="standalone-template"></a>Автономный шаблон

В следующем примере кода показан базовый, многократно используемый настраиваемый шаблон.


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



### <a name="inline-template"></a>Встроенный шаблон

В следующих примерах кода показан базовый встроенный пользовательский шаблон для группы из четырех кнопок.

В этом разделе кода показаны объявления команд для группы кнопок. Здесь также указаны крупные и небольшие ресурсы изображений.


```XML
<!-- Button -->
<Command Name="cmdButtonGroup"
         Symbol="cmdButtonGroup"
         Comment="Button Group"
         LabelTitle="ButtonGroup"/>
<Command Name="cmdButton1"
         Symbol="cmdButton1"
         Comment="Button1"
         LabelTitle="Button1"/>
<Command Name="cmdButton2"
         Symbol="cmdButton2"
         Comment="Button2"
         LabelTitle="Button2"/>
<Command Name="cmdButton3"
         Symbol="cmdButton3"
         Comment="Button3"
         LabelTitle="Button3"/>
<Command Name="cmdButtonGroup2"
         Symbol="cmdButtonGroup2"
         Comment="Button Group2"
         LabelTitle="ButtonGroup2"/>
<Command Name="cmdButtonG21"
         Symbol="cmdButtonG21"
         Comment="ButtonG21"
         LabelTitle="ButtonG21">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG22"
         Symbol="cmdButtonG22"
         Comment="ButtonG22"
         LabelTitle="ButtonG22">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG23"
         Symbol="cmdButtonG23"
         Comment="ButtonG23"
         LabelTitle="ButtonG23">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
<Command Name="cmdButtonG24"
         Symbol="cmdButtonG24"
         Comment="ButtonG24"
         LabelTitle="ButtonG24">
  <Command.LargeImages>
    <Image Source="res/large.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/small.bmp"/>
  </Command.SmallImages>
</Command>
```



В этом разделе кода показано, как определить крупные, средние и малые шаблоны [**граупсизедефинитион**](windowsribbon-element-groupsizedefinition.md) для отображения четырех кнопок в различных размерах и макетах. Объявление [**скалингполици**](windowsribbon-element-scalingpolicy.md) для вкладки определяет, какой шаблон используется для группы элементов управления на основе размера ленты и пространства, необходимого активной вкладке.


```XML
        <Tab CommandName="cmdTab6">
          <Tab.ScalingPolicy>
            <ScalingPolicy>
              <ScalingPolicy.IdealSizes>
                <Scale Group="cmdButtonGroup"
                       Size="Large"/>
                <Scale Group="cmdButtonGroup2"
                       Size="Large"/>
                <Scale Group="cmdToggleButtonGroup"
                       Size="Large"/>
              </ScalingPolicy.IdealSizes>
              <Scale Group="cmdButtonGroup"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Medium"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Small"/>
              <Scale Group="cmdButtonGroup2"
                     Size="Popup"/>
            </ScalingPolicy>
          </Tab.ScalingPolicy>

          <Group CommandName="cmdButtonGroup2">
            <SizeDefinition>
              <ControlNameMap>
                <ControlNameDefinition Name="button1"/>
                <ControlNameDefinition Name="button2"/>
                <ControlNameDefinition Name="button3"/>
                <ControlNameDefinition Name="button4"/>
              </ControlNameMap>
              <GroupSizeDefinition Size="Large">
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Large"
                                         IsLabelVisible="true" />
                </ControlGroup>
                <ColumnBreak ShowSeparator="true"/>
                <ControlGroup>
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Large"
                                        IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                        ImageSize="Large"
                                        IsLabelVisible="true" />
                </ControlGroup>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Medium">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                </Row>
              </GroupSizeDefinition>
              <GroupSizeDefinition Size="Small">
                <Row>
                  <ControlSizeDefinition ControlName="button1"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button3"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
                <Row>
                  <ControlSizeDefinition ControlName="button2"
                                         ImageSize="Small"
                                         IsLabelVisible="true" />
                  <ControlSizeDefinition ControlName="button4"
                                         ImageSize="Small"
                                         IsLabelVisible="false" />
                </Row>
              </GroupSizeDefinition>
            </SizeDefinition>
            <Button CommandName="cmdButtonG21"></Button>
            <Button CommandName="cmdButtonG22"></Button>
            <Button CommandName="cmdButtonG23"></Button>
            <Button CommandName="cmdButtonG24"></Button>
          </Group>
          <Group CommandName="cmdCheckBoxGroup">
            <CheckBox CommandName="cmdCheckBox"></CheckBox>
          </Group>
          <Group CommandName="cmdToggleButtonGroup"
                 SizeDefinition="OneButton">
            <ToggleButton CommandName="cmdToggleButton"></ToggleButton>
          </Group>
          <Group CommandName="cmdButtonGroup"
                 SizeDefinition="ThreeButtons">
            <Button CommandName="cmdButton1"></Button>
            <Button CommandName="cmdButton2"></Button>
            <Button CommandName="cmdButton3"></Button>
          </Group>
        </Tab>
```



На следующих изображениях показано, как шаблоны из предыдущего примера применяются к пользовательскому интерфейсу Ribbon для уменьшения размера ленты.



|  Тип  |      Образ                                                                                         |
|--------|----------------------------------------------------------------------------------------------------|
| большой  | ![Рисунок встроенного большого пользовательского шаблона.](images/overviews/sizedefinition-custom-large.png)   |
| Средний | ![Рисунок встроенного пользовательского шаблона среднего уровня.](images/overviews/sizedefinition-custom-medium.png) |
| Small  | ![Рисунок встроенного небольшого настраиваемого шаблона.](images/overviews/sizedefinition-custom-small.png)   |
| Контекстное меню  | ![Рисунок встроенного всплывающего пользовательского шаблона.](images/overviews/sizedefinition-custom-popup.png)   |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**сизедефинитион**](windowsribbon-element-sizedefinition.md)
</dt> <dt>

[**Масштабирование**](windowsribbon-element-scale.md)
</dt> <dt>

[**Группа**](windowsribbon-element-group.md)
</dt> </dl>

 

 





