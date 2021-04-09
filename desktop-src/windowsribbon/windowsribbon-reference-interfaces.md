---
title: Интерфейсы (платформа Ribbon)
description: Справочная документация по интерфейсам платформы Windows Ribbon.
ms.assetid: d5fd6e4f-ca10-4010-aab4-d2728b0ac53c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c168a342b7f362d2d679d578a88011c9d14977
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134994"
---
# <a name="interfaces-ribbon-framework"></a>Интерфейсы (платформа Ribbon)

Справочная документация по интерфейсам платформы Windows Ribbon.

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



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по платформе ленты Windows](windowsribbon-reference-entry.md)
</dt> </dl>

 

