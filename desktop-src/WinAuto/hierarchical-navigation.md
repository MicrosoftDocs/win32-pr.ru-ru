---
title: Иерархическая навигация
description: Часто клиенты должны перемещаться между объектами на основе их отношений типа «родители-потомки». Например, клиент может уже иметь сведения об элементе управления ToolBar, но не содержать сведения о кнопках, содержащихся в ней.
ms.assetid: 7adf803c-140a-4f7d-8dc5-71abca706800
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c48ae366f2dd1caba4dfa6ff69aa1f57a23cbf07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253252"
---
# <a name="hierarchical-navigation"></a>Иерархическая навигация

Часто клиенты должны перемещаться между объектами на основе их отношений типа «родители-потомки». Например, клиент может уже иметь сведения об элементе управления ToolBar, но не содержать сведения о кнопках, содержащихся в ней.

Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляет иерархические связи между объектами. Клиенты могут переходить от родительского объекта к его дочерним объектам или из дочернего объекта в родительский объект путем вызова метода [**IAccessible:: Get \_ Аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) или [**IAccessible:: Get \_ аккчилд**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild).

 

 




