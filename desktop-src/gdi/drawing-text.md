---
description: Рисование текста
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Рисование текста (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811968"
---
# <a name="drawing-text-windows-gdi"></a>Рисование текста (Windows GDI)

После того как приложение выберет подходящий шрифт, задает необходимые параметры форматирования текста и вычислит необходимые значения ширины и высоты символов для строки текста, он может начать рисовать символы и символы, вызвав любую из функций вывода текста:

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [дравтекстекс](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [Текст](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [таббедтекстаут](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Когда приложение вызывает одну из этих функций, операционная система передает вызов модулю Graphics, который, в свою очередь, передает вызов соответствующему драйверу устройства. На уровне драйвера устройства все эти вызовы поддерживаются одним или несколькими вызовами функции [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) или [текста](/windows/desktop/api/Wingdi/nf-wingdi-textouta) драйвера. Приложение обеспечит самое быстрое выполнение путем вызова [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), которое быстро преобразуется в вызов **ExtTextOut** для устройства. Однако существуют экземпляры, когда приложение должно вызвать одну из других трех функций. Например, чтобы нарисовать несколько строк текста внутри границ заданной прямоугольной области, более эффективно вызывать [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Чтобы создать таблицу с несколькими столбцами с выровненными столбцами текста, более эффективно вызывать [**таббедтекстаут**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
