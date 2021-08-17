---
title: Контекстное всплывающее окно
description: всплывающее контекстное меню — это основной элемент управления в представлении контекстпопуп платформы ленты Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964421"
---
# <a name="context-popup"></a>Контекстное всплывающее окно

всплывающее контекстное меню — это основной элемент управления в [**представлении контекстпопуп**](windowsribbon-element-contextpopup.md) платформы ленты Windows. Это обширная система контекстного меню, доступная только для платформы в качестве расширения для реализации ленты — платформа не предоставляет всплывающее окно контекста как независимый элемент управления.

-   [Компоненты всплывающего контекстного меню](#context-popup)
-   [Реализация всплывающего контекстного меню](#implement-the-context-popup)
    -   [разметку](#markup)
    -   [Код](#code)
-   [Свойства всплывающего контекстного меню](#context-popup-properties)
-   [Связанные темы](#related-topics)

## <a name="components-of-the-context-popup"></a>Компоненты всплывающего контекстного меню

Всплывающее контекстное меню — это логический контейнер для контекстного дерева, а Mini-Toolbar вложенные элементы управления, доступные через элементы разметки [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) соответственно:

-   [**ContextMenu**](windowsribbon-element-contextmenu.md) предоставляет меню команд и коллекций.
-   [**Минитулбар**](windowsribbon-element-minitoolbar.md) предоставляет плавающую панель инструментов различных команд, коллекций и сложных элементов управления, таких как [элемент управления шрифта](windowsribbon-controls-fontcontrol.md) и [поле со списком](windowsribbon-controls-combobox.md).

Каждый подэлемент управления может отображаться в контекстном меню не более одного раза.

На следующем снимке экрана показан контекст всплывающего окна и его вложенные элементы управления.

![снимок экрана с выносками, в которых отображаются контекстные компоненты пользовательского интерфейса ленты.](images/controls/contextpopup.png)

Всплывающее контекстное меню является исключительно концептуальным и не предоставляет никаких функциональных возможностей пользовательского интерфейса, таких как позиционирование или изменение размера.

> [!Note]  
> Всплывающее контекстное меню обычно выводится щелчком правой кнопкой мыши (или нажатием клавиши SHIFT + F10) на интересующем объекте. Однако действия, необходимые для вывода контекстного всплывающего окна, определяются приложением.

 

## <a name="implement-the-context-popup"></a>Реализация всплывающего контекстного меню

аналогично другим Windows элементам управления платформы Ribbon контекстное меню реализуется с помощью компонента разметки, который указывает сведения о презентации и компонент кода, управляющий его функциональностью.

В следующей таблице перечислены элементы управления, поддерживаемые каждым всплывающим контекстным элементом управления.



| Элемент                                                                  | Mini-Toolbar | Контекстное меню |
|--------------------------------------------------------------------------|--------------|--------------|
| [Кнопка](windowsribbon-controls-button.md)                              | x            | x            |
| [Флажок](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Поле со списком](windowsribbon-controls-combobox.md)                         | x            |              |
| [Кнопка раскрывающегося списка](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Выбор цвета для раскрывающегося списка](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Раскрывающийся список](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Элемент управления шрифтами](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Кнопка "Справка"](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Коллекция на ленте](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Spinner](windowsribbon-controls-spinner.md)                            |              |              |
| [Разворачивающаяся кнопка](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Коллекция разделенных кнопок](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Выключатель](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>разметку

Каждый всплывающий элемент контекстного меню должен быть объявлен отдельно в разметке.

### <a name="mini-toolbar"></a>Mini-Toolbar

При добавлении элементов управления в контекстное меню мини-панели инструментов следует учитывать следующие две рекомендации.

-   Элементы управления должны быть хорошо распознаваемыми и предоставляют очевидные функциональные возможности. Знание является ключом, так как метки и подсказки не доступны для элементов управления Mini-Toolbar.
-   Каждая команда, предоставляемая элементом управления, должна быть представлена в любом расположении в пользовательском интерфейсе ленты. Mini-Toolbar не поддерживает навигацию по клавишам.

В следующем примере показана базовая разметка для элемента [**минитулбар**](windowsribbon-element-minitoolbar.md) , который содержит три элемента управления ["Кнопка"](windowsribbon-controls-button.md) .

> [!Note]  
> Для каждой строки элементов управления на мини-панели инструментов указан один элемент [**менуграуп**](windowsribbon-element-menugroup.md) .

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Контекстное меню

В следующем примере показана базовая разметка для элемента [**ContextMenu**](windowsribbon-element-contextmenu.md) , содержащего три элемента управления ["Кнопка"](windowsribbon-controls-button.md) .

> [!Note]  
> Каждый набор элементов управления в элементе [**менуграуп**](windowsribbon-element-menugroup.md) отделяется горизонтальной чертой в контекстном меню.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Хотя всплывающее контекстное меню может содержать не более одного из дочерних элементов управления, в разметке ленты можно использовать несколько объявлений элементов [**ContextMenu**](windowsribbon-element-contextmenu.md) и [**минитулбар**](windowsribbon-element-minitoolbar.md) . Это позволяет приложению поддерживать различные сочетания контекстного меню и Mini-Toolbar элементов управления на основе критериев, определенных приложением, например контекста рабочей области.

Дополнительные сведения см. в описании элемента [**контекстмап**](windowsribbon-element-contextmap.md) .

В следующем примере показана базовая разметка для элемента [**контекстпопуп**](windowsribbon-element-contextpopup.md) .


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a>Код

Чтобы вызвать всплывающее контекстное меню, метод [**иуиконтекстуалуи:: шоватлокатион**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) вызывается, когда окно верхнего уровня приложения на ленте получает \_ уведомление WM CONTEXTMENU.

В этом примере показано, как управлять \_ уведомлением WM CONTEXTMENU в методе WndProc () приложения Ribbon.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



В следующем примере показано, как приложение ленты может отображать контекстное всплывающее окно в определенном месте на экране с помощью метода [**иуиконтекстуалуи:: шоватлокатион**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .

Жеткуррентконтекст () имеет значение `cmdContextMap` , определенное в предыдущем примере разметки.

g \_ паппликатион — это ссылка на интерфейс [**иуифрамеворк**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



Ссылку на [**иуиконтекстуалуи**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) можно освободить до закрытия всплывающего окна контекста, как показано в предыдущем примере. Однако ссылка должна быть освобождена в некоторый момент, чтобы избежать утечек памяти.

> [!Caution]  
> Mini-Toolbar имеет встроенный эффект исчезания, основанный на указателе мыши. По этой причине рекомендуется, чтобы Mini-Toolbar отображались как можно ближе к указателю мыши. В противном случае, в связи с конфликтующими механизмами отображения, Mini-Toolbar может отображаться не так, как ожидалось.

 

## <a name="context-popup-properties"></a>Свойства всплывающего контекстного меню

Нет ключей свойств, связанных с всплывающим элементом управления контекстом.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Библиотека элементов управления платформы ленты](windowsribbon-controls-entry.md)
</dt> <dt>

[Пример Контекстпопуп](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 