---
title: инвалидроле
description: инвалидроле
ms.assetid: B0707B90-59D6-4F86-8CBB-1DF57FDBEE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acecf91e90f93ccb1d220e9b2d91cbaa012b8d436b18a910daa73bf6ca3f1fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860004"
---
# <a name="invalidrole"></a>инвалидроле

## <a name="text"></a>Текст

Целочисленное значение, возвращенное из Get \_ аккроле, не является допустимой константой роли, системой роли IE \_\_\*

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Элемент сообщает о недопустимой роли MSAA. Например, метод [**Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) возвращает целочисленное значение, которое не соответствует допустимой константе роли объекта (например, \_ системе роли \_ ).

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку элементы могут быть неверно идентифицированы для пользователя.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет набор ролей MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккроле**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**Роли объектов**](object-roles.md)
</dt> </dl>

 

 




