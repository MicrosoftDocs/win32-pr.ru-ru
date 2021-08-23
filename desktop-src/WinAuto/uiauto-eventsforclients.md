---
title: Подписка на события модели автоматизации пользовательского интерфейса
description: Автоматизация пользовательского интерфейса Майкрософт позволяет клиентам подписываться на интересующие вас события. Эта возможность повышает производительность, устраняя необходимость постоянного опроса элементов пользовательского интерфейса в системе, чтобы проверить, изменились ли сведения, структура или состояние.
ms.assetid: 7019ecb8-6123-4e00-926c-6725d7e71385
keywords:
- Клиенты, события модели автоматизации пользовательского интерфейса
- Клиенты, события для автоматизации пользовательского интерфейса
- Модель автоматизации пользовательского интерфейса, события для клиентов
- Модель автоматизации пользовательского интерфейса, события клиента
- Автоматизация пользовательского интерфейса, подписка на события
- Модель автоматизации пользовательского интерфейса, методы подписки
- Модель автоматизации пользовательского интерфейса, примеры кода
- Модель автоматизации пользовательского интерфейса, примеры
- Модель автоматизации пользовательского интерфейса, примеры
- подписка на события модели автоматизации пользовательского интерфейса
- события, подписка на модель автоматизации пользовательского интерфейса
- Примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a0e8dd4cb2d810ad8423c1fa4f75020a9489ceb72acbe1483cb439e943b5676
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505304"
---
# <a name="subscribing-to-ui-automation-events"></a>Подписка на события модели автоматизации пользовательского интерфейса

Автоматизация пользовательского интерфейса Майкрософт позволяет клиентам подписываться на интересующие вас события. Эта возможность повышает производительность, устраняя необходимость постоянного опроса элементов пользовательского интерфейса в системе, чтобы проверить, изменились ли сведения, структура или состояние.

Эффективность также повышается благодаря возможности прослушивания событий только в заданной области. Например, клиент может прослушивать изменения выбора на элементе списка, в самом списке или во всем диалоговом окне.

> [!Note]  
> Не считайте, что все возможные события вызываются поставщиком автоматизации пользовательского интерфейса. например, не все изменения свойств приводят к возникновению событий стандартными поставщиками прокси для Windows Forms и элементов управления Microsoft Win32.

 

Более широкое представление о событиях модели автоматизации пользовательского интерфейса см. в разделе [Общие сведения о событиях модели автоматизации пользовательского интерфейса](uiauto-eventsoverview.md).

> [!Note]  
> Перед реализацией обработчика событий необходимо ознакомиться с проблемами, описанными в разделе [Общие сведения о проблемах с потоками](uiauto-threading.md).

 

В этом разделе содержатся следующие подразделы.

-   [Регистрация обработчиков событий](#registering-event-handlers)
-   [Примеры](#examples)
-   [Связанные темы](#related-topics)

## <a name="registering-event-handlers"></a>Регистрация обработчиков событий

Клиентские приложения подписываются на события определенного типа путем регистрации обработчика событий с помощью одного из следующих методов [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .



| Метод подписки                                                                                                                                                                                                | Тип события       | Интерфейс обратного вызова                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------------------------------------------------------------------------------------------------|
| [**аддфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler)                                                                                                                            | Изменение фокуса     | [**иуиаутоматионфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler)         |
| [**Аддпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler), [ **аддпропертичанжедевенсандлернативеаррай**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray) | Изменение свойства  | [**иуиаутоматионпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler)   |
| [**аддструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler)                                                                                                                    | Изменение структуры | [**иуиаутоматионструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) |
| [**адднотификатионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler)                                                                                                                           | Уведомление     | [**иуиаутоматионнотификатионевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationnotificationeventhandler)         |
| [**аддаутоматионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler)                                                                                                                                | Другие события     | [**иуиаутоматионевенсандлер**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationeventhandler)                                 |



 

Когда клиент добавляет обработчик событий для всех потомков ([**TreeScope \_ потомков**](/windows/desktop/api/UIAutomationClient/ne-uiautomationclient-treescope)), модель автоматизации пользовательского интерфейса добавляет только один обработчик для корня поддерева, а обработчик прослушивает все потомки. Автоматизация пользовательского интерфейса не добавляет обработчики событий рекурсивно.

Когда клиент вызывает метод [**иуиаутоматион:: ремовеаллевенсандлерс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers) , модель автоматизации пользовательского интерфейса удаляет все обработчики событий из клиентского процесса.

Для получения и обработки событий необходимо реализовать объект обработки событий, который предоставляет интерфейс обратного вызова, и необходимо зарегистрировать объект, вызвав метод регистрации события, такой как [**иуиаутоматион:: аддпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler). Интерфейс обратного вызова имеет единственный метод; Модель автоматизации пользовательского интерфейса вызывает этот метод при обработке события.

При завершении работы или когда события модели автоматизации пользовательского интерфейса больше не интересуются приложением, клиенты автоматизации пользовательского интерфейса должны вызывать один или несколько из следующих методов [**иуиаутоматион**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) .

> [!Note]  
> Клиент автоматизации пользовательского интерфейса не должен использовать несколько потоков для добавления или удаления обработчиков событий. Непредвиденное поведение может возникнуть, если один или несколько обработчиков событий добавляются или удаляются в рамках одного и того же клиентского процесса.

 



| Метод                                                                                                | Описание                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ремовеаутоматионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removeautomationeventhandler)             | Отменяет регистрацию обработчика событий, зарегистрированного с помощью [**аддаутоматионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addautomationeventhandler).                                                                                                                                  |
| [**ремовефокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removefocuschangedeventhandler)         | Отменяет регистрацию обработчика событий, зарегистрированного с помощью [**аддфокусчанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addfocuschangedeventhandler).                                                                                                                              |
| [**ремовепропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removepropertychangedeventhandler)   | Отменяет регистрацию обработчика событий, зарегистрированного с помощью [**аддпропертичанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) или [**аддпропертичанжедевенсандлернативеаррай**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray). |
| [**ремовеструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removestructurechangedeventhandler) | Отменяет регистрацию обработчика событий, зарегистрированного с помощью [**аддструктуречанжедевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addstructurechangedeventhandler).                                                                                                                      |
| [**ремовенотификатионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-removenotificationeventhandler)        | Отменяет регистрацию обработчика событий, Богданов зарегистрированных с помощью [**адднотификатионевенсандлер**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation5-addnotificationeventhandler).                                                                                                                            |
| [**ремовеаллевенсандлерс**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-removealleventhandlers)                         | Отменяет регистрацию всех зарегистрированных обработчиков событий.                                                                                                                                                                                                                                      |



 

Событие может доставляться в обработчик событий после отмены подписки обработчика, если событие получено одновременно с запросом на отмену подписки на событие. Рекомендуется следовать стандарту модели COM и избегать уничтожения объекта обработчика событий до тех пор, пока его число ссылок не достигнет нуля. Уничтожение обработчика событий сразу после отмены подписки на события может привести к нарушению прав доступа, если событие доставляется позднее.

## <a name="examples"></a>Примеры

Примеры кода, демонстрирующие обработку событий автоматизации пользовательского интерфейса, см. [в разделе Реализация обработчиков событий](uiauto-howto-implement-event-handlers.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Обзор событий автоматизации пользовательского интерфейса](uiauto-eventsoverview.md)
</dt> <dt>

[Основные сведения о проблемах с потоками](uiauto-threading.md)
</dt> </dl>

 

 




