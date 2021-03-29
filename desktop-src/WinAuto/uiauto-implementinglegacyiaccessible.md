---
title: Шаблон элемента управления Легацииакцессибле
description: Описывает правила и соглашения для использования Илегацииакцессиблепровидер, включая сведения о свойствах, методах и событиях.
ms.assetid: 4d66b9b8-ddbe-4bbc-b475-72dad1fe9393
keywords:
- Модель автоматизации пользовательского интерфейса, реализация шаблона элемента управления Легацииакцессибле
- Модель автоматизации пользовательского интерфейса, шаблон элемента управления Легацииакцессибле
- Модель автоматизации пользовательского интерфейса, Илегацииакцессиблепровидер
- илегацииакцессиблепровидер
- реализация шаблонов элементов управления Легацииакцессибле модели автоматизации пользовательского интерфейса
- Шаблоны элементов управления Легацииакцессибле
- шаблоны элементов управления, Илегацииакцессиблепровидер
- шаблоны элементов управления, реализация модели автоматизации пользовательского интерфейса Легацииакцессибле
- шаблоны элементов управления, Легацииакцессибле
- интерфейсы, Илегацииакцессиблепровидер
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cffbd205b072f6f900ea5b5eb5a9f6ddfb5ddc5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777711"
---
# <a name="legacyiaccessible-control-pattern"></a>Шаблон элемента управления Легацииакцессибле

Описывает правила и соглашения для использования [**илегацииакцессиблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider), включая сведения о свойствах, методах и событиях. Шаблон элемента управления **легацииакцессибле** поддерживается в Microsoft Active Accessibility для прокси-сервера автоматизации пользовательского интерфейса Майкрософт.

Поставщики приложений и элементов управления никогда не реализуют интерфейс [**илегацииакцессиблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider) .

Шаблон элемента управления **легацииакцессибле** предоставляет интерфейс [**иуиаутоматионлегацииакцессиблепаттерн**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern) клиентам автоматизации пользовательского интерфейса, что позволяет им получить доступ к базовой реализации [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) для некоторых элементов пользовательского интерфейса. Однако **иуиаутоматионлегацииакцессиблепаттерн** не поддерживает методы, которые устарели или избыточны с помощью функций автоматизации пользовательского интерфейса.

В этом разделе содержатся следующие подразделы.

-   [Правила и соглашения реализации](#implementation-guidelines-and-conventions)
-   [Элементы шаблона элемента управления **легацииакцессибле**](#members-of-the-legacyiaccessible-control-pattern)
-   [См. также](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Правила и соглашения реализации

Ни один из приложений или элементов управления не реализует [**илегацииакцессиблепровидер**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ilegacyiaccessibleprovider). Платформа автоматизации пользовательского интерфейса автоматически предоставляет реализацию поставщика для собственного сервера Microsoft Active Accessibility.

Шаблон элемента управления **легацииакцессибле** недоступен для элементов управления, основанных на модели автоматизации пользовательского интерфейса.

## <a name="members-of-the-legacyiaccessible-control-pattern"></a>Элементы шаблона элемента управления **легацииакцессибле**

Следующие свойства, методы и события являются членами шаблона элемента управления **легацииакцессибле** . Заметки предназначены для клиентов автоматизации пользовательского интерфейса.



| Элементы                                                                        | Тип члена | Примечания                                                                                                                                |
|--------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [**чилдид**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_childid)                   | Свойство    | Возвращает **чилдид \_ Self** (0) для дочернего объекта.                                                                                |
| [**DefaultAction**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_defaultaction)       | Свойство    | Нет                                                                                                                                 |
| [**Описание**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_description)           | Свойство    | Нет                                                                                                                                 |
| [**Справка**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_help)                         | Свойство    | Нет                                                                                                                                 |
| [**KeyboardShortcut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_keyboardshortcut) | Свойство    | Нет                                                                                                                                 |
| [**Имя**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_name)                         | Свойство    | Нет                                                                                                                                 |
| [**Role**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_role)                         | Свойство    | Используйте функцию [**жетролетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) для получения локализованной строки.                                                    |
| [**Выборка**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getselection)         | Метод      | Извлекает указатель интерфейса [**иуиаутоматионелементаррай**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray) .                                |
| [**State**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_state)                       | Свойство    | Используйте функцию [**жетстатетекст**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta) для получения локализованной строки.                                                  |
| [**Значение**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-get_value)                       | Свойство    | Нет                                                                                                                                 |
| [**додефаултактион**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-dodefaultaction)   | Метод      | Нет                                                                                                                                 |
| [**жетиакцессибле**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-getiaccessible)     | Метод      | Нет                                                                                                                                 |
| [**Метьте**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-select)                     | Метод      | Флаг выбора — это значение Microsoft Active Accessibility **селфлаг** . Дополнительные сведения см. в разделе [константы селфлаг](selflag.md). |
| [**SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ilegacyiaccessibleprovider-setvalue)                 | Метод      | Нет                                                                                                                                 |



 

Этот шаблон элемента управления не имеет связанных событий.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Типы элементов управления и поддерживаемые ими шаблоны элементов управления](uiauto-controlpatternmapping.md)
</dt> <dt>

[Общие сведения о шаблонах элементов управления модели автоматизации пользовательского интерфейса](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Общие сведения о дереве модели автоматизации пользовательского интерфейса](uiauto-treeoverview.md)
</dt> </dl>

 

 




