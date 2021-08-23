---
title: Интерфейсы (платформа Ribbon)
description: справочная документация по интерфейсам платформы ленты Windows.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e159d66b8eac8501f231e847555823da431e7d1be3417e0fb803f0929be679bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028672"
---
# <a name="interfaces-ribbon-framework"></a>Интерфейсы (платформа Ribbon)

справочная документация по интерфейсам платформы ленты Windows.

### <a name="interfaces"></a>Интерфейсы



| Раздел                                                                                  | Содержимое                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication)                       | Интерфейс [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) реализуется приложением и определяет методы точки входа обратного вызова для платформы Ribbon.<br/>                                                                                                                                                                                                              |
| [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)                         | Интерфейс [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) реализуется платформой Ribbon. Интерфейс **иуиколлектион** определяет методы для динамического управления элементами управления на основе коллекций, таких как различные [коллекции](ribbon-controls-galleries.md) лент и панель быстрого доступа (QAT) во время выполнения.<br/>                                              |
| [**иуиколлектиончанжедевент**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) | Интерфейс [**иуиколлектиончанжедевент**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) реализуется приложением и определяет метод, необходимый для управления изменениями в коллекции во время выполнения.<br/>                                                                                                                                                                                |
| [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler)                 | Интерфейс [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) реализуется приложением и определяет методы для сбора сведений о командах и обработки событий команд из платформы Ribbon.<br/>                                                                                                                                                              |
| [**иуиконтекстуалуи**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)                     | Интерфейс [**иуиконтекстуалуи**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui)реализуется платформой Ribbon и предоставляет основные функциональные возможности для [контекстного представления контекста](windowsribbon-controls-contextpopup.md).<br/>                                                                                                                                                                       |
| [**иуифрамеворк**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)                           | Интерфейс [**иуифрамеворк**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) реализуется платформой Ribbon и определяет методы, предоставляющие основные функциональные возможности для платформы.<br/>                                                                                                                                                                                                     |
| [**иуиимаже**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage)                                   | Интерфейс [**иуиимаже**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) реализуется приложением и определяет метод для получения изображения, отображаемого на ленте и в КОНТЕКСТном интерфейсе всплывающего окна платформы Ribbon.<br/>                                                                                                                                                                          |
| [**иуиимажефромбитмап**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap)               | [**Иуиимажефромбитмап**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimagefrombitmap) — это фабричный интерфейс, реализованный платформой Ribbon, который определяет метод создания объекта [**иуиимаже**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiimage) .<br/>                                                                                                                                                             |
| [**иуириббон**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon)                                 | Интерфейс [**иуириббон**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiribbon) реализуется платформой Ribbon и предоставляет возможность указывать параметры и свойства для ленты. <br/>                                                                                                                                                                                                               |
| [**иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)           | [**Иуисимплепропертисет**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)— это интерфейс только для чтения, определяющий метод получения значения, идентифицируемого ключом свойства. Этот интерфейс реализуется платформой Ribbon, а также реализуется ведущим приложением для каждого элемента в объекте [**иуиколлектион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)коллекции элементов.<br/> |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Windows Справочник по платформе ленты](windowsribbon-reference-entry.md)
</dt> </dl>

 

