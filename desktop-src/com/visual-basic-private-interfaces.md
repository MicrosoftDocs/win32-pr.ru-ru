---
title: Visual Basic Частные интерфейсы
description: Visual Basic Частные интерфейсы
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd69e70d351245ebafa62d521a133726be568a0437f4e04ece4ef761535f4625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047712"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Частные интерфейсы

для категорий компонентов определяются два интерфейса, реализованные Visual Basic. Не ожидается, что элементы управления должны требовать эти категории, поскольку элементы управления могут предлагать альтернативные функции, если они недоступны.

интерфейс [**ивбформат**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) позволяет элементам управления лучше интегрироваться в среду Visual Basic при форматировании данных.

CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} \_ ВБФОРМАТ CATID

Интерфейс [**ивбжетконтрол**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) позволяет элементу управления перечислять другие элементы управления в форме VB.

CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} \_ ВБЖЕТКОНТРОЛ CATID

Два дополнительных частного интерфейса, [**ижетвбаобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) и [**ижетолеобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), описаны здесь, несмотря на то, что они не определяют категории компонентов. Использовать эти четыре интерфейса не рекомендуется, так как они не поддерживаются контейнерами, отличными от Visual Basic.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Категории компонентов](component-categories.md)
</dt> </dl>

 

 




