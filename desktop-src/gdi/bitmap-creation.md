---
description: Чтобы создать точечный рисунок, используйте функции Креатебитмап, Креатебитмапиндирект или Креатекомпатиблебитмап, Креатедибитмап и Креатедискардаблебитмап.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Создание растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db37dd14f8be47ebf93c7ee7f586c54c2e55ea900402d9c255a3196987aaed43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038262"
---
# <a name="bitmap-creation"></a>Создание растрового изображения

Чтобы создать точечный рисунок, используйте функции [**креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)или [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)и [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).

Эти функции позволяют указать ширину и высоту точечного рисунка в пикселях. Функция [**креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) и [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) также позволяет указать количество цветовых плоскостей и количество битов, необходимых для определения цвета. С другой стороны, функции [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) и [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) используют заданный контекст устройства для получения количества цветовых плоскостей и количества битов, необходимых для определения цвета.

Функция [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) создает точечный рисунок, зависящий от устройства, из точечного рисунка, не зависящего от устройства. Он содержит таблицу цветов, описывающую, как значения пикселей соответствуют значениям цвета RGB. Дополнительные сведения см. в разделе аппаратно [-зависимые точечные рисунки](device-dependent-bitmaps.md) и [аппаратно-независимые точечные рисунки](device-independent-bitmaps.md).

После создания растрового изображения нельзя изменить его размер, число цветовых плоскостей или число битов, необходимое для его распознавания.

Если точечный рисунок больше не нужен, вызовите функцию [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) , чтобы удалить ее.

 

 



