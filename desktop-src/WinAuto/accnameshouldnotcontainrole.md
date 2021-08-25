---
title: аккнамешаулднотконтаинроле
description: аккнамешаулднотконтаинроле
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f09bd9ccdf27c5f52a45466b6b8145cfe23248cc175777f57202aac6530791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899734"
---
# <a name="accnameshouldnotcontainrole"></a>аккнамешаулднотконтаинроле

## <a name="text"></a>Текст

Имя элемента ( {0} ) не должно содержать текст роли элемента ( {1} )

## <a name="type"></a>Тип

Предупреждение

## <a name="description"></a>Описание

Имя элемента включает свою роль MSAA или тип элемента управления UIA. Например, это предупреждение может возникать, если метод [**Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) , используемый для получения имени MSAA элемента, Возвращает «роль \_ системы роли \_ \_ \* ».

Эта проблема вызывает проблемы для людей, которые используют средство чтения с экрана и клавиатуру для навигации, так как роль будет прочитана дважды или не может быть произношена или интуитивно понятна для пользователей.

## <a name="possible-causes"></a>Возможные причины

-   Элемент или его родитель имеет неправильно назначенное имя или подпись.
-   Элемент или его родитель имеет имя по умолчанию, которое не было изменено на понятное имя. Например, button1.
-   Разработчик не знает, что читатели экрана считывают имена.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IAccessible:: Get \_ аккнаме**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Свойство Name](name-property.md)
</dt> </dl>

 

 




