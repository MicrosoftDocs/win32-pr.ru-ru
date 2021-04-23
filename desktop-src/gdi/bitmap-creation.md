---
description: Чтобы создать точечный рисунок, используйте функции Креатебитмап, Креатебитмапиндирект или Креатекомпатиблебитмап, Креатедибитмап и Креатедискардаблебитмап.
ms.assetid: 313072fc-68c9-4ece-95bb-2748ccbd7f57
title: Создание растрового изображения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00a0bc5a39d1b5e6053a34a87c28d6792a42b0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263698"
---
# <a name="bitmap-creation"></a><span data-ttu-id="dd719-103">Создание растрового изображения</span><span class="sxs-lookup"><span data-stu-id="dd719-103">Bitmap Creation</span></span>

<span data-ttu-id="dd719-104">Чтобы создать точечный рисунок, используйте функции [**креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect)или [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) , [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap)и [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span><span class="sxs-lookup"><span data-stu-id="dd719-104">To create a bitmap, use the [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap), [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect), or [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) function, [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap), and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap).</span></span>

<span data-ttu-id="dd719-105">Эти функции позволяют указать ширину и высоту точечного рисунка в пикселях.</span><span class="sxs-lookup"><span data-stu-id="dd719-105">These functions allow you to specify the width and height, in pixels, of the bitmap.</span></span> <span data-ttu-id="dd719-106">Функция [**креатебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) и [**креатебитмапиндирект**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) также позволяет указать количество цветовых плоскостей и количество битов, необходимых для определения цвета.</span><span class="sxs-lookup"><span data-stu-id="dd719-106">The [**CreateBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmap) and [**CreateBitmapIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbitmapindirect) function also allow you to specify the number of color planes and the number of bits required to identify the color.</span></span> <span data-ttu-id="dd719-107">С другой стороны, функции [**креатекомпатиблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) и [**креатедискардаблебитмап**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) используют заданный контекст устройства для получения количества цветовых плоскостей и количества битов, необходимых для определения цвета.</span><span class="sxs-lookup"><span data-stu-id="dd719-107">On the other hand, the [**CreateCompatibleBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatiblebitmap) and [**CreateDiscardableBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-creatediscardablebitmap) functions use a specified device context to obtain the number of color planes and the number of bits required to identify the color.</span></span>

<span data-ttu-id="dd719-108">Функция [**креатедибитмап**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) создает точечный рисунок, зависящий от устройства, из точечного рисунка, не зависящего от устройства.</span><span class="sxs-lookup"><span data-stu-id="dd719-108">The [**CreateDIBitmap**](/windows/desktop/api/Wingdi/nf-wingdi-createdibitmap) function creates a device-dependent bitmap from a device-independent bitmap.</span></span> <span data-ttu-id="dd719-109">Он содержит таблицу цветов, описывающую, как значения пикселей соответствуют значениям цвета RGB.</span><span class="sxs-lookup"><span data-stu-id="dd719-109">It contains a color table that describes how pixel values correspond to RGB color values.</span></span> <span data-ttu-id="dd719-110">Дополнительные сведения см. в разделе аппаратно [-зависимые точечные рисунки](device-dependent-bitmaps.md) и [аппаратно-независимые точечные рисунки](device-independent-bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="dd719-110">For more information, see [Device-Dependent Bitmaps](device-dependent-bitmaps.md) and [Device-Independent Bitmaps](device-independent-bitmaps.md).</span></span>

<span data-ttu-id="dd719-111">После создания растрового изображения нельзя изменить его размер, число цветовых плоскостей или число битов, необходимое для его распознавания.</span><span class="sxs-lookup"><span data-stu-id="dd719-111">After the bitmap has been created, you cannot change its size, number of color planes, or number of bits required to identify the color.</span></span>

<span data-ttu-id="dd719-112">Если точечный рисунок больше не нужен, вызовите функцию [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) , чтобы удалить ее.</span><span class="sxs-lookup"><span data-stu-id="dd719-112">When you no longer need a bitmap, call the [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject) function to delete it.</span></span>

 

 



