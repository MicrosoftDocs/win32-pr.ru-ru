---
title: аккнамеленгстулонг
description: аккнамеленгстулонг
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9df4b9001460b9ad96cf5c987a0e8c744ec8df183901494311275052ea4146
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327710"
---
# <a name="accnamelengthtoolong"></a>аккнамеленгстулонг

## <a name="text"></a>Текст

Имя элемента не должно возвращать строку длиннее {0} символа

## <a name="type"></a>Тип

Error

## <a name="description"></a>Описание

Имя элемента содержит слишком много символов. Например, метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, возвращает строку, превышающую ограничение в 32000 символов.

Эта проблема вызывает проблемы для тех, кто полагается на средство чтения с экрана и клавиатуру для навигации, так как элемент может иметь непонятное имя, не являющееся интуитивно понятным.

## <a name="possible-causes"></a>Возможные причины

Элемент или его родитель имеет неправильно назначенное имя или подпись.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> </dl>

 

 




