---
title: Отображение контекстных вкладок
description: В приложении Windows Ribbon Framework контекстная вкладка — это скрытый элемент управления "Вкладка", который отображается в строке вкладки при выборе или выделении объекта в рабочей области приложения, например изображения.
ms.assetid: 2059ca42-6a99-43a2-b1f5-ce5554156993
keywords:
- Лента Windows, контекстные вкладки
- Лента, контекстные вкладки
- Отображение контекстных вкладок ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a1e81ac6587e39a04114fa2f938a6da0e9a4d1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791676"
---
# <a name="displaying-contextual-tabs"></a>Отображение контекстных вкладок

В приложении Windows Ribbon Framework контекстная вкладка — это скрытый элемент управления ["Вкладка](windowsribbon-controls-tab.md) ", который отображается в строке вкладки при выборе или выделении объекта в рабочей области приложения, например изображения.

-   [Введение](#introduction)
-   [Реализация контекстных вкладок](#implementing-contextual-tabs)
    -   [разметку](#markup)
    -   [Код](#code)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

В отличие от основных вкладок, которые содержат различные общие команды, относящиеся к контексту рабочей области, контекстные вкладки обычно содержат одну или несколько команд, применимых только к выбранному или выделенному объекту.

Если объект выбран или выделен в рабочей области приложения, для типа и контекста объекта могут потребоваться разнородные команды, которые не имеют смысла работать на одной контекстной вкладке. В таких случаях может потребоваться несколько контекстных вкладок, содержащихся в [группе вкладок](windowsribbon-controls-tabgroup.md). Например, для выбора изображения, содержащегося в ячейке таблицы, могут потребоваться две контекстные вкладки, предоставляющие функциональные возможности работы с таблицами и изображениями.

> [!Note]  
> В дополнение к нескольким контекстным вкладкам платформа Ribbon также поддерживает несколько элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) на ленте.

 

При отображении контекстных вкладок платформа Ribbon обеспечивает базовый набор поведений, включающий:

-   Контекстные вкладки располагаются в том порядке, в котором они объявляются, и справа от основных вкладок в строке вкладки ленты.
-   При изменении размера ленты вкладки масштабируются, а метки вкладок усекаются, как требуется. Однако видимые контекстные вкладки получают более высокий приоритет отображения, в котором они масштабируются и усекаются последними.
-   Метка для [группы вкладок](windowsribbon-controls-tabgroup.md) отображается в строке заголовка приложения и охватывает все связанные контекстные вкладки.
-   Если одновременно отображается несколько элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) , фон каждой группы вкладок в заголовке окна приложения назначается одному из пяти уникальных цветов. Этот цвет также используется в качестве цвета выделения для контекстных вкладок в группе вкладок.
-   Назначение цвета [группы вкладок](windowsribbon-controls-tabgroup.md) основано на порядке объявления элементов группы вкладок в разметке. Цвета определяются платформой и не могут быть заданы приложением.
-   Цвета [группы вкладок](windowsribbon-controls-tabgroup.md) , определенные в инфраструктуре, можно изменить непрямо через ключи свойств [платформы](windowsribbon-reference-properties-framework.md) . Дополнительные сведения см. в разделе [Настройка цветов ленты](ribbon-color.md).
-   Если в любое одиночное время отображается более пяти элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) , платформа циклически переводит соответствующие цвета.
-   Максимальное число элементов управления ["Вкладка"](windowsribbon-controls-tab.md) на ленте ограничено 100. К ним относятся контекстные вкладки, видимые или нет.

На следующем снимке экрана показана контекстная вкладка из Windows 7 Paint.

![снимок экрана, на котором показан контекстный элемент управления вкладки.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a>Реализация контекстных вкладок

В этом разделе обсуждаются сведения о реализации контекстных вкладок ленты и описывается их внедрение в приложение для ленты.

### <a name="markup"></a>разметку

В следующих примерах демонстрируется базовая разметка для элемента [**табграуп**](windowsribbon-element-tabgroup.md) , который содержит две контекстные вкладки.

В этом разделе кода показаны объявления команд [**табграуп**](windowsribbon-element-tabgroup.md) и [Tab](windowsribbon-controls-tab.md) .


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



В этом разделе кода показаны объявления элементов управления, необходимые для отображения двух контекстных вкладок в [**табграуп**](windowsribbon-element-tabgroup.md).


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



### <a name="code"></a>Код

[Пользовательский интерфейс \_ PKEY \_ контекставаилабле](windowsribbon-reference-properties-uipkey-contextavailable.md) — это единственный ключ свойства, определенный платформой для указания видимости и состояния контекстных вкладок. При выборе объекта в рабочей области приложения этому свойству может быть присвоено одно из трех значений из перечисления [**\_ Контекставаилабилити пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) , которое определяет, существует ли контекстная вкладка, и, если она есть, отображается ли она как активная вкладка.

Приложение запрашивает обновление [группы вкладок](windowsribbon-controls-tabgroup.md) путем непроверки и обновления свойства [контекставаилабле UI \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-contextavailable.md) при изменении контекста рабочей области.

В следующих разделах кода показано, как отобразить контекстную вкладку при выборе изображения в рабочей области приложения.


```C++
// Initialize the image tools contextual tab visibility setting.
UI_CONTEXTAVAILABILITY g_ImageTools = UI_CONTEXTAVAILABILITY_NOTAVAILABLE;

// Called when an image is selected in the application.
void SelectImage()
{
  ...
  g_ImageTools = UI_CONTEXTAVAILABILITY_ACTIVE;

  // Invalidate the UI_PKEY_ContextAvailable property of the image tools  
  // contextual tab Command and trigger the UpdatePropery callback function.
  pUIFramework->InvalidateUICommand(
                  cmdImageTabSet, 
                  UI_INVALIDATIONS_PROPERTY, 
                  UI_PKEY_ContextAvailable);
  ...
}

// Update Tab Group properties.
HRESULT MyTabGroupCommandHandler::UpdateProperty(
                                  UINT nCmdID,
                                  REFPROPERTYKEY key,
                                  const PROPVARIANT* ppropvarCurrentValue,
                                  PROPVARIANT* ppropvarNewValue)
{
  HRESULT hr = E_FAIL;

  if (key == UI_PKEY_ContextAvailable)
  {
    hr = UIInitPropertyFromUInt32(key, g_ImageTools, ppropvarNewValue);
  }
  ...
  return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Рекомендации по работе пользователя с лентой](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Процесс разработки ленты](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 