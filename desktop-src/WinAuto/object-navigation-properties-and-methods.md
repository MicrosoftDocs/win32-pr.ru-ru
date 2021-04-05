---
title: Свойства и методы навигации по объектам
description: Клиенты переходят от одного объекта к другому с помощью таких методов, как IAccessible Аккнавигате и IAccessible Акчиттест.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e7645d5179015280fd40f6618722191e588c74a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986373"
---
# <a name="object-navigation-properties-and-methods"></a>Свойства и методы навигации по объектам

Клиенты *переходят* от одного объекта к другому с помощью таких методов, как [**IAccessible:: аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) и [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Эти методы позволяют клиентам извлекать либо дочерний идентификатор, либо адрес интерфейса [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) другого объекта. Навигация позволяет клиентам исследовать взаимосвязь между объектами. Обратите внимание, что переход к другому объекту не изменяет выделенный фрагмент или фокус.

Интерфейс [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) предоставляет свойства и методы, поддерживающие следующие виды навигации:

-   [Иерархическая навигация](hierarchical-navigation.md)
-   [Пространственное и логическое перемещение](spatial-and-logical-navigation.md)
-   [Навигация с помощью проверки попадания и расположения на экране](navigation-through-hit-testing-and-screen-location.md)

 

 




