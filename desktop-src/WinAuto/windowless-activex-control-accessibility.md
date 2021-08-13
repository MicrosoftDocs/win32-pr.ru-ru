---
title: специальные возможности элемента управления ActiveX без окон
description: в этом разделе описано, как использовать интерфейс API Windows специальных возможностей, чтобы обеспечить доступность безоконных элементов управления Microsoft ActiveX.
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563459"
---
# <a name="windowless-activex-control-accessibility"></a>специальные возможности элемента управления ActiveX без окон

в этом разделе описано, как использовать интерфейс API Windows специальных возможностей, чтобы обеспечить доступность безоконных элементов управления Microsoft ActiveX.

Windows 8 включает новые интерфейсы API специальных возможностей Windows, которые упрощают задачу реализации специальных возможностей для элементов управления ActiveX без окон. API включает интерфейсы, реализованные в безоконном элементе управления и в контейнере элемента управления, что позволяет без оконного контроля и его контейнера работать вместе, чтобы предоставить сведения о специальных возможностях для безоконного элемента управления. API поддерживает следующие сценарии.

-   Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элемента управления Microsoft Active Accessibility.
-   Microsoft Active Accessibility безоконные элементы управления, размещенные в контейнере элементов управления Microsoft UI Automation.
-   Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элемента управления Microsoft Active Accessibility.
-   Элементы управления без окон модели автоматизации пользовательского интерфейса, размещенные в контейнере элементов управления модели автоматизации пользовательского интерфейса.

в следующей таблице перечислены интерфейсы, которые поддерживают элементы управления ActiveX без окон и определяют объекты, реализующие интерфейсы.



| Объект              | MSAA                                                                             | автоматизация пользовательского интерфейса                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Управляющий объект      | [**иакцессиблехандлер**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| Сайт управления        | [**иакцессиблевиндовлесссите**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**иравелементпровидервиндовлесссите**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| Корневой элемент главного окна | [**иакцессиблехостинжелементпровидерс**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**иравелементпровидерхостингакцессиблес**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>Содержание раздела

-   [использование модели автоматизации пользовательского интерфейса для обеспечения доступа к безоконному ActiveX управления](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [использование MSAA для обеспечения возможности управления ActiveX без окон](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [размещение элемента управления ActiveX без окон автоматизации пользовательского интерфейса](host-a-ui-automation-windowless-activex-control.md)
-   [размещение элемента управления ActiveX без окна MSAA](host-an-msaa-windowless-activex-control.md)

 

 