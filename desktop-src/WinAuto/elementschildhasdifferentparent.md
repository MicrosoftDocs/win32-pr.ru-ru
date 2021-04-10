---
title: елементсчилдхасдифферентпарент
description: елементсчилдхасдифферентпарент
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332656"
---
# <a name="elementschildhasdifferentparent"></a>елементсчилдхасдифферентпарент

## <a name="text"></a>Текст

Дочерний элемент ( {0} ) имеет другой родительский {1} элемент (), чем element

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Эта ошибка означает, что при вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочерних элементов целевого элемента дочерние элементы не сообщают о единообразном родительском элементе.

![Пример дочерних элементов одного элемента с сообщением о нестабильном родительском элементе](images/accchecker-inconsistent-parent.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




