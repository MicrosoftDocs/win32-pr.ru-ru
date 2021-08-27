---
title: AccNavigate_ReturnedElementWithIncorrectParent
description: Аккнавигате \_ ретурнеделементвисинкорректпарент
ms.assetid: 44447E47-04D5-4784-B5E9-E8C62A9834CE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd040cda80e9dcb19543c8ee5134271693546dfdb8af76053b5a281340080765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122473"
---
# <a name="accnavigate_returnedelementwithincorrectparent"></a>Аккнавигате \_ ретурнеделементвисинкорректпарент

## <a name="text"></a>Текст

Вызов Аккнавигате ((Live Search), 0, НАВДИР \_ FIRSTCHILD) вернул (x-Gadget:///gadget.html) неверный родительский элемент ( \[ null \] ), а не (динамический поиск)

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

При вызове [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) для дочернего элемента, возвращенного [**аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (с помощью \_ констант навигации навдир FIRSTCHILD или навдир \_ LASTCHILD), возвращаемый родительский элемент не соответствует родительскому элементу, указанному в вызове **аккнавигате** .

![Пример недопустимой реализации MSAA, возвращающей неверный родительский элемент.](images/accchecker-invalid-msaa-parent.png)

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Аккнавигате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




