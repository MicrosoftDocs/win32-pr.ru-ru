---
description: Когда приложение вызывает функцию рисования для рисования фигуры, система позиционирует кисть в начале операции рисования и сопоставляет пиксел в битовой карте кисти с клиентской областью в исходном окне, расположенном в левом верхнем углу окна.
ms.assetid: b951fd9a-1e87-4b17-9be8-263896c73922
title: Источник кисти
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 016237b97a52da6fd7fa14a3b6ba2dc25b03b96e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560866"
---
# <a name="brush-origin"></a><span data-ttu-id="03105-103">Источник кисти</span><span class="sxs-lookup"><span data-stu-id="03105-103">Brush Origin</span></span>

<span data-ttu-id="03105-104">Когда приложение вызывает функцию рисования для рисования фигуры, система позиционирует кисть в начале операции рисования и сопоставляет пиксел в битовой карте кисти с клиентской областью в *исходном окне*, расположенном в левом верхнем углу окна.</span><span class="sxs-lookup"><span data-stu-id="03105-104">When an application calls a drawing function to paint a shape, the system positions a brush at the start of the paint operation and maps a pixel in the brush bitmap to the client area at the *window origin*, which is the upper-left corner of the window.</span></span> <span data-ttu-id="03105-105">Координаты пикселя, который сопоставляется системой, называется *источником кисти*.</span><span class="sxs-lookup"><span data-stu-id="03105-105">The coordinates of the pixel that the system maps are called the *brush origin*.</span></span> <span data-ttu-id="03105-106">Источник кисти по умолчанию расположен в левом верхнем углу растрового изображения кисти в координатах (0,0).</span><span class="sxs-lookup"><span data-stu-id="03105-106">The default brush origin is located in the upper-left corner of the brush bitmap, at the coordinates (0,0).</span></span> <span data-ttu-id="03105-107">Затем система копирует кисть в клиентской области, формируя шаблон, который имеет высоту в виде точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="03105-107">The system then copies the brush across the client area, forming a pattern that is as tall as the bitmap.</span></span> <span data-ttu-id="03105-108">Операция копирования продолжится по строке, пока не будет заполнена вся область клиента.</span><span class="sxs-lookup"><span data-stu-id="03105-108">The copy operation continues, row by row, until the entire client area is filled.</span></span> <span data-ttu-id="03105-109">Однако шаблон кисти видим только внутри границ указанной фигуры.</span><span class="sxs-lookup"><span data-stu-id="03105-109">However, the brush pattern is visible only within the boundaries of the specified shape.</span></span>

<span data-ttu-id="03105-110">Существуют экземпляры, когда не следует использовать источник кисти по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="03105-110">There are instances when the default brush origin should not be used.</span></span> <span data-ttu-id="03105-111">Например, может потребоваться, чтобы приложение использовало ту же кисть для рисования фона родительского и дочернего окон и смешать фон дочернего окна с родительским окном.</span><span class="sxs-lookup"><span data-stu-id="03105-111">For example, it may be necessary for an application to use the same brush to paint the backgrounds of its parent and child windows and blend a child window's background with that of the parent window.</span></span> <span data-ttu-id="03105-112">Для этого приложение должно сбросить начало координат кисти, вызвав функцию [**сетбрушоржекс**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) и сдвигясь на требуемое количество пикселей.</span><span class="sxs-lookup"><span data-stu-id="03105-112">To do this, the application should reset the brush origin by calling the [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex) function and shifting the origin the required number of pixels.</span></span> <span data-ttu-id="03105-113">(Приложение может получить текущий источник кисти, вызвав функцию [**жетбрушоржекс**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) .)</span><span class="sxs-lookup"><span data-stu-id="03105-113">(An application can retrieve the current brush origin by calling the [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex) function.)</span></span>

<span data-ttu-id="03105-114">На следующем рисунке показана пятиконечная звезда, заполненная с помощью определяемой приложением кисти.</span><span class="sxs-lookup"><span data-stu-id="03105-114">The following illustration shows a five-pointed star filled by using an application-defined brush.</span></span> <span data-ttu-id="03105-115">На рисунке изображено изображение кисти, а также расположение, в котором она была сопоставлена в начале операции рисования.</span><span class="sxs-lookup"><span data-stu-id="03105-115">The illustration shows a zoomed image of the brush, as well as the location to which it was mapped at the beginning of the paint operation.</span></span>

![Иллюстрация, показывающая, что источник кисти сопоставлен с исходным окном](images/csbru-01.png)

 

 



