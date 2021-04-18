---
title: аккнамеконтаинсинвалидстринг
description: аккнамеконтаинсинвалидстринг
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691368"
---
# <a name="accnamecontainsinvalidstring"></a>аккнамеконтаинсинвалидстринг

## <a name="text"></a>Текст

Аккнаме не должно содержать строку {0}

## <a name="type"></a>Тип

Ошибка

## <a name="description"></a>Описание

Имя элемента содержит недопустимые символы (эти символы заменяются на Аккчеккер). Например, метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, возвращает строку, содержащую символы табуляции, новой строки или амперсанда.

Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет неправильно назначенное имя или подпись.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> </dl>

 

 




