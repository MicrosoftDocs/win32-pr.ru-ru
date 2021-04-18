---
description: В регионах используются следующие функции.
ms.assetid: 3a42fc7a-4c07-4540-99a7-520f99532f33
title: Функции Region (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de0f55549f978dd2868f231b9ff042f6f825459d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984833"
---
# <a name="region-functions-windows-gdi"></a>Функции Region (Windows GDI)

В регионах используются следующие функции.



| Функция                                                       | Описание                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**комбинергн**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)                               | Объединяет два региона и сохраняет результат в третьем регионе.                                |
| [**креатиллиптикргн**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgn)                 | Создает эллиптическую область.                                                                |
| [**креатиллиптикргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createellipticrgnindirect) | Создает эллиптическую область.                                                                |
| [**креатеполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolygonrgn)                   | Создает многоугольную область.                                                                  |
| [**креатеполиполигонргн**](/windows/desktop/api/Wingdi/nf-wingdi-createpolypolygonrgn)           | Создает регион, состоящий из ряда многоугольников.                                         |
| [**креатеректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgn)                         | Создает прямоугольную область.                                                                |
| [**креатеректргниндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createrectrgnindirect)         | Создает прямоугольную область.                                                                |
| [**креатераундректргн**](/windows/desktop/api/Wingdi/nf-wingdi-createroundrectrgn)               | Создает прямоугольную область со скругленными углами.                                           |
| [**екуалргн**](/windows/desktop/api/Wingdi/nf-wingdi-equalrgn)                                   | Проверяет два указанных региона, чтобы определить, идентичны ли они.                    |
| [**ексткреатерегион**](/windows/desktop/api/Wingdi/nf-wingdi-extcreateregion)                     | Создает регион из указанной области и данных преобразования.                          |
| [**филлргн**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn)                                     | Заполняет область, используя указанную кисть.                                                 |
| [**фрамергн**](/windows/desktop/api/Wingdi/nf-wingdi-framergn)                                   | Рисует границу вокруг указанной области, используя указанную кисть.                     |
| [**жетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)                     | Извлекает режим заливки текущего многоугольника.                                                     |
| [**жетрегиондата**](/windows/desktop/api/Wingdi/nf-wingdi-getregiondata)                         | Заполняет указанный буфер данными, описывающими регион.                                    |
| [**жетргнбокс**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox)                                 | Извлекает ограничивающий прямоугольник указанной области.                                    |
| [**инвертргн**](/windows/desktop/api/Wingdi/nf-wingdi-invertrgn)                                 | Инвертирует цвета в указанной области.                                                  |
| [**оффсетргн**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)                                 | Перемещает регион по указанным смещениям.                                                     |
| [**паинтргн**](/windows/desktop/api/Wingdi/nf-wingdi-paintrgn)                                   | Закрашивает указанную область с помощью кисти, выбранной в данный момент в контексте устройства.   |
| [**птинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-ptinregion)                               | Определяет, находится ли указанная точка в указанной области.                       |
| [**ректинрегион**](/windows/desktop/api/Wingdi/nf-wingdi-rectinregion)                           | Определяет, находится ли какая-либо часть указанного прямоугольника в границах области. |
| [**сетполифиллмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode)                     | Задает режим заливки многоугольника для функций, заполняющих многоугольники.                                 |
| [**сетректргн**](/windows/desktop/api/Wingdi/nf-wingdi-setrectrgn)                               | Преобразует область в прямоугольную область с указанными координатами.                  |



 

 

 



