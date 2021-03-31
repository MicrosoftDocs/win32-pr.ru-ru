---
title: Вариантнотинт (Чеккроле)
description: Вариантнотинт (Чеккроле)
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330219"
---
# <a name="variantnotint-checkrole"></a>Вариантнотинт (Чеккроле)

## <a name="text"></a>Текст

Вариант, возвращаемый методом, {0} должен быть, {1} но является {2} .

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Элемент сообщает о недопустимой роли MSAA. Например, метод [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) , используемый для получения роли MSAA элемента, должен возвращать целочисленное значение, представляющее одну из констант роли MSAA, но вместо этого возвращает другой вариант.

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элементы могут быть неверно идентифицированы для пользователя.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет набор ролей MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Роли объектов**](object-roles.md)
</dt> </dl>

 

 




