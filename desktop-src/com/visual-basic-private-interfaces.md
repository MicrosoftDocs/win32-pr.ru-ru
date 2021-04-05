---
title: Visual Basic закрытых интерфейсов
description: Visual Basic закрытых интерфейсов
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068620"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic закрытых интерфейсов

Для категорий компонентов определяются два интерфейса, реализованные Visual Basic. Не ожидается, что элементы управления должны требовать эти категории, поскольку элементы управления могут предлагать альтернативные функции, если они недоступны.

Интерфейс [**ивбформат**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) позволяет элементам управления лучше интегрироваться в среду Visual Basic при форматировании данных.

CATID-{02496840-3AC4-11cf-87B9-00AA006C8166} \_ ВБФОРМАТ CATID

Интерфейс [**ивбжетконтрол**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) позволяет элементу управления перечислять другие элементы управления в форме VB.

CATID-{02496841-3AC4-11cf-87B9-00AA006C8166} \_ ВБЖЕТКОНТРОЛ CATID

Два дополнительных частного интерфейса, [**ижетвбаобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) и [**ижетолеобжект**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), описаны здесь, несмотря на то, что они не определяют категории компонентов. Использовать эти четыре интерфейса не рекомендуется, так как они не поддерживаются контейнерами, отличными от Visual Basic.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Категории компонентов](component-categories.md)
</dt> </dl>

 

 




