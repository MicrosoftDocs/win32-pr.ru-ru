---
title: Функции для поставщиков
description: В этом разделе описываются функции поставщика автоматизации пользовательского интерфейса для приложений Microsoft Win32.
ms.assetid: 76012ec7-0114-4b6b-a35e-5cfde5b90230
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea0542c3d0b313e1bed8ec040924349e37a29fea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105681622"
---
# <a name="functions-for-providers"></a>Функции для поставщиков

В этом разделе описываются функции поставщика автоматизации пользовательского интерфейса для приложений Microsoft Win32.

## <a name="in-this-section"></a>Содержание раздела



| Функция                                                                                                 | Описание                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**уиаклиентсарелистенинг**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaclientsarelistening)<br/>                       | Возвращает значение, указывающее, подписано ли какое-либо клиентское приложение на события модели автоматизации пользовательского интерфейса Майкрософт.<br/>                                             |
| [**уиадисконнекталлпровидерс**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectallproviders)<br/>                         | Освобождает все ресурсы модели автоматизации пользовательского интерфейса, удерживаемые всеми поставщиками, связанными с вызывающим процессом. <br/>                                               |
| [**уиадисконнектпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiadisconnectprovider)<br/>                                 | Освобождает все ссылки, которые определенный поставщик содержит в объекты модели автоматизации пользовательского интерфейса.<br/>                                                                      |
| [**уиажетресерведмикседаттрибутевалуе**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservedmixedattributevalue)<br/> | Извлекает зарезервированное значение, указывающее, что значение атрибута Text модели автоматизации пользовательского интерфейса различается в пределах текстового диапазона.<br/>                                      |
| [**уиажетресерведнотсуппортедвалуе**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiagetreservednotsupportedvalue)<br/>     | Извлекает зарезервированное значение, указывающее, что свойство модели автоматизации пользовательского интерфейса или текстовый атрибут не поддерживается.<br/>                                               |
| [**уиахостпровидерфромхвнд**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)<br/>                     | Возвращает поставщик узла для окна.<br/>                                                                                                                    |
| [**уиаиакцессиблефромпровидер**](/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider)<br/>                   | Извлекает реализацию [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , которая предоставляет данные Microsoft Active Accessibility от имени поставщика автоматизации пользовательского интерфейса.<br/> |
| [**уиапровидерфорнонклиент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfornonclient)<br/>                     | Возвращает поставщик для всей неклиентской области окна или для элемента управления в области окна, не являющейся клиентской.<br/>                                      |
| [**уиапровидерфромиакцессибле**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaproviderfromiaccessible)<br/>               | Создает поставщик автоматизации пользовательского интерфейса на основе указанного объекта Microsoft Active Accessibility.<br/>                                                          |
| [**уиараисеасинкконтентлоадедевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseasynccontentloadedevent)<br/>     | Вызывается поставщиком для уведомления ядра автоматизации пользовательского интерфейса о том, что содержимое загружается асинхронно.<br/>                                                      |
| [**уиараисеаутоматионевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationevent)<br/>                     | Уведомляет прослушиватели о событии.<br/>                                                                                                                         |
| [**уиараисеаутоматионпропертичанжедевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent)<br/>    | Вызывается поставщиками для уведомления ядра автоматизации пользовательского интерфейса о том, что свойство элемента изменилось.<br/>                                                              |
| [**уиараисечанжесевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisechangesevent)<br/>                           | Вызывается поставщиками для уведомления ядра автоматизации пользовательского интерфейса о том, что произошло изменение.<br/>                                                                        |
| [**уиараисенотификатионевент**](https://www.bing.com/search?q=**UiaRaiseNotificationEvent**)<br/>             | Вызывается поставщиками для инициации события уведомления.<br/>                                                                                                   |
| [**уиараисеструктуречанжедевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisestructurechangedevent)<br/>         | Вызывается поставщиком для уведомления ядра автоматизации пользовательского интерфейса о том, что структура дерева изменилась.<br/>                                                              |
| [**уиараисетекстедиттекстчанжедевент**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent)<br/>   | Вызывается поставщиком для уведомления ядра автоматизации пользовательского интерфейса об изменении текста в элементе управления "текст" программными средствами.<br/>                                            |
| [**уиаретурнравелементпровидер**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)<br/>             | Возвращает интерфейс для поставщика автоматизации пользовательского интерфейса для окна.<br/>                                                                                           |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Поставщики автоматизации пользовательского интерфейса](uiauto-entry-uiautoprovidersforwin32apps.md)
</dt> </dl>

 

