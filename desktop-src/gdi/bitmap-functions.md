---
description: С точечными рисунками используются следующие функции.
ms.assetid: ef3abc8a-5d95-41d0-8eb6-47719d472414
title: Функции точечного рисунка (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e61ef02f5065d746f0d82a7b3352c3445ebf61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997434"
---
# <a name="bitmap-functions-windows-gdi"></a>Функции точечного рисунка (Windows GDI)

С точечными рисунками используются следующие функции.



| Функция                                                 | Описание                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [**алфабленд**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend)                         | Отображает точечный рисунок с прозрачными или полупрозрачными пикселами.  |
| [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt)                                 | Выполняет перенос битового блока.                                 |
| [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap)                     | Создает точечный рисунок.                                              |
| [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)     | Создает точечный рисунок.                                              |
| [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) | Создает точечный рисунок, совместимый с устройством.                     |
| [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)                 | Создает аппаратно-зависимый точечный рисунок (DDB) из DIB.            |
| [**креатедибсектион**](/windows/desktop/api/Wingdi/nf-wingdi-createdibsection)             | Создает DIB, который приложения могут выполнять запись непосредственно.         |
| [**екстфлудфилл**](/windows/desktop/api/Wingdi/nf-wingdi-extfloodfill)                     | Заполняет область области отображения текущей кистью.   |
| [**жетбитмапдименсионекс**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapdimensionex)     | Возвращает размеры точечного рисунка.                               |
| [**жетдибколортабле**](/windows/desktop/api/Wingdi/nf-wingdi-getdibcolortable)             | Получает значения цвета RGB из битовой карты раздела DIB.          |
| [**жетдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-getdibits)                           | Копирует растровое изображение в буфер.                                 |
| [**С точкой**](/windows/desktop/api/Wingdi/nf-wingdi-getpixel)                             | Возвращает значение цвета RGB пикселя в заданной координате.   |
| [**жетстретчблтмоде**](/windows/desktop/api/Wingdi/nf-wingdi-getstretchbltmode)           | Возвращает текущий режим растяжения.                              |
| [**градиентфилл**](/windows/desktop/api/WinGdi/nf-wingdi-gradientfill)                     | Выполняет заливку прямоугольников и структур треугольников.                       |
| [**лоадбитмап**](/windows/desktop/api/Winuser/nf-winuser-loadbitmapa)                         | Загружает точечный рисунок из исполняемого файла модуля.                |
| [**маскблт**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt)                               | Объединяет цветовые данные в исходном и целевом точечных рисунках. |
| [**плгблт**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt)                                 | Выполняет перенос битового блока.                                 |
| [**сетбитмапдименсионекс**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapdimensionex)     | Устанавливает предпочтительные размеры растрового изображения.                     |
| [**сетдибколортабле**](/windows/desktop/api/Wingdi/nf-wingdi-setdibcolortable)             | Устанавливает значения RGB в формате DIB.                                      |
| [**сетдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-setdibits)                           | Задает пикселы в точечном рисунке, используя цветовые данные из DIB.       |
| [**сетдибитстодевице**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice)           | Задает Пиксели прямоугольника, используя цветовые данные из DIB.    |
| [**SetPixel**](/windows/desktop/api/Wingdi/nf-wingdi-setpixel)                             | Задает цвет для пикселя.                                    |
| [**сетпикселв**](/windows/desktop/api/Wingdi/nf-wingdi-setpixelv)                           | Задает в пикселе наилучшее приближение цвета.             |
| [**сетстретчблтмоде**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode)           | Задает режим растяжения растрового изображения.                               |
| [**стретчблт**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)                         | Копирует точечный рисунок и растягивает его или сжимает.                |
| [**стретчдибитс**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits)                   | Копирует данные цвета в DIB.                                |
| [**транспарентблт**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt)                 | Выполняет побитовую пересылку данных цвета.                   |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Следующие функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Microsoft Windows:

-   [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap)
-   [**флудфилл**](/windows/desktop/api/Wingdi/nf-wingdi-floodfill)
-   [**жетбитмапбитс**](/windows/desktop/api/Wingdi/nf-wingdi-getbitmapbits)
-   [**сетбитмапбитс**](/windows/desktop/api/Wingdi/nf-wingdi-setbitmapbits)

 

 



