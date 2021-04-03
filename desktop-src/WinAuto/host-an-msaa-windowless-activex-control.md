---
title: Размещение элемента управления ActiveX без окна MSAA
description: Узнайте, как создать контейнер элементов управления, который может содержать безоконные элементы управления Microsoft ActiveX, реализующие Microsoft Active Accessibility.
ms.assetid: 9497561C-37ED-4094-A6B0-C219F63C04B6
keywords:
- MSAA, безоконный элемент управления ActiveX
- Безоконный элемент управления ActiveX, MSAA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9de45313b19490af3c3fffb633f3822ad93d25a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791791"
---
# <a name="how-to-host-an-msaa-windowless-activex-control"></a>Размещение элемента управления ActiveX без окна MSAA

Узнайте, как создать контейнер элементов управления, который может содержать безоконные элементы управления Microsoft ActiveX, реализующие Microsoft Active Accessibility. Выполнив описанные здесь действия, можно убедиться, что любые элементы управления без окон на Active Accessibility Майкрософт, размещенные в контейнере управления, доступны для клиентских приложений с поддержкой специальных возможностей (AT).

## <a name="what-you-need-to-know"></a>Что необходимо знать

### <a name="technologies"></a>Технологии

-   [Элементы управления ActiveX](/windows/desktop/com/activex-controls)
-   [Microsoft Active Accessibility](microsoft-active-accessibility.md)

### <a name="prerequisites"></a>Предварительные условия

-   C/C++
-   Программирование Microsoft Win32 и объектной модели компонентов (COM)
-   Элементы управления ActiveX без окон
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

    

    | Основание диапазона | Размер диапазона | Control   |
    |------------|------------|-----------|
    | 1000       | 500        | Элемент управления 1 |
    | 1500       | 1000       | Управление 2 |
    | 2500       | 2000       | Элемент управления 1 |

    

     

    Контейнер элементов управления должен поддерживать сопоставление диапазонов ИДЕНТИФИКАТОРов объектов с безоконными элементами управления для самого себя и всех безоконных дочерних элементов. Диапазоны ИДЕНТИФИКАТОРов объектов не должны быть смежными друг с другом. Кроме того, чтобы избежать атак типа "отказ в обслуживании", контейнер элемента управления может ограничить количество диапазонов, предоставленных конкретному элементу управления. Тем не менее, чтобы обеспечить увеличение размера элемента управления, полезно разрешать более одного диапазона для каждого элемента управления.

### <a name="step-4-optional-implement-the-iaccessiblehostingelementproviders-interface"></a>Шаг 4. необязательный: реализация интерфейса Иакцессиблехостинжелементпровидерс.

Реализуйте интерфейс [**иакцессиблехостинжелементпровидерс**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) , если контейнер элемента управления имеет реализацию Microsoft Active Accessibility Server, а сервер является корнем дерева специальных возможностей, который включает элементы управления ActiveX без окон, поддерживающие АВТОМАТИЗАЦИЮ пользовательского интерфейса. Интерфейс **иакцессиблехостинжелементпровидерс** содержит один метод [**жетембеддедфрагментрутс**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-getembeddedfragmentroots), который получает указатели интерфейса [**Иравелементпровидерфрагментрут**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot) для всех элементов управления ActiveX без окон модели автоматизации пользовательского интерфейса, размещенных в контейнере элементов управления.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Размещение элемента управления ActiveX без окон UI Automation](host-a-ui-automation-windowless-activex-control.md)
</dt> <dt>

[Специальные возможности элемента управления ActiveX без окон](windowless-activex-control-accessibility.md)
</dt> </dl>

 

 