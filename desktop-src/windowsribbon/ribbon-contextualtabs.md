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
# <a name="displaying-contextual-tabs"></a><span data-ttu-id="e747a-106">Отображение контекстных вкладок</span><span class="sxs-lookup"><span data-stu-id="e747a-106">Displaying Contextual Tabs</span></span>

<span data-ttu-id="e747a-107">В приложении Windows Ribbon Framework контекстная вкладка — это скрытый элемент управления ["Вкладка](windowsribbon-controls-tab.md) ", который отображается в строке вкладки при выборе или выделении объекта в рабочей области приложения, например изображения.</span><span class="sxs-lookup"><span data-stu-id="e747a-107">In a Windows Ribbon framework application, a contextual tab is a hidden [Tab](windowsribbon-controls-tab.md) control that is displayed in the tab row when an object in the application workspace, such as an image, is selected or highlighted.</span></span>

-   [<span data-ttu-id="e747a-108">Введение</span><span class="sxs-lookup"><span data-stu-id="e747a-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="e747a-109">Реализация контекстных вкладок</span><span class="sxs-lookup"><span data-stu-id="e747a-109">Implementing Contextual Tabs</span></span>](#implementing-contextual-tabs)
    -   [<span data-ttu-id="e747a-110">разметку</span><span class="sxs-lookup"><span data-stu-id="e747a-110">Markup</span></span>](#markup)
    -   [<span data-ttu-id="e747a-111">Код</span><span class="sxs-lookup"><span data-stu-id="e747a-111">Code</span></span>](#code)
-   [<span data-ttu-id="e747a-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e747a-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="e747a-113">Введение</span><span class="sxs-lookup"><span data-stu-id="e747a-113">Introduction</span></span>

<span data-ttu-id="e747a-114">В отличие от основных вкладок, которые содержат различные общие команды, относящиеся к контексту рабочей области, контекстные вкладки обычно содержат одну или несколько команд, применимых только к выбранному или выделенному объекту.</span><span class="sxs-lookup"><span data-stu-id="e747a-114">In contrast to core tabs, which contain various common Commands that are relevant regardless of workspace context, contextual tabs typically contain one or more Commands that are applicable to a selected or highlighted object only.</span></span>

<span data-ttu-id="e747a-115">Если объект выбран или выделен в рабочей области приложения, для типа и контекста объекта могут потребоваться разнородные команды, которые не имеют смысла работать на одной контекстной вкладке. В таких случаях может потребоваться несколько контекстных вкладок, содержащихся в [группе вкладок](windowsribbon-controls-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="e747a-115">When an object is selected or highlighted in the application workspace, the type and context of the object might require disparate Commands that do not make organizational or functional sense on one contextual tab. In these cases, multiple contextual tabs, which are contained within a [Tab Group](windowsribbon-controls-tabgroup.md), may be required.</span></span> <span data-ttu-id="e747a-116">Например, для выбора изображения, содержащегося в ячейке таблицы, могут потребоваться две контекстные вкладки, предоставляющие функциональные возможности работы с таблицами и изображениями.</span><span class="sxs-lookup"><span data-stu-id="e747a-116">For example, selecting an image contained in a table cell might require two contextual tabs that expose both table and image functionality.</span></span>

> [!Note]  
> <span data-ttu-id="e747a-117">В дополнение к нескольким контекстным вкладкам платформа Ribbon также поддерживает несколько элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) на ленте.</span><span class="sxs-lookup"><span data-stu-id="e747a-117">In addition to multiple contextual tabs, the Ribbon framework also supports multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls within a ribbon.</span></span>

 

<span data-ttu-id="e747a-118">При отображении контекстных вкладок платформа Ribbon обеспечивает базовый набор поведений, включающий:</span><span class="sxs-lookup"><span data-stu-id="e747a-118">When displaying contextual tabs, the Ribbon framework enforces a basic set of behaviors that include:</span></span>

-   <span data-ttu-id="e747a-119">Контекстные вкладки располагаются в том порядке, в котором они объявляются, и справа от основных вкладок в строке вкладки ленты.</span><span class="sxs-lookup"><span data-stu-id="e747a-119">Contextual tabs are positioned in the order they are declared and to the right of core tabs in the ribbon tab row.</span></span>
-   <span data-ttu-id="e747a-120">При изменении размера ленты вкладки масштабируются, а метки вкладок усекаются, как требуется.</span><span class="sxs-lookup"><span data-stu-id="e747a-120">When the ribbon is resized, tabs are scaled and tab labels are truncated as space requires.</span></span> <span data-ttu-id="e747a-121">Однако видимые контекстные вкладки получают более высокий приоритет отображения, в котором они масштабируются и усекаются последними.</span><span class="sxs-lookup"><span data-stu-id="e747a-121">However, visible contextual tabs are given a higher display priority in which they are scaled and truncated last.</span></span>
-   <span data-ttu-id="e747a-122">Метка для [группы вкладок](windowsribbon-controls-tabgroup.md) отображается в строке заголовка приложения и охватывает все связанные контекстные вкладки.</span><span class="sxs-lookup"><span data-stu-id="e747a-122">The label for a [Tab Group](windowsribbon-controls-tabgroup.md) is displayed in the application title bar and spans all associated contextual tabs.</span></span>
-   <span data-ttu-id="e747a-123">Если одновременно отображается несколько элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) , фон каждой группы вкладок в заголовке окна приложения назначается одному из пяти уникальных цветов.</span><span class="sxs-lookup"><span data-stu-id="e747a-123">When multiple [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at the same time, one of five unique colors is assigned to the background of each Tab Group in the application title bar.</span></span> <span data-ttu-id="e747a-124">Этот цвет также используется в качестве цвета выделения для контекстных вкладок в группе вкладок.</span><span class="sxs-lookup"><span data-stu-id="e747a-124">This color is also used as a highlight color for the contextual tabs in the Tab Group.</span></span>
-   <span data-ttu-id="e747a-125">Назначение цвета [группы вкладок](windowsribbon-controls-tabgroup.md) основано на порядке объявления элементов группы вкладок в разметке.</span><span class="sxs-lookup"><span data-stu-id="e747a-125">The [Tab Group](windowsribbon-controls-tabgroup.md) color assignment is based on the order the Tab Group elements are declared in markup.</span></span> <span data-ttu-id="e747a-126">Цвета определяются платформой и не могут быть заданы приложением.</span><span class="sxs-lookup"><span data-stu-id="e747a-126">The colors are defined by the framework and cannot be specified by the application.</span></span>
-   <span data-ttu-id="e747a-127">Цвета [группы вкладок](windowsribbon-controls-tabgroup.md) , определенные в инфраструктуре, можно изменить непрямо через ключи свойств [платформы](windowsribbon-reference-properties-framework.md) .</span><span class="sxs-lookup"><span data-stu-id="e747a-127">The [Tab Group](windowsribbon-controls-tabgroup.md) colors defined by the framework can be modified indirectly through the [Framework Properties](windowsribbon-reference-properties-framework.md) property keys.</span></span> <span data-ttu-id="e747a-128">Дополнительные сведения см. в разделе [Настройка цветов ленты](ribbon-color.md).</span><span class="sxs-lookup"><span data-stu-id="e747a-128">For more information, see [Customizing Ribbon Colors](ribbon-color.md).</span></span>
-   <span data-ttu-id="e747a-129">Если в любое одиночное время отображается более пяти элементов управления [группы вкладок](windowsribbon-controls-tabgroup.md) , платформа циклически переводит соответствующие цвета.</span><span class="sxs-lookup"><span data-stu-id="e747a-129">When more than five [Tab Group](windowsribbon-controls-tabgroup.md) controls are displayed at any single time, the framework cycles the associated colors.</span></span>
-   <span data-ttu-id="e747a-130">Максимальное число элементов управления ["Вкладка"](windowsribbon-controls-tab.md) на ленте ограничено 100.</span><span class="sxs-lookup"><span data-stu-id="e747a-130">The maximum number of [Tab](windowsribbon-controls-tab.md) controls in a ribbon is limited to 100.</span></span> <span data-ttu-id="e747a-131">К ним относятся контекстные вкладки, видимые или нет.</span><span class="sxs-lookup"><span data-stu-id="e747a-131">This includes contextual tabs, visible or not.</span></span>

<span data-ttu-id="e747a-132">На следующем снимке экрана показана контекстная вкладка из Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="e747a-132">The following screen shot shows a contextual tab from Windows 7 Paint.</span></span>

![снимок экрана, на котором показан контекстный элемент управления вкладки.](images/controls/contextualtab.png)

## <a name="implementing-contextual-tabs"></a><span data-ttu-id="e747a-134">Реализация контекстных вкладок</span><span class="sxs-lookup"><span data-stu-id="e747a-134">Implementing Contextual Tabs</span></span>

<span data-ttu-id="e747a-135">В этом разделе обсуждаются сведения о реализации контекстных вкладок ленты и описывается их внедрение в приложение для ленты.</span><span class="sxs-lookup"><span data-stu-id="e747a-135">This section discusses the implementation details of Ribbon contextual tabs and walks through how to incorporate them in a Ribbon application.</span></span>

### <a name="markup"></a><span data-ttu-id="e747a-136">разметку</span><span class="sxs-lookup"><span data-stu-id="e747a-136">Markup</span></span>

<span data-ttu-id="e747a-137">В следующих примерах демонстрируется базовая разметка для элемента [**табграуп**](windowsribbon-element-tabgroup.md) , который содержит две контекстные вкладки.</span><span class="sxs-lookup"><span data-stu-id="e747a-137">The following examples demonstrate the basic markup for a [**TabGroup**](windowsribbon-element-tabgroup.md) element that contains two contextual tabs.</span></span>

<span data-ttu-id="e747a-138">В этом разделе кода показаны объявления команд [**табграуп**](windowsribbon-element-tabgroup.md) и [Tab](windowsribbon-controls-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="e747a-138">This section of code shows the [**TabGroup**](windowsribbon-element-tabgroup.md) and [Tab](windowsribbon-controls-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="e747a-139">В этом разделе кода показаны объявления элементов управления, необходимые для отображения двух контекстных вкладок в [**табграуп**](windowsribbon-element-tabgroup.md).</span><span class="sxs-lookup"><span data-stu-id="e747a-139">This section of code shows the control declarations required to display two contextual tabs within a [**TabGroup**](windowsribbon-element-tabgroup.md).</span></span>


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



### <a name="code"></a><span data-ttu-id="e747a-140">Код</span><span class="sxs-lookup"><span data-stu-id="e747a-140">Code</span></span>

<span data-ttu-id="e747a-141">[Пользовательский интерфейс \_ PKEY \_ контекставаилабле](windowsribbon-reference-properties-uipkey-contextavailable.md) — это единственный ключ свойства, определенный платформой для указания видимости и состояния контекстных вкладок.</span><span class="sxs-lookup"><span data-stu-id="e747a-141">[UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) is the single property key defined by the framework for specifying the visibility and state of contextual tabs.</span></span> <span data-ttu-id="e747a-142">При выборе объекта в рабочей области приложения этому свойству может быть присвоено одно из трех значений из перечисления [**\_ Контекставаилабилити пользовательского интерфейса**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) , которое определяет, существует ли контекстная вкладка, и, если она есть, отображается ли она как активная вкладка.</span><span class="sxs-lookup"><span data-stu-id="e747a-142">When an object is selected in the application workspace, this property can be assigned one of three values from the [**UI\_CONTEXTAVAILABILITY**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_contextavailability) enumeration that define whether a contextual tab exists and, if it does, whether it is shown as the active tab.</span></span>

<span data-ttu-id="e747a-143">Приложение запрашивает обновление [группы вкладок](windowsribbon-controls-tabgroup.md) путем непроверки и обновления свойства [контекставаилабле UI \_ PKEY \_ ](windowsribbon-reference-properties-uipkey-contextavailable.md) при изменении контекста рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e747a-143">An application requests a [Tab Group](windowsribbon-controls-tabgroup.md) update by invalidating and updating the [UI\_PKEY\_ContextAvailable](windowsribbon-reference-properties-uipkey-contextavailable.md) property when the workspace context changes.</span></span>

<span data-ttu-id="e747a-144">В следующих разделах кода показано, как отобразить контекстную вкладку при выборе изображения в рабочей области приложения.</span><span class="sxs-lookup"><span data-stu-id="e747a-144">The follow sections of code demonstrate how to display a contextual tab when an image is selected in an application workspace.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e747a-145">См. также</span><span class="sxs-lookup"><span data-stu-id="e747a-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e747a-146">Рекомендации по работе пользователя с лентой</span><span class="sxs-lookup"><span data-stu-id="e747a-146">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="e747a-147">Процесс разработки ленты</span><span class="sxs-lookup"><span data-stu-id="e747a-147">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 