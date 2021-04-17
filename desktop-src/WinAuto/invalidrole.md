---
title: инвалидроле
description: инвалидроле
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531aa9917bd68b615c2cd2457d7a24bfc4af336c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710041"
---
# <a name="invalidrole"></a>инвалидроле

## <a name="text"></a>Текст

Целочисленное значение, возвращенное из Get \_ аккроле, не является допустимой константой роли, системой роли IE \_\_\*

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Элемент сообщает о недопустимой роли MSAA. Например, метод [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) возвращает целочисленное значение, которое не соответствует допустимой константе роли объекта (например, \_ системе роли \_ ).

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элементы могут быть неверно идентифицированы для пользователя.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет набор ролей MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Роли объектов**](object-roles.md)
</dt> </dl>

 

 




