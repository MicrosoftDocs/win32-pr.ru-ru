---
title: переход на платформу ленты Windows
description: приложение, основанное на традиционных меню, панелях инструментов и диалоговых окнах, может быть перенесено в многофункциональный, динамический и контекстно-ориентированный пользовательский интерфейс в системе командной строки платформы Windows Ribbon.
ms.assetid: 3a8ca41e-18b3-4c9d-865b-5f4c5fcf7ceb
keywords:
- Windows Лента, миграция в
- Лента, миграция в
- переход на Windows ленту
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a011e9b5dad52f6f71fab272f0fded39ec59eb71cc7311ab9cf5ffccb4dfbca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841124"
---
# <a name="migrating-to-the-windows-ribbon-framework"></a>переход на платформу ленты Windows

приложение, основанное на традиционных меню, панелях инструментов и диалоговых окнах, может быть перенесено в многофункциональный, динамический и контекстно-ориентированный пользовательский интерфейс в системе командной строки платформы Windows Ribbon. Это простой и эффективный способ модернизировать и ревитализе приложение, одновременно улучшая доступность, удобство использования и возможность обнаружения его функциональных возможностей.

## <a name="introduction"></a>Введение

Как правило, перенос существующего приложения на платформу Ribbon включает в себя следующее:

-   Разработка макета ленты и управления организацией, которая предоставляет функциональные возможности существующего приложения и является достаточно гибкой для поддержки новых функциональных возможностей.
-   Адаптация кода существующего приложения.
-   Перенос существующих ресурсов приложения (строк и изображений) в платформу ленты.

> [!Note]  
> Чтобы определить, является ли приложение подходящим кандидатом для ленты, необходимо проверить [рекомендации по работе пользователя с лентой](https://msdn.microsoft.com/library/cc872782.aspx) .

 

## <a name="design-the-ribbon-layout"></a>Создание макета ленты

Потенциальные разработки ленты и макеты элементов управления можно определить, выполнив следующие действия.

1.  Инвентаризация всех существующих функций.
2.  Преобразование этой функции в команды ленты.
3.  Упорядочение команд в логические группы.

### <a name="take-inventory"></a>Взять инвентаризацию

В платформе Ribbon функциональные возможности, предоставляемые приложением, которое управляет состоянием или представлением рабочей области или документа, рассматриваются как команда. Состав команды может различаться и зависит от природы и домена существующего приложения.

В следующей таблице приведен набор основных команд для гипотетического приложения для редактирования текста:



| Символ           | ID     | Описание               |
|------------------|--------|---------------------------|
| \_файл идентификатора \_ New    | 0xE100 | Новый документ              |
| файл идентификатора — \_ \_ Сохранение   | 0xE103 | Сохранить документ             |
| \_файл идентификатора \_ SAVEAS | 0xE104 | Сохранить как... Откроется       |
| \_файл идентификатора \_ открыт   | 0xE101 | Открыть... Откроется          |
| \_ \_ выход из файла идентификатора   | 0xE102 | Выход из приложения      |
| \_Отмена изменения \_ идентификатора   | 0xE12B | Отменить                      |
| \_Изменение идентификатора \_ Вырезать    | 0xE123 | Вырезать выделенный текст         |
| Идентификатор \_ изменения \_ копии   | 0xE122 | Копировать выделенный текст        |
| изменение кода при \_ \_ вставке  | 0xE125 | Вставить текст из буфера обмена |
| ID \_ Правка \_ очистить  | 0xE120 | Удалить выделенный текст      |
| \_масштаб представления \_ идентификатора   | 1242   | Масштаб... Откроется          |



 

При создании инвентаризации команд Изучите существующие меню и панели инструментов. Рассмотрим все способы взаимодействия пользователя с рабочей областью. Хотя не каждая команда подходит для включения на ленту, это упражнение может очень хорошо представлять команды, которые ранее были скрыты слоями пользовательского интерфейса.

### <a name="translate"></a>Перевод

Не все команды должны быть представлены в пользовательском интерфейсе ленты. Например, при вводе текста, изменении выделенного фрагмента, прокрутки или перемещении точки вставки с помощью мыши все поля указываются как команды в гипотетическом текстовом редакторе, однако они не подходят для отображения на панели команд, так как каждая из них включает непосредственное взаимодействие с пользовательским интерфейсом приложения.

И наоборот, некоторые функции могут не рассматриваться как команды в традиционном смысле. Например, вместо скрытия в диалоговом окне настройки полей принтера могут быть представлены на ленте как группа элементов управления "Счетчик" в контекстной вкладке или [режиме приложения](ribbon-applicationmodes.md).

> [!Note]  
> Запишите числовой идентификатор, который может быть назначен каждой команде. Некоторые платформы пользовательского интерфейса, такие как Microsoft Foundation Classes (MFC), определяют идентификаторы для таких команд, как меню File и Edit (0xE100 to 0xE200).

 

### <a name="organize"></a>Организация

Прежде чем пытаться упорядочить учетные записи команд, необходимо ознакомиться с рекомендациями [пользователя на ленте](https://msdn.microsoft.com/library/cc872782.aspx) , чтобы получить рекомендации при реализации пользовательского интерфейса Ribbon.

Как правило, к организации команды ленты можно применить следующие правила.

-   Команды, которые работают с файлом или общим приложением, скорее всего, находятся в [меню приложения](windowsribbon-controls-applicationmenu.md).
-   Часто используемые команды, такие как вырезание, копирование и вставка (как в примере текстового редактора), обычно размещаются на вкладке «Главная» по умолчанию. В более сложных приложениях они могут дублироваться в других местах в пользовательском интерфейсе ленты.
-   Важные или часто используемые команды могут гарантировать включение по умолчанию на [панели быстрого доступа](windowsribbon-controls-quickaccesstoolbar.md).

Платформа Ribbon также предоставляет элементы управления ContextMenu и Минитулбар через представление Контекстпопуп. Эти функции не являются обязательными, но если приложение содержит одно или несколько существующих контекстных меню, миграция содержащихся в них команд может привести к повторному использованию существующей базы кода с автоматической привязкой к существующим ресурсам.

Так как каждое приложение отличается, ознакомьтесь с рекомендациями и попытайтесь применить их к максимальному экстенту. Одной из целей платформы Ribbon является предоставление привычного, единообразного взаимодействия с пользователем, и эта цель будет более достижима, если разработка новых приложений потребует максимально возможного отражения существующих приложений ленты.

## <a name="adapt-your-code"></a>Адаптация кода

После того как команды ленты определены и организованы в логические группы, количество этапов, связанных с внедрением платформы Ribbon в существующий код приложения, зависит от сложности исходного приложения. Как правило, существует три основных шага:

-   Создайте разметку ленты на основе схемы команды и спецификации макета.
-   Замените функциональные возможности меню и панелей инструментов прежними возможностями на ленте.
-   Реализация адаптера Иуикоммандхандлер.

### <a name="create-the-markup"></a>Создание разметки

Список команд, а также их организация и макет объявляются через файл разметки ленты, используемый [компилятором разметки ленты](windowsribbon-intentcl.md).

> [!Note]  
> Многие шаги, необходимые для адаптации существующего приложения, похожи на те, которые необходимы для запуска нового приложения на ленте. Дополнительные сведения см. в руководстве по [созданию приложения](windowsribbon-stepbystep.md) для создания ленты.

 

Разметка ленты состоит из двух основных разделов. Первый раздел представляет собой манифест команд и связанных с ними ресурсов (строк и изображений). Во втором разделе задается структура и размещение элементов управления на ленте.

Разметка для простого текстового редактора может выглядеть примерно так, как показано в следующем примере:

> [!Note]  
> Ресурсы изображений и строк описаны далее в этой статье.

 


```C++
<?xml version="1.0" encoding="utf-8"?>
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">

  <Application.Commands>
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" />
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" />
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" />
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" />
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" />
    <Command Name="cmdUndo" Id="0xE12B" Symbol="ID_CMD_UNDO" LabelTitle="Undo" />
    <Command Name="cmdCut" Id="0xE123" Symbol="ID_CMD_CUT" LabelTitle="Cut" />
    <Command Name="cmdCopy" Id="0xE122" Symbol="ID_CMD_COPY" LabelTitle="Copy" />
    <Command Name="cmdPaste" Id="0xE125" Symbol="ID_CMD_PASTE" LabelTitle="Paste" />
    <Command Name="cmdDelete" Id="0xE120" Symbol="ID_CMD_DELETE" LabelTitle="Delete" />
    <Command Name="cmdZoom" Id="1242" Symbol="ID_CMD_ZOOM" LabelTitle="Zoom" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.ApplicationMenu>
        <ApplicationMenu>
          <MenuGroup>
            <Button CommandName="cmdNew" />
            <Button CommandName="cmdOpen" />
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdSaveAs" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdExit" />
          </MenuGroup>
        </ApplicationMenu>
      </Ribbon.ApplicationMenu>
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar>
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdSave" />
            <Button CommandName="cmdUndo" />
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
      <Ribbon.Tabs>
        <Tab>
          <Group CommandName="grpClipboard" SizeDefinition="FourButtons">
            <Button CommandName="cmdPaste" />
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdDelete" />
          </Group>
        </Tab>
        <Tab>
          <Group CommandName="grpView" SizeDefinition="OneButton">
            <Button CommandName="cmdZoom" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>

</Application>
```



Чтобы избежать переопределения символов, определяемых платформой пользовательского интерфейса, например MFC, в предыдущем примере для каждой команды используются несколько различных имен символов (идентификатор \_ файла \_ New или \_ cmd \_ New). Однако числовой идентификатор, назначенный каждой команде, должен остаться прежним.

Чтобы интегрировать файл разметки в приложение, настройте пользовательский этап сборки для запуска компилятора разметки ленты UICC.exe. Полученные файлы заголовков и ресурсов затем включаются в существующий проект. Если в примере текстового редактора текстовое приложение имеет имя "Риббонпад", требуется Командная строка с пользовательской сборкой, аналогичная следующей:


```
UICC.exe res\RibbonPad_ribbon.xml res\RibbonPad_ribbon.bin 
         /header:res\RibbonPad_ribbon.h /res:res\RibbonPad_ribbon.rc2
```



Компилятор разметки создает двоичный файл, файл заголовка (H) и файл ресурса (RC). Поскольку существующее приложение, скорее всего, имеет существующий RC-файл, включите созданные файлы H и RC в этот RC-файл, как показано в следующем примере:


```C++
#ifndef APSTUDIO_INVOKED
/////////////////////////////////////////////////////////////////////////////
//
// Generated from the TEXTINCLUDE 3 resource.
//

#define _AFX_NO_SPLITTER_RESOURCES
#define _AFX_NO_OLE_RESOURCES
#define _AFX_NO_TRACKER_RESOURCES
#define _AFX_NO_PROPERTY_RESOURCES

#if !defined(AFX_RESOURCE_DLL) || defined(AFX_TARG_ENU)
LANGUAGE 9, 1
#pragma code_page(1252)

#include "res\RibbonPad_ribbon.h"  // Ribbon resources
#include "res\RibbonPad_ribbon.rc2"  // Ribbon resources

#include "res\RibbonPad.rc2"  // non-Microsoft Visual C++ edited resources
#include "afxres.rc"    // Standard components
#include "afxprint.rc"  // printing/print preview resources
#endif
#endif    // not APSTUDIO_INVOKED
```



### <a name="replace-legacy-menus-and-toolbars"></a>Замена устаревших меню и панелей инструментов

Для замены стандартных меню и панелей инструментов на ленту в устаревшем приложении необходимо следующее:

1.  Удаление ссылок на ресурсы панели инструментов и меню из файла ресурсов приложения.
2.  Удалить все коды инициализации панели инструментов и строки меню.
3.  Удалите код, используемый для присоединения панели инструментов или строки меню к окну верхнего уровня приложения.
4.  Создайте экземпляр платформы Ribbon.
5.  Присоедините ленту к окну верхнего уровня приложения.
6.  Загрузите скомпилированную разметку.

> [!IMPORTANT]
> Существующие строки состояния и таблицы сочетаний клавиш должны сохраняться, так как платформа Ribbon не заменяет эти функции.

 

В следующем примере показано, как инициализировать платформу с помощью [**иуифрамеворк:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize):


```C++
int CMainFrame::OnCreate(LPCREATESTRUCT lpCreateStruct)
{
    if (CFrameWnd::OnCreate(lpCreateStruct) == -1)
        return -1;
    
    if (!m_RibbonBar.Create(this, WS_CHILD|WS_DISABLED|WS_VISIBLE|CBRS_TOP|CBRS_HIDE_INPLACE,0))
        return -1;      // fail to create

    if (!m_wndStatusBar.Create(this) || !m_wndStatusBar.SetIndicators(indicators,sizeof(indicators)/sizeof(UINT)))
        return -1;      // fail to create

    // Ribbon initialization
    InitRibbon(this, &m_spUIFramework);

    return 0;
}
```



В следующем примере показано, как использовать [**иуифрамеворк:: лоадуи**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) для загрузки скомпилированной разметки:


```C++
HRESULT InitRibbon(CMainFrame* pMainFrame, IUnknown** ppFramework)
{
    // Create the IUIFramework instance.
    CComPtr<IUIFramework> spFramework;
    HRESULT hr = ::CoCreateInstance(CLSID_UIRibbonFramework, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&spFramework));
    if (FAILED(hr))
        return hr;
    
    // Instantiate the CApplication object.
    CComObject<CApplication>* pApplication;
    hr = CComObject<CApplication>::CreateInstance(&pApplication);   // Refcount is 0
    
    // Call AddRef on the CApplication object. The smart pointer will release the refcount when it is out of scope.
    CComPtr< CComObject<CApplication> > spApplication(pApplication);

    if (FAILED(hr))
        return hr;

    // Initialize and load the Ribbon.
    spApplication->Initialize(pMainFrame);

    hr = spFramework->Initialize(*pMainFrame, spApplication);
    if (FAILED(hr))
        return hr;

    hr = spFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
        return hr;

    // Return IUIFramework interface to the caller.
    hr = spFramework->QueryInterface(ppFramework);

    return hr;
}
```



Класс Каппликатион, упомянутый выше, должен реализовать пару интерфейсов модели COM, определенных платформой Ribbon: [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) и [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler).

[**Иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) предоставляет основной интерфейс обратного вызова между платформой и приложением (например, высота ленты передается через [**Иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged)), а обратные вызовы для отдельных команд предоставляются в ответ на [**иуиаппликатион:: онкреатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand).

**Совет.** Для некоторых платформ приложений, таких как MFC, необходимо учитывать высоту линейки ленты при отрисовке пространства документа приложения. В таких случаях Добавление скрытого окна для наложения панели ленты и принудительное заполнение области документа необходимой высотой. Пример такого подхода, в котором функция макета вызывается на основе высоты ленты, возвращенной методом [**иуириббон:: Height**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiribbon-getheight) , см. в [примере хтмледитриббон](windowsribbon-htmleditribbonsample.md).

В следующем примере кода демонстрируется реализация [**иуиаппликатион:: онвиевчанжед**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-onviewchanged) :


```C++
// This is the Ribbon implementation that is done by an application.
// Applications have to implement IUIApplication and IUICommandHandler to set up communication with the Windows Ribbon.
class CApplication
    : public CComObjectRootEx<CComSingleThreadModel>
    , public IUIApplication
    , public IUICommandHandler
{
public:

    BEGIN_COM_MAP(CApplication)
        COM_INTERFACE_ENTRY(IUIApplication)
        COM_INTERFACE_ENTRY(IUICommandHandler)
    END_COM_MAP()

    CApplication() : _pMainFrame(NULL)
    {
    }

    void Initialize(CMainFrame* pFrame)
    {
        // Hold a reference to the main frame.
        _pMainFrame = pFrame;
    }

    void FinalRelease()
    {
        // Release the reference.
        _pMainFrame = NULL;
        __super::FinalRelease();
    }

    STDMETHOD(OnViewChanged)(UINT32 nViewID, __in UI_VIEWTYPE typeID, __in IUnknown* pView, UI_VIEWVERB verb, INT32 uReasonCode)
    {
        HRESULT hr;

        // The Ribbon size has changed.
        if (verb == UI_VIEWVERB_SIZE)
        {
            CComQIPtr<IUIRibbon> pRibbon = pView;
            if (!pRibbon)
                return E_FAIL;

            UINT ulRibbonHeight;
            // Get the Ribbon height.
            hr = pRibbon->GetHeight(&ulRibbonHeight);
            if (FAILED(hr))
                return hr;

            // Update the Ribbon bar so that the main frame can recalculate the child layout.
            _pMainFrame->m_RibbonBar.SetRibbonHeight(ulRibbonHeight);
            _pMainFrame->RecalcLayout();
        }

        return S_OK;
    }

    STDMETHOD(OnCreateUICommand)(UINT32 nCmdID, 
                               __in UI_COMMANDTYPE typeID,
                               __deref_out IUICommandHandler** ppCommandHandler)
    {
        // This application uses one command handler for all ribbon commands.
        return QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }

    STDMETHOD(OnDestroyUICommand)(UINT32 commandId, __in UI_COMMANDTYPE typeID,  __in_opt  IUICommandHandler *commandHandler)
    {        
        return E_NOTIMPL;
    }

private:
    CMainFrame* _pMainFrame;
};
```



### <a name="implement-an-iuicommandhandler-adapter"></a>Реализация адаптера Иуикоммандхандлер

В зависимости от структуры исходного приложения может быть проще иметь несколько реализаций обработчиков команд или один обработчик команд для промежуточного вызова, вызывающий логику существующей команды приложения. Многие приложения используют \_ Командные сообщения WM для этой цели, где достаточно предоставить один обработчик команд для всех целей, который просто перенаправляет \_ Командные сообщения WM в окно верхнего уровня.

Однако этот подход требует специальной обработки команд, таких как **выход** или **закрытие**. Поскольку лента не может быть уничтожена во время обработки окна сообщения, \_ сообщение закрытия WM должно быть отправлено в поток пользовательского интерфейса приложения и не должно обрабатываться синхронно, как показано в следующем примере:


```C++
// User action callback, with transient execution parameters.
    STDMETHODIMP Execute(UINT nCmdID,
        UI_EXECUTIONVERB verb, 
        __in_opt const PROPERTYKEY* key,
        __in_opt const PROPVARIANT* ppropvarValue,
        __in_opt IUISimplePropertySet* pCommandExecutionProperties)
    {       
        switch(nCmdID)
        {
        case cmdExit:
            ::PostMessage(*_pMainFrame, WM_CLOSE, nCmdID, 0);
            break;
        default:
            ::SendMessage(*_pMainFrame, WM_COMMAND, nCmdID, 0);
        }
        return S_OK;
    }

    STDMETHODIMP UpdateProperty(UINT32 nCmdID, 
                                __in REFPROPERTYKEY key,
                                __in_opt  const PROPVARIANT *currentValue,
                                __out PROPVARIANT *newValue) 
    {        
        return S_OK;
    }

```



## <a name="migrating-resources"></a>Перенос ресурсов

Когда манифест команд определен, была объявлена структура ленты и код приложения, адаптированный для размещения платформы Ribbon, последний шаг — это спецификация строковых и графических ресурсов для каждой команды.

> [!Note]  
> Строковые и графические ресурсы обычно предоставляются в файле разметки. Однако их можно создавать или заменять программно, реализовав метод обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

 

### <a name="string-resources"></a>Строковые ресурсы

[**Command. лабелтитле**](windowsribbon-element-command-labeltitle.md) — это наиболее распространенное строковое свойство, определенное для команды. Они подготавливаются к просмотру как текстовые метки для вкладок, групп и отдельных элементов управления. Строку метки из устаревшего элемента меню обычно можно повторно использовать для **команды. лабелтитле** без изменения.

Однако следующие соглашения были изменены с появлением ленты.

-   Суффикс многоточия (...), используемый для обозначения команды запуска диалогового окна, больше не требуется.
-   Амперсанд (&) по-прежнему может использоваться для указания сочетания клавиш для команды, отображаемой в меню, но свойство [**Command. KeyTip**](windowsribbon-element-command-keytip.md) , поддерживаемое платформой, соответствует той же цели.

При обращении к примеру текстового редактора можно указать следующие строки для Лабелтитле и KeyTip:



| Символ           | Исходная строка | Строка Лабелтитле | Строка keytip |
|------------------|-----------------|-------------------|---------------|
| \_файл идентификатора \_ New    | &New            | &New              | Нет             |
| файл идентификатора — \_ \_ Сохранение   | &сохранить           | &сохранить             | S             |
| \_файл идентификатора \_ SAVEAS | Сохранить &как...       | Сохранить &как          | Объект             |
| \_файл идентификатора \_ открыт   | &открыть...          | &amp;Open             | O             |
| \_ \_ выход из файла идентификатора   | Вы&ход           | Вы&ход             | X             |
| \_Отмена изменения \_ идентификатора   | &отменить           | Отменить              | Z             |
| \_Изменение идентификатора \_ Вырезать    | Cu&t            | Cu&t              | X             |
| Идентификатор \_ изменения \_ копии   | Копирование &           | Копирование &             | C             |
| изменение кода при \_ \_ вставке  | &вставить          | &вставить            | V             |
| ID \_ Правка \_ очистить  | &удалить         | &удалить           | D             |
| \_масштаб представления \_ идентификатора   | &масштаб...          | Масштабирование              | Z             |



 

Ниже приведен список других свойств строки, которые должны быть установлены для большинства команд:

-   [**Command. Лабелдескриптион**](windowsribbon-element-command-labeldescription.md)
-   [**Command. Тултиптитле**](windowsribbon-element-command-tooltiptitle.md)
-   [**Command. Тултипдескриптион**](windowsribbon-element-command-tooltipdescription.md)

Вкладки, группы и другие функции пользовательского интерфейса ленты теперь можно объявить с помощью всех указанных строковых и графических ресурсов.

В следующем примере разметки ленты показаны различные строковые ресурсы.


```C++
<Application.Commands>
    <!-- Tabs -->
    <Command Name="tabHome" LabelTitle="Home" Keytip="H" />
    <Command Name="tabView" LabelTitle="View" Keytip="V" />

    <!-- Groups -->
    <Command Name="grpClipboard" LabelTitle="Clipboard" />
    <Command Name="grpZoom" LabelTitle="Zoom" />

    <!-- App menu commands -->
    <Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSave" Id="0xE103" Symbol="ID_CMD_SAVE" LabelTitle="Save" Keytip="S">
      <Command.TooltipTitle>Save (Ctrl+S)</Command.TooltipTitle>
      <Command.TooltipDescription>Save the current document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdSaveAs" Id="0xE104" Symbol="ID_CMD_SAVEAS" LabelTitle="Save as" Keytip="A">
      <Command.TooltipDescription>Save the current document with a new name.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdOpen" Id="0xE101" Symbol="ID_CMD_OPEN" LabelTitle="Open" Keytip="O">
      <Command.TooltipTitle>Open (Ctrl+O)</Command.TooltipTitle>
      <Command.TooltipDescription>Open a document.</Command.TooltipDescription>
    </Command>
    <Command Name="cmdExit" Id="0xE102" Symbol="ID_CMD_EXIT" LabelTitle="Exit" Keytip="X">
      <Command.TooltipDescription>Exit the application.</Command.TooltipDescription>
    </Command>

    <!-- ...other commands -->

  </Application.Commands>
```



### <a name="image-resources"></a>Ресурсы изображений

Платформа Ribbon поддерживает форматы изображений, обеспечивающие более широкие возможности оформления, чем форматы изображений, поддерживаемые предыдущими компонентами меню и панелей инструментов.

для Windows 8 и более поздних версий платформа Ribbon поддерживает следующие форматы графики: 32-битовые растровые файлы ARGB (BMP) и png-файлы с прозрачностью.

для Windows 7 и более ранних версий ресурсы изображений должны соответствовать стандартному графическому формату BMP, используемому в Windows.

> [!Note]  
> Существующие файлы изображений можно преобразовать в любой из форматов. Однако результаты могут быть менее удовлетворительными, если файлы изображений не поддерживают сглаживание и прозрачность.

 

Невозможно указать один размер по умолчанию для ресурсов изображений в платформе Ribbon. Однако для поддержки [адаптивного макета](windowsribbon-templates.md) элементов управления изображения могут быть указаны в двух размерах (большие и небольшие). Все изображения в платформе ленты масштабируются в соответствии с разрешением точек на дюйм (DPI) монитора с точно отображаемым размером, зависящим от этого параметра dpi. Дополнительные сведения см. в разделе [указание ресурсов изображения ленты](windowsribbon-imageformats.md) .

В следующем примере показано, как в разметке указываются ссылки на образы, относящиеся к dpi.


```C++
<Command Name="cmdNew" Id="0xE100" Symbol="ID_CMD_NEW" LabelTitle="New document" Keytip="N" >
      <Command.TooltipTitle>New (Ctrl+N)</Command.TooltipTitle>
      <Command.TooltipDescription>Create a new document.</Command.TooltipDescription>
      <Command.LargeImages>
        <Image Source="cmdNew-32px.png" MinDPI="96" />
        <Image Source="cmdNew-40px.png" MinDPI="120" />
        <Image Source="cmdNew-48px.png" MinDPI="144" />
        <Image Source="cmdNew-64px.png" MinDPI="192" />
      </Command.LargeImages>
      <Command.SmallImages>
        <Image Source="cmdNew-16px.png" MinDPI="96" />
        <Image Source="cmdNew-20px.png" MinDPI="120" />
        <Image Source="cmdNew-24px.png" MinDPI="144" />
        <Image Source="cmdNew-32px.png" MinDPI="192" />
      </Command.SmallImages>
    </Command>
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Указание ресурсов изображения ленты](windowsribbon-imageformats.md)
</dt> </dl>

 

 