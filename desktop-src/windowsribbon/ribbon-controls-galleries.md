---
title: Работа с коллекциями
description: платформа Windows Ribbon предоставляет разработчикам надежную и согласованную модель управления динамическим содержимым в различных элементах управления, основанных на коллекциях.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Лента, коллекции
- Лента, коллекции
- Windows Лента, элемент управления Дропдовнгаллери
- Лента, элемент управления Дропдовнгаллери
- Windows Лента, элемент управления Сплитбуттонгаллери
- Лента, элемент управления Сплитбуттонгаллери
- Элемент управления Дропдовнгаллери
- Элемент управления Сплитбуттонгаллери
- коллекции для Windows ленты
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933453"
---
# <a name="working-with-galleries"></a>Работа с коллекциями

платформа Windows Ribbon предоставляет разработчикам надежную и согласованную модель управления динамическим содержимым в различных элементах управления, основанных на коллекциях. Адаптируя и перестраивая ленту, эти динамические элементы управления позволяют платформе реагировать на взаимодействие пользователя как в ведущем приложении, так и на ленте, а также обеспечивают гибкость при обработке различных сред выполнения.

-   [Введение](#introduction)
-   [Коллекции](#working-with-galleries)
    -   [Коллекции элементов](#item-galleries)
    -   [Коллекции команд](#command-galleries)
    -   [Элементы управления галереи](#working-with-galleries)
-   [Реализация коллекции](#how-to-implement-a-gallery)
    -   [Основные компоненты](#the-basic-components)
    -   [Объявление элементов управления в разметке](#declare-the-controls-in-markup)
    -   [Создание обработчика команд](#create-a-command-handler)
    -   [Привязка обработчика команд](#bind-the-command-handler)
    -   [Инициализация коллекции](#initialize-a-collection)
    -   [Обработку событий коллекции](#handle-collection-events)
-   [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

Эта возможность платформы Ribbon динамически адаптируется к условиям времени выполнения, требованиям приложений и вводу конечных пользователей, что приводит к расширению возможностей пользовательского интерфейса платформы и предоставляет разработчикам гибкие возможности для удовлетворения широкого спектра потребностей клиентов.

Основное внимание в этом руководства состоит в том, чтобы описать динамические элементы управления галереи, поддерживаемые платформой, объяснить их различия, обсудить, когда и где их лучше использовать, и продемонстрировать, как они могут быть включены в приложение ленты.

## <a name="galleries"></a>Коллекции

Галереи функционально и графически имеют богатые элементы управления "список". Коллекцию элементов коллекции можно упорядочить по категориям, отображаемым в гибких макетах столбцов и строк, представленных изображениями и текстом, а также в зависимости от типа коллекции, поддерживающей динамический просмотр.

Коллекции функционально отличаются от других динамических элементов управления ленты по следующим причинам.

-   Коллекции реализуют интерфейс [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , который определяет различные методы управления коллекциями элементов коллекции.
-   Коллекции можно обновлять во время выполнения на основе действий, которые выполняются непосредственно на ленте, например, когда пользователь добавляет команду на панель быстрого доступа (QAT).
-   Коллекции могут обновляться во время выполнения на основе действий, которые происходят косвенно из среды выполнения, например, если драйвер принтера поддерживает только книжные макеты страниц.
-   Коллекции можно обновлять во время выполнения на основе действий, которые происходят косвенно в ведущем приложении, например, когда пользователь выбирает элемент в документе.

Платформа Ribbon предоставляет два типа коллекций: коллекции элементов и коллекции команд.

### <a name="item-galleries"></a>Коллекции элементов

Коллекции элементов содержат коллекцию связанных элементов, основанную на индексах, где каждый элемент представлен изображением, строкой или обоими элементами. Элемент управления привязан к одному обработчику команды, который использует значение индекса, определяемое свойством [UI \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) .

Коллекции элементов поддерживают динамическое представление, что означает отображение результата команды на основе фокуса ввода-вывода без фиксации или фактического вызова команды.

> [!IMPORTANT]
> Платформа не поддерживает размещение коллекций элементов в меню приложения.

 

### <a name="command-galleries"></a>Коллекции команд

Коллекции команд содержат коллекцию уникальных неиндексированных элементов. Каждый элемент представлен одним элементом управления, привязанным к обработчику команд с помощью идентификатора команды. Как и автономные элементы управления, каждый элемент в коллекции команд направляет события ввода в связанный обработчик команды — сама коллекция команд не прослушивает события.

Коллекции команд не поддерживают динамический просмотр.

### <a name="gallery-controls"></a>Элементы управления галереи

В платформе Ribbon есть четыре элемента управления галереи: [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md), [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md), [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)и [**ComboBox**](windowsribbon-element-combobox.md). Все, за исключением **поля со списком** , можно реализовать как коллекцию элементов или коллекцию команд.

### <a name="dropdowngallery"></a>дропдовнгаллери

[**Дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) — это кнопка, которая отображает раскрывающийся список, содержащий коллекцию взаимоисключающих элементов или команд.

на следующем снимке экрана показан [раскрывающийся список](windowsribbon-controls-dropdowngallery.md) элементов управления "лента" в Microsoft Paint для Windows 7.

![снимок экрана с раскрывающимся элементом управления галереи в Microsoft Paint для Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>сплитбуттонгаллери

[**Сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) — это составной элемент управления, предоставляющий один элемент или команду по умолчанию из своей коллекции на основной кнопке и отображающий другие элементы или команды в взаимоисключающем раскрывающемся списке, который отображается при нажатии на вторичную кнопку.

на следующем снимке экрана показан элемент управления ["коллекция кнопок с разделением ленты"](windowsribbon-controls-splitbuttongallery.md) в Microsoft Paint для Windows 7.

![снимок экрана: элемент управления "коллекция разделенных кнопок" в Microsoft Paint для Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>инриббонгаллери

[**Инриббонгаллери**](windowsribbon-element-inribbongallery.md) — это коллекция, в которой отображается коллекция связанных элементов или команд на ленте. Если в коллекции слишком много элементов, для показа остальной части коллекции в развернутой области предоставляется стрелка развертывания.

на следующем снимке экрана показана лента в элементе управления " [коллекция ленты](windowsribbon-controls-inribbongallery.md) " в Microsoft Paint для Windows 7.

![снимок экрана: элемент управления "Коллекция на ленте" на ленте Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

[**ComboBox**](windowsribbon-element-combobox.md) — это список из одного столбца, который содержит коллекцию элементов со статическим элементом управления или элементом управления "поле ввода" и стрелкой раскрывающегося списка. Часть элемента управления отображается в списке, когда пользователь щелкает стрелку раскрывающегося списка.

на следующем снимке экрана показан элемент управления ["поле со списком"](windowsribbon-controls-combobox.md) на ленте Киностудия Windows Live.

![снимок экрана элемента управления ComboBox на ленте Microsoft Paint.](images/controls/combobox.png)

Поскольку [**ComboBox**](windowsribbon-element-combobox.md) является исключительно коллекцией элементов, он не поддерживает командные элементы. Он также является единственным элементом управления "Коллекция", который не поддерживает пространство команд. (Пространство команд — это коллекция команд, которые объявляются в разметке и перечислены в нижней части коллекции элементов или коллекции команд.)

В следующем примере кода показана разметка, необходимая для объявления пространства команд с тремя кнопками в [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md).


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



На следующем снимке экрана показана Командная область из трех кнопок в предыдущем примере кода.

![снимок экрана командного пространства с тремя кнопками в дропдовнгаллери.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Реализация коллекции

В этом разделе обсуждаются сведения о реализации коллекций лент и описывается их внедрение в приложение для ленты.

### <a name="the-basic-components"></a>Основные компоненты

В этом разделе описывается набор свойств и методов, образующих основу динамического содержимого в платформе Ribbon и поддерживающий Добавление, удаление, обновление и иным образом Управление содержимым и визуальным макетом коллекций лент во время выполнения.

### <a name="iuicollection"></a>иуиколлектион

Для коллекций требуется базовый набор методов для доступа к отдельным элементам в коллекциях и управления ими.

Интерфейс [иенумункновн](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) определяет эти методы, а платформа дополняет свои функциональные возможности дополнительными методами, определенными в интерфейсе [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . **Иуиколлектион** реализуется платформой для каждого объявления галереи в разметке ленты.

Если требуется дополнительная функциональность, не предоставляемую интерфейсом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , то пользовательский объект коллекции, реализуемый ведущим приложением и производный от [иенумункновн](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) , можно заменить на коллекцию платформы.

### <a name="iuicollectionchangedevent"></a>иуиколлектиончанжедевент

Чтобы приложение отвечало на изменения коллекции коллекции, оно должно реализовать интерфейс [**иуиколлектиончанжедевент**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) . Приложения могут подписываться на уведомления из объекта [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) с помощью прослушивателя событий [**иуиколлектиончанжедевент:: OnChanged**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged) .

Когда приложение заменяет коллекцию коллекции, предоставленную платформой, пользовательской коллекцией, приложение должно реализовать интерфейс [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) . Если [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) не реализован, приложение не сможет уведомить платформу об изменениях в пользовательской коллекции, требующих динамических обновлений для элемента управления галереи.

В тех случаях, когда [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) не реализован, элемент управления галереи может быть обновлен только путем недействительности через [**Иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) и [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)или путем вызова [**иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>иуисимплепропертисет

Приложения должны реализовывать Иуисимплепропертисет для каждого элемента или команды в коллекции коллекции. Однако свойства, которые могут быть запрошены с помощью [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) , различаются.

Элементы определяются и привязываются к коллекции через ключ свойства [ \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) и предоставляют свойства объекту [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) .

Допустимые свойства элементов коллекций элементов ([**\_ \_ коллекция COMMANDTYPE ИП**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) описаны в следующей таблице.

> [!Note]  
> Некоторые свойства элементов, например [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md), могут быть определены в разметке. Дополнительные сведения см. в справочной документации по [ключам свойств](windowsribbon-reference-properties.md) .

 



Control

Свойства

[**ComboBox**](windowsribbon-element-combobox.md)

[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)

[**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)

[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md) , [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)

[**инриббонгаллери**](windowsribbon-element-inribbongallery.md)

[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md) , [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)

[**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md)

[Пользовательский интерфейс \_ \_Метка PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ итемимаже](windowsribbon-reference-properties-uipkey-itemimage.md), [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)

[Пользовательский интерфейс \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) — это свойство коллекции элементов.



 

Допустимые свойства элементов для коллекций команд ([**Пользовательский интерфейс \_ COMMANDTYPE \_ COMMANDCOLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) описаны в следующей таблице.



| Control                                                                | Свойства                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md)       | [Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md) , [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**инриббонгаллери**](windowsribbon-element-inribbongallery.md)       | [Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md) , [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) | [Пользовательский интерфейс \_ PKEY \_ CommandId](windowsribbon-reference-properties-uipkey-commandid.md), [Пользовательский \_ интерфейс \_ PKEY](windowsribbon-reference-properties-uipkey-commandtype.md), [ \_ \_ КодТипа ИП, Пользовательский интерфейс PKEY](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

Категории используются для упорядочения элементов и команд в коллекциях. Категории определяются и привязываются к коллекции через ключ свойства " [ \_ \_ категории PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-categories.md) " и предоставляют свойства с объектом [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) , относящимся к категории.

Категории не имеют CommandType и не поддерживают взаимодействие с пользователем. Например, категории не могут стать SelectedItem в коллекции элементов и не привязаны к команде в коллекции команд. Как и другие свойства элемента коллекции, свойства категории, такие как [ \_ \_ Метка PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md) и свойство [UI \_ PKEY \_](windowsribbon-reference-properties-uipkey-categoryid.md) , могут быть получены путем вызова [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**Иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) должен возвращать [**\_ коллекцию UI \_ инвалидиндекс**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) , когда для элемента, не имеющего связанной категории, запрашивается [ \_ \_ КодТипа пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-categoryid.md) .

 

### <a name="declare-the-controls-in-markup"></a>Объявление элементов управления в разметке

Коллекции, как и все элементы управления ленты, должны быть объявлены в разметке. Коллекция определяется в разметке как коллекция элементов или коллекция команд, и объявляются различные сведения о презентации. В отличие от других элементов управления, коллекции должны объявляться в разметке только базовый элемент управления или контейнер коллекции. Фактические коллекции заполняются во время выполнения. При объявлении коллекции в разметке атрибут *Type* используется, чтобы указать, является ли коллекция коллекцией элементов коллекции команд.

Существует ряд необязательных атрибутов макета для каждого из обсуждаемых здесь элементов управления. Эти атрибуты предоставляют разработчикам параметры для платформы, которые непосредственно влияют на то, как элемент управления заполняется и отображается на ленте. Параметры, применимые в разметке, связаны с шаблонами вывода и макета и поведением, обсуждаемым в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).

Если определенный элемент управления не разрешает предпочтения макета непосредственно в разметке или не заданы параметры макета, платформа определяет зависящие от конкретного элемента соглашения о отображении в зависимости от объема доступного пространства экрана.

В следующих примерах показано, как включить набор коллекций в ленту.

### <a name="command-declarations"></a>Объявления команд

Команды должны объявляться с атрибутом *CommandName* , который используется для связывания элемента управления или набора элементов управления с командой.

Атрибут *CommandId* , используемый для привязки команды к обработчику команд при компиляции разметки, также можно указать здесь. Если идентификатор не указан, то он создается платформой.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Объявления элементов управления

Этот раздел содержит примеры, демонстрирующие базовую разметку элемента управления, необходимую для различных типов коллекций. В них показано, как объявить элементы управления галереи и связать их с командой с помощью атрибута *CommandName* .

В следующем примере показано объявление элемента управления для [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) , где атрибут *Type* используется, чтобы указать, что это коллекция команд.


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



В следующем примере показано объявление элемента управления для [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



В следующем примере показано объявление элемента управления для [**инриббонгаллери**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Поскольку [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) предназначен для вывода на ленту подмножества коллекции элементов без активации раскрывающегося меню, он предоставляет ряд необязательных атрибутов, управляющих его размером и макетом элемента при инициализации ленты. Эти атрибуты являются уникальными для **инриббонгаллери** и недоступны из других динамических элементов управления.

 


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



В следующем примере показано объявление элемента управления для [**ComboBox**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Создание обработчика команд

Для каждой команды платформе Ribbon требуется соответствующий обработчик команд в ведущем приложении. Обработчики команд реализуются ведущим приложением ленты и являются производными от интерфейса [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .

> [!Note]  
> К одному обработчику команды можно привязать несколько команд.

 

Обработчик команд выполняет две задачи:

-   [**Иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) отвечает на запросы обновления свойств. Значения свойств команд, таких как [ \_ \_ включенный ИП UI](windowsribbon-reference-properties-uipkey-enabled.md) или [ \_ \_ подпись PKEY пользовательского интерфейса](windowsribbon-reference-properties-uipkey-label.md), задаются посредством вызовов [**иуифрамеворк:: сетуикоммандпроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) или [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) отвечает на выполнение событий. Этот метод поддерживает следующие три состояния выполнения, заданные параметром [**\_ Ексекутионверб пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .
    -   Состояние выполнения (или фиксация в) выполняет все команды, с которыми связан обработчик.
    -   Предварительный просмотр позволяет просмотреть все команды, к которым привязан обработчик. Это по сути выполняет команды без фиксации в результате.
    -   Состояние Канцелпревиев отменяет все предварительно просмотрные команды. Это необходимо для поддержки прохода по меню или списку и последовательного предварительного просмотра и отмены результатов по мере необходимости.

В следующем примере показан обработчик команд коллекции.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Привязка обработчика команд

После определения обработчика команд должна быть привязана к обработчику.

В следующем примере показано, как привязать команду коллекции к конкретному обработчику команды. В этом случае элементы управления [**ComboBox**](windowsribbon-element-combobox.md) и Gallery привязываются к соответствующим обработчикам команд.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Инициализация коллекции

В следующем примере демонстрируется пользовательская реализация [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) для коллекций элементов и команд.

Класс Цитемпропертиес в этом примере является производным от [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). В дополнение к обязательному методу [**иуисимплепропертисет:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)класс Цитемпропертиес реализует набор вспомогательных функций для инициализации и отслеживания индексов.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Обработку событий коллекции

В следующем примере демонстрируется реализация Иуиколлектиончанжедевент.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Свойства коллекции](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Создание приложения для ленты](windowsribbon-stepbystep.md)
</dt> <dt>

[Основные сведения о командах и элементах управления](windowsribbon-commandscontrols.md)
</dt> <dt>

[Рекомендации по работе пользователя с лентой](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Процесс разработки ленты](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Пример коллекции](windowsribbon-gallerysample.md)
</dt> </dl>

 

 