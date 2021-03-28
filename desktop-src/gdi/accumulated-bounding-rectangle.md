---
description: Накопленный ограничивающий прямоугольник — это самый маленький прямоугольник, включающий в себя часть окна или клиентской области, затронутую последними операциями рисования.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Накопленный ограничивающий прямоугольник
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544559"
---
# <a name="accumulated-bounding-rectangle"></a><span data-ttu-id="194bd-103">Накопленный ограничивающий прямоугольник</span><span class="sxs-lookup"><span data-stu-id="194bd-103">Accumulated Bounding Rectangle</span></span>

<span data-ttu-id="194bd-104">*Накопленный ограничивающий прямоугольник* — это самый маленький прямоугольник, включающий в себя часть окна или клиентской области, затронутую последними операциями рисования.</span><span class="sxs-lookup"><span data-stu-id="194bd-104">The *accumulated bounding rectangle* is the smallest rectangle enclosing the portion of a window or client area affected by recent drawing operations.</span></span> <span data-ttu-id="194bd-105">Приложение может использовать этот прямоугольник для удобного определения степени изменений, вызванных операциями рисования.</span><span class="sxs-lookup"><span data-stu-id="194bd-105">An application can use this rectangle to conveniently determine the extent of changes caused by drawing operations.</span></span> <span data-ttu-id="194bd-106">Иногда он используется вместе с [**локквиндовупдате**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) , чтобы определить, какая часть клиентской области должна быть перерисована после очистки блокировки обновления.</span><span class="sxs-lookup"><span data-stu-id="194bd-106">It is sometimes used in conjunction with [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) to determine which portion of the client area must be redrawn after the update lock is cleared.</span></span>

<span data-ttu-id="194bd-107">Приложение использует функцию [**сетбаундсрект**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (УКАЗАВ \_ параметр DCB Enable), чтобы начать накопление ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="194bd-107">An application uses the [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) function (specifying DCB\_ENABLE) to begin accumulating the bounding rectangle.</span></span> <span data-ttu-id="194bd-108">Затем система накапливает точки для ограничивающего прямоугольника, так как приложение использует указанный контекст устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="194bd-108">The system subsequently accumulates points for the bounding rectangle as the application uses the specified display device context.</span></span> <span data-ttu-id="194bd-109">Приложение может получить текущий ограничивающий прямоугольник в любое время с помощью функции [**жетбаундсрект**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) .</span><span class="sxs-lookup"><span data-stu-id="194bd-109">The application can retrieve the current bounding rectangle at any time by using the [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) function.</span></span> <span data-ttu-id="194bd-110">Приложение останавливает накопление, вызывая **сетбаундсрект** еще раз, задавая \_ значение параметра DCB Disable.</span><span class="sxs-lookup"><span data-stu-id="194bd-110">The application stops the accumulation by calling **SetBoundsRect** again, specifying the DCB\_DISABLE value.</span></span>

 

 



