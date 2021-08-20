---
title: елементсчилдхасдифферентпарент
description: елементсчилдхасдифферентпарент
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 885a5d930892d6e202764de8e58371f02690edee6715155f34533aaa110d7080
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829192"
---
# <a name="elementschildhasdifferentparent"></a>елементсчилдхасдифферентпарент

## <a name="text"></a>Текст

Дочерний элемент ( {0} ) имеет другой родительский {1} элемент (), чем element

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Эта ошибка означает, что при вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочерних элементов целевого элемента дочерние элементы не сообщают о единообразном родительском элементе.

![Пример дочерних элементов одного элемента с сообщением о нестабильном родительском элементе](images/accchecker-inconsistent-parent.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**акцессиблечилдрен**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




