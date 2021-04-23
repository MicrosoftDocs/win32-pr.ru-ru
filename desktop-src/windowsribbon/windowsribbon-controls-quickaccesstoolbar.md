---
title: Панель быстрого доступа
description: Панель быстрого доступа (QAT) — это небольшая настраиваемая панель инструментов, предоставляющая набор команд, которые задаются приложением или выбираются пользователем.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a50d562477e5c626d2d2bffa8ee5e0ecc84919
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070021"
---
# <a name="quick-access-toolbar"></a><span data-ttu-id="c82d1-103">Панель быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="c82d1-103">Quick Access Toolbar</span></span>

<span data-ttu-id="c82d1-104">Панель быстрого доступа (QAT) — это небольшая настраиваемая панель инструментов, предоставляющая набор команд, которые задаются приложением или выбираются пользователем.</span><span class="sxs-lookup"><span data-stu-id="c82d1-104">The Quick Access Toolbar (QAT) is a small, customizable toolbar that exposes a set of Commands that are specified by the application or selected by the user.</span></span>

- [<span data-ttu-id="c82d1-105">Введение</span><span class="sxs-lookup"><span data-stu-id="c82d1-105">Introduction</span></span>](#introduction)
- [<span data-ttu-id="c82d1-106">Реализация панели быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="c82d1-106">Implement the Quick Access Toolbar</span></span>](#implement-the-quick-access-toolbar)
  - [<span data-ttu-id="c82d1-107">разметку</span><span class="sxs-lookup"><span data-stu-id="c82d1-107">Markup</span></span>](#markup)
  - [<span data-ttu-id="c82d1-108">Код</span><span class="sxs-lookup"><span data-stu-id="c82d1-108">Code</span></span>](#code)
- [<span data-ttu-id="c82d1-109">Сохраняемость QAT</span><span class="sxs-lookup"><span data-stu-id="c82d1-109">QAT Persistence</span></span>](#qat-persistence)
- [<span data-ttu-id="c82d1-110">Свойства панели быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="c82d1-110">Quick Access Toolbar Properties</span></span>](#quick-access-toolbar-properties)
- [<span data-ttu-id="c82d1-111">См. также</span><span class="sxs-lookup"><span data-stu-id="c82d1-111">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="c82d1-112">Введение</span><span class="sxs-lookup"><span data-stu-id="c82d1-112">Introduction</span></span>

<span data-ttu-id="c82d1-113">По умолчанию панель быстрого доступа (QAT) находится в заголовке окна приложения, но ее можно настроить для показа под лентой.</span><span class="sxs-lookup"><span data-stu-id="c82d1-113">By default, the Quick Access Toolbar (QAT) is located in the title bar of the application window but can be configured to display below the ribbon.</span></span> <span data-ttu-id="c82d1-114">Помимо предоставления команд, панель быстрого доступа (QAT) также включает в себя настраиваемое раскрывающееся меню, содержащее полный набор команд панели быстрого доступа по умолчанию (QAT) (скрытый или отображаемый на панели быстрого доступа (QAT)) и набор параметров панели быстрого доступа (QAT) и ленты.</span><span class="sxs-lookup"><span data-stu-id="c82d1-114">In addition to exposing Commands, the Quick Access Toolbar (QAT) also includes a customizable drop-down menu that contains the complete set of default Quick Access Toolbar (QAT) Commands (whether hidden or displayed in the Quick Access Toolbar (QAT)) and a set of Quick Access Toolbar (QAT) and ribbon options.</span></span>

<span data-ttu-id="c82d1-115">На следующем снимке экрана показан пример панели быстрого доступа к ленте (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-115">The following screen shot shows an example of the Ribbon Quick Access Toolbar (QAT).</span></span>

![снимок экрана QAT на ленте Microsoft Paint.](images/markup/qat-and-menu.png)

<span data-ttu-id="c82d1-117">Панель быстрого доступа (QAT) состоит из комбинации до 20 команд, заданных приложением (список по умолчанию для приложений) или выбранных пользователем.</span><span class="sxs-lookup"><span data-stu-id="c82d1-117">The Quick Access Toolbar (QAT) consists of a combination of up to 20 Commands either specified by the application (known as the application defaults list) or selected by the user.</span></span> <span data-ttu-id="c82d1-118">Панель быстрого доступа (QAT) может содержать уникальные команды, недоступные в других местах в пользовательском интерфейсе ленты.</span><span class="sxs-lookup"><span data-stu-id="c82d1-118">The Quick Access Toolbar (QAT) can contain unique Commands that are not available elsewhere in the ribbon UI.</span></span>

> [!Note]
> <span data-ttu-id="c82d1-119">Хотя почти все элементы управления ленты позволяют добавлять связанную команду на панель быстрого доступа (QAT) через контекстное меню, показанное на следующем снимке экрана, команды, представленные в [контекстном всплывающем](windowsribbon-controls-contextpopup.md) окне, не предоставляют этого контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="c82d1-119">While almost all ribbon controls allow their associated Command to be added to the Quick Access Toolbar (QAT) through the context menu shown in the following screen shot, Commands exposed in a [Context Popup](windowsribbon-controls-contextpopup.md) do not provide this context menu.</span></span>
>
> ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a><span data-ttu-id="c82d1-121">Реализация панели быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="c82d1-121">Implement the Quick Access Toolbar</span></span>

<span data-ttu-id="c82d1-122">Как и в случае со всеми элементами управления Windows Ribbon Framework, для полного использования панели быстрого доступа (QAT) требуется компонент разметки, который управляет его представлением на ленте, и компонентом кода, который управляет его функциональными возможностями.</span><span class="sxs-lookup"><span data-stu-id="c82d1-122">As with all Windows Ribbon framework controls, taking full advantage of the Quick Access Toolbar (QAT) requires both a markup component that controls its presentation within the ribbon and a code component that governs its functionality.</span></span>

### <a name="markup"></a><span data-ttu-id="c82d1-123">разметку</span><span class="sxs-lookup"><span data-stu-id="c82d1-123">Markup</span></span>

<span data-ttu-id="c82d1-124">Элемент управления панели быстрого доступа (QAT) объявляется и связывается с ИДЕНТИФИКАТОРом команды в разметке с помощью элемента [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-124">The Quick Access Toolbar (QAT) control is declared, and associated with a Command ID, in markup through the [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span> <span data-ttu-id="c82d1-125">Идентификатор команды используется для идентификации и привязки панели быстрого доступа (QAT) к обработчику команд, определенному приложением.</span><span class="sxs-lookup"><span data-stu-id="c82d1-125">The Command ID is used to identify and bind the Quick Access Toolbar (QAT) to a Command handler defined by the application.</span></span>

<span data-ttu-id="c82d1-126">В дополнение к базовому обработчику команд для основной панели быстрого доступа (QAT), объявление необязательного атрибута элемента *кустомизекомманднаме* [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) приводит к тому, что платформа добавляет в список команд раскрывающегося меню панели быстрого доступа (QAT) элемент **больше команд** , требующий определения дополнительного обработчика команд.</span><span class="sxs-lookup"><span data-stu-id="c82d1-126">In addition to the basic Command handler for primary Quick Access Toolbar (QAT) functionality, declaring the optional *CustomizeCommandName* [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element attribute causes the framework to add a **More Commands** item to the Command list of the Quick Access Toolbar (QAT) drop-down menu that requires a secondary Command handler be defined.</span></span>

<span data-ttu-id="c82d1-127">Для согласованности в приложениях ленты рекомендуется запустить обработчик команд *кустомизекомманднаме* в диалоговом окне настройки панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-127">For consistency across Ribbon applications, it is recommended that the *CustomizeCommandName* Command handler launch a Quick Access Toolbar (QAT) customization dialog.</span></span> <span data-ttu-id="c82d1-128">Поскольку платформа Ribbon предоставляет только точку запуска в пользовательском интерфейсе, приложение несет исключительно ответственность за предоставление реализации диалогового окна настройки при получении уведомления о обратном вызове для этой команды.</span><span class="sxs-lookup"><span data-stu-id="c82d1-128">Because the Ribbon framework only provides the launching point in the UI, the application is solely responsible for providing the customization dialog implementation when the callback notification for this Command is received.</span></span>

<span data-ttu-id="c82d1-129">На следующем снимке экрана показано раскрывающееся меню панели быстрого доступа (QAT) с элементом команды " **другие команды** ".</span><span class="sxs-lookup"><span data-stu-id="c82d1-129">The following screen shot shows a Quick Access Toolbar (QAT) drop-down menu with the **More Commands** Command item.</span></span>

![снимок экрана: меню QAT с командами "Дополнительно"... элемент команды.](images/markup/qat-customizecommandname.png)

<span data-ttu-id="c82d1-131">Список по умолчанию для панели быстрого доступа (QAT) задается с помощью свойства [куиккакцесстулбар. аппликатиондефаултс](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , которое определяет список рекомендуемых команд по умолчанию, которые перечислены в раскрывающемся меню панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-131">The application defaults list for the Quick Access Toolbar (QAT) is specified through the [QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) property which identifies a default list of recommended Commands, all of which are listed in the Quick Access Toolbar (QAT) drop-down menu.</span></span>

<span data-ttu-id="c82d1-132">Чтобы отобразить команды из списка значений по умолчанию для приложений на панели инструментов панели быстрого доступа (QAT), атрибут *аппликатиондефаултс.* InAttribute каждого элемента управления должен иметь значение `true` .</span><span class="sxs-lookup"><span data-stu-id="c82d1-132">To display Commands from the application defaults list in the Quick Access Toolbar (QAT) toolbar, the *ApplicationDefaults.IsChecked* attribute of each control element must have a value of `true`.</span></span> <span data-ttu-id="c82d1-133">На приведенных выше изображениях показаны результаты установки этого атрибута в `true` для команд **сохранить**, **отменить** и **повторить** .</span><span class="sxs-lookup"><span data-stu-id="c82d1-133">The preceding images show the results of setting this attribute to `true` for the **Save**, **Undo**, and **Redo** Commands.</span></span>

<span data-ttu-id="c82d1-134">[Куиккакцесстулбар. аппликатиондефаултс](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) поддерживает три типа элементов управления ленты: [кнопка](windowsribbon-controls-button.md), [выключатель](windowsribbon-controls-togglebutton.md)и [флажок](windowsribbon-controls-checkbox.md).</span><span class="sxs-lookup"><span data-stu-id="c82d1-134">[QuickAccessToolbar.ApplicationDefaults](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) supports three types of Ribbon controls: [Button](windowsribbon-controls-button.md), [Toggle Button](windowsribbon-controls-togglebutton.md), and [Check Box](windowsribbon-controls-checkbox.md).</span></span>

> [!Note]
> <span data-ttu-id="c82d1-135">Windows 8 и более поздние версии: поддерживаются все элементы управления на основе галереи ([ComboBox](windowsribbon-element-combobox.md), [инриббонгаллери](windowsribbon-element-inribbongallery.md), [сплитбуттонгаллери](windowsribbon-element-splitbuttongallery.md)и [дропдовнгаллери](windowsribbon-element-dropdowngallery.md)).</span><span class="sxs-lookup"><span data-stu-id="c82d1-135">Windows 8 and newer: All gallery-based controls are supported ([ComboBox](windowsribbon-element-combobox.md), [InRibbonGallery](windowsribbon-element-inribbongallery.md), [SplitButtonGallery](windowsribbon-element-splitbuttongallery.md), and [DropDownGallery](windowsribbon-element-dropdowngallery.md)).</span></span>
>
> <span data-ttu-id="c82d1-136">Элементы в элементе управления "Коллекция" могут поддерживать выделение при наведении указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="c82d1-136">Items in a gallery control can support highlighting on hover.</span></span> <span data-ttu-id="c82d1-137">Чтобы обеспечить поддержку выделения при наведении, коллекция должна быть коллекцией элементов и использовать [фловменулайаут](windowsribbon-element-flowmenulayout.md) типа [вертикалменулайаут](windowsribbon-element-verticalmenulayout.md).</span><span class="sxs-lookup"><span data-stu-id="c82d1-137">To support hover highlighting, the gallery must be an items gallery and use a [FlowMenuLayout](windowsribbon-element-flowmenulayout.md) of type [VerticalMenuLayout](windowsribbon-element-verticalmenulayout.md).</span></span>

<span data-ttu-id="c82d1-138">В следующем примере показана базовая разметка для элемента [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-138">The following example demonstrates the basic markup for a [QuickAccessToolbar](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

<span data-ttu-id="c82d1-139">В этом разделе кода показаны объявления команд для элемента [панели быстрого доступа (QAT)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-139">This section of code shows the Command declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

<span data-ttu-id="c82d1-140">В этом разделе кода показаны объявления элементов управления для элемента [панели быстрого доступа (QAT)](windowsribbon-element-quickaccesstoolbar.md) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-140">This section of code shows the control declarations for a [Quick Access Toolbar (QAT)](windowsribbon-element-quickaccesstoolbar.md) element.</span></span>

```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```

### <a name="code"></a><span data-ttu-id="c82d1-141">Код</span><span class="sxs-lookup"><span data-stu-id="c82d1-141">Code</span></span>

<span data-ttu-id="c82d1-142">Приложение платформы Ribbon должно предоставлять метод обратного вызова обработчика команд для управления панелью быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-142">The Ribbon framework application must provide a Command handler callback method to manipulate the Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="c82d1-143">Этот обработчик работает аналогичным образом обработчикам коллекции команд, за исключением того, что панель быстрого доступа (QAT) не поддерживает категории.</span><span class="sxs-lookup"><span data-stu-id="c82d1-143">This handler works in a similar fashion to Command gallery handlers, except that the Quick Access Toolbar (QAT) does not support categories.</span></span> <span data-ttu-id="c82d1-144">Дополнительные сведения см. в разделе [Работа с галереями](ribbon-controls-galleries.md).</span><span class="sxs-lookup"><span data-stu-id="c82d1-144">For more information, see [Working with Galleries](ribbon-controls-galleries.md).</span></span>

<span data-ttu-id="c82d1-145">Коллекция команд панели быстрого доступа (QAT) извлекается как объект [иуиколлектион](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) через ключ свойства [ \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-145">The Quick Access Toolbar (QAT) Command collection is retrieved as an [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) object through the [UI\_PKEY\_ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) property key.</span></span> <span data-ttu-id="c82d1-146">Добавление команд на панель быстрого доступа (QAT) во время выполнения достигается путем добавления объекта [иуисимплепропертисет](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) в **иуиколлектион**.</span><span class="sxs-lookup"><span data-stu-id="c82d1-146">Adding Commands to the Quick Access Toolbar (QAT) at run time is accomplished by adding an [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object to the **IUICollection**.</span></span>

<span data-ttu-id="c82d1-147">В отличие от коллекций команд, свойство типа команды ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) не требуется для объекта [ИУИСИМПЛЕПРОПЕРТИСЕТ](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-147">Unlike Command galleries, a command type property ([UI\_PKEY\_CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) is not required for the Quick Access Toolbar (QAT) [IUISimplePropertySet](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object.</span></span> <span data-ttu-id="c82d1-148">Однако команда должна существовать на ленте или панели быстрого доступа (QAT) список значений по умолчанию для приложений. новую команду нельзя создать во время выполнения и добавить на панель быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-148">However, the Command must exist in the ribbon or Quick Access Toolbar (QAT) application defaults list; a new Command cannot be created at run time and added to the Quick Access Toolbar (QAT).</span></span>

> [!Note]  
> <span data-ttu-id="c82d1-149">Приложение ленты не может заменить панель быстрого доступа (QAT) [иуиколлектион](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) на пользовательский объект коллекции, производный от иенумункновн.</span><span class="sxs-lookup"><span data-stu-id="c82d1-149">The Ribbon application cannot replace the Quick Access Toolbar (QAT) [IUICollection](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) with a custom collection object derived from IEnumUnknown.</span></span>

<span data-ttu-id="c82d1-150">В следующем примере показана базовая реализация обработчика команд панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-150">The following example demonstrates a basic Quick Access Toolbar (QAT) Command handler implementation.</span></span>

```C++
/* QAT COMMAND HANDLER IMPLEMENTATION */
class CQATCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
  public:
    BEGIN_COM_MAP(CQATCommandHandler)
      COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    // QAT command handler's Execute method
    STDMETHODIMP Execute(UINT nCmdID,
                         UI_EXECUTIONVERB verb, 
                         const PROPERTYKEY* key,
                         const PROPVARIANT* ppropvarValue,
                         IUISimplePropertySet* pCommandExecutionProperties)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(verb);
      UNREFERENCED_PARAMETER(ppropvarValue);
      UNREFERENCED_PARAMETER(pCommandExecutionProperties);

      // Do not expect Execute callback for a QAT command
      return E_NOTIMPL;
    }

    // QAT command handler's UpdateProperty method
    STDMETHODIMP UpdateProperty(UINT nCmdID,
                                REFPROPERTYKEY key,
                                const PROPVARIANT* ppropvarCurrentValue,
                                PROPVARIANT* ppropvarNewValue)
    {
      UNREFERENCED_PARAMETER(nCmdID);
      UNREFERENCED_PARAMETER(ppropvarNewValue);

      HRESULT hr = E_NOTIMPL;

      if (key == UI_PKEY_ItemsSource)
      {
        ATLASSERT(ppropvarCurrentValue->vt == VT_UNKNOWN);

        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        UINT nCount;
        if (SUCCEEDED(hr = spCollection->GetCount(&nCount)))
        {
          if (nCount == 0)
          {
            // If the current Qat list is empty, then we will add a few items here.
            UINT commands[] =  { cmdSave, cmdUndo};

            int count = _countof(commands);

            for (int i = 0; i < count; i++)
            {
              PROPERTYKEY keys[1] = {UI_PKEY_CommandId};
              CComObject<CItemProperties> *pItem = NULL;
              if (SUCCEEDED(CComObject<CItemProperties>::CreateInstance(&pItem)))
              {
                PROPVARIANT vars[1];

                InitPropVariantFromUInt32(commands[i], &vars[0]);

                pItem->Initialize(NULL, _countof(vars), keys, vars);

                CComPtr<IUnknown> spUnknown;
                pItem->QueryInterface(&spUnknown);
                spCollection->Add(spUnknown);
                            
                FreePropVariantArray(_countof(vars), vars);
              }
            }
          }
          else
          {
            // Do nothing if the Qat list is not empty.
            // Return S_FALSE to indicate the callback succeeded.
            return S_FALSE; 
          }
        }
      }
    return hr;
  }
};
```

## <a name="qat-persistence"></a><span data-ttu-id="c82d1-151">Сохраняемость QAT</span><span class="sxs-lookup"><span data-stu-id="c82d1-151">QAT Persistence</span></span>

<span data-ttu-id="c82d1-152">Элементы и параметры команды панели быстрого доступа (QAT) можно сохранять в сеансах приложения с помощью функций [иуириббон:: савесеттингстостреам](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) и [Иуириббон:: лоадсеттингсфромстреам](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-152">Quick Access Toolbar (QAT) Command items and settings can be persisted across application sessions using the [IUIRibbon::SaveSettingsToStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) and [IUIRibbon::LoadSettingsFromStream](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) functions.</span></span> <span data-ttu-id="c82d1-153">Дополнительные сведения см. в разделе [Сохранение состояния ленты](ribbon-statepersistence.md).</span><span class="sxs-lookup"><span data-stu-id="c82d1-153">For more information, see [Persisting Ribbon State](ribbon-statepersistence.md).</span></span>

## <a name="quick-access-toolbar-properties"></a><span data-ttu-id="c82d1-154">Свойства панели быстрого доступа</span><span class="sxs-lookup"><span data-stu-id="c82d1-154">Quick Access Toolbar Properties</span></span>

<span data-ttu-id="c82d1-155">Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-155">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Quick Access Toolbar (QAT) control.</span></span>

<span data-ttu-id="c82d1-156">Как правило, свойство панели быстрого доступа (QAT) обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [иуифрамеворк:: инвалидатеуикомманд](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-156">Typically, a Quick Access Toolbar (QAT) property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [IUIFramework::InvalidateUICommand](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c82d1-157">Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [иуикоммандхандлер:: упдатепроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-157">The invalidation event is handled, and the property updates defined, by the [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c82d1-158">Метод обратного вызова [иуикоммандхандлер:: упдатепроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы.</span><span class="sxs-lookup"><span data-stu-id="c82d1-158">The [IUICommandHandler::UpdateProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c82d1-159">Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.</span><span class="sxs-lookup"><span data-stu-id="c82d1-159">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c82d1-160">В некоторых случаях свойство можно получить с помощью метода [иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [Иуифрамеворк:: сетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="c82d1-160">In some cases, a property can be retrieved through the [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

<span data-ttu-id="c82d1-161">В следующей таблице перечислены ключи свойств, связанные с элементом управления панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="c82d1-161">The following table lists the property keys that are associated with the Quick Access Toolbar (QAT) control.</span></span>

| <span data-ttu-id="c82d1-162">Ключ свойства</span><span class="sxs-lookup"><span data-stu-id="c82d1-162">Property Key</span></span> | <span data-ttu-id="c82d1-163">Примечания</span><span class="sxs-lookup"><span data-stu-id="c82d1-163">Notes</span></span> |
|---|---|
| [<span data-ttu-id="c82d1-164">ItemsSource пользовательского интерфейса \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="c82d1-164">UI\_PKEY\_ItemsSource</span></span>](windowsribbon-reference-properties-uipkey-itemssource.md) | <span data-ttu-id="c82d1-165">Поддерживает [иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (не поддерживает [Иуифрамеворк:: сетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [Иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) возвращает указатель на объект иуиколлектион, представляющий команды в QAT.</span><span class="sxs-lookup"><span data-stu-id="c82d1-165">Supports [IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (does not support [IUIFramework::SetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)).[IUIFramework::GetUICommandProperty](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) returns a pointer to an IUICollection object that represents the commands in the QAT.</span></span> <span data-ttu-id="c82d1-166">Каждая команда определяется по ИДЕНТИФИКАТОРу команды, который получается путем вызова метода [иуисимплепропертисет:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) и передачи ключа свойства [ \_ PKEY \_ CommandId UI](windowsribbon-reference-properties-uipkey-commandid.md).</span><span class="sxs-lookup"><span data-stu-id="c82d1-166">Each Command is identified by its Command ID, which is obtained by calling the [IUISimplePropertySet::GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method and passing in the property key [UI\_PKEY\_CommandId](windowsribbon-reference-properties-uipkey-commandid.md).</span></span> |

<span data-ttu-id="c82d1-167">Нет ключей свойств, связанных с элементом команды " **другие команды** " в раскрывающемся меню панели быстрого доступа (QAT)</span><span class="sxs-lookup"><span data-stu-id="c82d1-167">There are no property keys associated with the **More Commands** Command item of the Quick Access Toolbar (QAT) drop-down menu</span></span>

## <a name="related-topics"></a><span data-ttu-id="c82d1-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c82d1-168">Related topics</span></span>

- [<span data-ttu-id="c82d1-169">Библиотека элементов управления платформы Windows ленты</span><span class="sxs-lookup"><span data-stu-id="c82d1-169">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
- [<span data-ttu-id="c82d1-170">Куиккакцесстулбар, элемент разметки</span><span class="sxs-lookup"><span data-stu-id="c82d1-170">QuickAccessToolbar markup element</span></span>](windowsribbon-element-quickaccesstoolbar.md)