---
title: Специальные возможности элемента управления ActiveX без окон
description: В этом разделе описывается использование интерфейса API специальных возможностей Windows для обеспечения доступности элементов управления Microsoft ActiveX без окон.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413351"
---
# <a name="windowless-activex-control-accessibility"></a>Специальные возможности элемента управления ActiveX без окон

В этом разделе описывается использование интерфейса API специальных возможностей Windows для обеспечения доступности элементов управления Microsoft ActiveX без окон.

В Windows 8 включены новые интерфейсы API специальных возможностей Windows, упрощающие задачу реализации специальных возможностей для элементов управления ActiveX без окон. API включает интерфейсы, реализованные в безоконном элементе управления и в контейнере элемента управления, что позволяет без оконного контроля и его контейнера работать вместе, чтобы предоставить сведения о специальных возможностях для безоконного элемента управления. API поддерживает следующие сценарии.

-   Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элемента управления Microsoft Active Accessibility.
-   Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элементов управления Microsoft UI Automation.
-   Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элемента управления Microsoft Active Accessibility.
-   Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элементов управления модели автоматизации пользовательского интерфейса.

В следующей таблице перечислены интерфейсы, которые поддерживают элементы управления ActiveX без окон и идентифицируются объекты, реализующие интерфейсы.



| Объект              | MSAA                                                                             | автоматизация пользовательского интерфейса                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Управляющий объект      | [**иакцессиблехандлер**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Сайт управления        | [**иакцессиблевиндовлесссите**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**иравелементпровидервиндовлесссите**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Корневой элемент главного окна | [**иакцессиблехостинжелементпровидерс**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**иравелементпровидерхостингакцессиблес**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Содержание раздела

-   [Использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному элементу управления ActiveX](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [Как использовать MSAA, чтобы сделать безоконный элемент управления ActiveX доступным](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [Размещение элемента управления ActiveX без окон UI Automation](host-a-ui-automation-windowless-activex-control.md)
-   [Размещение элемента управления ActiveX без окна MSAA](host-an-msaa-windowless-activex-control.md)

 

 