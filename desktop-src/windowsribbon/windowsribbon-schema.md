---
title: Объявление команд и элементов управления с разметкой ленты
description: Платформа Windows Ribbon использует язык разметки на основе XAML (XAML) для декларативной реализации внешнего вида приложения с лентой.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Лента Windows, структура разметки
- Лента, структура разметки
- Лента Windows, отделение презентации от логики команды
- Лента, отделение представления от логики команды
- Лента Windows, компоненты
- Лента, компоненты
- система команд для ленты Windows
- элементы управления для ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413384"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Объявление команд и элементов управления с разметкой ленты

Платформа Windows Ribbon использует язык разметки на основе XAML (XAML) для декларативной реализации внешнего вида приложения с лентой.

-   [Отделение представления от логики команды](#separating-presentation-from-command-logic)
-   [Структура разметки](#markup-structure)
-   [Компоненты ленты](#ribbon-components)
-   [См. также](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Отделение представления от логики команды

Разделение представлений и визуальных атрибутов из логики команды на ленте осуществляется через две разные, но зависимые платформы разработки. Макеты элементов управления, поведение масштабирования, объявления команд и спецификации ресурсов — это домен времени разработки декларативного синтаксиса разметки на основе спецификации [XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) . Функции нижнего уровня, перехватчики приложения и обработчики команд определены в реализациях интерфейса на основе модели объектов (COM).

Такое разделение представления и логики предоставляет следующие преимущества.

-   Более эффективный цикл разработки приложений, позволяющий разработчикам пользовательского интерфейса и дизайнерам реализовывать графический интерфейс приложения Ribbon независимо от основных функциональных возможностей приложения. Эта основная функциональность может быть оставлена выделенным разработчикам программного обеспечения.
-   Менее дорогостоящее обслуживание, поскольку изменения графического пользовательского интерфейса возможны без изменений в основных функциях (и наоборот).
-   Простая спецификация строковых и графических ресурсов с помощью разметки.
-   Простота создания прототипов.

## <a name="markup-structure"></a>Структура разметки

В структуре разметки платформы ленты существуют две отдельные ветви.

Первая ветвь содержит манифест объявлений команд и ресурсов (строк и изображений). Каждая запись команды используется платформой для привязки элемента управления ленты с помощью идентификатора команды к обработчику команд, определенному в коде приложения.

Вторая ветвь содержит фактические объявления элементов управления. Каждый элемент управления связан с командой через атрибут *CommandName* , сопоставляемый с атрибутом *Name* , указанным в каждом объявлении команды.

## <a name="ribbon-components"></a>Компоненты ленты

Функциональность пользовательского интерфейса платформы ленты предоставляется через [представления](windowsribbon-reference-elements-view.md). Представление — это, по сути, контейнер, такой как [**Ribbon**](windowsribbon-element-ribbon.md) и [**контекстпопуп**](windowsribbon-element-contextpopup.md), который используется для представления элементов управления платформы и команд, к которым они привязаны.

Представление [**ленты**](windowsribbon-element-ribbon.md) состоит из нескольких компонентов, включающих [меню приложения](windowsribbon-controls-applicationmenu.md), [панель быстрого доступа (QAT)](windowsribbon-controls-quickaccesstoolbar.md) для отображения часто используемых команд из ленты, ядра и контекстных [вкладок](windowsribbon-controls-tab.md) , которые содержат [группы](windowsribbon-controls-group.md) элементов управления, и систему расширенного контекстного меню [**контекстпопуп**](windowsribbon-element-contextpopup.md).

Все компоненты ленты объявляются в отдельном файле разметки, который:

-   Задает основные свойства для каждого элемента.
-   Четко отображает иерархические связи.
-   Предоставляет параметры макета и указания по масштабированию. Дополнительные сведения о шаблонах макета Ribbon Framework см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).
-   Предоставляет способ определения ресурсов, таких как изображения и метки. Дополнительные сведения о ресурсах с изображениями см. в разделе [указание ресурсов изображения ленты](windowsribbon-imageformats.md).

В следующих двух примерах разметки ленты показано, как набор элементов меню приложения ленты связан с именем команды и ИДЕНТИФИКАТОРом.

1.  В этом разделе показаны объявления команд, необходимые для меню приложения с основными командами, такими как создание, открытие и сохранение.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  В этом разделе показаны связанные объявления элементов управления.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Если разметка компилируется с помощью средства компиляции команд пользовательского интерфейса (УИКК), имена команд и идентификаторы помещаются в файл заголовка, используемый ведущим приложением ленты.

Ниже приведен пример файла заголовка, созданного УИКК.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Компиляция разметки ленты](windowsribbon-intentcl.md)
</dt> </dl>

 

 