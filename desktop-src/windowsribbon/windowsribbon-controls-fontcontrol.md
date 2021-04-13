---
title: Элемент управления шрифтами
description: Для упрощения интеграции и настройки поддержки шрифтов в приложениях, требующих обработки текста и возможности редактирования текстов, платформа Windows Ribbon предоставляет специализированный элемент управления шрифтом, предоставляющий широкий спектр свойств шрифта, таких как имя гарнитуры, стиль, размер точки и эффекты.
ms.assetid: 6052f2e3-2c9e-432e-9ed6-c1e3a50843d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e179296ae03163bf03e08d2fbf7287264792e6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413220"
---
# <a name="font-control"></a>Элемент управления шрифтами

Для упрощения интеграции и настройки поддержки шрифтов в приложениях, требующих обработки текста и возможности редактирования текстов, платформа Windows Ribbon предоставляет специализированный элемент управления шрифтом, предоставляющий широкий спектр свойств шрифта, таких как имя гарнитуры, стиль, размер точки и эффекты.

-   [Введение](#introduction)
-   [Единообразный интерфейс](#a-consistent-experience)
-   [Простота интеграции и настройки](#easy-integration-and-configuration)
-   [Выравнивание с помощью общих текстовых структур GDI](#alignment-with-common-gdi-text-structures)
-   [Добавление Фонтконтрол](#add-a-fontcontrol)
    -   [Объявление Фонтконтрол в разметке](#declaring-a-fontcontrol-in-markup)
    -   [Свойства элемента управления "Шрифт"](#font-control-properties)
-   [Определение обработчика команд Фонтконтрол](#define-a-fontcontrol-command-handler)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Элемент управления "Шрифт" — это составной элемент управления, состоящий из кнопок, выключателей, раскрывающихся списков и полей со списком, которые используются для указания конкретного свойства шрифта или параметра форматирования.

На следующем снимке экрана показан элемент управления шрифтом ленты в WordPad для Windows 7.

![снимок экрана элемента фонтконтрол с атрибутом ричфонт, для которого установлено значение true.](images/controls/fontcontrol.png)

## <a name="a-consistent-experience"></a>Единообразный интерфейс

Как встроенный элемент управления "лента", элемент управления "Шрифт" улучшает общие функции управления шрифтами, выбора и форматирования, а также обеспечивает широкие возможности согласованного взаимодействия с пользователем во всех приложениях ленты.

Этот единый интерфейс включает

-   Стандартизированное форматирование и выбор шрифтов для различных приложений ленты.
-   Стандартизованное представление шрифтов для приложений ленты.
-   Автоматический, в Windows 7 Активация шрифта, основанная на параметре **Показать** или **Скрыть** для каждого шрифта на панели управления **шрифты** . Элемент управления "Шрифт" отображает только те шрифты, которые установлены для **отображения**.
    > [!Note]  
    > В Windows Vista панель элементов управления " **шрифты** " не предлагает функции " **Показать** или **Скрыть** ", поэтому активируются все шрифты.

     

-   Управление шрифтами, доступ к которому осуществляется непосредственно из элемента управления.

    На следующем снимке экрана показано, что доступ к панели элементов управления " **шрифты** " можно получить непосредственно из элемента управления "Шрифт".

    ![снимок экрана со списком семейств шрифтов в WordPad для Windows 7.](images/controls/fontcontrol-fontcpl.png)

-   Поддержка автоматического предварительного просмотра.
-   Раскрытие шрифтов, которые наиболее важны для пользователя, например
    -   Локализованные списки шрифтов для международных пользователей.
    -   Списки шрифтов на основе устройства ввода.

    > [!Note]  
    > Поддержка этой функции доступна не на всех платформах, предшествующих Windows 7.

     

## <a name="easy-integration-and-configuration"></a>Простота интеграции и настройки

Предоставляя стандартные, многократно используемые и легко используемые функции, элемент управления "шрифт ленты" упрощает интеграцию поддержки шрифтов в приложение.

Сведения о выделении и форматировании шрифта упаковываются в один самодостаточный логический элемент, который

-   Устраняет сложное управление взаимозависимостями элементов управления, характерной для реализаций элементов управления шрифтами.
-   Требуется один обработчик команд для всех функций, предоставляемых подэлементами управления шрифтами.

Этот обработчик единственных команд позволяет элементу управления "Шрифт" управлять функциональностью различных подэлементов управления внутренним образом. вложенный элемент управления никогда не взаимодействует напрямую с приложением, независимо от его функции.

К другим функциям элемента управления "Шрифт" относятся

-   Автоматическое, поддерживающее DPI создание WYSIWYG (то есть что вы получаете) растровое представление для каждого шрифта в меню **семейства шрифтов** .
-   Интеграция [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) .
-   Рисунки и подсказки для локализованных семейств шрифтов.
-   Перечисление шрифтов, группирование и метаданные для управления и представления шрифтов.
    > [!Note]  
    > Поддержка этой функции доступна не на всех платформах, предшествующих Windows 7.

     

-   Раскрывающиеся цвета раскрывающегося списка Цвет **текста** и **выделения текста** , которые отражают поведение [средства выбора цвета](windowsribbon-controls-dropdowncolorpicker.md) раскрывающегося списка ленты.
-   Поддержка автоматического предварительного просмотра всеми подэлементами управления на основе коллекции шрифтов: **семейство шрифтов**, **Размер шрифта**, **Цвет текста** и **Цвет выделения текста**.

## <a name="alignment-with-common-gdi-text-structures"></a>Выравнивание с помощью общих текстовых структур GDI

Компоненты стека текста [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) используются для предоставления функций выбора шрифта и форматирования с помощью элемента управления шрифта ленты. Различные функции шрифтов, поддерживаемые [структурой LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [структурой CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)и [структурой CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) , предоставляются через вложенные элементы управления, которые включены в элемент управления Font.

Подэлементы управления, отображаемые в элементе управления Font, зависят от шаблона *фонттипе* , объявленного в разметке ленты. Шаблоны *фонттипе* (подробно рассматриваются в следующем разделе) предназначены для согласования с общими текстовыми структурами [Windows интерфейс графических устройств (GDI)](../gdi/windows-gdi.md) .

## <a name="add-a-fontcontrol"></a>Добавление Фонтконтрол

В этом разделе описаны основные шаги по добавлению элемента управления шрифтом в приложение для ленты.

### <a name="declaring-a-fontcontrol-in-markup"></a>Объявление Фонтконтрол в разметке

Как и другие элементы управления Ribbon, элемент управления "Шрифт" объявляется в разметке с помощью элемента [**фонтконтрол**](windowsribbon-element-fontcontrol.md) и связывается с объявлением команды с помощью идентификатора команды. При компиляции приложения идентификатор команды используется для привязки команды к обработчику команд в ведущем приложении.

> [!Note]  
> Если идентификатор команды не объявлен с [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в разметке, то он создается платформой.

 

Поскольку подэлементы управления шрифтами не предоставляются напрямую, Настройка элемента управления шрифта ограничена тремя шаблонами макета *фонттипе* , определенными платформой.

Дальнейшая настройка элемента управления шрифтом может быть выполнена путем объединения шаблона макета с атрибутами [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , такими как *ишигхлигхтбуттонвисибле*, *исстрикесраугхбуттонвисибле* и *исундерлинебуттонвисибле*.

> [!Note]  
> Функции шрифта, не предоставляемые стандартными шаблонами и атрибутами элементов управления шрифтом, требуют реализации пользовательского элемента управления шрифтом, который выходит за рамки этой статьи.

 

В следующей таблице перечислены шаблоны элементов управления шрифтом и тип элемента управления Edit, с которым будет согласовываться каждый шаблон.



| Шаблон      | Поддерживает                                                                 |
|---------------|--------------------------------------------------------------------------|
| фонтонли      | [Структура LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta)     |
| фонтвисколор | [Структура CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)  |
| ричфонт      | [Структура CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a) |



 

В следующей таблице перечислены элементы управления, связанные с каждым шаблоном, и указаны элементы управления, которые являются необязательными для связанного шаблона.



Элементы управления

Шаблоны

**ричфонт**

**фонтвисколор**

**фонтонли**

Значение по умолчанию

Необязательно

Значение по умолчанию

Необязательно

Значение по умолчанию

Необязательно

Поле со списком " **Размер шрифта** "

Да

Нет

Да

Нет

Да

Нет

Поле со списком для **семейства шрифтов**

Да

Нет

Да

Нет

Да

Нет

Кнопка " **увеличить шрифт** "

Да

Да

Да

Да

\-

\-

Кнопка " **Сжать шрифт** "

Да

Да

Да

Да

\-

\-

Кнопка **полужирного шрифта**

Да

Нет

Да

Нет

Да

Нет

Кнопка с **курсивом**

Да

Нет

Да

Нет

Да

Нет

Кнопка **подчеркивания**

Да

Нет

Да

Да

Да

Да

Кнопка **перечеркивания**

Да

Нет

Да

Да

Да

Да

Кнопка **подстрочного сценария**

Да

Нет

\-

\-

\-

\-

Кнопка **надстрочного скрипта**

Да

Нет

\-

\-

\-

\-

Кнопка **цвета выделения текста**

Да

Нет

Да

Да

\-

\-

Кнопка **цвета текста**

Да

Нет

Да

Нет

\-

\-



 

При объявлении поведения макета элемента управления Font платформа Ribbon предоставляет необязательный шаблон макета *сизедефинитион* , `OneFontControl` который определяет две конфигурации подэлементов управления на основе размера ленты и места, доступного для элемента управления Font. Дополнительные сведения см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).

### <a name="adding-a-fontcontrol-to-a-ribbon"></a>Добавление Фонтконтрол на ленту

В следующих примерах кода демонстрируются основные требования к разметке для добавления элемента управления Font на ленту.

В этом разделе кода показана разметка объявления команды [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , включая команды [**Tab**](windowsribbon-element-tab.md) и [**Group**](windowsribbon-element-group.md) , необходимые для отображения элемента управления на [**ленте**](windowsribbon-element-ribbon.md).


```C++
<Command Name="cmdTab1"
  Comment="These comments are optional and are inserted into the header file."
  Symbol="cmdTab1" Id="10000" >
  <Command.LabelTitle>Tab 1</Command.LabelTitle>
</Command>
<Command Name="cmdGroup1" Comment="Group #1" Symbol="cmdGroup1" Id="20000">
  <!-- This image is used when the group scales to a pop-up. -->
  <Command.SmallImages>
    <Image>res/Button_Image.bmp</Image>
  </Command.SmallImages>
</Command>
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



В этом разделе кода показана разметка, необходимая для объявления и связывания [**фонтконтрол**](windowsribbon-element-fontcontrol.md) с [**командой**](windowsribbon-element-command.md) с помощью идентификатора команды. В этом конкретном примере содержатся объявления [**вкладок**](windowsribbon-element-tab.md) и [**групп**](windowsribbon-element-group.md) с параметрами масштабирования.


```C++
<Ribbon.Tabs>
  <Tab CommandName="cmdTab1">
    <Tab.ScalingPolicy>
      <ScalingPolicy>
        <ScalingPolicy.IdealSizes>
          <Scale Group="cmdGroup1" Size="Large" />
        </ScalingPolicy.IdealSizes>
        <!-- Describe how the FontControl group scales. -->
        <Scale Group="cmdGroup1" Size="Medium" />
        <Scale Group="cmdGroup1" Size="Popup" />
      </ScalingPolicy>
    <Group CommandName="cmdGroup1" SizeDefinition="OneFontControl">
      <FontControl CommandName="cmdFontControl" FontType="RichFont" />
    </Group>
  </Tab>
</Ribbon.Tabs>
```



### <a name="adding-a-fontcontrol-to-a-contextpopup"></a>Добавление Фонтконтрол в Контекстпопуп

Для добавления элемента управления шрифтом в [всплывающее контекстное меню](windowsribbon-controls-contextpopup.md) требуется процедура, аналогичная процедуре добавления элемента управления шрифта на ленту. Однако элемент управления шрифта в [**минитулбар**](windowsribbon-element-minitoolbar.md) ограничен набором элементов управления по умолчанию, которые являются общими для всех шаблонов элементов управления шрифтом: **семейство шрифтов**, **Размер шрифта**, **полужирный** и **курсив**.

В следующих примерах кода демонстрируются основные требования к разметке для добавления элемента управления шрифтом в [всплывающее контекстное меню](windowsribbon-controls-contextpopup.md):

В этом разделе кода показана разметка объявления команды [**фонтконтрол**](windowsribbon-element-fontcontrol.md) , необходимая для отображения **фонтконтрол** в [**контекстпопуп**](windowsribbon-element-contextpopup.md).


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" />
```



В этом разделе кода показана разметка, необходимая для объявления и связывания [**фонтконтрол**](windowsribbon-element-fontcontrol.md) с командой с помощью идентификатора команды.


```C++
<ContextPopup.MiniToolbars>
  <MiniToolBar Name="MiniToolbar1">
    <MenuCategory Class="StandardItems">
      <FontControl CommandName="cmdFontControl" />
    </MenuCategory>
  </MiniToolBar>
</ContextPopup.MiniToolbars>
```



### <a name="keytips"></a>Подсказки клавиш

Каждый подэлемент управления в элементе управления шрифтом ленты доступен через сочетание клавиш или keytip. Этот KeyTip является стандартным и назначается для каждого подэлементного управления платформой.

Если значение атрибута *KeyTip* присвоено элементу [**фонтконтрол**](windowsribbon-element-fontcontrol.md) в разметке, это значение добавляется в качестве префикса в определяемую платформой keytip.

> [!Note]  
> Для этого префикса приложение должно применять правило с одним символом.

 

В следующей таблице перечислены ключевые подсказки, определенные платформой. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Дополнительный элемент управления</th>
<th>Keytip</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Семейство шрифтов</td>
<td>C</td>
</tr>
<tr class="even">
<td>Стиль шрифта</td>
<td>T</td>
</tr>
<tr class="odd">
<td>Размер шрифта</td>
<td>S</td>
</tr>
<tr class="even">
<td>Увеличить шрифт</td>
<td>G</td>
</tr>
<tr class="odd">
<td>Сжать шрифт</td>
<td>K</td>
</tr>
<tr class="even">
<td>Жирный</td>
<td>B</td>
</tr>
<tr class="odd">
<td>Курсив</td>
<td>I</td>
</tr>
<tr class="even">
<td>Underline</td>
<td>U</td>
</tr>
<tr class="odd">
<td>Зачеркнутый</td>
<td>X</td>
</tr>
<tr class="even">
<td>Надстрочный</td>
<td>Y или Z
<blockquote>
[!Note]<br />
Если атрибут <em>KeyTip</em> не объявлен в разметке, keytip по умолчанию имеет значение Y; в противном случае KeyTip по умолчанию — <em>KeyTip</em> + Z.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Подстрочный</td>
<td>Объект</td>
</tr>
<tr class="even">
<td>Цвет шрифта</td>
<td>C</td>
</tr>
<tr class="odd">
<td>Выделение шрифта</td>
<td>H</td>
</tr>
</tbody>
</table>



 

Рекомендуемый префикс для ленты EN-US многоязыкового интерфейса пользователя — "F", как показано в следующем примере.


```C++
<Command Name="cmdFontControl" Symbol="cmdFontControl" Comment="FontControl" Id="25001" Keytip="F" />
```



На следующем снимке экрана показаны ключевые подсказки элемента управления шрифтом, определенные в предыдущем примере.

![снимок экрана: ключевые подсказки фонтконтрол в WordPad для Windows 7.](images/controls/fontcontrol-keytips.png)

### <a name="the-ribbon-resource-file"></a>Файл ресурсов ленты

При компиляции файла разметки создается файл ресурсов, содержащий все ссылки на ресурсы для приложения ленты.

Пример простого файла ресурсов:


```C++
// ******************************************************************************
// * This is an automatically generated file containing the ribbon resource for *
// * your application.                                                          *
// ******************************************************************************

#include ".\ids.h"

STRINGTABLE 
BEGIN
  cmdTab1_LabelTitle_RESID L"Tab 1" 
    /* LabelTitle cmdTab1_LabelTitle_RESID: These comments are optional and are 
       inserted into the header file. */
END

cmdGroup1_SmallImages_RESID    BITMAP    "res\\Button_Image.bmp" 
  /* SmallImages cmdGroup1_SmallImages_RESID: Group #1 */
STRINGTABLE 
BEGIN
  cmdFontControl_Keytip_RESID L"F" /* Keytip cmdFontControl_Keytip_RESID: FontControl */
END

FCSAMPLE_RIBBON    UIFILE    "Debug\\FCSample.bml"

```



### <a name="font-control-properties"></a>Свойства элемента управления "Шрифт"

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления Font и его составляющих вложенных элементов управления.

Как правило, свойство элемента управления шрифтом обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

В следующей таблице перечислены ключи свойств, связанные с элементом управления "Шрифт".



| Ключ свойства                                                                                                                  | Примечания                                                                                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [UI \_ PKEY \_ фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties.md)                                      | Представляется в статистическом выражении как объект [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , все свойства подсвойства элемента управления Font.<br/> Платформа запрашивает это свойство, когда `UI_INVALIDATIONS_VALUE` аргумент передается как значение *флагов* в вызове метода [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).<br/> |
| [UI \_ PKEY \_ фонтпропертиес \_ чанжедпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-changedproperties.md) | Предоставляет в статистическом выражении в виде объекта [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) только те свойства элемента управления шрифта, которые были изменены.<br/>                                                                                                                                                                                                        |
| [UI \_ PKEY \_ keytip](windowsribbon-reference-properties-uipkey-keytip.md)                                                      | Может обновляться только через недействительность.                                                                                                                                                                                                                                                                                                                                                      |
| [Пользовательский интерфейс \_ PKEY \_ включен](windowsribbon-reference-properties-uipkey-enabled.md)                                                    | Поддерживает [**иуифрамеворк:: жетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и [**Иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).                                                                                                                                                                  |



 

В дополнение к свойствам, поддерживаемым самим элементом управления шрифтом, платформа Ribbon также определяет [ключ свойства](windowsribbon-reference-properties.md) для каждого подэлементного элемента управления шрифта. Эти ключи свойств и их значения предоставляются платформой с помощью реализации интерфейса [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) , определяющей методы управления коллекцией, также называемые контейнером свойств, в парах имени и значения.

Приложение преобразует структуры шрифтов в свойства, доступные через методы интерфейса [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Эта модель подчеркивает различие между элементом управления шрифта и компонентами текстового стека Windows интерфейс графических устройств (GDI) ([Структура LOGFONT](/windows/win32/api/wingdi/ns-wingdi-logfonta), [Структура CHOOSEFONT](/windows/win32/api/commdlg/ns-commdlg-choosefonta)и [Структура CHARFORMAT2](/windows/win32/api/richedit/ns-richedit-charformat2a)), которые поддерживаются платформой.

В следующей таблице перечислены отдельные элементы управления и связанные с ними ключи свойств.



| Элементы управления                 | Ключ свойства                                                                                                                                                                                                                                                           | Примечания                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Размер шрифта**            | [\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | Если выделенный размер текста хетероженеаусли выделяется, платформа Ribbon устанавливает пустой элемент управления **размером шрифта** , а значение [UI \_ PKEY \_ фонтпропертиес \_ size](windowsribbon-reference-properties-uipkey-fontproperties-size.md) — 0. При нажатии кнопки **увеличить шрифт** или **Сжать шрифт** размер выделенного текста изменяется, но относительная разница в размерах текста сохраняется.                                                                                                                                                    |
| **Семейство шрифтов**          | [\_Семейство UI PKEY \_ фонтпропертиес \_](windowsribbon-reference-properties-uipkey-fontproperties-family.md)                                                                                                                                                                | Имена семейств шрифтов GDI зависят от национальной настройки системы. Таким образом, если значение [ \_ \_ \_ семейства UI PKEY фонтпропертиес](windowsribbon-reference-properties-uipkey-fontproperties-family.md) сохраняется в сеансах приложения, это значение должно быть получено в каждом новом сеансе.                                                                                                                                                                                                                                                                            |
| **Увеличить шрифт**            | [\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | См. **Размер шрифта**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Сжать шрифт**          | [\_ \_ Размер фонтпропертиес пользовательского интерфейса PKEY \_](windowsribbon-reference-properties-uipkey-fontproperties-size.md)                                                                                                                                                                    | См. **Размер шрифта**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Полужирный**                 | [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Bold](windowsribbon-reference-properties-uipkey-fontproperties-bold.md)                                                                                                                                                                    |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Наклонный**               | [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ курсивом](windowsribbon-reference-properties-uipkey-fontproperties-italic.md)                                                                                                                                                                |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Начертан**            | [Подчеркивание пользовательского интерфейса \_ PKEY \_ фонтпропертиес \_](windowsribbon-reference-properties-uipkey-fontproperties-underline.md)                                                                                                                                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Зачеркнутый**        | [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ Зачеркнутый](windowsribbon-reference-properties-uipkey-fontproperties-strikethrough.md)                                                                                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Индекс**            | [UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Если задана кнопка « **индекс** », то **Надстрочный индекс** также не может быть установлен.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Надстрочный**          | [UI \_ PKEY \_ фонтпропертиес \_ вертикалпоситионинг](windowsribbon-reference-properties-uipkey-fontproperties-verticalpositioning.md)                                                                                                                                      | Если задана кнопка **надстрочного скрипта** , то этот **индекс** также не может быть установлен.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Цвет выделения текста** | [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ BackgroundColor](/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolor), [UI \_ PKEY \_ фонтпропертиес \_ баккграундколортипе](windowsribbon-reference-properties-uipkey-fontproperties-backgroundcolortype.md) | Предоставляет те же функциональные возможности, что и `HighlightColors` шаблон элемента [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Мы настоятельно рекомендуем, чтобы приложение было установлено только первоначальное значение **цвета выделения текста** . Последнее выбранное значение должно быть сохранено и не задаваться при перемещении курсора в пределах документа. Это обеспечивает быстрый доступ к последнему выделенному пользователю, и средство выбора цвета не нужно открывать повторно.<br/> Образцы цветов не могут быть настроены.<br/> |
| **Цвет текста**           | [Пользовательский интерфейс \_ PKEY \_ фонтпропертиес \_ ForegroundColor](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolor.md), [UI \_ PKEY \_ фонтпропертиес \_ фореграундколортипе](windowsribbon-reference-properties-uipkey-fontproperties-foregroundcolortype.md)           | Предоставляет те же функциональные возможности, что и `StandardColors` шаблон элемента [**дропдовнколорпиккер**](windowsribbon-element-dropdowncolorpicker.md) .<br/> Мы настоятельно рекомендуем установить только исходное значение **цвета текста** , установленное приложением. Последнее выбранное значение должно быть сохранено и не задаваться при перемещении курсора в пределах документа. Это обеспечивает быстрый доступ к последнему выделенному пользователю, и средство выбора цвета не нужно открывать повторно.<br/> Образцы цветов не могут быть настроены.<br/>            |



 

## <a name="define-a-fontcontrol-command-handler"></a>Определение обработчика команд Фонтконтрол

В этом разделе описаны шаги, необходимые для привязки элемента управления "Шрифт" к обработчику команд.

> [!WARNING]
> Любая попытка выбрать цветовую палитру из палитры элементов управления шрифта может привести к нарушению прав доступа, если с элементом управления не связан ни один обработчик команд.

 

В следующем примере кода показано, как привязать команды, объявленные в разметке к обработчику команд.


```C++
//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup, to allow
//           the host application to bind a command handler to that command.
//
STDMETHODIMP CApplication::OnCreateUICommand(
  UINT nCmdID,
  __in UI_COMMANDTYPE typeID,
  __deref_out IUICommandHandler** ppCommandHandler)
{
  UNREFERENCED_PARAMETER(typeID);
  UNREFERENCED_PARAMETER(nCmdID);

  if (NULL == m_pCommandHandler)
  {
    HRESULT hr = CCommandHandler::CreateInstance(&m_pCommandHandler);
    if (FAILED(hr))
    {
      return hr;
    }
  }

  return m_pCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
}
```



В следующем примере кода показано, как реализовать метод [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) для элемента управления Font.


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a command is executed 
//           by the user. For example, when a button is pressed.
//
STDMETHODIMP CCommandHandler::Execute(
  UINT nCmdID,
  UI_EXECUTIONVERB verb,
  __in_opt const PROPERTYKEY* key,
  __in_opt const PROPVARIANT* ppropvarValue,
  __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if ((key) && (*key == UI_PKEY_FontProperties))
  {
    // Font properties have changed.
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Using the changed properties, set the new font on the selection on RichEdit control.
              g_pFCSampleAppManager->SetValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_PREVIEW:
      {
        hr = E_POINTER;
        if (pCommandExecutionProperties != NULL)
        {
          // Get the changed properties for the preview event.
          PROPVARIANT varChanges;
          hr = pCommandExecutionProperties->GetValue(UI_PKEY_FontProperties_ChangedProperties, &varChanges);
          if (SUCCEEDED(hr))
          {
            IPropertyStore *pChanges;
            hr = UIPropertyToInterface(UI_PKEY_FontProperties, varChanges, &pChanges);
            if (SUCCEEDED(hr))
            {
              // Set the previewed values on the RichEdit control.
              g_pFCSampleAppManager->SetPreviewValues(pChanges);
              pChanges->Release();
            }
            PropVariantClear(&varChanges);
          }
        }
        break;
      }
      case UI_EXECUTIONVERB_CANCELPREVIEW:
      {
        hr = E_POINTER;
        if (ppropvarValue != NULL)
        {
          // Cancel the preview.
          IPropertyStore *pValues;
          hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarValue, &pValues);
          if (SUCCEEDED(hr))
          {   
            g_pFCSampleAppManager->CancelPreview(pValues);
            pValues->Release();
          }
        }
        break;
      }
    }
  }

  return hr;
}
```



В следующем примере кода показано, как реализовать метод [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) для элемента управления Font.


```C++
//
//  FUNCTION: UpdateProperty()
//
//  PURPOSE: Called by the Ribbon framework when a command property (PKEY) needs to be updated.
//
//  COMMENTS:
//
//    This function is used to provide new command property values, such as labels, icons, or
//    tooltip information, when requested by the Ribbon framework.  
//    
//
STDMETHODIMP CCommandHandler::UpdateProperty(
  UINT nCmdID,
  __in REFPROPERTYKEY key,
  __in_opt const PROPVARIANT* ppropvarCurrentValue,
  __out PROPVARIANT* ppropvarNewValue)
{
  UNREFERENCED_PARAMETER(nCmdID);

  HRESULT hr = E_NOTIMPL;
  if (key == UI_PKEY_FontProperties)
  {
    hr = E_POINTER;
    if (ppropvarCurrentValue != NULL)
    {
      // Get the font values for the selected text in the font control.
      IPropertyStore *pValues;
      hr = UIPropertyToInterface(UI_PKEY_FontProperties, *ppropvarCurrentValue, &pValues);
      if (SUCCEEDED(hr))
      {
        g_pFCSampleAppManager->GetValues(pValues);

        // Provide the new values to the font control.
        hr = UIInitPropertyFromInterface(UI_PKEY_FontProperties, pValues, ppropvarNewValue);
        pValues->Release();
      }
    }
  }

  return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Библиотека элементов управления платформы Windows ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[**Фонтконтрол, элемент**](windowsribbon-element-fontcontrol.md)
</dt> <dt>

[Свойства элемента управления "Шрифт"](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Пример Фонтконтрол](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

