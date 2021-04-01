---
description: Контекст устройства (DC) — это структура данных, определяющая графические объекты, связанные с ними атрибуты, а также графические режимы, влияющие на выходные данные на устройстве. Чтобы создать контроллер домена, вызовите функцию Креатедк. чтобы получить контроллер домена, вызовите функцию GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Точечные рисунки, контексты устройств и поверхности рисования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263695"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a><span data-ttu-id="b08d6-104">Точечные рисунки, контексты устройств и поверхности рисования</span><span class="sxs-lookup"><span data-stu-id="b08d6-104">Bitmaps, Device Contexts, and Drawing Surfaces</span></span>

<span data-ttu-id="b08d6-105">*Контекст устройства* (DC) — это структура данных, определяющая графические объекты, связанные с ними атрибуты, а также графические режимы, влияющие на выходные данные на устройстве.</span><span class="sxs-lookup"><span data-stu-id="b08d6-105">A *device context* (DC) is a data structure defining the graphics objects, their associated attributes, and the graphics modes affecting output on a device.</span></span> <span data-ttu-id="b08d6-106">Чтобы создать контроллер домена, вызовите функцию [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . чтобы получить контроллер домена, вызовите функцию [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .</span><span class="sxs-lookup"><span data-stu-id="b08d6-106">To create a DC, call the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function; to retrieve a DC, call the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function.</span></span>

<span data-ttu-id="b08d6-107">Перед возвратом маркера, который идентифицирует контроллер домена, система выбирает поверхность рисования в контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="b08d6-107">Before returning a handle that identifies that DC, the system selects a drawing surface into the DC.</span></span> <span data-ttu-id="b08d6-108">Если приложение вызвало функцию [**креатедк**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) для создания контекста устройства для дисплея VGA, размеры этой области рисования будут со640-х 480 пикселей.</span><span class="sxs-lookup"><span data-stu-id="b08d6-108">If the application called the [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) function to create a device context for a VGA display, the dimensions of this drawing surface are 640-by-480 pixels.</span></span> <span data-ttu-id="b08d6-109">Если приложение называется функцией [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , измерения отразится на размере клиентской области.</span><span class="sxs-lookup"><span data-stu-id="b08d6-109">If the application called the [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) function, the dimensions reflect the size of the client area.</span></span>

<span data-ttu-id="b08d6-110">Прежде чем приложение сможет начать рисование, необходимо выбрать точечный рисунок с соответствующей шириной и высотой в контроллере домена, вызвав функцию [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="b08d6-110">Before an application can begin drawing, it must select a bitmap with the appropriate width and height into the DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span> <span data-ttu-id="b08d6-111">Когда приложение передает маркер контроллеру домена в одну из функций графического интерфейса графических устройств (GDI), запрошенные выходные данные отображаются на поверхности рисования, выбранной в контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="b08d6-111">When an application passes the handle to the DC to one of the graphics device interface (GDI) drawing functions, the requested output appears on the drawing surface selected into the DC.</span></span>

<span data-ttu-id="b08d6-112">Дополнительные сведения см. в разделе [контексты устройств памяти](memory-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="b08d6-112">For more information, see [Memory Device Contexts](memory-device-contexts.md).</span></span>

 

 



