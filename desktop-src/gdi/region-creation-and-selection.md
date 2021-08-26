---
description: Приложение создает регион, вызывая функцию, связанную с определенной фигурой. В следующей таблице показаны функции, связанные с каждой из стандартных форм.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Создание и выбор регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ce2711b2d1ae9dc6641748c72fd586d02e25964102a8c034593d6e60cbaa33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092694"
---
# <a name="region-creation-and-selection"></a>Создание и выбор регионов

Приложение создает регион, вызывая функцию, связанную с определенной фигурой. В следующей таблице показаны функции, связанные с каждой из стандартных форм.



| Фигура                                   | Функция                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Прямоугольная область                      | [**Креатеректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**креатеректргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**сетректргн**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Прямоугольная область с закругленными углами | [**креатераундректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Эллиптическая область                       | [**Креатиллиптикргн**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **креатиллиптикргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Многоугольная область                        | [**Креатеполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **креатеполиполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Каждая функция создания региона возвращает маркер, идентифицирующий новый регион. Приложение может использовать этот маркер для выбора региона в контексте устройства путем вызова функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) и предоставления этого маркера в качестве второго аргумента. После выбора региона в контексте устройства приложение может выполнять различные операции с ним.

 

 



