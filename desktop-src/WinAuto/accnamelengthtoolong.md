---
title: аккнамеленгстулонг
description: аккнамеленгстулонг
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700694"
---
# <a name="accnamelengthtoolong"></a>аккнамеленгстулонг

## <a name="text"></a>Текст

Имя элемента не должно возвращать строку длиннее {0} символа

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Имя элемента содержит слишком много символов. Например, метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, возвращает строку, превышающую ограничение в 32000 символов.

Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет неправильно назначенное имя или подпись.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> </dl>

 

 




