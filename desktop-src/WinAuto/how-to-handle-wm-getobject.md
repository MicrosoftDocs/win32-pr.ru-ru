---
title: Работа с WM_GETOBJECT
description: При получении \_ сообщения WM GetObject, содержащего \_ клиент OBJID, сервер должен вернуть указатель на объект, реализующий IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777252"
---
# <a name="how-to-handle-wm_getobject"></a>Как работать с WM \_ GetObject

При получении сообщения [**WM \_ GetObject**](wm-getobject.md) , содержащего [**\_ клиент OBJID**](object-identifiers.md), сервер должен вернуть указатель на объект, реализующий [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible). Этот указатель является LRESULT, полученным путем вызова [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, в сочетании с библиотекой COM, выполняет соответствующий маршалирование и передает указатель интерфейса **IAccessible** с сервера клиенту.

Серверы должны правильно выполнять подсчет ссылок на доступном объекте. Помните, что при создании COM-объекта счетчик ссылок равен 1. Затем [**функции lresultfromobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) несколько раз увеличивает число ссылок. Все ссылки, созданные с помощью **функции lresultfromobject** , автоматически освобождаются, когда объект больше не нужен, но сервер отвечает за освобождение начальной ссылки, и если это не так, то объект никогда не будет уничтожен. В примерах в следующих разделах показано, как освободить ссылки на доступные объекты.

Обычно серверы обрабатывали [**WM \_ GetObject**](wm-getobject.md) одним из следующих способов:

-   [Создание новых объектов со специальными возможностями](create-new-accessible-objects.md)
-   [Повторное использование существующих указателей на объекты](reuse-existing-pointers-to-objects.md)
-   [Создание новых интерфейсов для одного и того же объекта](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> В этом разделе, как и в оставшейся части документации, при обсуждении указателя на интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) этот указатель может фактически быть указателем на прокси-объект, который заключает в оболочку интерфейс **IAccessible** . Дополнительные сведения об объектах прокси см. в разделе [Создание прокси-объектов](creating-proxy-objects.md).

 

Общие сведения о [**WM \_ GetObject**](wm-getobject.md)см. в статье [как \_ работает WM GetObject](how-wm-getobject-works.md).

 

 




