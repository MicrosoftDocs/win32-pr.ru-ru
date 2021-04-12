---
title: Вариантнотинт (свойство CheckState)
description: Вариантнотинт (свойство CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253284"
---
# <a name="variantnotint-checkstate"></a>Вариантнотинт (свойство CheckState)

## <a name="text"></a>Текст

Вариант, возвращаемый методом, {0} должен быть, {1} но является {2} .

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Элемент сообщает о недопустимом состоянии MSAA. Например, метод [**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) , используемый для получения состояния MSAA элемента, должен возвращать целочисленное значение, представляющее одну из констант состояния MSAA, но вместо этого возвращает другой вариант.

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку пользователь может сообщить о неправильном состоянии элемента.

## <a name="possible-causes"></a>Возможные причины

Для элемента или его родителя задано неправильное состояние MSAA.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Константы состояния объектов**](object-state-constants.md)
</dt> </dl>

 

 




