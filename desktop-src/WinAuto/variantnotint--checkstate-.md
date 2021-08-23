---
title: Вариантнотинт (свойство CheckState)
description: Вариантнотинт (свойство CheckState)
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3334a3609e9d64c1bb7109cc6f5bb52a2d09f9f9ac18cc41abf5d761f8e939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052172"
---
# <a name="variantnotint-checkstate"></a>Вариантнотинт (свойство CheckState)

## <a name="text"></a>Текст

Вариант, возвращаемый методом, {0} должен быть, {1} но является {2} .

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Элемент сообщает о недопустимом состоянии MSAA. Например, метод [**Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) , используемый для получения состояния MSAA элемента, должен возвращать целочисленное значение, представляющее одну из констант состояния MSAA, но вместо этого возвращает другой вариант.

Эта проблема вызывает проблемы для пользователей, которые используют средство чтения с экрана и клавиатуру для навигации, поскольку пользователь может сообщить о неправильном состоянии элемента.

## <a name="possible-causes"></a>Возможные причины

Для элемента или его родителя задано неправильное состояние MSAA.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккстате**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Константы состояния объектов**](object-state-constants.md)
</dt> </dl>

 

 




