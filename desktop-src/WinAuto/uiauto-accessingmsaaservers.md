---
title: Доступ к серверам Microsoft Active Accessibility
description: Прокси-сервер автоматизации пользовательского интерфейса Microsoft Active Accessibility — это программный компонент, который позволяет клиентам автоматизации пользовательского интерфейса Майкрософт взаимодействовать с серверами Microsoft Active Accessibility, которые реализуют интерфейс IAccessible изначально.
ms.assetid: 44690b16-4a9d-4e8b-865a-b428ad616b1e
keywords:
- Автоматизация пользовательского интерфейса, доступ Active Accessibility
- Модель автоматизации пользовательского интерфейса, Active Accessibility
- Прокси-сервер автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, прокси-сервер автоматизации пользовательского интерфейса
- Шаблон элемента управления Легацииакцессибле
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Легацииакцессибле
- Microsoft Active Accessibility
- Active Accessibility
- Клиенты, доступ к Active Accessibility серверам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e6f6ccbc29695b7ca5d1413025a50a7bcf4a9cf679dbcd6a0b8f3160ff0b399
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030774"
---
# <a name="accessing-microsoft-active-accessibility-servers"></a>Доступ к серверам Microsoft Active Accessibility

Прокси-сервер автоматизации пользовательского интерфейса Microsoft Active Accessibility — это программный компонент, который позволяет клиентам автоматизации пользовательского интерфейса Майкрософт взаимодействовать с серверами Microsoft Active Accessibility, которые реализуют интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) изначально. Прокси-сервер поддерживает шаблон элемента управления [легацииакцессибле](uiauto-implementinglegacyiaccessible.md) и предоставляет экземпляр интерфейса [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) для каждого обнаруженного сервера Microsoft Active Accessibility. Клиенты автоматизации пользовательского интерфейса используют методы, предоставляемые **иуиаутоматионлегацииакцессиблепаттерн** для доступа к свойствам и объектам Microsoft Active Accessibility, поддерживаемым сервером.

Если элемент модели автоматизации пользовательского интерфейса имеет базовую реализацию Microsoft Active Accessibility, клиент может получить указатель интерфейса [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) для элемента, передав идентификатор шаблона элемента управления [**UIA \_ легацииакцессиблепаттернид**](uiauto-controlpattern-ids.md) одному из следующих методов [**иуиаутоматионелемент**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) :

-   [**жеткачедпаттерн**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpattern)
-   [**жеткачедпаттернас**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas)
-   [**GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern)
-   [**жеткуррентпаттернас**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas)

Интерфейс [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) недоступен для элементов управления, основанных на модели автоматизации пользовательского интерфейса.

Интерфейс [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) позволяет клиентам автоматизации пользовательского интерфейса получать доступ к базовой реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) элемента Microsoft Active Accessibility. Однако интерфейс не поддерживает устаревшие или избыточные методы, имеющие функции автоматизации пользовательского интерфейса. Например, **иуиаутоматионлегацииакцессиблепаттерн** не имеет метода, эквивалентного [**IAccessible:: акклокатион**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) , так как текущее расположение элемента пользовательского интерфейса доступно из свойства баундингректангле UI Automation.

Метод [**иуиаутоматионлегацииакцессиблепаттерн:: жетиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) позволяет клиенту получить указатель интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) из элемента модели автоматизации пользовательского интерфейса. Обратная возможность также возможна с помощью методов [**иуиаутоматион:: елементфромиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessible) и [**Иуиаутоматион:: елементфромиакцессиблебуилдкаче**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromiaccessiblebuildcache) .

[**Иуиаутоматионлегацииакцессиблепаттерн:: жетиакцессибле**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationlegacyiaccessiblepattern-getiaccessible) возвращает **значение NULL** , если интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для элемента предоставлен прокси-объектом из OLEACC.dll или из модели автоматизации пользовательского интерфейса в Microsoft Active Accessibility Bridge.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Модель автоматизации пользовательского интерфейса и Active Accessibility](uiauto-msaa.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




