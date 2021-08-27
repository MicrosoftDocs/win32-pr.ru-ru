---
title: Панель быстрого доступа
description: Панель быстрого доступа (QAT) — это небольшая настраиваемая панель инструментов, предоставляющая набор команд, которые задаются приложением или выбираются пользователем.
ms.assetid: b2adf4e9-0de1-4c4d-9293-693d0f7cf6fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d63eb3f7b1a2c1213430f86a9a12fe4517c738290ed736eb1d356420aa145cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110733"
---
# <a name="quick-access-toolbar"></a>Панель быстрого доступа

Панель быстрого доступа (QAT) — это небольшая настраиваемая панель инструментов, предоставляющая набор команд, которые задаются приложением или выбираются пользователем.

- [Введение](#introduction)
- [Реализация панели быстрого доступа](#implement-the-quick-access-toolbar)
  - [разметку](#markup)
  - [Код](#code)
- [Сохраняемость QAT](#qat-persistence)
- [Свойства панели быстрого доступа](#quick-access-toolbar-properties)
- [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

По умолчанию панель быстрого доступа (QAT) находится в заголовке окна приложения, но ее можно настроить для показа под лентой. Помимо предоставления команд, панель быстрого доступа (QAT) также включает в себя настраиваемое раскрывающееся меню, содержащее полный набор команд панели быстрого доступа по умолчанию (QAT) (скрытый или отображаемый на панели быстрого доступа (QAT)) и набор параметров панели быстрого доступа (QAT) и ленты.

На следующем снимке экрана показан пример панели быстрого доступа к ленте (QAT).

![снимок экрана QAT на ленте Microsoft Paint.](images/markup/qat-and-menu.png)

Панель быстрого доступа (QAT) состоит из комбинации до 20 команд, заданных приложением (список по умолчанию для приложений) или выбранных пользователем. Панель быстрого доступа (QAT) может содержать уникальные команды, недоступные в других местах в пользовательском интерфейсе ленты.

> [!Note]
> Хотя почти все элементы управления ленты позволяют добавлять связанную команду на панель быстрого доступа (QAT) через контекстное меню, показанное на следующем снимке экрана, команды, представленные в [контекстном всплывающем](windowsribbon-controls-contextpopup.md) окне, не предоставляют этого контекстного меню.
>
> ![снимок экрана: контекстное меню команды на ленте Microsoft Paint.](images/controls/qat-contextmenu-add.png) 

## <a name="implement-the-quick-access-toolbar"></a>Реализация панели быстрого доступа

как и для всех Windows элементов управления платформой ленты, для полного использования преимуществ панели быстрого доступа (QAT) требуется компонент разметки, который управляет его представлением на ленте, и компонентом кода, который управляет его функциональными возможностями.

### <a name="markup"></a>разметку

Элемент управления панели быстрого доступа (QAT) объявляется и связывается с ИДЕНТИФИКАТОРом команды в разметке с помощью элемента [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) . Идентификатор команды используется для идентификации и привязки панели быстрого доступа (QAT) к обработчику команд, определенному приложением.

В дополнение к базовому обработчику команд для основной панели быстрого доступа (QAT), объявление необязательного атрибута элемента *кустомизекомманднаме* [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) приводит к тому, что платформа добавляет в список команд раскрывающегося меню панели быстрого доступа (QAT) элемент **больше команд** , требующий определения дополнительного обработчика команд.

Для согласованности в приложениях ленты рекомендуется запустить обработчик команд *кустомизекомманднаме* в диалоговом окне настройки панели быстрого доступа (QAT). Поскольку платформа Ribbon предоставляет только точку запуска в пользовательском интерфейсе, приложение несет исключительно ответственность за предоставление реализации диалогового окна настройки при получении уведомления о обратном вызове для этой команды.

На следующем снимке экрана показано раскрывающееся меню панели быстрого доступа (QAT) с элементом команды " **другие команды** ".

![снимок экрана: меню QAT с командами "Дополнительно"... элемент команды.](images/markup/qat-customizecommandname.png)

Список по умолчанию для панели быстрого доступа (QAT) задается с помощью свойства [куиккакцесстулбар. аппликатиондефаултс](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) , которое определяет список рекомендуемых команд по умолчанию, которые перечислены в раскрывающемся меню панели быстрого доступа (QAT).

Чтобы отобразить команды из списка значений по умолчанию для приложений на панели инструментов панели быстрого доступа (QAT), атрибут *аппликатиондефаултс.* InAttribute каждого элемента управления должен иметь значение `true` . На приведенных выше изображениях показаны результаты установки этого атрибута в `true` для команд **сохранить**, **отменить** и **повторить** .

[Куиккакцесстулбар. аппликатиондефаултс](windowsribbon-element-quickaccesstoolbar-applicationdefaults.md) поддерживает три типа элементов управления ленты: [кнопка](windowsribbon-controls-button.md), [выключатель](windowsribbon-controls-togglebutton.md)и [флажок](windowsribbon-controls-checkbox.md).

> [!Note]
> Windows 8 и более поздних версий: поддерживаются все элементы управления на основе галереи ([ComboBox](windowsribbon-element-combobox.md), [инриббонгаллери](windowsribbon-element-inribbongallery.md), [сплитбуттонгаллери](windowsribbon-element-splitbuttongallery.md)и [дропдовнгаллери](windowsribbon-element-dropdowngallery.md)).
>
> Элементы в элементе управления "Коллекция" могут поддерживать выделение при наведении указателя мыши. Чтобы обеспечить поддержку выделения при наведении, коллекция должна быть коллекцией элементов и использовать [фловменулайаут](windowsribbon-element-flowmenulayout.md) типа [вертикалменулайаут](windowsribbon-element-verticalmenulayout.md).

В следующем примере показана базовая разметка для элемента [куиккакцесстулбар](windowsribbon-element-quickaccesstoolbar.md) .

В этом разделе кода показаны объявления команд для элемента [панели быстрого доступа (QAT)](windowsribbon-element-quickaccesstoolbar.md) .

```XML
<Command Name="cmdQAT"
         Symbol="ID_QAT"
         Id="40000"/>
<Command Name="cmdCustomizeQAT"
         Symbol="ID_CUSTOM_QAT"
         Id="40001"/>
```

В этом разделе кода показаны объявления элементов управления для элемента [панели быстрого доступа (QAT)](windowsribbon-element-quickaccesstoolbar.md) .

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

### <a name="code"></a>Код

Приложение платформы Ribbon должно предоставлять метод обратного вызова обработчика команд для управления панелью быстрого доступа (QAT). Этот обработчик работает аналогичным образом обработчикам коллекции команд, за исключением того, что панель быстрого доступа (QAT) не поддерживает категории. Дополнительные сведения см. в разделе [Работа с галереями](ribbon-controls-galleries.md).

Коллекция команд панели быстрого доступа (QAT) извлекается как объект [иуиколлектион](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) через ключ свойства [ \_ \_ ItemsSource пользовательского интерфейса PKEY](windowsribbon-reference-properties-uipkey-itemssource.md) . Добавление команд на панель быстрого доступа (QAT) во время выполнения достигается путем добавления объекта [иуисимплепропертисет](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) в **иуиколлектион**.

В отличие от коллекций команд, свойство типа команды ([UI \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md)) не требуется для объекта [ИУИСИМПЛЕПРОПЕРТИСЕТ](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) панели быстрого доступа (QAT). Однако команда должна существовать на ленте или панели быстрого доступа (QAT) список значений по умолчанию для приложений. новую команду нельзя создать во время выполнения и добавить на панель быстрого доступа (QAT).

> [!Note]  
> Приложение ленты не может заменить панель быстрого доступа (QAT) [иуиколлектион](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) на пользовательский объект коллекции, производный от иенумункновн.

В следующем примере показана базовая реализация обработчика команд панели быстрого доступа (QAT).

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

## <a name="qat-persistence"></a>Сохраняемость QAT

Элементы и параметры команды панели быстрого доступа (QAT) можно сохранять в сеансах приложения с помощью функций [иуириббон:: савесеттингстостреам](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-savesettingstostream) и [Иуириббон:: лоадсеттингсфромстреам](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-loadsettingsfromstream) . Дополнительные сведения см. в разделе [Сохранение состояния ленты](ribbon-statepersistence.md).

## <a name="quick-access-toolbar-properties"></a>Свойства панели быстрого доступа

Платформа ленты определяет коллекцию [ключей свойств](windowsribbon-reference-properties.md) для элемента управления панели быстрого доступа (QAT).

Как правило, свойство панели быстрого доступа (QAT) обновляется в пользовательском интерфейсе ленты путем непроверки команды, связанной с элементом управления, посредством вызова метода [иуифрамеворк:: инвалидатеуикомманд](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . Событие "недействительность" обрабатывается и задается обновлением свойства с помощью метода обратного вызова [иуикоммандхандлер:: упдатепроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

Метод обратного вызова [иуикоммандхандлер:: упдатепроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) не выполняется и приложение запрашивает обновленное значение свойства до тех пор, пока свойство не будет обязательно для платформы. Например, при активации вкладки и элементе управления, отображенном в ленте, или при отображении подсказки.

> [!Note]  
> В некоторых случаях свойство можно получить с помощью метода [иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) и задать с помощью метода [Иуифрамеворк:: сетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

В следующей таблице перечислены ключи свойств, связанные с элементом управления панели быстрого доступа (QAT).

| Ключ свойства | Примечания |
|---|---|
| [ItemsSource пользовательского интерфейса \_ PKEY \_](windowsribbon-reference-properties-uipkey-itemssource.md) | Поддерживает [иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) (не поддерживает [Иуифрамеворк:: сетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty)). [Иуифрамеворк:: жетуикоммандпроперти](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) возвращает указатель на объект иуиколлектион, представляющий команды в QAT. Каждая команда определяется по ИДЕНТИФИКАТОРу команды, который получается путем вызова метода [иуисимплепропертисет:: GetValue](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) и передачи ключа свойства [ \_ PKEY \_ CommandId UI](windowsribbon-reference-properties-uipkey-commandid.md). |

Нет ключей свойств, связанных с элементом команды " **другие команды** " в раскрывающемся меню панели быстрого доступа (QAT)

## <a name="related-topics"></a>Связанные темы

- [Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
- [Куиккакцесстулбар, элемент разметки](windowsribbon-element-quickaccesstoolbar.md)