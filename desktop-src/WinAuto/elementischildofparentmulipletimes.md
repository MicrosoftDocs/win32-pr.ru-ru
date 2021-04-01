---
title: елементисчилдофпарентмулиплетимес
description: елементисчилдофпарентмулиплетимес
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104259108"
---
# <a name="elementischildofparentmulipletimes"></a>елементисчилдофпарентмулиплетимес

## <a name="text"></a>Текст

Аккпарент элемента имеет значение ( {0} ), но исходный элемент — это дочернее {1} время

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Когда метод [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) вызывается для целевого элемента, он несколько раз передает дочерний элемент того же родителя.

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




