---
title: Работа с WM_GETOBJECT
description: При получении \_ сообщения WM GetObject, содержащего \_ клиент OBJID, сервер должен вернуть указатель на объект, реализующий IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f066ee42ffaeee2d585ac5480e5af31acf14c87ba9994d3d338b65e6cf427a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052731"
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

 

 




