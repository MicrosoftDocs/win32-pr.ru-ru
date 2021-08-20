---
title: размещение элемента управления ActiveX без окна MSAA
description: узнайте, как создать контейнер элементов управления, который может размещать безоконные элементы управления microsoft ActiveX, реализующие microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, безоконный контроль ActiveX
- безоконный контроль ActiveX, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d086fdc33c1b645294827ec62784612ffeb617f12caf5a101ea8472da3e765
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115135"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>размещение элемента управления ActiveX без окна MSAA

узнайте, как создать контейнер элементов управления, который может размещать безоконные элементы управления microsoft ActiveX, реализующие microsoft Active Accessibility. Выполнив описанные здесь действия, можно убедиться, что любые элементы управления без окон на Active Accessibility Майкрософт, размещенные в контейнере управления, доступны для клиентских приложений с поддержкой специальных возможностей (AT).

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Элементы управления ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Предварительные требования

-   C/C++
-   Программирование Microsoft Win32 и объектной модели компонентов (COM)
-   безоконные элементы управления ActiveX
-   Серверы Microsoft Active Accessibility

## <a name="instructions"></a>Инструкции

### <a name="step-1-provide-the-root-iaccessible-interface-on-behalf-of-the-windowless-control"></a>Шаг 1. предоставление корневого интерфейса IAccessible от имени элемента управления без окон.

Всякий раз, когда системе требуется указатель [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для корневого элемента управления без окон, система запрашивает контейнер элемента управления. Для получения указателя контейнер вызывает реализацию метода [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)) элемента управления без окон.

Если контейнер элемента управления имеет реализацию Microsoft Active Accessibility, он может вернуть в систему указатель [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) элемента управления без окон.

Если контейнер элемента управления имеет реализацию Microsoft UI Automation, вызовите функцию [**уиапровидерфромиакцессибле**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible) , чтобы получить указатель интерфейса [**иравелементпровидерсимпле**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) , представляющий элемент управления, а затем верните указатель интерфейса **иравелементпровидерсимпле** в систему.

### <a name="step-2-respond-to-the-wm_getobject-message-on-behalf-of-the-windowless-control"></a>Шаг 2. ответ на сообщение WM \_ GetObject от имени элемента управления без окон.

Когда клиентское приложение реагирует на WinEvent, вызванное безоконным элементом управления, контейнер элементов управления получает сообщение [**WM \_ GetObject**](wm-getobject.md) от имени элемента управления. Сообщение включает идентификатор объекта безоконного элемента управления, вызвавшего событие.

Контейнер элемента управления отвечает путем поиска безоконного элемента управления, которому "владеет" идентификатор объекта, и последующего вызова метода [**иакцессиблехандлер:: акцессиблеобжектфромид**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid) этого элемента управления. Метод **акцессиблеобжектфромид** возвращает указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента пользовательского интерфейса, а контейнер элементов управления возвращает указатель на систему, который пересылает его клиентскому приложению.

### <a name="step-3-implement-the-iaccessiblewindowlesssite-interface"></a>Шаг 3. Реализация интерфейса Иакцессиблевиндовлесссите.

1.  Реализуйте метод [**иакцессиблевиндовлесссите:: жетпарентакцессибле**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) .

    Когда клиентскому приложению требуются специальные сведения о доступности родителя корневого поставщика элемента управления без окна, система вызывает метод [**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) элемента управления без окон. Элемент управления отвечает вызовом метода [**иакцессиблевиндовлесссите:: жетпарентакцессибле**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-getparentaccessible) контейнера элемента управления, который предоставляет указатель [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) родителя элемента управления без окна.

2.  Реализуйте методы [**иакцессиблевиндовлесссите:: аккуиреобжектидранже**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-acquireobjectidrange), [**куерйобжектидранже**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-queryobjectidranges)и [**релеасеобжектидранже**](/windows/desktop/api/oleacc/nf-oleacc-iaccessiblewindowlesssite-releaseobjectidrange) .

    Контейнер элементов управления должен поддерживать сопоставление диапазонов ИДЕНТИФИКАТОРов объектов с безоконными элементами управления. Сопоставление позволяет контейнеру элемента управления определить элемент управления, который должен отвечать на определенный запрос идентификатора объекта. В следующей таблице приведен пример сопоставления диапазонов объектов с элементами управления без окон.

    

    | Основание диапазона | Размер диапазона | Элемент   |
    |------------|------------|-----------|
    | 1000       | 500        | Элемент управления 1 |
    | 1500       | 1000       | Управление 2 |
    | 2500       | 2000       | Элемент управления 1 |

    

     

    Контейнер элементов управления должен поддерживать сопоставление диапазонов ИДЕНТИФИКАТОРов объектов с безоконными элементами управления для самого себя и всех безоконных дочерних элементов. Диапазоны ИДЕНТИФИКАТОРов объектов не должны быть смежными друг с другом. Кроме того, чтобы избежать атак типа "отказ в обслуживании", контейнер элемента управления может ограничить количество диапазонов, предоставленных конкретному элементу управления. Тем не менее, чтобы обеспечить увеличение размера элемента управления, полезно разрешать более одного диапазона для каждого элемента управления.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Шаг 4. необязательный: реализация интерфейса Иакцессиблехостинжелементпровидерс.

реализуйте интерфейс [**иакцессиблехостинжелементпровидерс**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) , если контейнер элемента управления имеет реализацию Microsoft Active Accessibility server, а сервер является корнем дерева специальных возможностей, который включает элементы управления ActiveX без окон, поддерживающие автоматизацию пользовательского интерфейса. интерфейс **иакцессиблехостинжелементпровидерс** содержит один метод [**жетембеддедфрагментрутс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), который получает указатели интерфейса [**иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) для всех элементов управления без ActiveX окон модели автоматизации пользовательского интерфейса, которые размещаются в контейнере элементов управления.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[размещение элемента управления ActiveX без окон автоматизации пользовательского интерфейса](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[специальные возможности элемента управления ActiveX без окон](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 