---
title: елементисчилдофпарентмулиплетимес
description: елементисчилдофпарентмулиплетимес
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfed0716423d8b1fef182be7cb0cb8ef122cf70cff6a574069fe40b63549f744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829553"
---
# <a name="elementischildofparentmulipletimes"></a>елементисчилдофпарентмулиплетимес

## <a name="text"></a>Текст

Аккпарент элемента имеет значение ( {0} ), но исходный элемент — это дочернее {1} время

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Когда метод [**Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) вызывается для целевого элемента, он несколько раз передает дочерний элемент того же родителя.

Эта проблема может вызвать проблемы с навигацией для автоматизированных средств, так как обходные элементы могут быть неустойчивыми и непредсказуемыми.

## <a name="possible-causes"></a>Возможные причины

Неправильная или недопустимая реализация MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккпарент**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




