---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: Аккнавигате \_ ретурнеделементвисинкорректпарент
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3bdff54c9c594cde4e6e57fe1886a900c913eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104558773"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>Аккнавигате \_ ретурнеделементвисинкорректпарент

## <a name="text"></a>Текст

Вызов Аккнавигате ((Live Search), 0, НАВДИР \_ FIRSTCHILD) вернул (x-Gadget:///gadget.html) неверный родительский элемент ( \[ null \] ), а не (динамический поиск)

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

При вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочернего элемента, возвращенного [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (с помощью \_ констант навигации навдир FIRSTCHILD или навдир \_ LASTCHILD), возвращаемый родительский элемент не соответствует родительскому элементу, указанному в вызове **аккнавигате** .

![Пример недопустимой реализации MSAA, возвращающей неверный родительский элемент.](images/accchecker-invalid-msaa-parent.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




