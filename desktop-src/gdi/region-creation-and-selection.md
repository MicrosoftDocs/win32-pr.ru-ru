---
description: Приложение создает регион, вызывая функцию, связанную с определенной фигурой. В следующей таблице показаны функции, связанные с каждой из стандартных форм.
ms.assetid: e94ae371-8365-4e42-ac8c-04c3928fcffb
title: Создание и выбор регионов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27a7887e41a04a62015fa3fc9d82f5beeb01d6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984836"
---
# <a name="region-creation-and-selection"></a>Создание и выбор регионов

Приложение создает регион, вызывая функцию, связанную с определенной фигурой. В следующей таблице показаны функции, связанные с каждой из стандартных форм.



| Фигурная                                   | Функция                                                                                                                         |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Прямоугольная область                      | [**Креатеректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn), [**креатеректргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect), [**сетректргн**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn) |
| Прямоугольная область с закругленными углами | [**креатераундректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)                                                                                 |
| Эллиптическая область                       | [**Креатиллиптикргн**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn), [ **креатиллиптикргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect)                   |
| Многоугольная область                        | [**Креатеполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn), [ **креатеполиполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)                               |



 

Каждая функция создания региона возвращает маркер, идентифицирующий новый регион. Приложение может использовать этот маркер для выбора региона в контексте устройства путем вызова функции [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) и предоставления этого маркера в качестве второго аргумента. После выбора региона в контексте устройства приложение может выполнять различные операции с ним.

 

 



